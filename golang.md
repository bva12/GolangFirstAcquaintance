info о курсе - https://stepik.org/course/100208/info

# 2 Основы 

2.1 Привет, мир!

2.2 Пакеты

2.3 Импорт

2.4 Комментарии

2.5 Вопросы ко второму модулю
___
## 2.5.1  Задача
Дополните код таким образом, чтобы получилась рабочая программа на Go, которая будет выводить текст "Второй модуль позади!"
## Решение
```golang
package main

import "fmt"

func main() {
    fmt.Println("Второй модуль позади!")
}
```
## 2.5.2 Задача
Представьте себе, что вам нужно импортировать не только пакет "fmt", но и какой-нибудь другой. Например, пакет "math". Как это сделать? Напишите только код импорта этих двух пакетов.
## Решение
```go
import ("fmt";"math")
```
## 2.5.3 Задача
Ваш коллега попытался составить программу, которая должна выводить "GO" три раза на отдельных строках.
Однако он еще новичок в Go и допустил ряд ошибок в коде.

Отладьте и исправьте код, чтобы получить желаемый результат.
## Решение
```go
package main
import "fmt"

func main() {
   // выводим GO 3 раза
    fmt.Println("GO")
    fmt.Println("GO")
    fmt.Println("GO")
}
```
# 3 Базовые понятия
3.1 Переменные

3.2 Типы данных

3.3 Константы

3.4 Арифметические операции

3.5 Операторы сравнения

3.6 Принимаем ввод

3.7 Условный оператор if/else

3.8 Оператор switch

3.9 Циклы

3.10 Вопросы к третьему модулю
___
## 3.1 Задача
Допишите код программы, чтобы она создала переменную x и присвоила ей значение 42, после чего вывела эту переменную.
## Решение
```go
package main

import "fmt"

func main() {
    var x int = 42
    fmt.Println(x)
}
```
## 3.6 Задача
Допишите код, чтобы программа считывала два целых числа со входа и выводила их сумму
## Решение
```go
package main

import "fmt"

func main() {
    var a int
    var b int
    fmt.Scanln(&a)
    fmt.Scanln(&b)
    fmt.Println(a + b)
}
```
## 3.7 Задача
Дополните код (замените нижние подчеркивания), чтобы он выводил "Проходи", если переменная score будет больше или равна 75.
## Решение
```go
package main

import "fmt"

func main() {
    var score = 80
    if score >= 75 {
        fmt.Println("Проходи")
    }
}
```
## 3.8 Задача
Дополните код, чтобы получился правильный оператор switch под названием gender:
## Решение
```go
package main

import "fmt"

func main() {
    var gender int
    switch gender {
        case 1:
        fmt.Println("Мужчина")
        case 2:
        fmt.Println("Женщина")
        default:
        fmt.Println("Еще не определился")
    }
}
```
## 3.10.1 Задача
Дополните код (замените нижние подчеркивания), чтобы программа c помощью цикла выводила числа с 9 до 1. 

Помните, на одном из уроков речь шла о инкременте i++, операторе, который увеличивает счетчик на единицу. У этого оператора есть сводный брат - декремент, который уменьшает счетчик на единицу i-- В данной задаче как раз он и используется.
## Решение
```go
package main

import "fmt"

func main() {
    for i := 9; i > 0; i-- {
    fmt.Println(i)
    }
}
```
## 3.10.2 Задача
Давайте исправим еще одну программу. Нам нужно, чтобы получился правильный оператор if
## Решение
```go
package main

import "fmt"

func main() {
    height := 195
    if height > 185 {
        fmt.Println("Да")
    } else {
        fmt.Println("Нет")
    }
}
```
## 3.10.3 Задача
А теперь попробуем писать полноценные программы. Начнем с чего-то попроще.

### Язык программирования

На вход подается название языка программирования. Вам нужно считать его и вывести.

> Пример входных и выходных данных можно увидеть ниже в Sample Input и Sample Output. Всегда смотрите на них, если вам непонятно, что в задаче подается на вход и что нужно выводить.
## Решение
```go
package main

import "fmt"

func main() {
  var prog string
  fmt.Scanln(&prog)
  fmt.Println(prog)
}
```
## 3.10.4 Задача
### Сумма и произведение трех
На вход подаются три целых числа. Необходимо сосчитать и вывести их сумму и произведение на разных строках.
## Решение
```go
package main

import "fmt"

func main() {
  var a, b, c int
  fmt.Scanln(&a, &b, &c)
  fmt.Println(a+b+c)
  fmt.Println(a*b*c)
}
```
## 3.10.5 Задача
### Богач или бедняк?
На вход подается целое число, сумма денег, которые у вас есть. Ваша задача - вывести марку телефона, которую вы можете себе позволить купить.

Если сумма больше 1000 - вывести **Apple**

Если сумма от 500 до 1000 (включительно) - вывести **Samsung**

