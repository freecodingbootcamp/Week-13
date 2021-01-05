# Week-13 -- Day-2

## Module Import and Export

What good are modules if you cannot use them outside the module itself? So this is where imports and exports come in. You need to export a module and then you can you need to import them wherever you need them. Be aware there are multiple ways to do this! This part was always confusing to me. I would see at least three different ways this was happening. Alright, with that said let's get to it and let me know the show at least one way of how we can import and export modules. As with some of my previous notes, I will be using Odin project's curriculum for some of these examples. Here is the page I will be referencing:

https://www.theodinproject.com/courses/javascript/lessons/es6-modules

### Example 1

**export**
```javascript
// a file called functionOne.js
const functionOne = () => console.log('FUNCTION ONE!')

export { functionOne }
```

**import**
```javascript
// another JS file
import { functionOne } from './functionOne'

functionOne() //this should work as expected!
```

Do I need to go over it? Fine, I will. So the module consists of one file and one function both called functionOne. We have to make sure we explicitly export functionOne and then explicitly import it. Once we have done both we can use the function justnas if it was defined locally!

### Example 2
**export**
```javascript
const myName = (name) => 'Hi! My name is ' + name;
export default myName
```
**import**
```javascript
// import your function
import myName from './myName';

function component() {
  // use your function!
  console.log(myName('Henry'));
}
```

Notice the default part of the export and the lack of brackets in the import. This version of exporting and importing is good for a single function/object.  

### Example 3

Let's do one more that involves multiple exports within one file.

**export**
```javascript
const functionOne = () => 'ONE'
const functionTwo = () => 'TWO'

export {
  functionOne,
  functionTwo
}
```

**import**
```javascript
import {functionOne, functionTwo} from './myModule'
```

This one should definitely be clear. We are doing the same as the first example but with multiple exports.   
