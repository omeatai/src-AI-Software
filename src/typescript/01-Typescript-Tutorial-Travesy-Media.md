# TYPESCRIPT TUTORIAL - TRAVESY MEDIA

## [COURSE](https://www.youtube.com/watch?v=BCg4U1FzODs&ab_channel=TraversyMedia)

<details>
  <summary>1. Introduction </summary>

# Introduction

<img width="1211" alt="image" src="https://github.com/omeatai/My-Tutorials/assets/32337103/058ab52d-783f-4cfc-8961-5a4dacee5f5a">
<img width="1211" alt="image" src="https://github.com/omeatai/My-Tutorials/assets/32337103/721c660a-353a-4112-ab67-e952b85c84a2">

# Install Typescript globally

```x
sudo npm i -g typescript
```

# Get current Typescript Version

```x
tsc -v
```

# #END </details>

<details>
  <summary>2. Compiling to javascript </summary>

# Compiling to javascript

```x
tsc index
tsc --watch index
```

### TS/crash-course/index.ts:

```ts
let id: number = 5;

id = 5;
```

### TS/crash-course/index.js:

```ts
var id = 5;
id = 5;
```

<img width="908" alt="image" src="https://github.com/omeatai/My-Tutorials/assets/32337103/2b70751a-7762-42ac-b700-4204b1681712">
<img width="908" alt="image" src="https://github.com/omeatai/My-Tutorials/assets/32337103/087d8c81-9258-4dce-935a-8153dae154fe">

# #END </details>

<details>
  <summary>3. Setup Typescript Config File </summary>

# Setup Typescript Config File

```tsbs
tsc --init
```

# Make changes to Config Options

### TS/crash-course/tsconfig.json:

```tsbs
"target": "ES6" /* Set the JavaScript language version for emitted JavaScript and include compatible library declarations. */,
"rootDir": "./src" /* Specify the root folder within your source files. */,
 "outDir": "./dist" /* Specify an output folder for all emitted files. */,
```

### TS/crash-course/src/index.ts:

```ts
let id: number = 5;

console.log("ID: ", id);
```

### TS/crash-course/dist/index.html:

```ts
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>My Website</title>
  </head>
  <body>
    <h1>Hello World</h1>
    <script src="./index.js"></script>
  </body>
</html>
```

# Run to Compile

```ts
tsc
tsc --watch
```

<img width="908" alt="image" src="https://github.com/omeatai/My-Tutorials/assets/32337103/3c3ef754-0737-48ae-a2e8-0211afa54ad0">
<img width="906" alt="image" src="https://github.com/omeatai/My-Tutorials/assets/32337103/0953fe57-b11f-4fcd-a548-bb0bb79cf295">
<img width="908" alt="image" src="https://github.com/omeatai/My-Tutorials/assets/32337103/0f2ce8d8-7c91-496a-8101-0a71cbb5202f">
<img width="908" alt="image" src="https://github.com/omeatai/My-Tutorials/assets/32337103/1a59b84e-2003-42f1-9cca-bc1bbe161353">
<img width="1214" alt="image" src="https://github.com/omeatai/My-Tutorials/assets/32337103/fbcc5ca6-09bc-4a30-b4af-d34c91b3a8a5">

# #END </details>

<details>
  <summary>4. Basic Typescript Types </summary>

# Basic Typescript Types

### TS/crash-course/src/index.ts:

```ts
// Basic Types
let id: number = 5;
let company: string = "Traversy Media";
let isPublished: boolean = true;
let x: any = "Hello";

let ids: number[] = [1, 2, 3, 4, 5];
let arr: any[] = [1, true, "Hello"];

// Tuple
let person: [number, string, boolean] = [1, "Brad", true];

// Tuple Array
let employee: [number, string][];

employee = [
  [1, "Brad"],
  [2, "John"],
  [3, "Jill"],
];
```

### TS/crash-course/dist/index.js:

