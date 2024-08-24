# What is a Object
>Объект — это набор свойств, где каждое свойство ассоциировано с ключом (именем) и значением. Ключи — это строки (или символы), а значения могут быть любыми типами данных: числами, строками, массивами, функциями или даже другими объектами.
```js
const person = {
    name: "John",
    age: 30,
    isStudent: true,
    greet: function() {
        console.log("Hello!");
    }
    };
```
### Доступ к свойствам объекта
>Через точечную нотацию
```js
console.log(person.name); // "John"
person.greet(); // "Hello!"
```
>Через квадратные скобки
```js
console.log(person["name"]); // "John"
```
### Модификация объекта
>Добавление нового свойства:
```js
person.country = "Dushanbe";
```
>Изменение существующего свойства:
```js
person.age = 31;
```
>Удаление свойства
```js
delete person.isStudent;
```
### Перебор свойств объекта
>Для перебора свойств объекта часто используется цикл for...in:
```js
for (let key in person) {
    console.log(key, person[key]);
}
```
## Mетоды работы с объектами
### Object.keys(): Возвращает массив ключей объекта.
```js
console.log(Object.keys(person)); // ["name", "age", "greet", "country"]

```
### Object.values(): Возвращает массив значений объекта.
```js
console.log(Object.values(person)); // ["John", 31, ƒ, "USA"]
```
### Object.entries(): Возвращает массив пар [ключ, значение]
```js
console.log(Object.entries(person)); // [["name", "John"], ["age", 31], ["greet", ƒ], ["country", "USA"]]
```
