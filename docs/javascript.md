JavaScript 备忘清单
===

包含最重要概念、函数、方法等的 JavaScript 备忘单。 初学者的完整快速参考。

入门
----

### 介绍

JavaScript 是一种轻量级的解释型编程语言。

- [JSON 备忘清单](json.md)
- [JavaScript 中的正则表达式](/regex#regex-in-javascript)

### 打印调试

```javascript
// => Hello world!
console.log('Hello world!');
// => Hello QuickReference
console.warn('hello %s', 'QuickReference');
// 将错误消息打印到 stderr
console.error(new Error('Oops!'));
```

### 数字

```javascript
let amount = 6;
let price = 4.99;
```

### 变量

```javascript
let x = null;
let name = "Tammy";
const found = false;
// => Tammy, false, null
console.log(name, found, x);
var a;
console.log(a); // => undefined
```


### 字符串

```javascript
let single = 'Wheres my bandit hat?';
let double = "Wheres my bandit hat?";
// => 21
console.log(single.length);
```

### 算术运算符

```javascript
5 + 5 = 10     // 加法 Addition
10 - 5 = 5     // 加法 Subtraction
5 * 10 = 50    // 乘法 Multiplication
10 / 5 = 2     // 除法 Division
10 % 5 = 0     // 取模 Modulo
```


### 注释

```javascript
// 此行将表示注释
/* 
多行配置
部署前必须更改
以下配置。
*/
```

### 赋值运算符

```javascript
let number = 100;
// 两个语句都会加 10
number = number + 10;
number += 10;
console.log(number); 
// => 120
```

### 字符串插值

```javascript
let age = 7;
// 字符串拼接
'Tommy is ' + age + ' years old.';
// 字符串插值
`Tommy is ${age} years old.`;
```

### let 关键字

```javascript
let count; 
console.log(count); // => undefined
count = 10;
console.log(count); // => 10
```


### const 关键字

```javascript
const numberOfColumns = 4;
// TypeError: Assignment to constant...
numberOfColumns = 8;
```

JavaScript 条件
----


### if Statement (if 语句)

```javascript
const isMailSent = true;

if (isMailSent) {
  console.log('Mail sent to recipient');
}
```

### Ternary Operator (三元运算符)

```javascript
var x=1;

// => true
result = (x == 1) ? true : false;
```

### Operators
<!--rehype:data-warp-style=grid-row: span 2/span 2;-->

<!--rehype:-->
```javascript
true || false;       // true
10 > 5 || 10 > 20;   // true
false || false;      // false
10 > 100 || 10 > 20; // false
```

#### 逻辑运算符 &&

```javascript
true && true;        // true
1 > 2 && 2 > 1;      // false
true && false;       // false
4 === 4 && 3 > 1;    // true
```

#### 比较运算符

```javascript
1 > 3                 // false
3 > 1                 // true
250 >= 250            // true
1 === 1               // true
1 === 2               // false
1 === '1'             // false
```

#### 逻辑运算符 !

```javascript
let lateToWork = true;
let oppositeValue = !lateToWork;
// => false
console.log(oppositeValue); 
```

#### 空值合并运算符 ??

```javascript
null ?? 'I win';         //  'I win'
undefined ?? 'Me too';   //  'Me too'
false ?? 'I lose'        //  false
0 ?? 'I lose again'      //  0
'' ?? 'Damn it'          //  ''
```

### else if

```javascript
const size = 10;

if (size > 100) {
  console.log('Big');
} else if (size > 20) {
  console.log('Medium');
} else if (size > 4) {
  console.log('Small');
} else {
  console.log('Tiny');
}
// Print: Small
```

### switch 语句

```javascript
const food = 'salad';

switch (food) {
  case 'oyster':
    console.log('海的味道');
    break;
  case 'pizza':
    console.log('美味的馅饼');
    break;
  default:
    console.log('请您用餐');
}
```

### == vs ===

```javascript
0 == false   // true
0 === false  // false, 不同类型
1 == "1"     // true,  自动类型转换
1 === "1"    // false, 不同类型
null == undefined  // true
null === undefined // false
'0' == false       // true
'0' === false      // false
```

`==` 只检查值，`===` 检查值和类型。

JavaScript Functions 函数
----

### 函数

```javascript
// 定义函数：
function sum(num1, num2) {
  return num1 + num2;
}
// 调用函数：
sum(3, 6); // 9
```

### 匿名函数

```javascript
// Named function
function rocketToMars() {
  return 'BOOM!';
}
// Anonymous function
const rocketToMars = function() {
  return 'BOOM!';
}
```

### 箭头函数 (ES6)
<!--rehype:data-warp-style=grid-row: span 2/span 2;-->

#### 有两个参数

```javascript
const sum = (param1, param2) => { 
  return param1 + param2; 
}; 
console.log(sum(2,5)); // => 7 
```

#### 没有参数

```javascript
const printHello = () => { 
  console.log('hello'); 
}; 
printHello(); // => hello
```

#### 只有一个参数

```javascript
const checkWeight = weight => { 
  console.log(`Weight : ${weight}`); 
}; 
checkWeight(25); // => Weight : 25 
```

#### 简洁箭头函数

```javascript
const multiply = (a, b) => a * b; 
// => 60 
console.log(multiply(2, 30)); 
```

从 ES2015 开始提供[箭头函数](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions)

### 返回关键字

```javascript
// 有 return
function sum(num1, num2) {
  return num1 + num2;
}
// 该函数不输出总和
function sum(num1, num2) {
  num1 + num2;
}
```

### 调用函数

```javascript
// 定义函数
function sum(num1, num2) {
  return num1 + num2;
}
// 调用函数
sum(2, 4); // 6
```

### 函数表达式

```javascript
const dog = function() {
  return 'Woof!';
}
```

### 函数参数

```javascript
// 参数是 name
function sayHello(name) {
  return `Hello, ${name}!`;
}
```

### 函数声明

```javascript
function add(num1, num2) {
  return num1 + num2;
}
```

JavaScript 范围
----

### 范围

```javascript
function myFunction() {
  
  var pizzaName = "Margarita";
  // 这里的代码可以使用 PizzaName
  
}
// 这里的代码不能使用 PizzaName
```

### Block Scoped Variables

```javascript
const isLoggedIn = true;
if (isLoggedIn == true) {
  const statusMessage = 'Logged in.';
}
// Uncaught ReferenceError...
// 未捕获的引用错误...
console.log(statusMessage);
```

### 全局变量

```javascript
// 全局声明的变量
const color = 'blue';
function printColor() {
  console.log(color);
}
printColor(); // => blue
```

### `let` vs `var`

```javascript
for (let i = 0; i < 3; i++) {
  // 这是“let”的最大范围
  // i 可以访问 ✔️
}
// i 不能访问 ❌
```

---

```javascript
for (var i = 0; i < 3; i++) {
  // i 可以访问 ✔️
}
// i 可以访问 ✔️
```

`var` 的范围是最近的函数块，而 `let` 的范围是最近的封闭块。

### 带闭包的循环

```javascript
// 打印三次，不是我们的意思。
for (var i = 0; i < 3; i++) {
  setTimeout(_ => console.log(i), 10);
}
```

---

```javascript
// 按预期打印 0、1 和 2。
for (let j = 0; j < 3; j++) { 
  setTimeout(_ => console.log(j), 10);
}
```

变量使用 `let` 有自己的副本，变量有使用 `var` 的共享副本。

JavaScript Arrays
----


### 数组

```javascript
const fruits = ["apple", "orange", "banana"];
// 不同的数据类型
const data = [1, 'chicken', false];
```

### 属性 .length

```javascript
const numbers = [1, 2, 3, 4];
numbers.length // 4
```

### 索引

```javascript
// 访问数组元素
const myArray = [100, 200, 300];
console.log(myArray[0]); // 100
console.log(myArray[1]); // 200
```

### 可变图表

|           | add | remove | start | end |
|:----------|:---:|:------:|:-----:|:---:|
| `push`    | ✅  |        |       | ✅  |
| `pop`     |     | ✅     |       | ✅  |
| `unshift` | ✅  |        | ✅    |     |
| `shift`   |     | ✅     | ✅    |     |

### 方法 .push()

```javascript
// 添加单个元素：
const cart = ['apple', 'orange'];
cart.push('pear'); 
// 添加多个元素：
const numbers = [1, 2];
numbers.push(3, 4, 5);
```

将项目添加到末尾并返回新的数组长度。

### 方法 .pop()

```javascript
const fruits = ["apple", "orange", "banana"];
const fruit = fruits.pop(); // 'banana'
console.log(fruits); // ["apple", "orange"]
```

从末尾删除一个项目并返回已删除的项目。

### 方法 .shift()

```javascript
let cats = ['Bob', 'Willy', 'Mini'];
cats.shift(); // ['Willy', 'Mini']
```

从头删除一个项目并返回已删除的项目。

### 方法 .unshift()

```javascript
let cats = ['Bob'];
// => ['Willy', 'Bob']
cats.unshift('Willy');
// => ['Puff', 'George', 'Willy', 'Bob']
cats.unshift('Puff', 'George');
```

将项目添加到开头并返回新的数组长度。

### 方法 .concat()

```javascript
const numbers = [3, 2, 1]
const newFirstNumber = 4
    
// => [ 4, 3, 2, 1 ]
[newFirstNumber].concat(numbers)
    
// => [ 3, 2, 1, 4 ]
numbers.concat(newFirstNumber)
```

如果你想避免改变你的原始数组，你可以使用 concat。


JavaScript 循环
----

### While 循环

```javascript
while (condition) {
  // code block to be executed
}
let i = 0;
while (i < 5) {        
  console.log(i);
  i++;
}
```

### 反向循环

```javascript
const fruits = ["apple", "orange", "banana"];
for (let i = fruits.length - 1; i >= 0; i--) {
  console.log(`${i}. ${fruits[i]}`);
}
// => 2. banana
// => 1. orange
// => 0. apple
```

### Do...While 语句

```javascript
x = 0
i = 0
do {
  x = x + i;
  console.log(x)
  i++;
} while (i < 5);
// => 0 1 3 6 10
```

### For 循环

```javascript
for (let i = 0; i < 4; i += 1) {
  console.log(i);
};
// => 0, 1, 2, 3
```

### 遍历数组

```javascript
for (let i = 0; i < array.length; i++){
  console.log(array[i]);
}
// => 数组中的每一项
```

### Break

```javascript
for (let i = 0; i < 99; i += 1) {
  if (i > 5) {
     break;
  }
  console.log(i)
}
// => 0 1 2 3 4 5
```

### Continue

```javascript
for (i = 0; i < 10; i++) {
  if (i === 3) { continue; }
  text += "The number is " + i + "<br>";
}
```

### 嵌套循环

```javascript
for (let i = 0; i < 2; i += 1) {
  for (let j = 0; j < 3; j += 1) {
    console.log(`${i}-${j}`);
  }
}
```

### for...in 循环

```javascript
const fruits = ["apple", "orange", "banana"];
for (let index in fruits) {
  console.log(index);
}
// => 0
// => 1
// => 2
```

### for...of 循环

```javascript
const fruits = ["apple", "orange", "banana"];
for (let fruit of fruits) {
  console.log(fruit);
}
// => apple
// => orange
// => banana
```

JavaScript 迭代器(Iterators)
----
<!--rehype:data-body-style=grid-template-columns: repeat(2,minmax(0,1fr));-->

### 分配给变量的函数

```javascript
let plusFive = (number) => {
  return number + 5;  
};
// f 被赋值为 plusFive
let f = plusFive;
plusFive(3); // 8
// 由于 f 具有函数值，因此可以调用它。
f(9); // 14
```

### 回调函数

```javascript
const isEven = (n) => {
  return n % 2 == 0;
}
let printMsg = (evenFunc, num) => {
  const isNumEven = evenFunc(num);
  console.log(`${num} is an even number: ${isNumEven}.`)
}
// Pass in isEven as the callback function
printMsg(isEven, 4); 
// => The number 4 is an even number: True.
```

### 数组方法 .reduce()

```javascript
const numbers = [1, 2, 3, 4];
const sum = numbers.reduce((accumulator, curVal) => {  
  return accumulator + curVal;
});
console.log(sum); // 10
```

### 数组方法 .map()

```javascript
const members = ["Taylor", "Donald", "Don", "Natasha", "Bobby"];
const announcements = members.map((member) => {
  return member + " joined the contest.";
});
console.log(announcements);
```

### 数组方法 .forEach()

```javascript
const numbers = [28, 77, 45, 99, 27];
numbers.forEach(number => {  
  console.log(number);
}); 
```

### 数组方法 .filter()

```javascript
const randomNumbers = [4, 11, 42, 14, 39];
const filteredArray = randomNumbers.filter(n => {  
  return n > 5;
});
```

JavaScript 对象(Objects)
----
<!--rehype:data-body-style=grid-template-columns: repeat(2,minmax(0,1fr));-->

### 访问属性

```javascript
const apple = { 
  color: 'Green',
  price: { bulk: '$3/kg', smallQty: '$4/kg' }
};
console.log(apple.color);      // => Green
console.log(apple.price.bulk); // => $3/kg
```

### 命名属性

```javascript
// 无效键名示例
const trainSchedule = {
  // 由于单词之间的空格而无效。
  platform num: 10, 
  // 表达式不能是键。
  40 - 10 + 2: 30,
  // 除非用引号括起来，否则 + 号无效。
  +compartment: 'C'
}
```

### 不存在的属性

```javascript
const classElection = {
  date: 'January 12'
};
console.log(classElection.place); // undefined
```

### 可变的
<!--rehype:data-warp-style=grid-row: span 2/span 2;-->

<!--rehype:-->
```javascript
const student = {
  name: 'Sheldon',
  score: 100,
  grade: 'A',
}
console.log(student)
// { name: 'Sheldon', score: 100, grade: 'A' }
delete student.score
student.grade = 'F'
console.log(student)
// { name: 'Sheldon', grade: 'F' }
student = {}
// TypeError: TypeError：分配给常量变量。
```

### 赋值简写语法

```javascript
const person = {
  name: 'Tom',
  age: '22',
};
const {name, age} = person;
console.log(name); // 'Tom'
console.log(age);  // '22'
```

### 删除运算符

```javascript
const person = {
  firstName: "Matilda",
  age: 27,
  hobby: "knitting",
  goal: "learning JavaScript"
};
delete person.hobby; // or delete person[hobby];
console.log(person);
/*
{
  firstName: "Matilda"
  age: 27
  goal: "learning JavaScript"
}
*/
```

### 对象作为参数

```javascript
const origNum = 8;
const origObj = {color: 'blue'};
const changeItUp = (num, obj) => {
  num = 7;
  obj.color = 'red';
};
changeItUp(origNum, origObj);
// 将输出 8，因为整数是按值传递的。
console.log(origNum);
// 由于传递了对象，将输出“red”
// 通过引用，因此是可变的。
console.log(origObj.color);
```

### 速记对象创建

```javascript
const activity = 'Surfing';
const beach = { activity };
console.log(beach); // { activity: 'Surfing' }
```

### this 关键字

```javascript
const cat = {
  name: 'Pipey',
  age: 8,
  whatName() {
    return this.name  
  }
};
console.log(cat.whatName()); // => Pipey
```

### 工厂函数

```javascript
// 一个接受 'name'，'age' 和 'breed' 的工厂函数，
//  参数返回一个自定义的 dog 对象。
const dogFactory = (name, age, breed) => {
  return {
    name: name,
    age: age,
    breed: breed,
    bark() {
      console.log('Woof!');  
    }
  };
};
```

### 方法

```javascript
const engine = {
  // 方法简写，有一个参数
  start(adverb) {
    console.log(`The engine starts up ${adverb}...`);
  },  
  // 不带参数的匿名箭头函数表达式
  sputter: () => {
    console.log('The engine sputters...');
  },
};
engine.start('noisily');
engine.sputter();
```

### Getters 和 setters

```javascript
const myCat = {
  _name: 'Dottie',
  get name() {
    return this._name;  
  },
  set name(newName) {
    this._name = newName;  
  }
};
// 引用调用 getter
console.log(myCat.name);
// 赋值调用 setter
myCat.name = 'Yankee';
```

JavaScript Classes
----

### Static Methods

```javascript
class Dog {
  constructor(name) {
    this._name = name;  
  }
  
  introduce() { 
    console.log('This is ' + this._name + ' !');  
  }
  
  // A static method
  static bark() {
    console.log('Woof!');  
  }
}
const myDog = new Dog('Buster');
myDog.introduce();
// Calling the static method
Dog.bark();
```

### Class

```javascript
class Song {
  constructor() {
    this.title;
    this.author;
  }
  
  play() {
    console.log('Song playing!');
  }
}
const mySong = new Song();
mySong.play();
```

### Class Constructor

```javascript
class Song {
  constructor(title, artist) {
    this.title = title;
    this.artist = artist;
  }
}
const mySong = new Song('Bohemian Rhapsody', 'Queen');
console.log(mySong.title);
```

### Class Methods

```javascript
class Song {
  play() {
    console.log('Playing!');
  }
  
  stop() {
    console.log('Stopping!');
  }
}
```

### extends

```javascript
// Parent class
class Media {
  constructor(info) {
    this.publishDate = info.publishDate;
    this.name = info.name;
  }
}
// Child class
class Song extends Media {
  constructor(songData) {
    super(songData);
    this.artist = songData.artist;
  }
}
const mySong = new Song({ 
  artist: 'Queen', 
  name: 'Bohemian Rhapsody', 
  publishDate: 1975
});
```

JavaScript Modules
----
<!--rehype:data-body-style=grid-template-columns: repeat(2,minmax(0,1fr));-->

### Export 

```javascript
// myMath.js
// Default export
export default function add(x,y){
    return x + y
}
// Normal export
export function subtract(x,y){
    return x - y
}
// Multiple exports
function multiply(x,y){
    return x * y
}
function duplicate(x){
    return x * 2
}
export {
    multiply,
    duplicate
}
```

### Import 

```javascript
// main.js
import add, { subtract, multiply, duplicate } from './myMath.js';
console.log(add(6, 2)); // 8 
console.log(subtract(6, 2)) // 4
console.log(multiply(6, 2)); // 12
console.log(duplicate(5)) // 10
// index.html
<script type="module" src="main.js"></script>
```

### Export Module

```javascript
// myMath.js
function add(x,y){
    return x + y
}
function subtract(x,y){
    return x - y
}
function multiply(x,y){
    return x * y
}
function duplicate(x){
    return x * 2
}
// Multiple exports in node.js
module.exports = {
    add,
    subtract,
    multiply,
    duplicate
}
```

### 加载模块

```javascript
// main.js
const myMath = require('./myMath.js')
console.log(myMath.add(6, 2)); // 8 
console.log(myMath.subtract(6, 2)) // 4
console.log(myMath.multiply(6, 2)); // 12
console.log(myMath.duplicate(5)) // 10
```

JavaScript Promises
----
<!--rehype:data-body-style=grid-template-columns: repeat(2,minmax(0,1fr));-->

### Promise 状态 
<!--rehype:data-warp-style=grid-row: span 2/span 2;-->

<!--rehype:-->
```javascript
const promise = new Promise((resolve, reject) => {
  const res = true;
  // An asynchronous operation.
  if (res) {
    resolve('Resolved!');
  }
  else {
    reject(Error('Error'));
  }
});
promise.then((res) => console.log(res), (err) => console.error(err));
```

### 执行器函数

```javascript
const executorFn = (resolve, reject) => {
  resolve('Resolved!');
};
const promise = new Promise(executorFn);
```

### setTimeout()

```javascript
const loginAlert = () =>{
  console.log('Login');
};
setTimeout(loginAlert, 6000);
```

### .then() 方法

```javascript
const promise = new Promise((resolve, reject) => {    
  setTimeout(() => {
    resolve('Result');
  }, 200);
});
promise.then((res) => {
  console.log(res);
}, (err) => {
  console.error(err);
});
```

### .catch() 方法

```javascript
const promise = new Promise((resolve, reject) => {  
  setTimeout(() => {
    reject(Error('Promise Rejected Unconditionally.'));
  }, 1000);
});
promise.then((res) => {
  console.log(value);
});
promise.catch((err) => {
  console.error(err);
});
```

### Promise.all()

```javascript
const promise1 = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve(3);
  }, 300);
});
const promise2 = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve(2);
  }, 200);
});
Promise.all([promise1, promise2]).then((res) => {
  console.log(res[0]);
  console.log(res[1]);
});
```

### 避免嵌套的 Promise 和 .then()

```javascript
const promise = new Promise((resolve, reject) => {  
  setTimeout(() => {
    resolve('*');
  }, 1000);
});
const twoStars = (star) => {  
  return (star + star);
};
const oneDot = (star) => {  
  return (star + '.');
};
const print = (val) => {
  console.log(val);
};
// 将它们链接在一起
promise.then(twoStars).then(oneDot).then(print);
```

### 创建

```javascript
const executorFn = (resolve, reject) => {
  console.log('The executor function of the promise!');
};
const promise = new Promise(executorFn);
```

### 链接多个 .then()

```javascript
const promise = new Promise(resolve => setTimeout(() => resolve('dAlan'), 100));
promise.then(res => {
  return res === 'Alan' ? Promise.resolve('Hey Alan!') : Promise.reject('Who are you?')
}).then((res) => {
  console.log(res)
}, (err) => {
  console.error(err)
});
```

JavaScript Async-Await
----
<!--rehype:data-body-style=grid-template-columns: repeat(2,minmax(0,1fr));-->

### 异步

```javascript
function helloWorld() {
  return new Promise(resolve => {
    setTimeout(() => {
      resolve('Hello World!');
    }, 2000);
  });
}
const msg = async function() { // 异步函数表达式
  const msg = await helloWorld();
  console.log('Message:', msg);
}
const msg1 = async () => { // 异步箭头函数
  const msg = await helloWorld();
  console.log('Message:', msg);
}
msg(); // Message: Hello World! <-- 2 秒后
msg1(); // Message: Hello World! <-- 2 秒后
```

### 解决 Promises

```javascript
let pro1 = Promise.resolve(5);
let pro2 = 44;
let pro3 = new Promise(function(resolve, reject) {
  setTimeout(resolve, 100, 'foo');
});
Promise.all([pro1, pro2, pro3]).then(function(values) {
  console.log(values);
});
// expected => Array [5, 44, "foo"]
```

### 异步等待 Promises

```javascript
function helloWorld() {
  return new Promise(resolve => {
    setTimeout(() => {
      resolve('Hello World!');
    }, 2000);
  });
}
async function msg() {
  const msg = await helloWorld();
  console.log('Message:', msg);
}
msg(); // Message: Hello World! <-- 2 秒后
```

### 错误处理

```javascript
let json = '{ "age": 30 }'; // 数据不完整
try {
  let user = JSON.parse(json); // <-- 没有错误
  console.log( user.name ); // no name!
} catch (e) {
  console.error( "Invalid JSON data!" );
}
```

### 异步等待运算符

```javascript
function helloWorld() {
  return new Promise(resolve => {
    setTimeout(() => {
      resolve('Hello World!');
    }, 2000);
  });
}
async function msg() {
  const msg = await helloWorld();
  console.log('Message:', msg);
}
msg(); // Message: Hello World! <-- 2 秒后
```

JavaScript 请求
----

### JSON 

```JS
const jsonObj = {
  "name": "Rick",
  "id": "11A",
  "level": 4  
};
```

另见：[JSON 备忘单](./json)

### XMLHttpRequest

```javascript
const xhr = new XMLHttpRequest();
xhr.open('GET', 'mysite.com/getjson');
```

`XMLHttpRequest` 是一个浏览器级别的 API，它使客户端能够通过 JavaScript 编写数据传输脚本，而不是 JavaScript 语言的一部分。

### GET

```javascript
const req = new XMLHttpRequest();
req.responseType = 'json';
req.open('GET', '/getdata?id=65');
req.onload = () => {
  console.log(xhr.response);
};
req.send();
```

### POST
<!--rehype:data-warp-style=grid-row: span 2/span 2;-->

<!--rehype:-->
```javascript
const data = {
  fish: 'Salmon',
  weight: '1.5 KG',
  units: 5
};
const xhr = new XMLHttpRequest();
xhr.open('POST', '/inventory/add');
xhr.responseType = 'json';
xhr.send(JSON.stringify(data));
xhr.onload = () => {
  console.log(xhr.response);
};
```

### fetch api
<!--rehype:data-warp-style=grid-row: span 2/span 2;-->

<!--rehype:-->
```javascript
fetch(url, {
    method: 'POST',
    headers: {
      'Content-type': 'application/json',
      'apikey': apiKey
    },
    body: data
  }).then(response => {
    if (response.ok) {
      return response.json();
    }
    throw new Error('Request failed!');
  }, networkError => {
    console.log(networkError.message)
  })
}
```

### JSON 格式

```javascript
fetch('url-that-returns-JSON')
.then(response => response.json())
.then(jsonResponse => {
  console.log(jsonResponse);
});
```

### promise url 参数获取 API

```javascript
fetch('url')
.then(
  response  => {
    console.log(response);
  },
 rejection => {
    console.error(rejection.message);
);
```

### Fetch API 函数

```javascript
fetch('https://api-xxx.com/endpoint', {
  method: 'POST',
  body: JSON.stringify({id: "200"})
}).then(response => {
  if(response.ok){
	  return response.json();  
  }
	throw new Error('Request failed!');
}, networkError => {
  console.log(networkError.message);
}).then(jsonResponse => {
  console.log(jsonResponse);
})
```

### async await 语法
<!--rehype:data-warp-style=grid-column: span 2/span 2;-->

<!--rehype:-->
```javascript
const getSuggestions = async () => {
  const wordQuery = inputField.value;
  const endpoint = `${url}${queryParams}${wordQuery}`;
  try{
    const response = await fetch(endpoint, {cache: 'no-cache'});
    if(response.ok){
      const jsonResponse = await response.json()
    }
  }
  catch(error){
    console.log(error)
  }
}
```