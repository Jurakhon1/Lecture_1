# new Date ()
>new Date() в JavaScript — это конструктор, используемый для создания объектов даты. Эти объекты даты позволяют работать с датами и временем в JavaScript. Объект Date предоставляет несколько методов для работы с датами, включая получение и установку года, месяца, дня, часа, минуты, секунды и миллисекунды.
## Создание объектов даты
>new Date() Если конструктор вызывается без аргументов, он создаёт объект, представляющий текущую дату и время.
```js
const now = new Date();
console.log(now); // Текущая дата и время
```
>new Date(milliseconds) Создает объект даты, представляющий время, указанное в миллисекундах, прошедших с 1 января 1970 года (время Unix-эпохи)
```js
const dateFromMilliseconds = new Date(1609459200000); //1 января 2021 года
console.log(dateFromMilliseconds);
```
>new Date(dateString) Принимает строку, представляющую дату (например, в формате ISO или других форматах, поддерживаемых методом), и создает объект даты на основе этой строки.
```js
const dateFromString = new Date('2024-12-31');
console.log(dateFromString); // 31 декабря 2024 года
```
>new Date(year, monthIndex, [day, hour, minute, second, millisecond]) Создает объект даты с использованием указанных значений года, месяца (начиная с 0), дня и времени. Параметры дня и времени необязательны.
```js
const specificDate = new Date(2023, 11, 31); // Месяц 11 — это декабрь, потому что январь имеет индекс 0
console.log(specificDate); // 31 декабря 2023 года
```
## Методы объекта Date()
### getFullYear() — возвращает год (4 цифры).
```js
let date = new Date();
console.log('Год:', date.getFullYear());
```
### getMonth() — возвращает месяц (от 0 до 11).
```js
let date = new Date();
console.log('Месяц:', date.getMonth() + 1); // +1, так как месяцы начинаются с 0
```
### getDate() — возвращает день месяца (от 1 до 31).
```js
let date = new Date();
onsole.log('День:', date.getDate());
```
### getHours() — возвращает час (от 0 до 23).
```js
let date = new Date();
console.log('Часы:', date.getHours());
```
### getMinutes() — возвращает минуты (от 0 до 59).
```js
let date = new Date();
console.log('Минуты:', date.getMinutes());
```
### getSeconds() — возвращает секунды (от 0 до 59).
```js
let date = new Date();
console.log('Год:', date.Seconds());
```
### getMilliseconds() — возвращает миллисекунды (от 0 до 999).
```js
let date = new Date();
console.log('Год:', date.Milliseconds());
```
### getTime() — возвращает количество миллисекунд с 1 января 1970 года.
```js
let date = new Date();
console.log('Год:', date.getTime());
```
### setFullYear(year, [month], [day]) — устанавливает год, месяц и день.
```js
const myDate = new Date();
myDate.setFullYear(2025);
console.log(myDate); // Дата с годом 2025
```
### setMonth(month) — устанавливает месяц (0 = январь, 11 = декабрь).
```js
myDate.setMonth(11); // Устанавливает декабрь
console.log(myDate);
```
### setDate(day) — устанавливает день месяца.
```js
myDate.setHours(10); // Устанавливает 10 часов
console.log(myDate);
```
### setHours(hours) — устанавливает часы.
```js
myDate.setHours(10); // Устанавливает 10 часов
console.log(myDate);
```
### setMinutes(minutes) — устанавливает минуты.
```js
myDate.setMinutes(30); // Устанавливает 30 минут
console.log(myDate);
```
### setSeconds(seconds) — устанавливает секунды.
```js
myDate.setSeconds(45); // Устанавливает 45 секунд
console.log(myDate);
```
### setMilliseconds(milliseconds) — устанавливает миллисекунды.
```js
myDate.setMilliseconds(500); // Устанавливает 500 миллисекунд
console.log(myDate);
```
### setTime(milliseconds) — устанавливает время в миллисекундах с 1 января 1970 года (Unix время).
```js
myDate.setTime(1600000000000); // Устанавливает время
console.log(myDate);
```
# Map ()
>Map в JavaScript — это встроенный объект, который представляет коллекцию ключ-значение. В отличие от обычных объектов (Object), где ключи могут быть только строками или символами, в Map ключами могут быть значения любого типа — строки, числа, объекты и даже другие функции.
## Основные особенности Map
>Любой тип ключей: В Map ключами могут быть любые типы данных, в том числе объекты и функции.

>Порядок добавления: Map запоминает порядок вставки элементов, поэтому элементы будут обходиться в порядке их добавления.

