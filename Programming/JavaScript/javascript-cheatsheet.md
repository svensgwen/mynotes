# ⚡ JavaScript Cheat Sheet — Modern (ES6+)

![Javascript](../../Images/javascript.webp)

## 🚀 Basics
```js
let x = 10;       // block-scoped
const y = 20;     // cannot be reassigned
var z = 30;       // avoid (function-scoped)
```

## 📝 Data Types
```js
let n = 42;               // number
let s = "hello";          // string
let b = true;             // boolean
let u;                    // undefined
let v = null;             // null
let o = { a: 1 };         // object
let a = [1, 2, 3];        // array
let f = function() {};    // function
```

## 📤 Console
```js
console.log("hi");
console.error("error");
console.table({ a: 1, b: 2 });
```

## 🔁 Loops
```js
for (let i=0; i<5; i++) {}
while (x < 10) {}
do {} while (false);

// modern
for (const item of arr) {}
for (const key in obj) {}
arr.forEach(n => console.log(n));
```

## 🧩 Functions
```js
function add(a, b) { return a + b; }

// arrow function
const sub = (a, b) => a - b;

// default params
const mult = (x=1, y=1) => x * y;
```

## 🎁 Template Strings
```js
const name = "Shashank";
console.log(`Hello ${name}!`);
```

## 🫙 Objects
```js
const user = {
  name: "Bob",
  age: 20,
  greet() { console.log("hi"); }
};

user.name;
user["age"];
```

## ✨ Destructuring
```js
const { name, age } = user;
const [a1, a2] = [10, 20];
```

## 📦 Spread & Rest
```js
const arr = [1,2,3];
const arr2 = [...arr, 4];   // spread

function sum(...nums) {      // rest
  return nums.reduce((a,b)=>a+b);
}
```

## 🔗 Arrays
```js
arr.push(4);
arr.pop();
arr.shift();
arr.unshift(0);

arr.map(x => x * 2);
arr.filter(x => x > 2);
arr.reduce((a,b) => a+b, 0);
arr.find(x => x === 3);
```

## 🧮 Math & Random
```js
Math.floor(Math.random() * 10);
```

## 🧵 Promises
```js
const wait = ms => new Promise(res => setTimeout(res, ms));

wait(1000).then(() => console.log("done"));
```

## 🔥 async / await
```js
async function fetchData() {
  const res = await fetch("https://api.example.com");
  const data = await res.json();
  console.log(data);
}
```

## 📦 JSON
```js
JSON.stringify(obj);
JSON.parse(jsonStr);
```

## 🌐 Fetch API
```js
fetch(url)
  .then(r => r.json())
  .then(data => console.log(data));
```

## 🧱 Classes
```js
class Person {
  constructor(name) {
    this.name = name;
  }
  greet() { console.log("hi"); }
}
```

## 🗂️ Modules
```js
// export
export const pi = 3.14;
export default function hello() {}

// import
import hello, { pi } from "./file.js";
```

## 🧼 LocalStorage
```js
localStorage.setItem("key", "value");
localStorage.getItem("key");
localStorage.removeItem("key");
```

## 🌍 DOM Basics
```js
document.querySelector("h1");
document.querySelectorAll(".item");

const el = document.getElementById("app");
el.textContent = "Hello";
el.style.color = "red";
```

## 🎯 Events
```js
button.addEventListener("click", () => {
  console.log("clicked");
});
```

## ⚡ Short Tricks
```js
// ternary
let out = x > 10 ? "big" : "small";

// optional chaining
user?.profile?.email;

// nullish coalescing
let v = x ?? "default";
```

## 🧨 Errors
```js
try {
  throw new Error("oops");
} catch (e) {
  console.log(e.message);
}
```

## 🛠️ Node.js Quick Commands
```bash
npm init -y
npm install package
npm run dev
```

