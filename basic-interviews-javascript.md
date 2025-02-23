These are all great JavaScript questions, especially for interviews! Here are brief answers to each:

1. **Pass by Value vs. Pass by Reference**  
   - **Pass by Value**: The actual value is passed, and changes don't affect the original variable (e.g., primitives like numbers, strings, and booleans).  
   - **Pass by Reference**: A reference to the object is passed, so modifying it affects the original object (e.g., arrays and objects).

2. **map vs. filter**  
   - `map()`: Transforms each element and returns a new array.  
   - `filter()`: Returns a new array containing only elements that satisfy a condition.

3. **map() vs. forEach()**  
   - `map()`: Returns a new array.  
   - `forEach()`: Does not return a new array; it just iterates.

4. (You skipped number 4 😆)

5. **call(), apply(), and bind()**  
   - `call()`: Calls a function with a specific `this` and arguments passed one by one.  
   - `apply()`: Same as `call()`, but arguments are passed as an array.  
   - `bind()`: Returns a new function with `this` bound.

6. **Key Features of ES6**  
   - `let` and `const`, arrow functions, template literals, spread/rest operators, default parameters, classes, destructuring, promises, modules (`import/export`), and `Map`/`Set`.

7. **Spread Operator (`...`)**  
   Expands iterable values into individual elements. Example:  
   ```js
   let arr = [1, 2, 3];
   console.log([...arr, 4, 5]); // [1, 2, 3, 4, 5]
   ```

8. **Rest Operator (`...`)**  
   Collects multiple arguments into an array. Example:  
   ```js
   function sum(...nums) {
       return nums.reduce((a, b) => a + b, 0);
   }
   console.log(sum(1, 2, 3)); // 6
   ```

9. **Temporal Dead Zone (TDZ)**  
   The period between declaring a variable with `let`/`const` and its initialization.

10. **Polyfill**  
    A piece of code that provides modern functionality in older browsers.

11. **Prototype**  
    An object from which other objects inherit properties.

12. **IIFE (Immediately Invoked Function Expression)**  
    A function that runs immediately:  
    ```js
    (function() {
       console.log("Runs immediately");
    })();
    ```

13. **Data Types in JavaScript**  
    - Primitive: `String`, `Number`, `Boolean`, `Null`, `Undefined`, `Symbol`, `BigInt`  
    - Non-Primitive: `Object`, `Array`, `Function`

14. **Authentication vs Authorization**  
    - **Authentication**: Verifies who you are.  
    - **Authorization**: Determines what you can access.

15. **null vs. undefined**  
    - `null`: Explicit absence of value.  
    - `undefined`: Variable declared but not assigned.

16. **Output of `3+2+"7"`**  
    - `"57"` (First `3+2` is `5`, then `+"7"` converts to string).

17. **Slice vs. Splice**  
    - `slice(start, end)`: Returns a new array (does not modify original).  
    - `splice(start, deleteCount, ...items)`: Modifies the original array.

18. **Destructuring**  
    - Extracts values from arrays/objects:  
      ```js
      const [a, b] = [1, 2];
      ```

19. **setTimeout**  
    - Runs a function after a delay.

20. **setInterval**  
    - Repeats a function at intervals.

21. **Promises**  
    - Handle async operations:  
      ```js
      new Promise((resolve, reject) => {
          resolve("Success");
      });
      ```

22. **Closure**  
    - A function with access to its outer scope even after execution.

23. **Callback**  
    - A function passed to another function.  
      ```js
      function greet(name, callback) {
         console.log("Hello, " + name);
         callback();
      }
      ```

24. **Higher-Order Functions**  
    - Functions that take or return functions.

25. **== vs. ===**  
    - `==`: Checks value, allows type coercion.  
    - `===`: Checks value and type.

26. **Hoisting**  
    - Variables (`var`) and functions are moved to the top of scope before execution.

27. **let vs. var vs. const**  
    - `var`: Function-scoped, hoisted.  
    - `let`: Block-scoped, no hoisting.  
    - `const`: Block-scoped, cannot be reassigned.

28. **Arrow Function Limitations**  
    - No `this` binding, cannot be used as constructors, no `arguments` object.

29. **Shallow Copy vs. Deep Copy**  
    - **Shallow Copy**: Copies reference (modifications affect original).  
    - **Deep Copy**: Completely new object.

30. **Event Bubbling**  
    - Event propagates from child to parent.

31. **Event Capturing**  
    - Event propagates from parent to child.

32. **`this` in JavaScript**  
    - Refers to the context in which a function is called.

33. **Optimizing Performance**  
    - Code splitting, lazy loading, caching, reducing re-renders.

34. **Debouncing vs. Throttling**  
    - **Debouncing**: Executes function after a delay.  
    - **Throttling**: Ensures function runs at intervals.
