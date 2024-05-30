# Curriculum

## Short Specializations
- **0x00. ES6 Basics**  
  - **JavaScript**
  - **ES6**  
  - **Weight: 1**  
  - **Start:** May 27, 2024 6:00 AM  
  - **End:** May 28, 2024 6:00 AM  
  - **Checker release:** May 27, 2024 12:00 PM  
  - **Auto review:** at the deadline
  - **Complete Time:** 27 May 18:30

## Concepts
- JavaScript programming
- Software Linter

## Resources
- ECMAScript 6 - ECMAScript 2015
- Statements and declarations
- Arrow functions
- Default parameters
- Rest parameter
- Javascript ES6 — Iterables and Iterators

## Learning Objectives
By the end of this project, you should be able to explain:
- What ES6 is
- New features introduced in ES6
- The difference between a constant and a variable
- Block-scoped variables
- Arrow functions and function parameters default to them
- Rest and spread function parameters
- String templating in ES6
- Object creation and their properties in ES6
- Iterators and for-of loops

## Requirements
- Files executed on Ubuntu 18.04 LTS using NodeJS 12.11.x
- Allowed editors: vi, vim, emacs, Visual Studio Code
- Files should end with a new line
- A README.md file at the root of the project folder is mandatory
- Code should use the `.js` extension
- Code tested using Jest Testing Framework
- Code analyzed using ESLint with provided rules
- All functions must be exported

## Setup
1. **Install NodeJS 12.11.x:**
    ```sh
    curl -sL https://deb.nodesource.com/setup_12.x -o nodesource_setup.sh
    sudo bash nodesource_setup.sh
    sudo apt install nodejs -y
    nodejs -v
    # v12.11.1
    npm -v
    # 6.11.3
    ```

2. **Install Jest, Babel, and ESLint:**
    In your project directory, run:
    ```sh
    npm install
    ```

## Configuration files
Add the following files to your project directory:
- `package.json`
- `babel.config.js`
- `.eslintrc.js`

## Tasks

### 0. Const or let?
Modify:
- `taskFirst` to use `const`
- `taskNext` to use `let`

    ```javascript
    export function taskFirst() {
      const task = 'I prefer const when I can.';
      return task;
    }

    export function getLast() {
      return ' is okay';
    }

    export function taskNext() {
      let combination = 'But sometimes let';
      combination += getLast();
      return combination;
    }
    ```

### 1. Block Scope
Modify `taskBlock` so variables aren't overwritten inside the conditional block.

    ```javascript
    export default function taskBlock(trueOrFalse) {
      const task = false;
      const task2 = true;

      if (trueOrFalse) {
        const task = true;
        const task2 = false;
      }

      return [task, task2];
    }
    ```

### 2. Arrow functions
Rewrite to use ES6’s arrow syntax.

    ```javascript
    export default function getNeighborhoodsList() {
      this.sanFranciscoNeighborhoods = ['SOMA', 'Union Square'];

      this.addNeighborhood = (newNeighborhood) => {
        this.sanFranciscoNeighborhoods.push(newNeighborhood);
        return this.sanFranciscoNeighborhoods;
      };
    }
    ```

### 3. Parameter defaults
Condense function internals to 1 line using default parameter values.

    ```javascript
    export default function getSumOfHoods(initialNumber, expansion1989 = 89, expansion2019 = 19) {
      return initialNumber + expansion1989 + expansion2019;
    }
    ```

### 4. Rest parameter syntax
Modify function to return the number of arguments passed using the rest parameter syntax.

    ```javascript
    export default function returnHowManyArguments(...args) {
      return args.length;
    }
    ```

### 5. Spread syntax
Concatenate 2 arrays and each character of a string using spread syntax.

    ```javascript
    export default function concatArrays(array1, array2, string) {
      return [...array1, ...array2, ...string];
    }
    ```

### 6. Template literals
Rewrite return statement using template literals.

    ```javascript
    export default function getSanFranciscoDescription() {
      const year = 2017;
      const budget = {
        income: '$119,868',
        gdp: '$154.2 billion',
        capita: '$178,479',
      };

      return `As of ${year}, it was the seventh-highest income county in the United States, with a per capita personal income of ${budget.income}. As of 2015, San Francisco proper had a GDP of ${budget.gdp}, and a GDP per capita of ${budget.capita}.`;
    }
    ```

### 7. Object property shorthand
Modify function's budget object to use keyname shorthand.

    ```javascript
    export default function getBudgetObject(income, gdp, capita) {
      return { income, gdp, capita };
    }
    ```

### 8. Computed property names
Rewrite `getBudgetForCurrentYear` using computed property names.

    ```javascript
    function getCurrentYear() {
      return new Date().getFullYear();
    }

    export default function getBudgetForCurrentYear(income, gdp, capita) {
      return {
        [`income-${getCurrentYear()}`]: income,
        [`gdp-${getCurrentYear()}`]: gdp,
        [`capita-${getCurrentYear()}`]: capita,
      };
    }
    ```

### 9. ES6 method properties
Rewrite `getFullBudgetObject` using ES6 method properties.

    ```javascript
    import getBudgetObject from './7-getBudgetObject.js';

    export default function getFullBudgetObject(income, gdp, capita) {
      const budget = getBudgetObject(income, gdp, capita);
      return {
        ...budget,
        getIncomeInDollars(income) {
          return `$${income}`;
        },
        getIncomeInEuros(income) {
          return `${income} euros`;
        },
      };
    }
    ```

### 10. For...of Loops
Rewrite function using for...of loop.

    ```javascript
    export default function appendToEachArrayValue(array, appendString) {
      for (const value of array) {
        array[array.indexOf(value)] = appendString + value;
      }
      return array;
    }
    ```

### 11. Iterator
Write `createEmployeesObject` to return an object.

    ```javascript
    export default function createEmployeesObject(departmentName, employees) {
      return {
        [departmentName]: [...employees],
      };
    }
    ```

### 12. Report object
Write `createReportObject` to return an object containing `allEmployees` and a method `getNumberOfDepartments`.

    ```javascript
    export default function createReportObject(employeesList) {
      return {
        allEmployees: { ...employeesList },
        getNumberOfDepartments() {
          return Object.keys(this.allEmployees).length;
        },
      };
    }
    ```

---
**GitHub repository:** `alx-backend-javascript`
**Directory:** `0x00-ES6_basic`