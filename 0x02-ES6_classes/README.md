# Curriculum

## Short Specializations
**0x02. ES6 Classes**

- **OOP**
- **JavaScript**
- **ES6**
- **Weight:** 1

Project will start May 30, 2024, 6:00 AM, and must end by May 31, 2024, 6:00 AM.  
Checker was released on May 30, 2024, 12:00 PM.  
An auto review will be launched at the deadline.

## Resources
Read or watch:
- Classes
- Metaprogramming

## Learning Objectives
At the end of this project, you should be able to explain:
- How to define a Class
- How to add methods to a class
- Why and how to add a static method to a class
- How to extend a class from another
- Metaprogramming and symbols

## Requirements
- All files will be executed on Ubuntu 18.04 LTS using NodeJS 12.11.x
- Allowed editors: `vi`, `vim`, `emacs`, `Visual Studio Code`
- All files should end with a new line
- A `README.md` file at the root of the project is mandatory
- Your code should use the `.js` extension
- Your code will be tested using Jest and the command `npm run test`
- Your code will be verified against lint using ESLint
- Your code needs to pass all the tests and lint. Use `npm run full-test` to verify the entire project.

## Setup
1. Install NodeJS 12.11.x:
    ```sh
    curl -sL https://deb.nodesource.com/setup_12.x -o nodesource_setup.sh
    sudo bash nodesource_setup.sh
    sudo apt install nodejs -y
    nodejs -v
    v12.11.1
    npm -v
    6.11.3
    ```
2. Install Jest, Babel, and ESLint:
    ```sh
    npm install
    ```

## Configuration Files
Add the following files to your project directory:
- `package.json`
- `babel.config.js`
- `.eslintrc.js`

Don't forget to run `npm install` after adding `package.json`.

## Tasks
### 0. You used to attend a place like this at some point
Implement a class named `ClassRoom`:
- **Prototype:** `export default class ClassRoom`
- **Attribute:** `maxStudentsSize` (Number) assigned to `_maxStudentsSize`
    ```js
    import ClassRoom from "./0-classroom.js";
    const room = new ClassRoom(10);
    console.log(room._maxStudentsSize);
    ```
    **Repo:**
    - GitHub repository: `alx-backend-javascript`
    - Directory: `0x02-ES6_classes`
    - File: `0-classroom.js`

### 1. Let's make some classrooms
Implement a function named `initializeRooms`:
- Returns an array of 3 `ClassRoom` objects with sizes 19, 20, and 34.
    ```js
    import initializeRooms from './1-make_classrooms.js';
    console.log(initializeRooms());
    ```
    **Repo:**
    - GitHub repository: `alx-backend-javascript`
    - Directory: `0x02-ES6_classes`
    - File: `1-make_classrooms.js`

### 2. A Course, Getters, and Setters
Implement a class named `HolbertonCourse`:
- **Constructor attributes:**
  - `name` (String)
  - `length` (Number)
  - `students` (array of Strings)
- Verify types during object creation.
- Store attributes in "underscore" attribute versions (e.g., `_name`).
- Implement getters and setters for each attribute.
    ```js
    import HolbertonCourse from "./2-hbtn_course.js";
    const c1 = new HolbertonCourse("ES6", 1, ["Bob", "Jane"]);
    console.log(c1.name);
    c1.name = "Python 101";
    console.log(c1);
    ```
    **Repo:**
    - GitHub repository: `alx-backend-javascript`
    - Directory: `0x02-ES6_classes`
    - File: `2-hbtn_course.js`

### 3. Methods, static methods, computed methods names..... MONEY
Implement a class named `Currency`:
- **Constructor attributes:**
  - `code` (String)
  - `name` (String)
- Store attributes in "underscore" attribute versions (e.g., `_name`).
- Implement getters and setters for each attribute.
- Implement a method named `displayFullCurrency` that returns `name (code)`.
    ```js
    import Currency from "./3-currency.js";
    const dollar = new Currency('$', 'Dollars');
    console.log(dollar.displayFullCurrency());
    ```
    **Repo:**
    - GitHub repository: `alx-backend-javascript`
    - Directory: `0x02-ES6_classes`
    - File: `3-currency.js`

### 4. Pricing
Implement a class named `Pricing`:
- **Constructor attributes:**
  - `amount` (Number)
  - `currency` (Currency)
- Store attributes in "underscore" attribute versions (e.g., `_name`).
- Implement getters and setters for each attribute.
- Implement a method named `displayFullPrice` that returns `amount currency_name (currency_code)`.
- Implement a static method named `convertPrice` that accepts `amount` (Number) and `conversionRate` (Number), returning the amount multiplied by the conversion rate.
    ```js
    import Pricing from './4-pricing.js';
    import Currency from './3-currency.js';
    const p = new Pricing(100, new Currency("EUR", "Euro"));
    console.log(p);
    console.log(p.displayFullPrice());
    ```
    **Repo:**
    - GitHub repository: `alx-backend-javascript`
    - Directory: `0x02-ES6_classes`
    - File: `4-pricing.js`

