## [TIP] Logical OR (||) vs Nullish Coalescing Operator (??)

* **Logical OR (||)**

  This operator returns the right hand value if the left hand value coerce to false. And that not only includes undefined and null but also 0 and ''.
  ```javascript
  const paginate = (options = {}) => {
    return [1, 2, 3, 4, 5].splice(0, options.limit || 3);
  }

  paginate(1); // expected: [1], output: [1]
  paginate(); // expected: [1, 2, 3], output: [1, 2, 3]
  paginate(0); // expected: [], output: [1, 2, 3]
  ```
* **Nullish Coalescing Operator (??)**

  This operator returns the right hand value only if the left hand value is either null or undefined.
  ```javascript
  const paginate = (options = {}) => {
    return [1, 2, 3, 4, 5].splice(0, options.limit ?? 3);
  }

  paginate(1); // expected: [1], output: [1]
  paginate(); // expected: [1, 2, 3], output: [1, 2, 3]
  paginate(0); // expected: [], output: []
  ```
  
  [Link](https://dev.to/hereisnaman/logical-or-vs-nullish-coalescing-operator-in-javascript-3851)