Если сумма меньше 500 - вывести **Nokia с фонариком**
## Решение
```go
package main

import "fmt"

func main() {
  var d int
  fmt.Scanln(&d)
  switch {
    case d>1000:
    fmt.Println("Apple")
    case 500<=d && d<=1000:
    fmt.Println("Samsung")
    case d<500:
    fmt.Println("Nokia с фонариком")
  }
}
```
## 3.10.6 Задача
### Произведение всех
На вход подается целое число. Вам необходимо вывести произведение всех чисел от 1 до данного числа (включительно).

>Например, на вход подается число 5, вам нужно найти - 1*2*3*4*5 = 120

## Решение
```go
package main

import "fmt"

func main() {
  var x int
  reg:=1
  fmt.Scanln(&x)
  for i:=1; i<=x;i++ {
   reg*=i
  }
  fmt.Println(reg)
 
}
```
## 3.10.7 Задача
Легкие задания остались позади. Пора решить что-то посложнее. Итак...

Вы создаете робота, который может говорить цифры.
Ваш робот должен принимать на вход 3 целых числа (каждый с новой строки) в диапазоне от 0 до 10 (включительно) и выдавать соответствующий текст на русском языке.

Смотрите пример в Sample Input и Sample Output. Не забывайте, на вход могут подаваться разные числа, а ваше решение должно работать с любыми из них, не только с теми, которые в примере.

**0** выводим как **Ноль**
## Решение
```go
package main

import "fmt"

func main() {
    var a, b, c int
    fmt.Scanln(&a)
    fmt.Scanln(&b)
    fmt.Scanln(&c)
    input := []int{a, b, c}
    text := [11]string{"Ноль", "Один", "Два", "Три", "Четыре", "Пять", "Шесть", "Семь", "Восемь", "Девять", "Десять"}
    for _, v:=range input {
        for i,_:= range text{
            if v == i{
            fmt.Println(text[i])
            }
        }
    }
}
```
# 4 Функции
4.1 Введение в функции

4.2 Возврат из функции

4.3 Defer

4.4 Область видимости

4.5 Вопросы к четвертому модулю
___
## 4.1.1 Задача
Вам нужно написать строку кода, которая с помощью функции Println() выведет текст "Тест!"
## Решение
```go
fmt.Println("Тест!")
```
## 4.1.2 Задача
Ваша задача дополнить код (заменить нижние подчеркивания), чтобы создать функцию line, которая будет выводить линию "-----", а затем вызвать эту функцию в программе.
## Решение
```go
package main

import "fmt"

func line() {
    fmt.Println("-----")
}

func main() {
    line()
}
```
## 4.2.1 Задача
Дополните (замените нижние подчеркивания) код, чтобы определить функцию mult, которая принимает два целочисленных аргумента и выводит результат их произведения.
## Решение
```go
func mult(x, y int) {
    fmt.Println(x*y)
}
```
## 4.3.1 Задача
Дополните (замените нижние подчеркивания) код, чтобы определить функцию, которая принимает две строки в качестве аргументов и возвращает результат их объединения (конкатенации).
## Решение
```go
func concat(a, b string) string {
    return a + b
}
```
## 4.6.1 Задача
Напишите функцию max() которая должна принимать на вход два целых числа и возвращать большее из них.
## Решение
```go
func max(x, y int) int {
  if x>y{
    return x
  }else{
    return y
  }
}
```
## 4.6.2 Задача
Напишите функцию calc() которая должна принимать на вход одно целое число, а возвращать два значения - число умноженное на два и число возведенное в квадрат.
## Решение
```go
func calc(x int) (int, int) {
  return x*2, x*x
}
```
## 4.6.3 Задача
Напишите функцию isEven(), которая принимает в качестве аргумента одно целое число и возвращает true если оно четное и false в ином случае.
## Решение
```go
func isEven(x int) bool {
  var y bool
  switch {
    case x%2==0:
      y=true
    case x%2!=0:
      y=false
  }
  return y
}
```
## 4.6.4 Задача
Напишите функцию double_m(), которая должна принимать на вход два целых числа a и b и возвращать сумму квадратов чисел от a до b (включительно).
## Решение
```go
func double_m(a, b int) int {
  var sum int =0
  if a<b {
    for i:=a; i<=b; i++ {
      sum += i*i
    }
  }else{
    for i:=b; i<=a; i++ {
      sum += i*i
    }
  }
  return sum
}
```
## 4.6.5 Задача
Вам нужно написать функцию one_or_two().  На вход подается два целых числа и строка. Строка может иметь значения one, two или любой другой текст. 

Возвращать из функции вам нужно два значения. Если строка равна one, нужно вернуть первое число и саму строку. Если строка равна two, нужно вернуть второе число и саму строку. Если строка другая - нужно вернуть 0 и саму строку.
## Решение
```go
func one_or_two(x, y int, z string) (int, string) {
    var f int =0
    var d string=""
    switch z {
        case "one":
        f=x
        d=z
        case "two":
        f=y
        d=z
        default:
        d=z
    }
    return f, d
}
```
## 4.6.6 Задача
Сколько лет вам было бы на Марсе?
Год на Земле состоит из 365 дней (високосные года не учитываем), а год на Марсе - из 687 дней.

