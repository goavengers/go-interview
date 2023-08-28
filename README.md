<div align="center">
  <img width="325" height="281" src="https://github.com/goavengers/go-interview/blob/master/img/go-inter.jpeg">
  <h1>Вопросы и ответы для собеседования Back-end/Golang разработчика и не только</h1>
  <h5>Вместе мы разберемся!</h5>
</div>

Здесь собирается большая коллекция вопросов и ответов на них, необходимых не только для прохождения собеседований, но и для комплексного развития кругозора

## Содержание

0. [Разогрев](docs/what_is_going_on)
1. [Общие вопросы](docs/common)
    - [В чем отличие протоколов TCP и UDP? В каком случае UDP предпочтительнее?](docs/common#1-в-чем-отличие-протоколов-tcp-и-udp-в-каком-случае-udp-предпочтительнее)
    - [Что такое NAT?](docs/common#2-что-такое-nat)
    - [Что такое HTTP и HTTPS, в чем их отличия?](docs/common#3-что-такое-http-и-https-в-чем-их-отличия)
    - [Что такое SSL и TLS, есть ли между ними отличия?](docs/common#4-что-такое-ssl-и-tls-есть-ли-между-ними-отличия)
    - coming soon
2. [Вопросы по шаблонам проектирования](docs/design_patterns)
    - С какими паттернами проектирования знакомы?
    - Расскажите про паттерны Builder(Строитель), Factory(Фабрика), Closer(Доводчик), Singleton(Одиночка)
    - Расскажите, какой паттерн использовали в продукте/своем коде?
    - Знакомы ли с концепцией [12FA](https://12factor.net/ru/) для проектирования SaaS приложений? 
3. [Вопросы про микросервисы](docs/microservices)
    - Что такое микросервисная архитектура? (кратко)
    - Чем отличается микросервис от монолита?
    - Опишите плюсы и минусы двух концепций
4. [Вопросы про инфраструктуру и деплой](docs/infrastructure_and_deploy)
    - Что такое сине-зеленый деплой(blue-green deployment)?
    - Что такое Canary (канареечные развертывания)?
    - Что такое Dark (скрытые) или А/В-развертывания?
    - Что такое SLA, SLO, SLI?
    - Какие инструменты CI/CD вам известны?
    - Как обеспечить непрерывность и стабильность деплоя приложения?
    - С какими проблемами при деплое продукта вы сталкивались, как митигировали?
5. [Вопросы про кеширование и базам данных](docs/cache_and_db)
    - Что такое индексы в MySQL, как и для чего их использовать и создавать?
    - Что такое составной индекс, как и для чего их использовать и создавать?
    - Как использовать индексы в JOIN запросах Mysql?
    - Что такое частичные индексы, как и для чего их использовать и создавать?
    - В чем отличия InnoDB и MyISAM?
    - Возможен ли JOIN со вложенными запросами, как?
    - Что такое дедлоки (deadlock), почему возникают, как можно недопускать?
    - Что такое HAVING, что он делает как и зачем его использовать?
    - Разница между WHERE и HAVING и можно ли использовать HAVING без группировки данных?
    - Что такое EXPLAIN?
    - Как узнать версию Mysql?
    - Как можно оптимизировать ORDER BY RAND()?
    - Как удалить индекс MySQL?
    - Как правильно выбрать тип данных в Mysql, когда нужны:
      - NULL значения, когда лучше использовать?
      - Целые числа (TINYINT, SMALLINT, INT, BIGINT) и UNSIGNED, длинна числовых типов?
      - Большие числа: demical, что это и как работает?
      - Float | Double VS Demical, в чем разница, что и как использовать?
      - Строки VARCHAR и CHAR, отличия когда лучше использовать?
      - BLOB / TEXT, чем отличаются, как выполнять сортировку по полям данного типа?
      - ENUM, когда может пригодится?
      - DATETIME / TIMESTAMP, в чем их разница, какие максимальные значения?
    - Когда и зачем может пригодиться денормализация данных?
    - Что такое шардинг и репликация?
    - В чем отличие синхронной репликации от асинхронной? Какая подходит лучше для какого кейса?
    - Если индекс создан для 2-х колонок и запрос содержит только одну из них - будет ли он работать?
6. [Вопросы по языку Golang](docs/golang)
    - [Что из себя представляет тип данных string в языке Golang? Можно ли изменить определенный символ в строке? Что происходит при склеивании строк?](docs/golang#1)
    - [Вытекающий вопрос — как эффективно склеивать множество строк?](docs/golang#2)
    - Что будет происходить при конкурентной записи в map? Как можно решить эту проблему?
    - Расскажите о ООП в Golang.#1
    - [Какое будет значение у переменной x после выполнения программы?](docs/golang#12)
    - [Какое значение примет выражение (true && false) || (false && true) || !(false && false)?](docs/golang#13)
    - [Мы знаем, что в десятичной системе самое большое число из одной цифры - это 9, а из двух - 99. В бинарной системе самое большое число из двух цифр это 11 (3), самое большое число из трех цифр это 111 (7) и самое большое число из 4 цифр это 1111 (15). Вопрос: каково самое большое число из 8 цифр? (Подсказка: 101-1=9 и 102-1=99)](docs/golang#14)
    - [Что выведет следующая программа?](docs/golang#15)
    - [Что выведет следующая программа?](docs/golang#16)
    - [Как работает Garbage Collection в Go?](docs/golang#17)
    - Что такое interface, как они работают в Go?
    - Что такое slice, как устроены и чем отличаются от массивов?
    - Что такое len и capacity в slice Go?
    - Возможно ли предугадать, что GC отработает за константное время N?
    - Что будет, если создать канал и отправить туда запись, но у него нет читателей?
    - По какому алгоритму растет slice? (если знаете старую и новую формулу - круто)
    - Сколько весят такие структуры данных, как слайс, мапа, пустая строка, число в байтах?
    - В какой момент инициализированное значение переменной передается в defer? Как это связано с именованием функции?
7. [Вопросы о распределённых системах](docs/distributed_systems)
    - Как тестировать распределённую систему?
    - Знакомы ли с lock-free концепцией? Можете описать принцип работы?
8. [Вопросы по организации кода](docs/code_design)
    - Как тесты и TDD влияют на организацию кода?
    - В чём разница между сцеплением и связанностью?
    - Почему в TDD тесты пишутся прежде кода?
    - Если у вашего кода плохая организация, как вы это поймёте?
9. [Вопросы от Данила Подольского на позицию Senior Golang Backend Developer в компанию Evrone](docs/podolsky/)
    - [Go — императивный или декларативный? А в чем разница?](docs/podolsky#1)
    - [Что такое type switch?](docs/podolsky#2)
    - [Как сообщить компилятору, что наш тип реализует интерфейс?](docs/podolsky#3)
    - [Как работает append?](docs/podolsky#4)
    - [Какое у slice zero value? Какие операции над ним возможны?](docs/podolsky#5)
    - [Как устроен тип map?](docs/podolsky#6)
    - [Каков порядок перебора map?](docs/podolsky#7)
    - [Что будет, если читать из закрытого канала?](docs/podolsky#8)
    - [Что будет, если писать в закрытый канал?](docs/podolsky#9)
    - [Как вы отсортируете массив структур по алфавиту по полю Name?](docs/podolsky#10)
    - [Что такое сериализация? Зачем она нужна?](docs/podolsky#11)
    - [Сколько времени в минутах займет у вас написание процедуры обращения односвязного списка?](docs/podolsky#12)
    - [Где следует поместить описание интерфейса: в пакете с реализацией или в пакете, где этот интерфейс используется? Почему?](docs/podolsky#13)
    - [Предположим, ваша функция должна возвращать детализированные Recoverable и Fatal ошибки. Как это реализовано в пакете net? Как это надо делать в современном Go?](docs/podolsky#14)
    - [Главный недостаток стандартного логгера?](docs/podolsky#15)
    - [Есть ли для Go хороший orm? Ответ обоснуйте.](docs/podolsky#16)
    - [Какой у вас любимый линтер?](docs/podolsky#17)
    - [Можно ли использовать один и тот же буфер []byte в нескольких горутинах?](docs/podolsky#18)
    - [Какие типы мьютексов предоставляет stdlib?](docs/podolsky#19)
    - [Что такое lock-free структуры данных, и есть ли в Go такие?](docs/podolsky#20)
    - [Способы поиска проблем производительности на проде?](docs/podolsky#21)
    - [Стандартный набор метрик prometheus в Go -программе?](docs/podolsky#22)
    - [Как встроить стандартный профайлер в свое приложение?](docs/podolsky#23)
    - [Overhead от стандартного профайлера?](docs/podolsky#24)
    - [Почему встраивание — не наследование?](docs/podolsky#25)
    - [Какие средства обобщенного программирования есть в Go?](docs/podolsky#26)
    - [Какие технологические преимущества языка Go вы можете назвать?](docs/podolsky#27)
    - [Какие технологические недостатки языка Go вы можете назвать?](docs/podolsky#28)
10. [Популярные задачи на собеседованиях](docs/popular_tasks)
    - [На вход подаются два неупорядоченных слайса любой длины. Надо написать функцию, которая возвращает их пересечение](docs/popular_tasks#1)
    - [Написать генератор случайных чисел](docs/popular_tasks#2)
    - [Слить N каналов в один](docs/popular_tasks#3)
    - [Сделать конвейер чисел](docs/popular_tasks#4)
    - [Написать WorkerPool с заданной функцией](docs/popular_tasks#5)
    - [Сделать кастомную waitGroup на семафоре](docs/popular_tasks#6)
    - [Что выведет код?](docs/popular_tasks#7)
    - [Какая есть проблема в коде?](docs/popular_tasks#8)
    - [Что выведет код?](docs/popular_tasks#9)
    - [Что выведет код?](docs/popular_tasks#10)

<details>
  <summary>Ответ</summary>
  <br />
  
  Тут ответ
</details>

# Надо будет отсортировать!

Быстрый экскурс по вопросам Go. Будет дополняться

- [ ] практические задачи по темам
- [ ] дополнительные материалы
- [ ] просто практические задачки по Go

### Начнем! (Чисто для себя)

1. Что такое Go?

<details>
  <summary>Ответ</summary>
<br />
Go (Golang) — это компилируемый, статически типизированный, многопоточный язык программирования от Google с открытым исходным кодом. Считается языком общего назначения, но основное применение — разработка веб-сервисов и клиент-серверных приложений. Хотя также язык обладает возможностями по работе с графикой, низкоуровневыми возможностями и т.д.
<br /><br />
Язык Go был представлен в 2009 году в корпорации Google. Его полное название — Golang — производное от «Google language». Язык создали Роб Пайк и Кен Томпсон. Они работали в лаборатории Bell Labs, выпустившей операционную систему UNIX и языки программирования C и C++.
	
Цель проекта — создать современную альтернативу C и C++ и сделать разработку ПО в Google более быстрой.

Язык должен был решить такие проблемы, как:

- медленная сборка программ;
- неконтролируемые зависимости;
- использование программистами различных подмножеств языка;
- трудности с пониманием программ — из-за сложного синтаксиса, плохого документирования;
- дублирование разработок;
- высокая стоимость обновлений;
- сложности разработки инструментария;
- плохое межъязыковое взаимодействие.

В основе языка Golang — база лучших функций из языков C и C++, Python, Pascal, Oberon и Modula. Сначала Go использовали внутри Google, но затем он стал применяться в компаниях по всему миру: HP, Adobe, Microsoft, Facebook, BBC, Uber, Dropbox, Netflix, Яндекс, ВКонтакте, Avito, Ozon и других.
</details>

3. Какие основные отличия есть у Go перед языками Java, Python?

<details>
  <summary>Ответ</summary>
  <br />
  
Если охарактеризовать Go одним предложением, то можно сказать так: «Похож на Python, но быстрее и с лучшим параллелизмом». Как и Python, Go рассчитан на интенсивное использование функций, что позволяет разработчикам сравнительно быстро создавать мощную функциональность.

Однако, в отличие от Python, Go — компилируемый язык (технически Python также компилируется, но не в традиционном смысле). Как правило, это сокращает время выполнения программного кода. Кроме того, важной целью при проектировании Go было обеспечить удобный параллелизм (несколько задач могут выполняться одновременно). В большинстве других языков также реализован параллелизм, но благодаря таким функциям, как собственные встроенные подпрограммы, goroutine, проще реализовать высокоэффективный параллелизм в приложении Go. Это значимое преимущество в наш век микрослужб и многоядерных процессоров, когда нужно полностью использовать преимущества параллельных вычислений.


Что касается Java, то тут больше схожести, чем с Python. Java является таким же компилируемым, строго типизированным языком программирования с возможностью работать в многопточном режиме.

Пожалуй одним из главных отличий от Go (кроме синтаксиса), является объектно-ориентированная природа языка Java и то, что, для достижения кроссплатформенности, она работает на виртуальной машине JVM (Java Virtual Machine). В то же время Go программа исполняется в своем внутреннем Runtime и в Go нет классов с конструкторами. Вместо экземпляра методов, иерархии наследия классов и динамического метода, Go предоставляет структуры и интерфейсы.

Также в Java для реализации параллелизма исаользуются потоки (threads) и задачи (tasks), и более абстрагированные concurrency API - исполнители (executors), callable и фьючерсы  (future). 

В то время как в Go для достижения параллелизма есть горутины (goroutine) и каналы (channels), а вся "тяжелая" работа лежит на планировщике (sheduler) исполняемой программы.
</details>

4. Какие преимущества и недостатки есть у Go? (объективные)

<details>
  <summary>Ответ</summary>
  <br />
  
  **К преимуществам можно отнести:**
  
- Простой синтаксис.

В Go нет наследования, классов, объектов и сложных функций. Всё лаконично и аккуратно — это позволяет просто писать на Go и читать чужой код. Для понимания не понадобятся стандарты и комментарии — всё и так максимально прозрачно.

- Лёгкий для новичка.

Основное руководство Go занимает всего 50 страниц. Благодаря строгости и простому синтаксису изучение языка Go — тривиальная задача даже для тех, у кого совсем нет опыта в разработке. Он построен так, что буквально ведёт разработчика за руку и защищает от ошибок и опечаток.

- Много встроенных инструментов для разработчиков.

Внутрь языка встроены инструменты тестирования, утилита для создания документации, дополнения для поиска ошибок в коде и другие полезные функции. Поэтому разработка на языке Go — довольно простой и приятный процесс, нет чувства, что нужно постоянно искать какие-то сторонние инструменты для облегчения работы.

- Большое количество библиотек.

Практически для каждой задачи есть готовые стандартные библиотеки внутри языка. Сторонние тоже есть, их список постоянно растёт. К коду на Go можно подключать библиотеки С и С++, которых очень много из-за популярности этих языков.

- Высокая производительность.

Если переписать код с другого языка на Go, можно даже без специальной оптимизации повысить производительность в 5–10 раз.

- Надёжность.

Программы на Go грамотно используют память и вычислительные ресурсы, поэтому работают стабильно.

**Недостатки:**

- Ограниченный функционал.

Область применения языка Go — сетевые и серверные приложения. А вот с созданием графических интерфейсов он справляется плохо. Поэтому полностью написать на Go пользовательское приложение будет сложно из-за ограниченных возможностей, да и в целом он неприменим для многих задач. Его нужно использовать с умом и там, где он действительно нужен.

- Простота.

Это одновременно и плюс, и минус. Некоторые вещи, доступные на других языках, на Go сделать просто не выйдет. Например, разрабатывать большие проекты из-за отсутствия объектов, полезных для совместной работы с распределённым кодом.

</details>

### Слайсы и массивы:

Слайсы и массивы очень важная часть языка Go и их частенько любят спрашивать на собеседованиях.

1. Что такое слайс (slice) и массив (array)? Чем отличается массив от слайса?

<details>
  <summary>Ответ</summary>
<br />
В Go массивы и срезы представляют собой структуры данных, состоящие из упорядоченных последовательностей элементов. Эти наборы данных очень удобно использовать, когда вам требуется работать с большим количеством связанных значений. Они позволяют хранить вместе связанные данные, концентрировать код и одновременно применять одни и те же методы и операции к нескольким значениям.

Хотя и массивы, и срезы в Go представляют собой упорядоченные последовательности элементов, между ними имеются существенные отличия. Массив в Go представляет собой структуру данных, состоящую из упорядоченной последовательности элементов, емкость которой определяется в момент создания. После определения размера массива его нельзя изменить. Срез — это версия массива с переменной длиной, дающая разработчикам дополнительную гибкость использования этих структур данных. Срезы — это то, что обычно называют массивами в других языках.

**Массивы:**

Массивы представляют собой структурированные наборы данных с заданным количеством элементов. Поскольку массивы имеют фиксированный размер, память для структуры данных нужно выделить только один раз, в то время как для структур данных переменной длины требуется динамическое выделение памяти в большем или меньшем объеме. Хотя из-за фиксированной длины массивов они не отличаются гибкостью в использовании, одноразовое выделение памяти позволяет повысить скорость и производительность вашей программы. В связи с этим, разработчики обычно используют массивы при оптимизации программ, в том числе, когда для структур данных не требуется переменное количество элементов.

```go
var numbers [3]int
var strings [3]string

// Если вы не декларируете значения элементов массива, по умолчанию используются нулевые значения, 
// т. е. по умолчанию элементы массива будут пустыми. 
// Это означает, что целочисленные элементы будут иметь значение 0, а строки будут пустыми.
fmt.Println(numbers) // [ 0 0 0 ]
fmt.Println(strings) // [ "" "" "" ]
```

**Примечание:** важно помнить, что в каждом случае декларирования нового массива создается отдельный тип. Поэтому, хотя `[2]int` и `[3]int` содержат целочисленные элементы, из-за разницы длины типы данных этих массивов несовместимы друг с другом.

**Срезы:**

Срез — это тип данных Go, представляющий собой мутируемую или изменяемую упорядоченную последовательность элементов. Поскольку размер срезов не постоянный, а переменный, его использование сопряжено с дополнительной гибкостью. При работе с наборами данных, которые в будущем могут увеличиваться или уменьшаться, использование среза обеспечит отсутствие ошибок при попытке изменения размера набора. В большинстве случаев возможность изменения стоит издержек перераспределения памяти, которое иногда требуется для срезов, в отличие от массивов. Если вам требуется сохранить большое количество элементов или провести итерацию большого количества элементов, и при этом вам нужна возможность быстрого изменения этих элементов, вам подойдет тип данных среза.

```go
// Создадим срез, содержащий элементы строкового типа данных:
seaCreatures := []string{"shark", "cuttlefish", "squid", "mantis shrimp", "anemone"} // len: 5, cap: 5

// Если вы хотите создать срез определенной длины без заполнения элементов коллекции, 
// вы можете использовать встроенную функцию make()
oceans := make([]string, 3) // output: [ "" "" "" ], len: 3, cap: 3

// Если вы хотите заранее выделить определенный объем памяти, вы можете использовать в команде make() третий аргумент:
oceans := make([]string, 3, 5) // output: [ "" "" "" ], len: 3, cap: 5
```

</details>

2. Как устроен слайс в Go? Как устроен массив в Go?

<details>
  <summary>Ответ</summary>
  <br />
  
Cлайс - это структура go, которая включает в себя ссылку на базовый массив, а также две переменные len(length) и cap(capacity).

len - это длина слайса - то количество элементов, которое в нём сейчас находится.
cap - это ёмкость слайса - то количество элементов, которые мы можем записать в слайс сверх len без его дальнейшего расширения.

```go
// структура слайса
type slice struct {
	array unsafe.Pointer
	len   int
	cap   int
}
```

Массив - это последовательно выделенная область памяти. Частью типа array является его размер, который в том числе является не изменяемым.
</details>

3. Как можно создать слайс? Что такое zero-value и какое оно у слайса?
<details>
  <summary>Ответ</summary>
  <br />
  
Способы создания слайса:

```go
var nums []int 			// nil slice, длина 0 емкость 0
var nums = []int{1, 2, 3} 	// слайс с 3 значениями, длина 3, емкость 3
nums := []int{1, 2, 3} 		// тоже самое, что и выше, слайс с 3 значениями и емкостью 3
nums := make([]int{}, 0, 3) 	// слайс без значенией но с емкостью 3
nums := make([]int, 3) 		// слайс с длиной 3 и с емкостью 3
var (
	nums = make([]int{}, 0, 3) 	// аналог выше
	nums = make([]int, 3)		// аналог выше
)
```

Zero-value - переменным, объявленным без явного начального значения, присваивается нулевое значение.

```go
var i int
var f float64
var b bool
var s string
var p *int
var t time.Time

fmt.Printf("%v %v %v %q %v %v\n", i, f, b, s, p, t) // output: 0 0 false "" <nil> 0001-01-01 00:00:00 +0000 UTC
```

Zero-value для слайса - это nil, а len и cap равны нулю, так как "под ним" нет инициализированного массива:

```go
var a []int

fmt.Prinln((a == nil, len(a), cap(a)) // output: true 0 0
a = append(a, 1)
fmt.Println(a == nil, len(a), cap(a)) // output: false 1 1
```
</details>

4. Что такое nil слайс и чем отличается? Можно ли добавлять элементы в nil слайс?

<details>
  <summary>Ответ</summary>
  <br />
  
В Go с nil слайслм можно соверщать те же операции, которые могли бы делать с инициализированным слайсом

```go
var slice []int

fmt.Println(len(slice), cap(slice)) // output 0 0

slice = append(slice, 10)

fmt.Println(slice, len(slice), cap(slice)) // output [ 10 ] 1 1
```
</details>

5. Как проверить слайс на пустоту?

<details>
  <summary>Ответ</summary>
  <br />
  
Самый надежный спосб проверить слайс на пустоту в большинчтве случаем - это вроверить его длину на ноль. Не стоит проверять слайс на nil
  
```go
var a []int

// не правильно
fmt.Println(a == nil) // true

// а если так
a := []int{}
fmt.Println(a == nil) // false

// поэтому правильно так
fmt.Println(len(a) == 0) // true
```
</details>

6. Как работает базовая функция append для слайсов? Можно ли применить к массивам? Напишите свою функцию append.

<details>
  <summary>Ответ</summary>
  <br />
  
Функция принимает на вход слайс и переменное количество элементов для добавления в слайс. Append расширяет слайс за пределы его len, возвращая при этом новый слайс.

```go
// функция append
func append(slice []Type, elems ...Type) []Type
```

Если количество элементов, которые мы добавляем в слайс, не будет превышать cap, вернется новый слайс, который ссылается на тот же базовый массив, что и предыдущий слайс. Если количество добавляемых элементов превысит cap, то вернется новый слайс, базовым для которого будет новый массив.
	
```go
// в данном блоке кода продемонстрирована работа функции append
	
// создаем слайс с capacity равным 3 и длиной 0
slice := make([]int, 0, 3) 	// len: 0, cap: 3
	
// далее заполняем слайс тремя элементами
slice = append(slice, 1) 	// len: 1, cap: 3
slice = append(slice, 2, 3) 	// len: 3, cap: 3

// получаем ожидаемый результат
fmt.Println(slice) // output [ 1, 2, 3 ]

// окей, теперь попробуем присводить слайс другому слайсу
// помним то, что слайс является структурой из трех элементов len, cap и указателем н первый элемент массива
// поэтому в sliceCopy мы получаем скопированные значение len и cap, а так же указатель на тот же массив, что и у переменной slice
sliceCopy := slice

// пробуем менять первый элемент в новом слайсе
sliceCopy[1] = 10
	
// убеждаемся, что в обоих слайсах изменились значения, все из-за базового массива
fmt.Println(slice, sliceCopy) // output: slice: [ 1, 10, 3 ] sliceCopy: [ 1, 10, 3 ]

// хорошо, теперь пробуем добавить новый элемент в первый слайс
slice = append(slice, 4)
// тут у нас функция append "видит", что мест больше нет и увеличивает cap в двое, увеличивает len на один
// и создает новый базовый массив с местимостью в 6 элементов, что и видим на печати
fmt.Println(slice) // output: [ 1, 10, 3, 4] len: 4, cap: 6
// но что случилось тут? ничего, просто ничего, теперь первая переменная смотрит на другой базовый массив и они больше никак не связаны
fmt.Println(sliceCopy) // output: [ 1, 2, 3 ] len: 3, cap: 3

// точно не связаны? ну давай убедимся! пробуем менять значения первых элементов в обоих слайсах
sliceCopy[0] = 50
slice[0] = 80

// убедились? :)
fmt.Println(slice, sliceCopy) // output: slice: [ 80, 10, 3, 4 ] sliceCopy: [ 50, 10, 3 ]
```	

А вот с мссивами функцию append использовать нелья иначе получим ошибку: `first argument to append must be slice; have T`

```go
array := [3]int{}
array = append(array, 3) // first argument to append must be a slice; have array (variable of type [3]int)
```

Теперь напишем свою функцию:

```go
// она будет проще, только с добавлением одного элемента
func main() {
	fmt.Println(Append([]int{1, 2, 3}, 4))
}

func Append[T any](dst []T, el T) []T {
	var res []T

	resLen := len(dst) + 1
	if resLen <= cap(dst) {
		res = dst[:resLen]
	} else {
		resCap := resLen
		if resCap < 2*len(dst) {
			resCap = 2 * len(dst)
		}

		res = make([]T, resLen, resCap)
		copy(res, dst)
	}

	res[len(dst)] = el
	return res
}
```
</details>

7. Как можно добавить элементы в слайс? Что будет если элемент не вмещается в размер слайса?

<details>
  <summary>Ответ</summary>
  <br />
  
Один из способов добавления элементов с слайс мы уже обсудили выше, с использованием функцию append:

```go
slice := make([]int, 0, 10) // len: 0, cap: 10
for i := 0; i < 10; i++ {
	slice = append(slice, i*2)
}
```

но есть еще 1 способ, через индексы, выглядит это так

```go
slice := make([]int, 10) // len: 10, cap: 10
for i := 0; i < 10; i++ {
	slice[i] = i*2
}
```

но у последнего способа есть недостаток, если количество элементов, которые мы хотим добавить в слайс премвысит емкость исходного слайса, тогда мы получим панику: `panic: runtime error: index out of range [10] with length 10`

```go
// достаточно поменять условие на <= 
slice := make([]int, 10) // len: 10, cap: 10
for i := 0; i <= 10; i++ {
	slice[i] = i * 2
}
```

в то время append расширил бы базовый массив слайса и продолжил дальше раюотать не паникуя.

</details>

8. Как можно скопировать слайс? Что такое функция copy? Как добиться аналогичного поведения copy с помощью append?

<details>
  <summary>Ответ</summary>
  <br />
  
Встроенная функция copy копирует элементы в целевой срез dst из исходного среза src.

```go
func copy(dst, src []Type) int
```

Возвращает количество скопированных элементов, которое будет минимумом len(dst) и len(src). Результат не зависит от того, перекрываются ли аргументы.

```go
// Копировать из одного среза в другой
var slice = make([]int, 3)
num := copy(slice, []int{0, 1, 2, 3}) 

fmt.Println(num, slice) // output: num == 3, slice == []int{0, 1, 2}
```

Второй способ копирования слайсов - использовать функцию append

```go
slice := make([]byte, 0, len(a))
slice = append(c, []int{0, 1, 2, 3}...)

fmt.Println(slice) // output: slice == []int{0, 1, 2}
```
</details>

9. Как можно слить два слайса?

<details>
  <summary>Ответ</summary>
  <br />
  
Объединение фрагментов в Go легко достигается с помощью той же встроенной функции append. Как мы помним он принимает срез (s1) в качестве первого аргумента и все элементы из второго среза (s2) в качестве второго. Возвращается обновленный срез со всеми элементами из s1 и, который может быть присвоен другой переменной.

```go
s1 := []int{1, 2, 3}
s2 := []int{4, 5, 6}

s3 := append(s1, s2...)
fmt.Println(s3) // output: [ 1, 2, 3, 4, 5, 6 ]
```
</details>

10. Как можно нарезать слайс? Какие есть ньансы, подводные камни?

<details>
  <summary>Ответ</summary>
  <br />

В Go можно сделать подслайз из слайса или массива:

```go
slice := []int{1, 2, 3, 4, 5, 6, 7, 8, 9, 10}
subSlice := slice[3:8] // [ 4, 5, 6, 7, 8 ]
```

Но что будет, если мы изменим значение под слайса или еще хуже, добавим туда элементы через функцию append?

```go
subSlice[0] = 101

fmt.Println(slice) // [1 2 3 101 5 6 7 8 9 10]
fmt.Println(subSlice) // [101 5 6 7 8]
```

Видим, что в базовом слайсе тоже поменялись значения, а все потому, что у под слайса все тот же базовый массив, а для подслайса нулевой элемент это элемент под индексом 3 в базовом. Примерно такое же поведение наблюдается у функции append, если его применить к под слайсу базового слайса:

```go
slice := make([]int, 10, 25)
subSlice := slice[3:5] // [ 0, 0, 0, 0, 0 ]

fmt.Println(len(slice), cap(slice)) // 10 25
fmt.Println(len(subSlice), cap(subSlice)) // 2 22

subSlice = append(subSlice, 11)

fmt.Println(slice) // [0 0 0 0 0 11 0 0 0 0]
fmt.Println(subSlice) // [0 0 11]
```

причина данного поведения в том, что у обоих слайсов один базовый массив, а так же у под слайса своя "копия" слайса с полями len и cap и когда мы пытаемся добавить в дочерний слайс элемент, при условии, что в родитльском хватает емкости, мы просто перезаписываем значение в базовом массива.

</details>


**полезные материалы:**

- https://www.youtube.com/watch?v=10LW7NROfOQ
- https://habrahabr.ru/post/325468/#massivy
- https://habrahabr.ru/post/325468/#slaysy
- https://habrahabr.ru/post/325468/#dobavlenie-k-slaysu-append
- https://ueokande.github.io/go-slice-tricks/
- https://go.dev/blog/slices-intro
- https://gist.github.com/GimmyHchs/33bd06e68d72a913a8587b09d41b50d0

### Мапы:

1. Что такое Map? Как устроен в Go? Желательно приблизительно понимать структуру (type hmap struct) и его поля
2. Что такое хеш-функция?
3. Почему нельзя брать ссылку на значение, хранящееся по ключу в map?
4. Что такое эвакуация, и в каком случае она будет происходить?
5. Какие есть особенности синтаксиса получения и записи значений в map?
6. Как происходит поиск по ключу в map?
7. Каков порядок перебора map?
8. Что будет происходить при конкуррентной записи в map? Как можно решить эту проблему?
9. Как защититься от ошибки во время конкурентной записи в map?

**полезные материалы:**

- https://www.youtube.com/watch?v=P_SXTUiA-9Y
- https://www.youtube.com/watch?v=0UX4MIfOMEs

### Каналы в Go:

1. Что такое канал? Чем отличается буферизированный канал от небуферизированного?
2. Как создать канал? Как закрыть канал?
3. Как читать из канала и писать в канал?
4. Зачем нужны в целом каналы?
5. Что будет, если читать из закрытого канала?
6. Что будет, если писать в закрытый канал?
7. Что будет если закрыть закрытый канал?
8. Что такое nil канал и что будет если писать и читать от туда?

**полезные материалы:**

- https://www.youtube.com/watch?v=ZTJcaP4G4JM

### Строки:

1. Что из себя представляет тип данных string в языке Golang? Можно ли изменить определенный символ в строке? Что происходит при склеивании строк?
2. Как можно оперировать строками?
3. Что будет если сложить строки?
4. Как определить количество символов для строки?
5. Какие есть нюансы при итерации по строке?
6. Как эффективно склеивать строки (конкатенация строк)?

### Типы данных в Go:

1. Какие бывают типы в Go? Целочисленные, дробные, комплексные, структуы, интерфесы, время и дополнить.
2. Отличие uint от int?
3. Что такое обычный int и какие есть нюансы его реализации?
4. Как преобразовать строку в int и наоборот? Можно ли сделать int(string) и string(int) соответственно?
5. Сколько в памяти занимают реализации int32 и int64?
6. Какие предельные значения int32 и int64?
7. Какой результат получим если разделить int на 0 и float на 0?
8. Что такое константы и можно ли их изменять?
9. Что такое iota?
10. Что такое структура (stuct) в Go? Зачем они нужны?
11. Что такое метод? Как они выглядят?
12. Как осуществляется наследование в Go?
13. Что такое тип rune? Зачем их использовать?
14. Что такое тип byte?
15. Что такое goto?
16. Какие циклы есть в Go?

### Интерфейсы в Go:

1. Что такое интерфейсы в Go? Чем отличается от интерфейсов в дпугих языказ, например, Java, PHP. Что такое утиная типизация?
2. Внутренее устройство интерфейса, какое оно (структура iface, itab)?
3. Сделать интерфейс для вычисления площади круга и квадрата, реализовать их в структурах cicle и square.
4. Что такое пустой интерфейс?
5. Что такое nil интерфейс?
6. Что такое type switch? 
7. Как определить тип интерфейса?
8. Как преобразовать интерфейс к другому типу?
9. Где следует поместить описание интерфейса: в пакете с реализацией или в пакете, где этот интерфейс используется? Почему?

**полезные ресурсы:**

- https://www.youtube.com/watch?v=eYHCCht8eX4

### Вопросы по Go:

1. Зачем используется ключевое слово defer в Go?
2. Каков порядок возврата при использовании несколько функций с defer в рамках одной внешней функции?
3. Как передаются значения в функции, перед которыми указано ключевое слово defer? Пример:

```go
func main() {
	nums := 1 << 5 // 32

	defer fmt.Println(nums) // туть как?

	nums = nums >> 1 //16

	fmt.Println("done")
}
```

4. Какие бывают способоы синхронизации данных в Go? (про каналы тоже не забываем)
5. Что такое mutex, какие они бывают и как их использовать?
6. Что такое atomics, какие бывают и как и когда их лучше использовать?
7. Что такое sync.Map?
8. Что такое lock-free структуры данных, и есть ли в Go такие? Если интересно.
9. Как можно обработать панику с помощью defer и recovery?
10. Что такое context в Go? Какие бывают context в Go? Когда их нужно использовать и зачем?
11. Что такое указатели? Как передаются параметры в функцию по указателю или по значению? Какие типы неявно передаются как указатель? Как передать по указателю?
12. Что такое пакеты (package) в Go? Как их создавать и импортировать?
13. Можно ли реализовать sync.Mutex и sync.WaitGroup на каналах? Как?

### Вопросы по Runtime Go:

1. Что такое runtime (планировщик sheduler)? Как он устроен в Go?
2. Что такое Gorutine (горутина)?
3. В чем отличие горутины от потока?
4. Как устроены горутины, сколько памяти они занимают в стеке?
5. Кто управляет горутинами? Какой тип многозадачности используется в Go и какой был до версии Go 1.15?
6. Что такое GC (garbadge collector/сборщик мусора)?
7. Как работает сборщик мусора в Go?
8. Как проверить тип переменной в среде выполнения?

**полезные материалы:**

- https://www.youtube.com/watch?v=ZTJcaP4G4JM (тут про каналы, но еще рассказывает про рантайм и горутины, планировщик и тп)

### Вопросы по тестированию

1. Что такое unit тесты?
2. Что такое интеграционные тесты?
3. Как в Go пишут unit тесты со стандартным пакетом testing? Какие есть библиотеки, например, testify?
4. Что такое моки (mocks)?

### Вопросы по CI/CD:

0. Что такое CI/CD?
1. Что такое линтеры (linters) зачем они нужны и как их использовать?
2. Как можно измерить использование памяти в Go? Что такое pprof?
3. Что такое Prometheus и Grafana? Зачем они нужны?

### Практическая часть по всем вопросам: 

- 

### Полезные ссылки:

- https://nuancesprog.ru/p/12333/
- https://github.com/goavengers/go-interview
   
## Как мне добавить свой вопрос-ответ?

- [Ознакомьтесь с шаблоном составления](TEMPLATE.md)

### Maintainers

<table>
<tr>
<td align="center">
<img src="https://avatars1.githubusercontent.com/u/23422968?s=460&u=668229465690637b50f6581df0fa9918d7fb6c1e&v=4" width="100px;" alt=""/>
<br /><sub><b>zikwall</b></sub></a><br />
</td>
<td align="center">
<img src="https://avatars.githubusercontent.com/u/2690403?v=4" width="100px;" alt=""/>
<br /><sub><b>dreddsa5dies</b></sub></a><br />
</td>
</tr>
</table>
