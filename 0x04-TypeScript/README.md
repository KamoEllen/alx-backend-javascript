## Curriculum

**Short Specializations**

### 0x04. TypeScript

**Languages:**  
- JavaScript  
- TypeScript  

**Weight:** 1

**Project Timeline:**  
- **Start:** Jun 5, 2024, 6:00 AM  
- **End:** Jun 6, 2024, 6:00 AM 
- **Completed:** Jun 5, 2024, 22:00 PM 

**Review:**  
- Manual QA review must be done (request it when you are done with the project).

### Resources

- [TypeScript in 5 minutes](https://www.typescriptlang.org/docs/handbook/typescript-in-5-minutes.html)
- [TypeScript documentation](https://www.typescriptlang.org/docs/)

### Learning Objectives

By the end of this project, you should be able to explain the following concepts without the help of Google:

- Basic types in TypeScript
- Interfaces, Classes, and functions
- How to work with the DOM and TypeScript
- Generic types
- How to use namespaces
- How to merge declarations
- How to use an ambient namespace to import an external library
- Basic nominal typing with TypeScript

### Requirements

- Allowed editors: `vi`, `vim`, `emacs`, `Visual Studio Code`
- All your files should end with a new line
- All your files will be transpiled on Ubuntu 18.04
- Your TS scripts will be checked with jest (version 24.9.*)
- A `README.md` file at the root of the project folder is mandatory
- Your code should use the `.ts` extension when possible
- The TypeScript compiler should not show any warning or error when compiling your code

### Configuration Files

Please use these files for the following tasks:

- `package.json`
- `.eslintrc.js`
- `tsconfig.json`
- `webpack.config.js`

### Tasks

#### 0. Creating an interface for a student
- **Directory:** `task_0`
- **Files:** `main.ts`, `package.json`, `.eslintrc.js`, `tsconfig.json`, `webpack.config.js`
- **Details:** Create an interface `Student` with properties: `firstName`, `lastName`, `age`, and `location`. Create an array `studentsList` containing two students. Render a table with Vanilla JavaScript displaying the students' first names and locations.

#### 1. Let's build a Teacher interface
- **Directory:** `task_1`
- **Files:** `main.ts`, `package.json`, `tsconfig.json`, `webpack.config.js`
- **Details:** Create an interface `Teacher` with properties: `firstName`, `lastName`, `fullTimeEmployee`, `yearsOfExperience?`, `location`. Allow additional attributes.

#### 2. Extending the Teacher class
- **Directory:** `task_1`
- **Files:** `main.ts`
- **Details:** Create an interface `Directors` extending `Teacher` with an additional property `numberOfReports`.

#### 3. Printing teachers
- **Directory:** `task_1`
- **Files:** `main.ts`
- **Details:** Write a function `printTeacher` that returns the first letter of `firstName` and the full `lastName`.

#### 4. Writing a class
- **Directory:** `task_1`
- **Files:** `main.ts`
- **Details:** Create a class `StudentClass` with a constructor, `workOnHomework`, and `displayName` methods.

#### 5. Advanced types Part 1
- **Directory:** `task_2`
- **Files:** `main.ts`, `webpack.config.js`, `tsconfig.json`, `package.json`
- **Details:** Create `DirectorInterface` and `TeacherInterface`. Implement these interfaces in `Director` and `Teacher` classes respectively.

#### 6. Creating functions specific to employees
- **Directory:** `task_2`
- **Files:** `main.ts`
- **Details:** Write functions `isDirector` and `executeWork`.

#### 7. String literal types
- **Directory:** `task_2`
- **Files:** `main.ts`
- **Details:** Write a string literal type `Subjects` and a function `teachClass`.

#### 8. Ambient Namespaces
- **Directory:** `task_3`
- **Files:** `main.ts`, `interface.ts`, `crud.d.ts`
- **Details:** Create ambient namespace declarations and use them in TypeScript files.

#### 9. Namespace & Declaration merging
- **Directory:** `task_4`
- **Files:** `package.json`, `tsconfig.json`, `Teacher.ts`, `Subject.ts`, `Cpp.ts`, `Java.ts`, `React.ts`
- **Details:** Create interfaces and classes in a namespace with declaration merging.

#### 10. Update `main.ts`
- **Directory:** `task_4`
- **Files:** `main.ts`
- **Details:** Export constants and log details for different subjects and teachers.

#### 11. Brand convention & Nominal typing
- **Directory:** `task_5`
- **Files:** `main.ts`, `package.json`, `webpack.config.js`, `tsconfig.json`
- **Details:** Create interfaces `MajorCredits` and `MinorCredits` and functions `sumMajorCredits` and `sumMinorCredits`.

### Copyright
© 2024 ALX, All rights reserved.

---
