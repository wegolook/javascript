# ESLint Rules

Common ESLint rules for Node project are in [node.eslintrc](node.eslintrc).

## Usage

Copy [node.eslintrc](node.eslintrc) into `.eslintrc` for your project.

## Notable Style Choices

* 2-space indentation.
* Use semicolons.
* Use single quotes for strings, e.g. `const foo = 'bar'`.
* Use triple-equal comparisons, e.g. `foo === 'bar'`.
* `'use strict';` should be at the top of modules.
* Multiple variable declaration should be on separate lines.
  ```javascript
  // Good
  const a = 1;
  const b = 2;

  // Bad
  const a = 1, b = 2;
  ```
* Use `const` when possible and `let` the rest of the time.
* Do not use `var`.
* Prefer arrow functions.
  ```javascript
  const double = n => n * 2;
  const add = (a, b) => a + b;
  const retrieve = (id, callback) => {
    DB.retrieve(id, (err, value) => {
      if (err) {
        return callback(err);
      }

      callback(null, MyType.create(value));
    });
  };
  ```
