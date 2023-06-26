# 0x00-ES6_basic

This is the first task on the Alx Backend with Javascript, this task emphasizes javascript ES6 (ECMAScript 6), also known as ES2015 or ES6+.

## Learning Objectives

At the end of this task, I was able to learn :
- What ES6 is
- New features introduced in ES6
- The difference between a constant and a variable
- Block-scoped variables
- Arrow functions and function parameters default to them
- Rest and spread function parameters
- String templating in ES6
- Object creation and their properties in ES6
- Iterators and for-of loops

## Tasks

### 0. [Const or let](https://github.com/Sanctus-Peter/alx-backend-javascript/blob/main/0x00-ES6_basic/0-constants.js)
#### Description
Modify:

* function taskFirst to instantiate variables using const
* function taskNext to instantiate variables using let
```javascript
export function taskFirst() {
  var task = 'I prefer const when I can.';
  return task;
}

export function getLast() {
  return ' is okay';
}

export function taskNext() {
  var combination = 'But sometimes let';
  combination += getLast();

  return combination;
}
```
#### Execution Example:
```shell
$ cat 0-main.js
import { taskFirst, taskNext } from './0-constants.js';

console.log(`${taskFirst()} ${taskNext()}`);

$
$ npm run dev 0-main.js
I prefer const when I can. But sometimes let is okay
$
```

### 1. [Block Scope](https://github.com/Sanctus-Peter/alx-backend-javascript/blob/main/0x00-ES6_basic/1-block-scoped.js)
#### Description
Given what you’ve read about **var** and hoisting, modify the variables inside the function **taskBlock** so that the variables aren’t overwritten inside the conditional block.
```javascript
export default function taskBlock(trueOrFalse) {
  var task = false;
  var task2 = true;

  if (trueOrFalse) {
    var task = true;
    var task2 = false;
  }

  return [task, task2];
}
```
### 2. [Arrow functions](https://github.com/Sanctus-Peter/alx-backend-javascript/blob/main/0x00-ES6_basic/2-arrow.js)
#### Description
Rewrite the following standard function to use ES6’s arrow syntax of the function add (it will be an anonymous function after)
```javascript
export default function getNeighborhoodsList() {
  this.sanFranciscoNeighborhoods = ['SOMA', 'Union Square'];

  const self = this;
  this.addNeighborhood = function add(newNeighborhood) {
    self.sanFranciscoNeighborhoods.push(newNeighborhood);
    return self.sanFranciscoNeighborhoods;
  };
}
```
### 3. [Parameter defaults](https://github.com/Sanctus-Peter/alx-backend-javascript/blob/main/0x00-ES6_basic/3-default-parameter.js)
#### Description
Condense the internals of the following function to 1 line - without changing the name of each function/variable.

Hint: The key here to define default parameter values for the function parameters.
```javascript
export default function getSumOfHoods(initialNumber, expansion1989, expansion2019) {
  if (expansion1989 === undefined) {
    expansion1989 = 89;
  }

  if (expansion2019 === undefined) {
    expansion2019 = 19;
  }
  return initialNumber + expansion1989 + expansion2019;
}
```
### 4. [Rest parameter syntax for functions](https://github.com/Sanctus-Peter/alx-backend-javascript/blob/main/0x00-ES6_basic/4-rest-parameter.js)
#### Description
Modify the following function to return the number of arguments passed to it using the rest parameter syntax
```javascript
export default function returnHowManyArguments() {

}
```
### 5. [The wonders of spread syntax](https://github.com/Sanctus-Peter/alx-backend-javascript/blob/main/0x00-ES6_basic/5-spread-operator.js)
#### Description
Using spread syntax, concatenate 2 arrays and each character of a string by modifying the function below. Your function body should be one line long.
```javascript
export default function concatArrays(array1, array2, string) {
}
```