```ts
"use strict";
// Basic Types
let id = 5;
let company = "Traversy Media";
let isPublished = true;
let x = "Hello";
let ids = [1, 2, 3, 4, 5];
let arr = [1, true, "Hello"];
// Tuple
let person = [1, "Brad", true];
// Tuple Array
let employee;
employee = [
    [1, "Brad"],
    [2, "John"],
    [3, "Jill"],
];
```

<img width="910" alt="image" src="https://github.com/omeatai/My-Tutorials/assets/32337103/c8e881be-50a7-44af-bc7e-206386182cb5">
<img width="910" alt="image" src="https://github.com/omeatai/My-Tutorials/assets/32337103/fd0cb2ff-27e9-4e89-9c51-64479a59ba98">

# #END </details>

<details>
  <summary>5. Typescript Unions and Enum </summary>

# Typescript Unions and Enum

### TS/crash-course/src/index.ts:

```ts
// Union
let pid: string | number;
pid = "22";
pid = 22;

// Enum
enum Direction1 {
  Up = 1,
  Down,
  Left,
  Right,
}

console.log(Direction1.Up); // 1
console.log(Direction1.Down); // 2

enum Direction2 {
  Up = "Up",
  Down = "Down",
  Left = "Left",
  Right = "Right",
}

console.log(Direction2.Up); // Up
console.log(Direction2.Down); // Down
```

### TS/crash-course/dist/index.js:

```ts
"use strict";
// Union
let pid;
pid = "22";
pid = 22;
// Enum
var Direction1;
(function (Direction1) {
    Direction1[Direction1["Up"] = 1] = "Up";
    Direction1[Direction1["Down"] = 2] = "Down";
    Direction1[Direction1["Left"] = 3] = "Left";
    Direction1[Direction1["Right"] = 4] = "Right";
})(Direction1 || (Direction1 = {}));
console.log(Direction1.Up);
console.log(Direction1.Down);
var Direction2;
(function (Direction2) {
    Direction2["Up"] = "Up";
    Direction2["Down"] = "Down";
    Direction2["Left"] = "Left";
    Direction2["Right"] = "Right";
})(Direction2 || (Direction2 = {}));
console.log(Direction2.Up);
console.log(Direction2.Down);
```

<img width="910" alt="image" src="https://github.com/omeatai/My-Tutorials/assets/32337103/f5c6e107-a89d-42f4-8687-022aad43a976">
<img width="910" alt="image" src="https://github.com/omeatai/My-Tutorials/assets/32337103/3282f9a7-5a4a-4adf-a88e-4d16d8bf99d1">

# #END </details>

<details>
  <summary>6. Typescript Objects </summary>

# Typescript Objects

### TS/crash-course/src/index.ts:

```ts
// Objects

const user1: {
  id: number;
  name: string;
} = {
  id: 1,
  name: "John",
};

// Setting Type
type User = {
  id: number;
  name: string;
};

const user2: User = {
  id: 1,
  name: "John",
};
```

### TS/crash-course/dist/index.js:

```ts
"use strict";
// Objects
const user1 = {
    id: 1,
    name: "John",
};
const user2 = {
    id: 1,
    name: "John",
};
```

<img width="910" alt="image" src="https://github.com/omeatai/My-Tutorials/assets/32337103/024a64db-0f11-4e83-bdcf-7d4161dd4751">
<img width="910" alt="image" src="https://github.com/omeatai/My-Tutorials/assets/32337103/0d50afe4-4f99-463d-96df-f6555e4d581b">

# #END </details>

<details>
  <summary>7. Typescript Type Assertion </summary>

# Typescript Type Assertion

### TS/crash-course/src/index.ts:

```ts
// Type Assertion
let cid: any = 1;

let customerId1 = <number>cid;
let customerId2 = cid as number;

customerId1 = 2;
customerId2 = 3;
```

### TS/crash-course/dist/index.js:

