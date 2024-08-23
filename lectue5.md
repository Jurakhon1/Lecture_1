# What is Array in JavaScript
>Массив в JavaScript — это структура данных, используемая для хранения нескольких значений в одной переменной. Он может содержать различные типы данных и допускает динамическое изменение размера. Доступ к элементам осуществляется по их индексу, начиная с 0.
Элементы массива можно изменить, присвоив новое значение их соответствующему индексу.
# Array Methods
## pop()
>Метод pop() удаляет последний элемент из массива и возвращает его значение. Последний элемент массива или undefined, если массив пуст.
```js
let arr=["green","orange","yellow"]
let po=arr.pop()
console.log(arr)//["green","orange"]
console.log(po)//["yellow"]
```
### shift()
>Метод shift() удаляет первый элемент из массива и возвращает его значение. Этот метод изменяет длину массива.
```js
let arr=["green","orange","yellow"]
let po=arr.shift()
console.log(arr)//["orange","yellow"]
console.log(po)//["green"]
```
### push()
>Метод push() добавляет один или более элементов в конец массива и возвращает новую длину массива
```js
let arr=["green","orange","yellow"]
let ar2=arr.push("pink","blue")
console.log(arr)//['green','orange','yellow', 'pink','blue' ]
console.log(ar2)//5
```
### unshift()
>Метод unshift() добавляет один или более элементов в начало массива и возвращает новую длину массива.
```js
let arr=["green","orange","yellow"]
let ar2=arr.unshift("pink","blue")
console.log(arr) //["pink","blue","green","orange","yellow"]
console.log() //5
```
### concat()
> Метод concat() возвращает новый массив, состоящий из массива, на котором он был вызван, соединённого с другими массивами и/или значениями, переданными в качестве аргументов
```js
let arr1=['a','b','c']
let arr2=['d','e','f']
console.log(arr.concat(arr2))//[ 'a', 'b', 'c', 'd', 'e', 'f' ]
```
### slice()
> Метод slice() в JavaScript используется для извлечения части массива в новый массив, не изменяя оригинальный массив. Метод принимает два аргумента: начальный индекс (включительно) и конечный индекс (не включая). Если второй аргумент не указан, извлечение будет происходить до конца массива.
```js
let arr=["pink","blue","green","orange","yellow"]
console.log(arr.slice(0,3))//["pink","blue","green"]
```
### join()
>Метод join() в JavaScript используется для объединения всех элементов массива в одну строку. Элементы массива объединяются в строку с использованием указанного разделителя (по умолчанию разделителем является запятая).
```js
let arr=["pink","blue","green","orange","yellow"]
console.log(arr.join())//"pink","blue","green","orange","yellow"
console.log(arr.join("-"))//pink-blue-green-orange-yellow
```
### includes()
>Метод includes() экземпляров Array определяет, содержит ли массив определенное значение, возвращая true или false.
```js
 let arr=["pink","blue","green","orange","yellow"]
 console.log(arr.includes("blue"))//true
```
### indexOf()
>Метод indexOf() возвращает первый индекс, по которому данный элемент может быть найден в массиве или -1, если такого индекса нет.
```js
let arr=["pink","blue","green","orange","yellow"]
 console.log(arr.indexOf("blue"))//1
```
### splice()
>Метод splice() в JavaScript используется для изменения содержимого массива, добавляя, удаляя или заменяя элементы. Этот метод изменяет исходный массив и возвращает массив удалённых элементов.
```js
array.splice(start, deleteCount, item1, item2, ...);

let colors = ["red", "green", "blue"];
colors.splice(2, 0, "yellow", "purple");

console.log(colors); // ["red", "green", "yellow", "purple", "blue"]
```
### toString()
>Метод toString() в JavaScript используется для преобразования массива (или другого объекта) в строку, где все элементы массива объединяются и разделяются запятыми.
```js
let fruits = ["apple", "banana", "cherry"];
let String = fruits.toString();

console.log(String); // "apple,banana,cherry"
```
### toReversed()

