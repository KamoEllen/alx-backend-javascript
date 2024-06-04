# 0x03. ES6 Data Manipulation

This project focuses on manipulating data using JavaScript ES6 features. You'll work with arrays, typed arrays, and various data structures like sets and maps.

## Project Timeline

- **Start Date:** Jun 3, 2024 6:00 AM
- **End Date:** Jun 5, 2024 6:00 AM
- **Checker Release:** Jun 3, 2024 6:00 PM
- **Auto Review:** Launched at the deadline
- **Completed:** 04 June 2024 16:04

## Learning Objectives

By the end of this project, you should be able to:
- Use `map`, `filter`, and `reduce` on arrays
- Understand typed arrays
- Work with `Set`, `Map`, and `WeakMap` data structures

## Requirements

- **Environment:** Ubuntu 18.04 LTS, NodeJS 12.11.x
- **Editors:** vi, vim, emacs, Visual Studio Code
- **Code Style:** Files must end with a new line and use the `.js` extension
- **Testing:** Use Jest (`npm run test`)
- **Linting:** Use ESLint (must pass lint checks with `npm run full-test`)
- **File Exports:** All functions must be exported

## Setup

1. **Install NodeJS 12.11.x:**
    ```bash
    curl -sL https://deb.nodesource.com/setup_12.x -o nodesource_setup.sh
    sudo bash nodesource_setup.sh
    sudo apt install nodejs -y
    ```
2. **Verify installation:**
    ```bash
    nodejs -v
    npm -v
    ```
3. **Install Jest, Babel, and ESLint:**
    ```bash
    npm install
    ```

## Configuration Files

Add the following files to your project directory:
- `package.json`
- `babel.config.js`
- `.eslintrc.js`

Run `npm install` after adding `package.json`.

## Tasks Overview

1. **Basic List of Objects:**
   - Function: `getListStudents`
   - Returns an array of student objects (id, firstName, location)

2. **More Mapping:**
   - Function: `getListStudentIds`
   - Returns an array of ids from a list of student objects using `map`

3. **Filter:**
   - Function: `getStudentsByLocation`
   - Returns an array of students located in a specific city using `filter`

4. **Reduce:**
   - Function: `getStudentIdsSum`
   - Returns the sum of all student ids using `reduce`

5. **Combine:**
   - Function: `updateStudentGradeByCity`
   - Returns an array of students for a specific city with updated grades using `filter` and `map`

6. **Typed Arrays:**
   - Function: `createInt8TypedArray`
   - Returns a new ArrayBuffer with an Int8 value at a specific position

7. **Set Data Structure:**
   - Function: `setFromArray`
   - Returns a Set from an array

8. **More Set Data Structure:**
   - Function: `hasValuesFromArray`
   - Returns a boolean if all elements in the array exist within the set

9. **Clean Set:**
   - Function: `cleanSet`
   - Returns a string of set values that start with a specific string, separated by `-`

10. **Map Data Structure:**
    - Function: `groceriesList`
    - Returns a map of grocery items (name, quantity)

11. **More Map Data Structure:**
    - Function: `updateUniqueItems`
    - Updates the map for items with an initial quantity of 1 to 100, throws an error if not a map

## Repository Information

- **GitHub Repository:** `alx-backend-javascript`
- **Directory:** `0x03-ES6_data_manipulation`

## Note

Run `npm install` to install all dependencies before starting the project.