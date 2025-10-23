# JavaScript Interview Questions & Answers

## 1. What is JavaScript?
**Answer:** JavaScript is a lightweight, interpreted programming language primarily used to create interactive web pages.

## 2. What are the features of JavaScript?
**Answer:**
- Dynamic typing
- Object-oriented
- First-class functions
- Event-driven
- Interpreted language

## 3. Difference between var, let, and const?
**Answer:**
- `var`: function-scoped, can be redeclared
- `let`: block-scoped, cannot be redeclared in same scope
- `const`: block-scoped, cannot be redeclared or reassigned

## 4. What is hoisting?
**Answer:** Variables and function declarations are moved to the top of their scope during compilation.

## 5. Difference between == and ===?
**Answer:**
- `==`: checks value equality with type coercion
- `===`: checks value and type equality

## 6. What are closures?
**Answer:** Function that has access to its own scope, parent scope, and global scope even after parent function has closed.

## 7. What is event bubbling and capturing?
**Answer:**
- **Bubbling:** Event propagates from child to parent
- **Capturing:** Event propagates from parent to child

## 8. What is the difference between null and undefined?
**Answer:**
- `null`: explicitly assigned empty value
- `undefined`: variable declared but not assigned

## 9. What are arrow functions?
**Answer:** Shorter syntax for functions, does not have its own `this`.

```javascript
const sum = (a, b) => a + b;
```

## 10. What is IIFE?
**Answer:** Immediately Invoked Function Expression runs immediately after declaration.

```javascript
(function(){ console.log('IIFE'); })();
```

## 11. What is the difference between call, apply, and bind?
**Answer:**
- `call()`: invokes function with `this` and arguments separately
- `apply()`: invokes function with `this` and arguments as array
- `bind()`: returns new function with bound `this`

## 12. What are promises?
**Answer:** Object representing eventual completion or failure of async operation.

## 13. What is async/await?
**Answer:** Syntax to handle promises in a synchronous-like manner.

## 14. What is the difference between synchronous and asynchronous?
**Answer:**
- **Synchronous:** blocking operations
- **Asynchronous:** non-blocking, executes in background

## 15. What are data types in JavaScript?
**Answer:**
- Primitive: String, Number, Boolean, Null, Undefined, Symbol, BigInt
- Non-Primitive: Object, Array, Function

## 16. What is the difference between map, filter, and reduce?
**Answer:**
- `map()`: returns new array by transforming elements
- `filter()`: returns new array with elements passing condition
- `reduce()`: returns a single value by applying accumulator function

## 17. What are template literals?
**Answer:** String literals allowing embedded expressions using backticks.

```javascript
const name = 'John';
const greeting = `Hello ${name}`;
```

## 18. What is destructuring?
**Answer:** Extract values from arrays or objects into variables.

```javascript
const [a, b] = [1, 2];
const {name, age} = {name: 'John', age: 30};
```

## 19. What is the difference between shallow copy and deep copy?
**Answer:**
- Shallow copy copies only top-level properties
- Deep copy copies nested objects too

## 20. What is the difference between call stack and event loop?
**Answer:**
- Call stack: keeps track of function execution
- Event loop: manages async callbacks and task queue

## 21. What is the difference between undefined and not defined?
**Answer:**
- `undefined`: variable declared but not assigned
- `not defined`: variable not declared

## 22. What is the difference between window and document objects?
**Answer:**
- `window`: represents browser window
- `document`: represents HTML document loaded in the window

## 23. What is the difference between localStorage and sessionStorage?
**Answer:**
- `localStorage`: persists until explicitly cleared
- `sessionStorage`: persists until browser/tab closed

## 24. What is event delegation?
**Answer:** Handling events on a parent element for multiple child elements using event bubbling.

## 25. What is the difference between primitive and non-primitive types?
**Answer:**
- Primitive: stored by value, immutable
- Non-primitive: stored by reference, mutable

## 26. What are modules in JavaScript?
**Answer:** Reusable pieces of code exported and imported using `export` and `import` (ES6) or `module.exports` and `require()` (CommonJS).

## 27. What is the difference between for...in and for...of?
**Answer:**
- `for...in`: iterates over object keys
- `for...of`: iterates over iterable values (arrays, strings)

## 28. What is a symbol?
**Answer:** Unique and immutable primitive value, often used as object keys.

## 29. What are default parameters?
**Answer:** Values assigned to function parameters if no value is provided.

```javascript
function greet(name = 'Guest') {
  console.log(`Hello ${name}`);
}
```

## 30. What is a generator function?
**Answer:** Function that can pause and resume execution using `function*` and `yield`.

## 31. What is the difference between spread and rest operators?
**Answer:**
- Spread: expands iterable into elements
- Rest: collects multiple elements into array

## 32. What are getters and setters?
**Answer:**
- `get`: access property value
- `set`: set property value

## 33. What is the difference between setTimeout and setInterval?
**Answer:**
- `setTimeout`: executes once after delay
- `setInterval`: executes repeatedly at interval

## 34. What is NaN?
**Answer:** Stands for Not-a-Number, a result of invalid numeric operations.

## 35. What is the difference between Number() and parseInt()?
**Answer:**
- `Number()`: converts to number, returns NaN if invalid
- `parseInt()`: parses string and returns integer, ignores trailing characters