>Метод toReversed() в JavaScript используется для создания нового массива, содержащего элементы исходного массива в обратном порядке. Важно отметить, что этот метод не изменяет исходный массив, а возвращает его изменённую копию.
toReversed() — это современный метод, предложенный для стандартов JavaScript. Он часто используется для работы с массивами в новых версиях языка.
```js
let numbers = [1, 2, 3, 4, 5];
let reversedNumbers = numbers.toReversed();
console.log(reversedNumbers); //  [5, 4, 3, 2, 1]
console.log(numbers);         //  [1, 2, 3, 4, 5]
```
## JavaScript array methods callbacks
>В JavaScript колбэк (или функция обратного вызова) — это функция, которая передается в другую функцию в качестве аргумента. Эта колбэк-функция будет выполнена после завершения выполнения основной функции. 
### forEach()
>Метод forEach() в JavaScript используется для выполнения указанной функции один раз для каждого элемента массива. Этот метод не возвращает новое значение, а просто выполняет указанное действие для каждого элемента.
```js
array.forEach(function(element, index, array) {
  // действие с элементом

  let fruits = ["apple", "banana", "cherry"];

fruits.forEach(function(fruit) {
    console.log(fruit);
});
});
// apple
// banana
// cherry
```
### map()
>Метод map() в JavaScript используется для создания нового массива, где каждый элемент является результатом выполнения указанной функции на соответствующем элементе исходного массива. В отличие от forEach(), map() возвращает новый массив, а исходный массив остаётся неизменным.
```js
let numbers = [1, 2, 3, 4, 5];
let doubledNumbers = numbers.map(function(number) {
    return number * 2;
});
console.log(doubledNumbers); //  [2, 4, 6, 8, 10]
console.log(numbers);        //  [1, 2, 3, 4, 5]
```
### find()
>Метод find() в JavaScript используется для поиска первого элемента в массиве, который удовлетворяет условию, заданному в функции обратного вызова. Если элемент найден, find() возвращает его значение; если нет — возвращает undefined.
```js
let numbers = [10, 20, 30, 40, 50];
let foundNumber = numbers.find(function(number) {
    return number > 25;
});
console.log(foundNumber); // 30
```
### filter()
>Метод filter() в JavaScript используется для создания нового массива, содержащего все элементы исходного массива, которые удовлетворяют условию, заданному в функции обратного вызова. В отличие от find(), который возвращает только первый элемент, filter() возвращает массив, содержащий все подходящие элементы.
```js
let numbers = [10, 20, 30, 40, 50];
let filteredNumbers = numbers.filter(function(number) {
    return number > 25;
});
console.log(filteredNumbers); // [30, 40, 50]
```
### reduce()
> Метод reduce() в JavaScript используется для последовательной обработки каждого элемента массива с целью вычисления единого значения, например, суммы, произведения, объединения данных и так далее. reduce() позволяет аккумулировать (накапливать) результат, который затем возвращается.
```js
let numbers = [1, 2, 3, 4, 5];
let sum = numbers.reduce(function(accumulator, currentValue) {
    return accumulator + currentValue;
}, 0);
console.log(sum); // 15
```
### toSorted()
>Метод toSorted() в JavaScript — это новый метод для создания отсортированной копии массива. Он похож на метод sort(), но с той разницей, что toSorted() не изменяет исходный массив, а возвращает новый отсортированный массив. Это помогает избежать изменения оригинального массива, что может быть важно при работе с неизменяемыми данными.  
```js
let numbers = [3, 1, 4, 1, 5, 9];
let sortedNumbers = numbers.toSorted();
console.log(sortedNumbers); //  [1, 1, 3, 4, 5, 9]
console.log(numbers);       //  [3, 1, 4, 1, 5, 9] 
```
### Destructuring
>Деструктуризация в JavaScript — это синтаксис, который позволяет извлекать значения из массивов или свойства из объектов. Это позволяет упростить и сделать более читаемым код, возвращая только необходимые значения.
```js
const numbers = [1, 2, 3];
const [first, second, third] = numbers;
console.log(first);  // 1
console.log(second); // 2
console.log(third);  // 3
```
### Spread
>Оператор расширения (spread operator) в JavaScript обозначается знаком трёх точек (...) и позволяет развернуть итерируемый объект (например, массив или строку) в местах, где ожидаются ноль или более аргументов. Он даёт возможность легко копировать все или часть существующего массива или объекта в другой массив или объект.
```js
const array1 = [1, 2];
const array2 = [3, 4];
const combinedArray = [...array1, ...array2];
console.log(combinedArray); // [1, 2, 3, 4]
```
### rest
>В JavaScript "rest" - это синтаксис параметра, позволяющий функции принимать неопределенное количество аргументов в виде массива. Он обозначается тремя точками (…). Используя параметр rest, можно обрабатывать все оставшиеся аргументы, переданные в функцию, что делает обработку переменного числа параметров более удобной и гибкой.
```js
function sum(...numbers) {
  return numbers.reduce((total, num) => total + num, 0);
}
console.log(sum(1, 2, 3));      // 6
console.log(sum(1, 2, 3, 4, 5)); // 15

```
### Every()
>every — это метод массивов в JavaScript, который проверяет, удовлетворяют ли все элементы массива условию, заданному в передаваемой функции. Если все элементы соответствуют условию, метод возвращает true, иначе — false.
```js
array.every(callback(element[, index[, array]])[, thisArg])

const numbers = [2, 4, 6, 8];
const allEven = numbers.every((num) => num % 2 === 0);
console.log(allEven); // true, потому что все элементы массива чётные
```
### some
>Метод some проверяет, удовлетворяет ли хотя бы один элемент массива условию, заданному в передаваемой функции. Возвращает true или false.
```js
array.some(callback(element[, index[, array]])[, thisArg])

const numbers = [1, 2, 3, 4, 5];
const hasNegative = numbers.some((num) => num < 0);
console.log(hasNegative); // false

```
### fill
>Метод fill заполняет все элементы массива статическим значением, начиная с начального индекса и заканчивая конечным индексом.
```js
array.fill(value[, start[, end]])

const arr = [1, 2, 3, 4, 5];
arr.fill(0, 2, 4);
console.log(arr); // [1, 2, 0, 0, 5]
```
### flat
>Метод flat создает новый массив, в котором все элементы вложенных массивов были рекурсивно "подняты" на указанный уровень глубины.
```js
const newArray = array.flat([depth])

const arr = [1, 2, [3, 4, [5, 6]]];
const flattened = arr.flat(2);
console.log(flattened); // [1, 2, 3, 4, 5, 6]

```
### from
>Метод from создает новый массив из подобного массива или итерируемого объекта.
```js
Array.from(arrayLike[, mapFn[, thisArg]])

const str = 'Hello';
const arr = Array.from(str);
console.log(arr); // ['H', 'e', 'l', 'l', 'o']

```