### 5. A Building
Implement a class named `Building`:
- **Constructor attributes:**
  - `sqft` (Number)
- Store attributes in "underscore" attribute versions (e.g., `_name`).
- Implement a getter for each attribute.
- Consider this class as abstract. Ensure any class extending from it implements a method named `evacuationWarningMessage`. If not, throw an error with the message `Class extending Building must override evacuationWarningMessage`.
    ```js
    import Building from './5-building.js';
    const b = new Building(100);
    console.log(b);
    class TestBuilding extends Building {}
    try {
        new TestBuilding(200);
    } catch(err) {
        console.log(err);
    }
    ```
    **Repo:**
    - GitHub repository: `alx-backend-javascript`
    - Directory: `0x02-ES6_classes`
    - File: `5-building.js`

### 6. Inheritance
Implement a class named `SkyHighBuilding` that extends `Building`:
- **Constructor attributes:**
  - `sqft` (Number) (must be assigned to the parent class `Building`)
  - `floors` (Number)
- Store attributes in "underscore" attribute versions (e.g., `_name`).
- Implement a getter for each attribute.
- Override the method `evacuationWarningMessage` to return `Evacuate slowly the NUMBER_OF_FLOORS floors`.
    ```js
    import SkyHighBuilding from './6-sky_high.js';
    const building = new SkyHighBuilding(140, 60);
    console.log(building.sqft);
    console.log(building.floors);
    console.log(building.evacuationWarningMessage());
    ```
    **Repo:**
    - GitHub repository: `alx-backend-javascript`
    - Directory: `0x02-ES6_classes`
    - File: `6-sky_high.js`

### 7. Airport
Implement a class named `Airport`:
- **Constructor attributes:**
  - `name` (String)
  - `code` (String)
- Store attributes in "underscore" attribute versions (e.g., `_name`).
- The default string description of the class should return the airport code.
    ```js
    import Airport from "./7-airport.js";
    const airportSF = new Airport('San Francisco Airport', 'SFO');
    console.log(airportSF);
    console.log(airportSF.toString());
    ```
    **Repo:**
    - GitHub repository: `alx-backend-javascript`
    - Directory: `0x02-ES6_classes`
    - File: `7-airport.js`

### 8. Primitive - Holberton Class
Implement a class named `HolbertonClass`:
- **Constructor attributes:**
  - `size` (Number)
  - `location` (String)
- Store attributes in "underscore" attribute versions (e.g., `_name`).
- When the class is cast into a `Number`, it should return the size.
- When the class is cast into a `String`, it should return the location.
    ```js
    import HolbertonClass from "./8-hbtn_class.js";
    const hc = new HolbertonClass(12, "Mezzanine");
    console.log(Number(hc));
    console.log(String(hc));
    ```
    **Repo:**
    - GitHub repository: `alx-backend-javascript`
    - Directory: `0x02-ES6_classes`
    - File: `8-hbtn_class.js`

### 9. Hoisting
Fix this code and add new names to the array:
    ```js
    export default class App {
        static play() {
            return this;
        }

        static load() {
            this.students = new Array();
            this.students.push("John Doe");
            this.students.push("Mary Doe");
        }
    }
    App.load();
    App.play();
    ```
    **Repo:**
    - GitHub repository: `alx-backend-javascript`
    - Directory: `0x02-ES6_classes`
    - File: `9-hoisting.js`

### 10. Vroom
Implement a class named `Car`:
- **Constructor attributes:**
  - `brand` (String)
  - `motor` (String)
  - `color` (String)
- Store attributes in "underscore" attribute versions (e.g., `_name`).
- Implement a method named `cloneCar` that returns a new object of the class `Car`.
    ```js
    import Car from "./10-car.js";
    const car1 = new Car("Nissan", "V8", "Blue");
    const car2 = car1.cloneCar();
    console.log(car1);
    console.log(car2);
    ```
    **Repo:**
    - GitHub repository: `alx-backend-javascript`
    - Directory: `0x02-ES6_classes`
    - File: `10-car.js`

### 11. EVCar
Implement a class named `EVCar` that extends `Car`:
- **Constructor attributes:**
  - `brand` (String)
  - `motor` (String)
  - `color` (String)
  - `range` (String)
- Store attributes in "underscore" attribute versions (e.g., `_name`).
- Implement a method named `cloneCar` that returns a new object of the class `Car`.
    ```js
    import EVCar from "./11-ev_car.js";
    const ec1 = new EVCar("Tesla", "Engine", "Red", "100");
    const ec2 = ec1.cloneCar();
    console.log(ec1);
    console.log(ec2);
    ```
    **Repo:**
    - GitHub repository: `alx-backend-javascript`
    - Directory: `0x02-ES6_classes`
    - File: `11-ev_car.js`
