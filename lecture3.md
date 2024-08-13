# String
>Строка — это примитивный тип, который содержит последовательность символов. Строка в Javascript записывается: double quotes(двойные кавычки) "", single quotes (одинарные кавычки)'', backticks(обратные кавычки) ``
```js
"Hello"
'Hello'
`Hello`${ifvj}
```
## What is a method in JS
>Метод — это блок кода, который выполняется только тогда, когда он вызывается.Можно передавать данные, известные как параметры, в метод. Методы используются для выполнения определённых действий, и они также известны как функции.
## JavaScript Methods (JavaScript методы)
### CharAt()
>CharAt() возвращает символ находяшийся на указаной позииции в строке
```js
let str = "Hello";
console.log(str.charAt(1)); // "e"

```
### at()
> at() Возвращает символ по заданному индексу. Поддерживает отрицательные индексы для обратного отсчета с конца строки.
```js
let str = "Hello";
console.log(str.at(-1)); // "o"
```
### concat()
> Объединяет две или более строк и возвращает новую строку.
```js
let str1 = "Hello";
let str2 = "World";
console.log(str1.concat(" ", str2)); // "Hello World"
```
### trim()
> Удаляет пространство (пробелы) с начало и конаца строки. 
```js
let str = "  Hello World  ";
console.log(str.trim()); // "Hello World"
```
### includes()
> Проверяет, содержит ли строка определенную подстроку, и возвращает true или false.
```js
let str = "Hello World";
console.log(str.includes("World")); // true
```
### indexof()
>Возвращает индекс первого вхождения указанного значения, либо -1, если значение не найдено.
```js
let str = "Hello World";
console.log(str.indexOf("World")); // 6
```
### replace()
> Заменяет первое совпадение указанного значения на новое.
```js
let str = "Hello World";
console.log(str.replace("World", "Everyone")); // "Hello Everyone"
```
### replaceAll()
>Заменяет все совпадения указанного значения на новое.
```js
let str = "Hello World, World";
console.log(str.replaceAll("World", "Everyone")); // "Hello Everyone, Everyone"
```
### repeat()
>Возвращает новую строку, содержащую указанное количество повторений строки, на которой был вызван метод.
```js
let str = "Hello ";
console.log(str.repeat(3)); // "Hello Hello Hello "
```
### slice()
>Метод slice() извлекает часть строки и возвращает новую строку без изменения оригинальной строки.
```js
let str = "Hello World";
console.log(str.slice(0, 5)); // "Hello"
```
### substring()
>Метод substring() возвращает подстроку строки между двумя индексами, или от одного индекса и до конца строки.
```js
let str = "Hello World";
console.log(str.substring(1, 4)); // "ell"
```
### split()
>Метод split() разбивает объект String на массив строк путём разделения строки указанной подстрокой.
```js
let str = "Hello World";
console.log(str.split(" ")); // ["Hello", "World"]
```
### toString()
>Метод toString() возвращает строку, представляющую указанный объек
```js
let num = 123;
console.log(num.toString()); // "123"
```
### toLowerCase()
> Преобразует строку в нижний регистр.
```js
let str = "Hello World";
console.log(str.toLowerCase()); // "hello world"
```
### toUpperCase()
>Преобразует строку в верхний регистр.
```js
let str = "Hello World";
console.log(str.toUpperCase()); // "HELLO WORLD"
```

