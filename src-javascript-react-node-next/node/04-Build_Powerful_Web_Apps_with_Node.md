## +Linkedin-Build Powerful Web Apps with Node.js

## [COURSE](https://www.linkedin.com/learning/express-essentials-build-powerful-web-apps-with-node-js)

<details>
<summary>1. Check Node and npm version </summary>

# Check Node and npm version

```x
node -v
npm -v
```

<img width="1397" alt="image" src="https://github.com/user-attachments/assets/fd768588-8a3e-4251-b35c-42a9963b381e">


# #END</details>

<details>
<summary>2. Using Express Application Generator to creact an Example Project </summary>

# Using Express Application Generator to creact an Example Project

## [https://expressjs.com/en/starter/generator.html](https://expressjs.com/en/starter/generator.html)

![image](https://github.com/user-attachments/assets/2e952a6c-be2a-4ce6-b136-e4b362e2c02a)

## Create Project Folder

```x
mkdir example_project
cd example_project
```

## Create Express App with Application Generator

```x
npx express-generator --git --view=hbs example_app
```

```x
npm install express-generator
express --git --view=hbs example_app
```

## Install dependencies

```x
cd example_app
npm install
```

## On MacOS or Linux, run the app with this command

```x
DEBUG=example_app:* npm start
```

## Create Script to Run App

### src-AI-Software/my_projects/01_Build_Powerful_Web_Apps_with_Node/example_project/example_app/package.json:

```json
{
  "name": "example-app",
  "version": "0.0.0",
  "private": true,
  "scripts": {
    "start": "node ./bin/www",
    "dev": "DEBUG=example_app:* npm start"
  },
  "dependencies": {
    "cookie-parser": "^1.4.4",
    "debug": "^2.6.9",
    "express": "^4.16.1",
    "hbs": "^4.0.4",
    "http-errors": "^1.6.3",
    "morgan": "^1.9.1"
  }
}
```

## Run App

```x
npm run dev
```

### src-AI-Software/my_projects/01_Build_Powerful_Web_Apps_with_Node/example_project/example_app/app.js:

```js
var createError = require('http-errors');
var express = require('express');
var path = require('path');
var cookieParser = require('cookie-parser');
var logger = require('morgan');

var indexRouter = require('./routes/index');
var usersRouter = require('./routes/users');

var app = express();

// view engine setup
app.set('views', path.join(__dirname, 'views'));
app.set('view engine', 'hbs');

app.use(logger('dev'));
app.use(express.json());
app.use(express.urlencoded({ extended: false }));
app.use(cookieParser());
app.use(express.static(path.join(__dirname, 'public')));

app.use('/', indexRouter);
app.use('/users', usersRouter);

// catch 404 and forward to error handler
app.use(function(req, res, next) {
  next(createError(404));
});

// error handler
app.use(function(err, req, res, next) {
  // set locals, only providing error in development
  res.locals.message = err.message;
  res.locals.error = req.app.get('env') === 'development' ? err : {};

  // render the error page
  res.status(err.status || 500);
  res.render('error');
});

module.exports = app;

```

### src-AI-Software/my_projects/01_Build_Powerful_Web_Apps_with_Node/example_project/example_app/routes/index.js:

```js
var express = require("express");
var router = express.Router();

/* GET home page. */
router.get("/", function (req, res, next) {
  res.render("index", { title: "Express" });
});

module.exports = router;

```

### src-AI-Software/my_projects/01_Build_Powerful_Web_Apps_with_Node/example_project/example_app/views/index.hbs:

```hbs
<h1>{{title}}</h1>
<p>Welcome to {{title}}</p>

```

![image](https://github.com/user-attachments/assets/53ad2975-7e46-41f8-97fb-78c6c5a5e3eb)

<img width="1397" alt="image" src="https://github.com/user-attachments/assets/57232fde-e820-44c4-adeb-048532b84bd9">
<img width="1397" alt="image" src="https://github.com/user-attachments/assets/42cb7369-acba-4039-9565-92ee0a269a49">
<img width="1397" alt="image" src="https://github.com/user-attachments/assets/8e5c90cb-1026-4d9f-975d-b89221f9c9c9">
<img width="1397" alt="image" src="https://github.com/user-attachments/assets/3e9523a7-e376-4756-be30-e8ec718799d8">
<img width="1397" alt="image" src="https://github.com/user-attachments/assets/94935ea0-e41d-49cc-9cf7-71b097b5b86d">

# #END</details>

<details>
<summary>3. Setup Basic Express Project - express_project </summary>

# Setup Basic Express Project - express_project

## Create Project Folder

```x
mkdir express_project
cd express_project
```

## Initialize npm Project

```x
npm init -y
```

### src-AI-Software/my_projects/01_Build_Powerful_Web_Apps_with_Node/express_project/package.json:

```json
{
  "name": "express_project",
  "version": "1.0.0",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "description": ""
}

```

## install Dependencies - Express and Nodemon, @babel/core, @babel/cli, @babel/preset-env and @babel/node

```x
npm install --save express nodemon
npm install --save-dev @babel/core @babel/cli @babel/preset-env @babel/node
```

```x
{
  "name": "express_project",
  "version": "1.0.0",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "description": "",
  "dependencies": {
    "express": "^4.19.2",
    "nodemon": "^3.1.4"
  },
  "devDependencies": {
    "@babel/cli": "^7.24.8",
    "@babel/core": "^7.24.9",
    "@babel/node": "^7.24.8",
    "@babel/preset-env": "^7.24.8"
  }
}
```

## Create babel file

```x
touch .babelrc
```

### src-AI-Software/my_projects/01_Build_Powerful_Web_Apps_with_Node/express_project/.babelrc:

```x
{
    "presets": [
        "@babel/preset-env"
    ]
}
```

<img width="1397" alt="image" src="https://github.com/user-attachments/assets/5fe7b8e8-ca9f-46e2-83d5-c23b8ee2b1eb">
<img width="1397" alt="image" src="https://github.com/user-attachments/assets/05afcdc8-d29b-48aa-99f1-338ec35eb9be">

# #END</details>

<details>
<summary>4. Setup Package.json file with ES6 module and scripts </summary>

# Setup Package.json file with ES6 module and scripts

### src-AI-Software/my_projects/01_Build_Powerful_Web_Apps_with_Node/express_project/package.json:

```js
{
  "name": "express_project",
  "type": "module",
  "version": "1.0.0",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "start": "nodemon --experimental-json-modules --exec babel-node index.js"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "description": "",
  "dependencies": {
    "express": "^4.19.2",
    "nodemon": "^3.1.4"
  },
  "devDependencies": {
    "@babel/cli": "^7.24.8",
    "@babel/core": "^7.24.9",
    "@babel/node": "^7.24.8",
    "@babel/preset-env": "^7.24.8"
  }
}
```

## Create Entry File: index.js

```x
touch index.js
```

### src-AI-Software/my_projects/01_Build_Powerful_Web_Apps_with_Node/express_project/index.js:

```js
import express from "express";

const app = express();

const PORT = 3000;

app.listen(PORT, () => {
  console.log(`Server running on port ${PORT}`);
});

```

## Run Server:

```x
npm run start
```

<img width="1397" alt="image" src="https://github.com/user-attachments/assets/f91afc08-cb4b-479c-aa82-d6656f20fa67">
<img width="1397" alt="image" src="https://github.com/user-attachments/assets/9929c67d-d63e-4544-a601-bf08155941b1">
<img width="1397" alt="image" src="https://github.com/user-attachments/assets/867a7fdf-3be7-4695-88e9-c9f975ff4dcf">

# #END</details>

<details>
<summary>5. Generating Mock Data for Server </summary>

# Generating Mock Data for Server

[https://www.mockaroo.com/](https://www.mockaroo.com/)

![image](https://github.com/user-attachments/assets/0d716a52-796d-49a3-aabd-c263da6b3a10)

<img width="1397" alt="image" src="https://github.com/user-attachments/assets/3b15ad81-6c6e-4b48-a2b1-d589462982fc">
<img width="1397" alt="image" src="https://github.com/user-attachments/assets/c2588be1-677a-43de-9837-cb021dc2351f">

### src-AI-Software/my_projects/01_Build_Powerful_Web_Apps_with_Node/express_project/data/mock.json:

```x
[
    {
        "id": 1,
        "first_name": "Eada",
        "last_name": "Parren",
        "email": "eparren0@tuttocitta.it"
    },
    {
        "id": 2,
        "first_name": "Renato",
        "last_name": "Sutherby",
        "email": "rsutherby1@bigcartel.com"
    },
    {
        "id": 3,
        "first_name": "Joshuah",
        "last_name": "Abercrombie",
        "email": "jabercrombie2@blog.com"
    },
    {
        "id": 4,
        "first_name": "Sutton",
        "last_name": "Ferronier",
        "email": "sferronier3@yale.edu"
    },
    ...........
]
```

### src-AI-Software/my_projects/01_Build_Powerful_Web_Apps_with_Node/express_project/index.js:

```js
import express from "express";
import data from "./data/mock.json" with { type: "json" };

const app = express();

const PORT = 3000;

app.listen(PORT, () => {
  console.log(`Server running on port ${PORT}`);
  console.log("Press CTRL+C to stop server");
  console.log(data);
});

```

```x
➜  express_project git:(main) ✗ npm run start

> express_project@1.0.0 start
> nodemon --experimental-json-modules --exec babel-node index.js

[nodemon] 3.1.4
[nodemon] to restart at any time, enter `rs`
[nodemon] watching path(s): *.*
[nodemon] watching extensions: js,mjs,cjs,json
[nodemon] starting `babel-node --experimental-json-modules index.js`
(node:31564) ExperimentalWarning: Importing JSON modules is an experimental feature and might change at any time
(Use `node --trace-warnings ...` to show where the warning was created)
Server running on port 3000
Press CTRL+C to stop server
[
  {
    id: 1,
    first_name: 'Eada',
    last_name: 'Parren',
    email: 'eparren0@tuttocitta.it'
  },
  {
    id: 2,
    first_name: 'Renato',
    last_name: 'Sutherby',
    email: 'rsutherby1@bigcartel.com'
  },
  {
    id: 3,
    first_name: 'Joshuah',
    last_name: 'Abercrombie',
    email: 'jabercrombie2@blog.com'
  },
  {
    id: 4,
    first_name: 'Sutton',
    last_name: 'Ferronier',
    email: 'sferronier3@yale.edu'
  },
  ..........
]
```

<img width="1397" alt="image" src="https://github.com/user-attachments/assets/7709ec54-6201-4eec-a4ca-decf6f350d4a">
<img width="1397" alt="image" src="https://github.com/user-attachments/assets/431e37e6-cfc2-4a56-b984-ea2bb6a8d1f7">

![image](https://github.com/user-attachments/assets/a51f9afd-23d2-4350-b866-be1c27ed48d7)

# #END</details>

<details>
<summary>6. Create HTTP Routes for Server </summary>

# Create HTTP Routes for Server

```js

```

```js

```

```js

```

```js

```

```js

```

```js

```

```js

```

```js

```

```js

```

```js

```

```js

```

```js

```

```js

```

```js

```

```js

```

```js

```

```js

```

```js

```

# #END</details>