>Размер коллекции: Map предоставляет свойство size, которое возвращает количество элементов в коллекции.
### Создание
```js
let map=new Map()
// c данными
let map = new Map([
  ['ключ1', 'значение1'],
  ['ключ2', 'значение2'],
  [42, 'числовой ключ']
]);
```
## Основные методы Map
### set(key, value) — добавляет элемент с заданным ключом и значением в коллекцию Map. Если ключ уже существует, его значение будет обновлено.
```js
let map = new Map([
  ['ключ1', 'значение1'],
  ['ключ2', 'значение2'],
  [42, 'числовой ключ']
]);

map.set('ключ3', 'значение3');
```
### get(key) — возвращает значение, связанное с указанным ключом. Если ключ не найден, возвращает undefined.
```js
console.log(map.get('ключ1')); // "значение1"
```
### has(key) — возвращает true, если ключ присутствует в коллекции, иначе false.
```js
console.log(map.has('ключ2')); // true
```
### delete(key) — удаляет элемент по указанному ключу. Возвращает true, если элемент был успешно удален, иначе false.
```py
map.delete('ключ3')
```
### clear() — удаляет все элементы из Map.
```py
map.clear()
```
### size — возвращает количество элементов в Map.
```js
console.log(map.size); // 0
```
## Итерация по Map
>Map является итерируемым объектом, поэтому можно использовать конструкции для перебора элементов:
### for..of для перебора ключей и значений:
```js
let map= new Map([
    ["name","Bob"],
    [true,30],
    [{ city: 'New York' }, 'City object']
    
])
for(let [key, value] of map)
{
  console.log(`${key}: ${value}`);
  
}  // name: Bob true: 30 [object Object]: City object
```
### map.keys() — возвращает итерируемый объект для ключей.
```js
let map= new Map([
    ["name","Bob"],
    [true,30],
    [{ city: 'New York' }, 'City object']
])
for(let key of map.keys())
{
  console.log(`${key}`); //name true [object Object]
}
```
### map.values() — возвращает итерируемый объект для значений.
```js
let map= new Map([
    ["name","Bob"],
    [true,30],
    [{ city: 'New York' }, 'City object']
])
for(let key of map.values())
{
  console.log(`${key}`); //Bob 30 City object
} 
```
### map.entries() — возвращает итерируемый объект для пар [ключ, значение].
```js
let map= new Map([
    ["name","Bob"],
    [true,30],
    [{ city: 'New York' }, 'City object']
])
for(let [key, value ]of map.entries())
{
  console.log(`${key}: ${value}`); //name: Bob true: 30[object Object]: City object
}
```
## Преимущества Map над обычными объектами
>Тип ключей: Позволяет использовать любые типы данных в качестве ключей.

>Производительность: Быстрее для частых операций вставки и поиска, особенно при большом количестве элементов.

>Сохранение порядка: Сохраняет порядок добавления элементов, что может быть важно в некоторых случаях.

## new Set()
>Set в JavaScript — это встроенный объект, который представляет коллекцию уникальных значений. В Set каждое значение может появляться только один раз, что делает его идеальным для хранения уникальных элементов.
## Основные особенности Set
>Уникальные значения: Set автоматически удаляет дублирующиеся значения.
Любой тип данных: В Set могут храниться значения любого типа, включая примитивы (строки, числа и т.д.) и объекты.
Итерируемость: Set является итерируемым объектом, что позволяет использовать циклы и другие методы для работы с его элементами.
### Создание и использование Set
>Создание пустого объекта Set:
```js
const set = new Set();

// с данными
const set = new Set([1, 2, 3, 4, 5, 5, 6]); // Дубликаты будут удалены автоматически
console.log(set); // Set(6) {1, 2, 3, 4, 5, 6}
```
## Основные методы Set
### add(value) — добавляет элемент в Set. Если элемент уже присутствует, Set не изменяется.
```js
set.add(7);
set.add(1); // 1 уже существует, не добавится снова
console.log(set); // Set(7) {1, 2, 3, 4, 5, 6, 7}
```
### delete(value) — удаляет элемент из Set. Возвращает true, если элемент был удален, иначе false.
```js
set.delete(3);
console.log(set); // Set(6) {1, 2, 4, 5, 6, 7}
```
### has(value) — возвращает true, если элемент присутствует в Set, иначе false.
```js
console.log(set.has(4)); // true
console.log(set.has(10)); // false
```
### clear() — удаляет все элементы из Set.
```js
set.clear();
console.log(set); // Set(0) {}
```
### size — возвращает количество элементов в Set.
```js
console.log(set.size); // 0
```
## Итерация по Set
>Поскольку Set является итерируемым объектом, можно использовать различные конструкции для перебора его элементов:
### for..of для перебора значений:
```js
for (const value of set) {
  console.log(value);
}
```
### set.keys() — возвращает итерируемый объект для значений (аналогично values()).
```js
for (const key of set.keys()) {
  console.log(key);
}
```
### set.values() — возвращает итерируемый объект для значений.
```js
for (const value of set.values()) {
  console.log(value);
}
```
### set.entries() — возвращает итерируемый объект для пар [value, value] (используется для совместимости с Map).
```js
for (const [key, value] of set.entries()) {
  console.log(key, value); // key и value будут одинаковыми
}
```
## Преимущества Set над массивами
>Уникальность значений: Set автоматически удаляет дублирующиеся значения, что удобно для хранения уникальных элементов.

>Быстрая проверка наличия: Метод has работает быстрее для проверки существования элемента в коллекции, чем аналогичный метод в массиве.

>Упрощенная работа с большими объемами данных: Set часто имеет лучшую производительность для операций добавления, удаления и поиска элементов.