```ts
"use strict";
// Type Assertion
let cid = 1;
let customerId1 = cid;
let customerId2 = cid;
customerId1 = 2;
customerId2 = 3;
```

<img width="910" alt="image" src="https://github.com/omeatai/My-Tutorials/assets/32337103/e37eb1b6-26cd-433b-b490-8a5a0ba6b2ac">
<img width="910" alt="image" src="https://github.com/omeatai/My-Tutorials/assets/32337103/eafb0eb4-68da-4f8a-832f-e2d41f49f86a">

# #END </details>

<details>
  <summary>8. Typescript Functions </summary>

# Typescript Functions

### TS/crash-course/src/index.ts:

```ts
// Functions
function addNum(x: number, y: number): number {
  return x + y;
}

console.log(addNum(1, 2));

// Void
function log(message: string | number): void {
  console.log(message);
}
```

### TS/crash-course/dist/index.js:

```ts
"use strict";
// Functions
function addNum(x, y) {
    return x + y;
}
console.log(addNum(1, 2));
// Void
function log(message) {
    console.log(message);
}
```

<img width="910" alt="image" src="https://github.com/omeatai/My-Tutorials/assets/32337103/14d5b40d-0069-478c-93de-c16ba4c79819">
<img width="910" alt="image" src="https://github.com/omeatai/My-Tutorials/assets/32337103/7c8c89ba-57d6-4d89-b98a-65c3916fb964">

# #END </details>

<details>
  <summary>9. Typescript Interfaces </summary>

# Typescript Interfaces

### TS/crash-course/src/index.ts:

```ts
// Interfaces
interface UserInterface {
  readonly id: number;
  name: string;
  age?: number;
}

const user1: UserInterface = {
  id: 1,
  name: "John",
};

//Type
type Point = number | string;
const p1: Point = 1;

// Interface with Functions
interface MathFunc {
  (x: number, y: number): number;
}

const add: MathFunc = (x: number, y: number): number => x + y;
const sub: MathFunc = (x: number, y: number): number => x - y;
```

### TS/crash-course/dist/index.js:

```ts
"use strict";
const user1 = {
    id: 1,
    name: "John",
};
const p1 = 1;
const add = (x, y) => x + y;
const sub = (x, y) => x - y;
```

<img width="910" alt="image" src="https://github.com/omeatai/My-Tutorials/assets/32337103/ca4211fc-8bd2-4aa7-a93c-cb9ccf6c813a">
<img width="910" alt="image" src="https://github.com/omeatai/My-Tutorials/assets/32337103/c4efcf6d-3c40-44af-8723-62c3867a700e">

# #END </details>

<details>
  <summary>10. Typescript Classes </summary>

# Typescript Classes

### TS/crash-course/src/index.ts:

```ts
//Class Interface
interface PersonInterface {
  age: number;
  register(): string;
}

// Classes
class Person implements PersonInterface {
  private id: number;
  protected name: string;
  public age: number;

  constructor(id: number, name: string, age: number) {
    this.id = id;
    this.name = name;
    this.age = age;
    console.log(this.id, this.name, this.age);
  }

  register() {
    return `${this.name} is now registered`;
  }
}

const brad = new Person(1, "Brad Traddy", 30);
const mike = new Person(2, "Mike Jordan", 25);

console.log(brad, mike);
console.log(brad.age);
console.log(brad.register());

//SubClass
class Employee extends Person {
  position: string;

  constructor(id: number, name: string, age: number, position: string) {
    super(id, name, age);
    this.position = position;
  }
}

const emp = new Employee(3, "Shawn", 34, "Developer");
console.log(emp);
```

### TS/crash-course/dist/index.js:

