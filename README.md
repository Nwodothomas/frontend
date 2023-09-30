# ES6 Basic - JavaScript Project

This project focuses on ES6 (ECMAScript 2015) features and concepts in JavaScript. You'll be working on various tasks to understand and apply ES6 features.

## Table of Contents

- [Project Description](#project-description)
- [Requirements](#requirements)
- [Setup](#setup)
- [Tasks](#tasks)
  1. [Const or Let?](#1-const-or-let)
  2. [Block Scope](#2-block-scope)
  3. [Arrow Functions](#3-arrow-functions)
  4. [Parameter Defaults](#4-parameter-defaults)
  5. [Rest Parameter Syntax](#5-rest-parameter-syntax)
  6. [Spread Syntax](#6-spread-syntax)
  7. [Template Literals](#7-template-literals)
  8. [Object Property Value Shorthand](#8-object-property-value-shorthand)
  9. [Computed Property Names](#9-computed-property-names)
  10. [ES6 Method Properties](#10-es6-method-properties)
  11. [For...of Loops](#11-forof-loops)
  12. [Iterator](#12-iterator)
  13. [Iterating Through Report Objects](#13-iterating-through-report-objects)
  14. [Iterate Through Object](#14-iterate-through-object)

## Project Description

In this project, you will work with various ES6 features and concepts in JavaScript. You will complete a series of tasks, each focusing on different aspects of ES6.

### Requirements

- Ubuntu 18.04 LTS
- NodeJS 12.11.x
- Allowed Editors: vi, vim, emacs, Visual Studio Code
- All files should have a `.js` extension.
- Project should use Jest Testing Framework for testing.
- ESLint should be used with specific rules provided.
- All functions must be exported.

### Setup

To set up the project, follow these steps:

1. Install NodeJS 12.11.x:
   ```bash
   curl -sL https://deb.nodesource.com/setup_12.x -o nodesource_setup.sh
   sudo bash nodesource_setup.sh
   sudo apt install nodejs -y

## Check NodeJS and npm versions:
    nodejs -v
    npm -v

## Install Jest, Babel, and ESLint
In your project directory, install Jest, Babel and ESList by using the supplied package.json and run npm install.

## Configuration files
Add the files below to your project directory

package.json

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


babel.config.js

```javascript
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

.eslintrc.js

```javascript
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

### Finally…
Don’t forget to run npm install from the terminal of your project folder to install all necessary project dependencies.





