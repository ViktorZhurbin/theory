## Синтаксис расширения

`spread` 'раскрывает' массив - получаем несколько переменных из одной.
```js
var params = [ "hello", true, 7 ];
var other = [ 1, 2, ...params ]; // other => [1,2,"hello", true, 7]

// Here, ...params spreads so as to assing all of its elements to other
// Internally javaScript does following:
var other = [1, 2].concat(params);
```

 ```js
var abc = ['a', 'b', 'c'];
var def = ['d', 'e', 'f'];
var alpha = [ ...abc, ...def ];
console.log(alpha)// alpha == ['a', 'b', 'c', 'd', 'e', 'f'];
```

Spread позволяет расширять массивы или строки там, где ожидается ноль и более аргументов (при вызовах функции) или элементов (для массивов), или объекты там, где ожидается ноль и более пар ключ-значение.

```js
// function calls
myFunction(...iterableObj);

// array literals or strings
[...iterableObj, '4', 'five', 6];

// object literals (new in ECMAScript 2018)
let objClone = { ...obj };
```

### Функция

```js
function myFunction(x, y, z) { }
var args = [0, 1, 2];
myFunction(...args);

// Any argument in the argument list can use spread syntax
// and it can be used multiple times.
function myFunction(v, w, x, y, z) { }
var args = [0, 1];
myFunction(-1, ...args, 2, ...[3]);
```

### Массив

```js
var parts = ['shoulders', 'knees'];
var lyrics = ['head', ...parts, 'and', 'toes'];
// ["head", "shoulders", "knees", "and", "toes"]
```


### Объект

```js
var obj1 = { foo: 'bar', x: 42 };
var obj2 = { foo: 'baz', y: 13 };

var clonedObj = { ...obj1 };
// Object { foo: "bar", x: 42 }

var mergedObj = { ...obj1, ...obj2 };
// Object { foo: "baz", x: 42, y: 13 }
```