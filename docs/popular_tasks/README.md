## <a name="infrastructure_deploy_questions"></a>Популярные задачи на собеседованиях

### <a name="1"></a> 1. На вход подаются два неупорядоченных слайса любой длины. Надо написать функцию, которая возвращает их пересечение

Можно решить сортировкой, за более долгое время, но без выделения дополнительной памяти. 
А можно выделить дополнительную память и решить за линейное время.

Надо посчитать количество появлений элементов первого массива (лучше брать тот, что покороче) — используем для этого словарь. 
Потом пройтись по второму массиву и вычитать из словаря те элементы, которые есть в нем. 
По ходу добавляем в результат те элементы, у которых частота появлений больше нуля.

 - [x] Советуем посетить [Математические операции над множествами](https://github.com/goavengers/go-datastructure#-point_right-%D0%BC%D0%BD%D0%BE%D0%B6%D0%B5%D1%81%D1%82%D0%B2%D0%B0-sets)

```go
package main

import (
	"fmt"
)

// На вход подаются два неупорядоченных массива любой длины.
// Необходимо написать функцию, которая возвращает пересечение массивов
func intersection(a, b []int) []int {
	counter := make(map[int]int)
	var result []int

	for _, elem := range a {
		counter[elem]++
	}
	
	for _, elem := range b {
		if count, ok := counter[elem]; ok && count > 0 {
			counter[elem] -= 1	
			result = append(result, elem)
		}
	}
	return result
}

func main() {

	a := []int{23, 3, 1, 2}
	b := []int{6, 2, 4, 23}
	// [2, 23]
	fmt.Printf("%v\n", intersection(a, b))
	a = []int{1, 1, 1}
	b = []int{1, 1, 1, 1}
	// [1, 1, 1]
	fmt.Printf("%v\n", intersection(a, b))
}
```

### <a name="2"></a> 2. Написать генератор случайных чисел

В принципе, легкая задача, на базовые знания по асинхронному взаимодействию в Go. 
Для решения я бы использовал небуфферезированный канал. Будем асинхронно писать туда случайные числа и закроем его, когда закончим писать.

Плюс ее можно использовать в немного измененном виде в задаче на [слияние N каналов](#3).

```go
package main

import (
	"fmt"
	"math/rand"
	"time"
)

func randNumsGenerator(n int) <-chan int {
	r := rand.New(rand.NewSource(time.Now().UnixNano()))

	out := make(chan int)
	go func() {
		for i := 0; i < n; i++ {
			out <- r.Intn(n)
		}
		close(out)
	}()
	return out
}

func main() {
	for num := range randNumsGenerator(10) {
		fmt.Println(num)
	}
}
```

### <a name="3"></a> 3. Слить N каналов в один

Даны n каналов типа chan int. Надо написать функцию, которая смерджит все данные из этих каналов в один и вернет его.

Мы хотим, чтобы результат работы функции выглядел примерно так:

```go
for num := range joinChannels(a, b, c) {
       fmt.Println(num)
}
```

Для этого напишем функцию, которая будет асинхронно читать из исходных каналов, которые ей передадут в качестве аргументов, и писать в результирующий канал, который вернется из функции.

- Создаем канал, куда будем сливать все данные. 
Он будет небуферезированный, потому что мы не знаем, сколько данных придет из каналов.
- Дальше асинхронно прочитаем из исходных каналов и закроем результирующий канал для мерджа, когда все чтение закончится. 
- Чтобы дождаться конца чтения, просто обернем этот цикл по каналам в wait group.

```go
package main

import (
	"sync"
)

func joinChannels(chs ...<-chan int) <-chan int {
	mergedCh := make(chan int)

	go func() {
		wg := &sync.WaitGroup{}

		wg.Add(len(chs))

		for _, ch := range chs {
			go func(ch <-chan int, wg *sync.WaitGroup) {
				defer wg.Done()
				
				for id := range ch {
					mergedCh <- id
				}
			}(ch, wg)
		}

		wg.Wait()
		close(mergedCh)
	}()

	return mergedCh
}
```

```go
package main

import (
	"fmt"
)

func main() {

	a := make(chan int)
	b := make(chan int)
	c := make(chan int)

	go func() {
		for _, num := range []int{1, 2, 3} {
			a <- num
		}
		close(a)
	}()

	go func() {
		for _, num := range []int{20, 10, 30} {
			b <- num
		}
		close(b)
	}()

	go func() {
		for _, num := range []int{300, 200, 100} {
			c <- num
		}
		close(c)
	}()

	for num := range joinChannels(a, b, c) {
		fmt.Println(num)
	}
}
```

### <a name="4"></a> 4. Сделать конвейер чисел

Даны два канала. 
В первый пишутся числа. 
Нужно, чтобы числа читались из первого по мере поступления, 
что-то с ними происходило (допустим, возводились в квадрат) и результат записывался во второй канал.

Довольно частая задача, более подробно можно почитать [тут](https://blog.golang.org/pipelines).

Решается довольно прямолинейно — запускаем две горутины. 
- В одной пишем в первый канал. 
- Во второй читаем из первого канала и пишем во второй. 

Главное — не забыть закрыть каналы, чтобы ничего нигде не заблокировалось.

```go
package main

import (
	"fmt"
)

func main() {
	naturals := make(chan int)
	squares := make(chan int)

	go func() {
		for x := 0; x <= 10; x++ {
			naturals <- x
		}
		
		close(naturals)
	}()

	go func() {
		for x := range naturals {
			squares <- x * x
		}
		
		close(squares)
	}()

	for x := range squares {
		fmt.Println(x)
	}
}
```

### <a name="5"></a> 5. Написать WorkerPool с заданной функцией

Довольно распространенная задача, плюс подобные задачи встречаются на практике.

Нам нужно разбить процессы на несколько горутин — при этом не создавать новую горутину каждый раз, 
а просто переиспользовать уже имеющиеся. 
- Для этого создадим канал с джобами и результирующий канал. 
- Для каждого воркера создадим горутину, который будет ждать новую джобу, применять к ней заданную функцию и пулять ответ в результирующий канал.

```go
package main

import (
	"fmt"
)

func worker(id int, f func(int) int, jobs <-chan int, results chan<- int) {
    for j := range jobs {
        results <- f(j)
    }
}

func main() {

    const numJobs = 5
    jobs := make(chan int, numJobs)
    results := make(chan int, numJobs)

    multiplier := func(x int) int {
	    return x * 10
    }

    for w := 1; w <= 3; w++ {
        go worker(w,  multiplier, jobs, results)
    }

    for j := 1; j <= numJobs; j++ {
        jobs <- j
    }
    
    close(jobs)

    for i := 1; i <= numJobs; i++ {
        fmt.Println(<-results)
    }
}
```

### <a name="6"></a> 6. Сделать кастомную waitGroup на семафоре

Семафор можно легко получить из канала.
Чтоб не аллоцировать лишние данные, будем складывать туда пустые структуры.

В нашем случае мы хотим сделать семафор, который будет ждать выполнения пяти горутин.
- Для этого просто добавим вместо обычного канала буфферизированный.
- И внутри каждой горутины положим в него значение.
- А в конце будем дожидаться, что все ок — мы вычитаем все значения из канала.

```go
package main

import (
	"fmt"
)

type sema chan struct{}

func New(n int) sema {
	return make(sema, n)
}

func (s sema) Inc(k int) {
	for i := 0; i < k; i++ {
		s <- struct{}{}
	}
}

func (s sema) Dec(k int) {
	for i := 0; i < k; i++ {
		<-s
	}
}

func main() {
	numbers := []int{1, 2, 3, 4, 5}
	n := len(numbers)

	sem := New(n)

	for _, num := range numbers {
		go func(n int) {
			fmt.Println(n)
			sem.Inc(1)
		}(num)
	}

	sem.Dec(n)

}
```