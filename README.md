Curriculum <br>
**Short Specializations** <br>

# 0x00. ES6 Basics

`JavaScript` `ES6`

#### Concepts

_For this project, look at these concepts:_

* [Modern JavaScript](https://intranet.alxswe.com/concepts/541)
* [Software Linter](https://intranet.alxswe.com/concepts/542)

## Resourses

**Read or watch:**

* [ECMAScript 6 - ECMAScript 2015]()
* [Statements and declarations]()
* [Arrow functions]()
* [Default parameters]()
* [Rest parameters]()
* [JavaScript ES6 -- Iterables and Iterators]()

## Learning Objectives

* ES6, New Features
* Constant and Variable
* Blocked Scoped Variables
* Arrow functions, default parameters
* Rest, spread function parameters
* ES6 string templates
* ES6 object creation and properties
* Iterators, for-of loops

## Requirements

* Ubuntu 18.04 LTS, NodeJS 12.11.x
* `vi`, `vim`, `emacs`, `Visual Studio Code`
* `README.md` file
* `Jest Testing Framework`
* `ESLint`
* Exported functions

## Setup

**Install NodeJS 12.11.x**

(in the home directory):

```
curl -sL https://deb.nodesource.com/setup_12.x -o nodesource_setup.sh
sudo bash nodesource_setup.sh
sudo apt install nodejs -y
```

```
$ nodejs -v
v12.11.1
$ npm -v
6.11.3
```

**Install Jest, Babel, and ESLint**

in the project directory:

* Install Jest using: `npm install --save-dev jest`
* Install Babel using: `npm install --save-dev babel-jest @babel/core @babel/preset-env`
* Install ESLint using: `npm install --save-dev eslint`

**Configuration files**

`package.json`

<details>
  <summary>Click to show/hide file contents</summary>
  
  ```json
  {
      "scripts": {
        "lint": "./node_modules/.bin/eslint",
        "check-lint": "lint [0-9]*.js",
        "dev": "npx babel-node",
        "test": "jest",
        "full-test": "./node_modules/.bin/eslint [0-9]*.js && jest"
      },
      "devDependencies": {
      "@babel/core": "^7.6.0",
      "@babel/node": "^7.8.0",
      "@babel/preset-env": "^7.6.0",
      "eslint": "^6.4.0",
      "eslint-config-airbnb-base": "^14.0.0",
      "eslint-plugin-import": "^2.18.2",
      "eslint-plugin-jest": "^22.17.0",
      "jest": "^24.9.0"
    }
  }
  ```
</details>

`babel.config.js`

<details>
  <summary>Click to show/hide file contents</summary>
  
  ```js
  module.exports = {
    presets: [
      [
        '@babel/preset-env',
        {
          targets: {
            node: 'current',
          },
        },
      ],
    ],
  };
  ```
</details>

`.eslintrc.js`

<details>
  <summary>Click to show/hide file contents</summary>
  
  ```js
  module.exports = {
    env: {
      browser: false,
      es6: true,
      jest: true,
    },
    extends: [
      'airbnb-base',
      'plugin:jest/all',
    ],
    globals: {
      Atomics: 'readonly',
      SharedArrayBuffer: 'readonly',
    },
    parserOptions: {
      ecmaVersion: 2018,
      sourceType: 'module',
    },
    plugins: ['jest'],
    rules: {
      'no-console': 'off',
      'no-shadow': 'off',
      'no-restricted-syntax': [
        'error',
        'LabeledStatement',
        'WithStatement',
      ],
    },
    overrides:[
      {
        files: ['*.js'],
        excludedFiles: 'babel.config.js',
      }
    ]
  };
  ```
</details>

**Finally...**

Run `npm install` from the project terminal to install dependencies

## More also...