```ts
"use strict";
// Classes
class Person {
    constructor(id, name, age) {
        this.id = id;
        this.name = name;
        this.age = age;
        console.log(this.id, this.name, this.age);
    }
    register() {
        return `${this.name} is now registered`;
    }
}
const brad = new Person(1, "Brad Traddy", 30);
const mike = new Person(2, "Mike Jordan", 25);
console.log(brad, mike);
console.log(brad.age);
console.log(brad.register());
//SubClass
class Employee extends Person {
    constructor(id, name, age, position) {
        super(id, name, age);
        this.position = position;
    }
}
const emp = new Employee(3, "Shawn", 34, "Developer");
console.log(emp);
```

<img width="910" alt="image" src="https://github.com/omeatai/My-Tutorials/assets/32337103/096f49aa-2c0d-47c8-9e7b-a96aa27350ec">
<img width="910" alt="image" src="https://github.com/omeatai/My-Tutorials/assets/32337103/9f960bdf-a3ac-49e6-99d6-5d9b90726d8f">

# #END </details>

<details>
  <summary>11. Typescript Generics </summary>

# Typescript Generics

### TS/crash-course/src/index.ts:

```ts
function getArray(items: any[]): any[] {
  return new Array().concat(items);
}

let numArray = getArray([1, 2, 3, 4]);
let strArray = getArray(["brad", "John", "Jill"]);

numArray.push("hello");
strArray.push(3);

// Generics
function getArray2<T>(items: T[]): T[] {
  return new Array().concat(items);
}

let numArray2 = getArray2<number>([1, 2, 3, 4]);
let strArray2 = getArray2<string>(["brad", "John", "Jill"]);

numArray2.push(5);
strArray2.push("Jane");
```

### TS/crash-course/dist/index.js:

```ts
"use strict";
function getArray(items) {
    return new Array().concat(items);
}
let numArray = getArray([1, 2, 3, 4]);
let strArray = getArray(["brad", "John", "Jill"]);
numArray.push("hello");
strArray.push(3);
// Generics
function getArray2(items) {
    return new Array().concat(items);
}
let numArray2 = getArray2([1, 2, 3, 4]);
let strArray2 = getArray2(["brad", "John", "Jill"]);
numArray2.push(5);
strArray2.push("Jane");
```

<img width="910" alt="image" src="https://github.com/omeatai/My-Tutorials/assets/32337103/eaab4b2d-2292-4284-9417-3c88b344cf46">
<img width="910" alt="image" src="https://github.com/omeatai/My-Tutorials/assets/32337103/bb4100ea-1da2-4103-b8d5-301231afcfea">

# #END </details>

<details>
  <summary>12. Typescript with React </summary>

# Typescript with React

<img width="910" alt="image" src="https://github.com/omeatai/My-Tutorials/assets/32337103/4e98c78b-1a2a-46a4-b031-39459420168d">
<img width="910" alt="image" src="https://github.com/omeatai/My-Tutorials/assets/32337103/16226a7c-5d30-4751-bc55-f91248094dbd">
<img width="1179" alt="image" src="https://github.com/omeatai/My-Tutorials/assets/32337103/3baaaaa8-f263-4717-bfe5-b711fe98fd46">

# Install React App with Typescript

```tsbs
npx create-react-app . --template typescript
npx create-react-app reactts-app --template typescript
OR
yarn create react-app reactts-app --template typescript
OR
yarn create react-app reactts-app
yarn add typescript @types/node @types/react @types/react-dom @types/jest
```

### TS/reactts-app/src/App.tsx:

```ts
import "./App.css";
import Header from "./Header";

function App() {
  return (
    <div className="App">
      <Header title="Hello World" color="red" />
    </div>
  );
}

export default App;
```

### TS/reactts-app/src/Header.tsx:

```ts
import React from "react";

export interface Props {
  title: string;
  color?: string;
}

const Header = (props: Props) => {
  return (
    <header>
      <h1 style={{ color: props.color ? props.color : "blue" }}>
        {props.title}
      </h1>
    </header>
  );
};

export default Header;
```

# #END </details>

# #END