Есть некая программа, которая принимает на вход ваш возраст в земных годах и выводит соответствующий возраст на Марсе.

Вам нужно написать для этой программы функцию mars_age(), которая будет принимать на вход целое число, возраст в земных годах, а возвращать возраст на Марсе. Возвращать функция должна целое число. Округлять ничего не надо. Просто отбрасываем дробную часть.
## Решение
```go
func mars_age(x int) int{
    return ((x*365)/687)
}
```
# 5 Указатели и структуры
5.1 Указатели

5.2 Передача указателей в функции

5.3 Структуры

5.4 Указатели на структуры

5.5 Методы

5.6 Вопросы к пятому модулю
___
## 5.3 Задача
Вам нужно создать структуру Car, которая должна иметь три поля: color и brand строчного типа, а также year целочисленного.
## Решение
```go
type Car struct {
    color string
    brand string
    year int
}
```
## 5.6 Задача
Вам нужно создать структуру Student, которая должна иметь два поля: name и university строчного типа.
## Решение
```go
type Student struct {
    name string
    university string
}
```
# 6 Массив, диапазон, карта
6.1 Массивы

6.2 Срезы (slice)

6.3 Диапазон (range)

6.4 Карта (maps)

6.5 Функции с переменным количеством аргументов

6.6 Вопросы к шестому модулю
___
## 6.1 Задача
Создайте массив name, который может хранить три строковые значения.
## Решение
```go
var name [3]string
```
## 6.3 Задача
Дан массив nums. Ваша задача написать цикл для перебора его значений с использованием range.  В цикле нужно посчитать сумму всех элементов. Для этого объявлена переменная sum.
## Решение
```go
sum := 0
for _,v := range nums {
    sum += v
}
```
## 6.4 Задача
Дополните (замените нижние подчеркивания) код, чтобы получилась правильная карта countries.
## Решение
```go
countries := map [string]string {
    "us": "USA",
    "fr": "France",
    "ch": "China"}
```
## 6.6 Задача
Вы создаете программу для анализа результатов спортивных матчей и подсчета очков заданной команды.
Результаты матчей хранятся в массиве results.
Каждый матч имеет один из следующих результатов:

"w" - выиграл

"l" - проиграл

"d" - ничья


Победа добавляет три очка, ничья - одно очко, а проигранный матч не добавляет очков.

Ваша программа должна принять на вход результат последнего матча и добавить его в массив результатов. После этого необходимо вычислить и вывести общее количество очков, набранных командой по результатам матчей из массива results.
## Решение
```go
package main

import "fmt"

func main() {
    results := []string{"w", "l", "w", "d", "w", "l", "l", "l", "d", "d", "w", "l", "w", "d"}
    var input string
    fmt.Scanln(&input)
    results = append(results, input)
    sum_results := 0
    for _, v:=range results{
       switch v {
           case "w":
           sum_results +=3
           case "d":
           sum_results +=1
           default:
           sum_results +=0
       }
    }
    fmt.Println(sum_results)
}
```
# 7 Многопоточность
7.1 введение в многопоточность

7.2 Горутины

7.3 Каналы

7.4 Выбор (Select)

7.5 Вопросы к седьмому модулю
___
##  7.5 Задача
Вы создаете программу для загрузки файлов.
Чтобы ускорить загрузку, вы решили использовать многопоточность. Каждая загрузка файла будет выполняться как отдельная горутина.

Для имитации загрузки файла функция download() должна принимать в качестве аргумента целое число (которое будет играть роль размера файла) и подсчитывать сумму всех целых чисел от 0 до этого числа (включительно).

Данная программа принимает три размера файлов в качестве входных данных и вызывает функцию download() как горутину для каждого файла.
Завершите программу, объявив функции download() и отправив результат их работы в main() с помощью каналов. Результаты работы трех функций должны быть сложены и выведены на экран.

>Вы можете использовать каналы, чтобы получить данные из функций download() и сложить их вместе.

## Решение
```go
package main
import "fmt"

func download(to int, ch chan int){
    result := 0
    for i:=0; i<=to; i++ {
        result += i
    }
    ch <- result
}


func main() {
    ch1 := make(chan int)
    ch2 := make(chan int)
    ch3 := make(chan int)

    var s1, s2, s3 int
    fmt.Scanln(&s1)
    fmt.Scanln(&s2)
    fmt.Scanln(&s3)

    go download(s1, ch1)
    go download(s2, ch2)
    go download(s3, ch3)

    //выведите сумму всех результатов
    fmt.Println(<-ch1 + <-ch2 + <-ch3)
}
```