
# VARIABLES

- It is a container for data.

## Let, Const, Var

```javascript
let name = "shashwat";
console.log(name);

const name = "shashwat";
console.log(name);
```

- var is not used after 2015 because of ES6.
- In `let`, variables cannot be redeclared and can be updated.
- In `const`, variables cannot be redeclared or updated.

# DATA TYPE

## Primitive

- `number`
- `string`
- `boolean`
- `undefined`
- `null`
- `bigint` (rarely used)
- `symbol` (rarely used)

## Non-primitive

- `objects`: collection of values

```javascript
const student = {
    fullName: "shashwat",
    age: 22,
    cgpa: 7.2,
    isPass: true
};
```

**How to target, let's say, age of student?**

```javascript
console.log(student.age);
```

# COMMENTS

- Single-line: `//`
- Multi-line: `/* */`

# OPERATORS

- Arithmetic: `+ - * / %`, exponential (`^`), increment (`++`), decrement (`--`)
  - `a++` (post-increment) - it changes value in the next line of code
  - `++a` (pre-increment) - it will change the value first and then proceed further

## Assignment Operators

- `= += -= *= %= ^=`

## Comparison Operators

- `==` equal to
- `===` equal to and also check data type (strict)
- `!=` not equal to
- `!==` not equal to and also check data type (strict)
- `> >= < <=`

## Logical Operators

- `and`, `or`, `not`

# CONDITIONAL STATEMENT

## If Statement

```javascript
let age = 22;
if (age > 18) {
    console.log("you can vote");
}
if (age < 18) {
    console.log("you cannot vote");
}
```

## If-Else Statement

```javascript
let color;
if (color === "dark-mode") {
    color = "black";
} else {
    color = "white";
}
```

## Else-If Statement

```javascript
if (condition1) {
    // code
} else if (condition2) {
    // code
}
// so on
```

It is used where we have to check multiple conditions.

```javascript
if (age < 18) {
    console.log("junior");
} else if (age == 18) {
    console.log("mediocre");
} else if (age > 18) {
    console.log("senior");
}
```

# PROMPT

Pop-ups like features which are used to take inputs from the user.

# LOOPS

It is used to execute a piece of code again and again several times. It is of various types such as:

## For Loop

```javascript
for (let i = 1; i <= 5; i++) {
    console.log("shashwat");
}
```

**Output**

```
shashwat
shashwat
shashwat
shashwat
shashwat
```

## While Loop

```javascript
while (stoppingCondition) {
    // code
}
```

Example:

```javascript
let i = 1;
while (i <= 5) {
    console.log(i);
    i++;
}
```

## Do-While Loop

```javascript
do {
    // code
} while (condition);
```

It runs at least once.

Example:

```javascript
let i = 20;
do {
    console.log("shashwat");
    i++;
} while (i <= 10);
```

## For-Of Loop

A special type of loop used in specific data types such as arrays and strings.

```javascript
for (let val of str) {
    // code
}
```

Example:

```javascript
let str = "shashwat";
let size = 0;
for (let i of str) {
    console.log(i);
    size++;
}
console.log(size);
```

## For-In Loop

A special type of loop used in specific data types such as objects and arrays.

```javascript
for (let var in obj) {
    // code
}
```

Example:

```javascript
let student = {
    name: "shashwat",
    age: 20,
    cgpa: 7.2,
    isPass: true
};

for (let key in student) {
    console.log(key);
}
```

# STRINGS

It is a sequence of characters used to represent text.

## Create String

```javascript
let str = "shashwat";
```

## String Length

```javascript
str.length;
```

## String Index

```javascript
str[0], str[1], etc.
```

# TEMPLATE LITERALS

Ways to embed expressions in strings.

```javascript
`shashwat`
```

Example:

```javascript
let obj = {
    item: "pen",
    price: 10,
};
console.log(`The cost of ${obj.item} is ${obj.price}`);
```

# STRING INTERPOLATION

To create strings by substituting placeholders.

```javascript
`string text ${expression} string text`
```

# STRING METHODS

- `str.toUpperCase()`
- `str.toLowerCase()`
- `str.trim()`
- `str.slice(start, end?)`
- `str1.concat(str2)`
- `str.replace(searchValue, newValue)`
- `str.charAt()`

# ARRAYS

It is a collection of items.

```javascript
let name = ["shashwat", "resham"];
let marks = [89, 76];
```

Arrays are mutable in JavaScript. Strings are not mutable in JavaScript.

## Array Methods

- `push()`
- `pop()`
- `toString()`: convert array to string
- `concat()`
- `shift()`: delete from start and return
- `unshift()`: add to start
- `slice()`: return a piece of array
- `splice()`: change original array (add, remove, replace)

```javascript
.splice(startIndex, deleteCount, newElements)
```

# FUNCTION

A block of code that performs a specific task and can be called whenever needed.

## Custom Function

```javascript
function functionName() {
    // do some work
}
```

# PARAMETER AND ARGUMENTS

Parameters are inputs at the time of function definition, whereas arguments are inputs at the time of function call.

# ARROW FUNCTION

It is a part of modern JavaScript. A compact way of writing a function.

```javascript
const functionName = (param1, param2) => {
    // code
}
```

# CALLBACK FUNCTION

A function which is passed as an argument to another function.

```javascript
arr.forEach((val) => {
    console.log(val);
});
```

Here, it is a function to execute for each element in the array. (value, index, array) these three parameters can be passed in a callback function.

# HIGHER-ORDER FUNCTION

Those functions which take functions as parameters or return functions. Callback functions are higher-order functions.

# MAP METHOD FOR ARRAY

It is the same as forEach. It is used when we want to do some work for each element. The only difference is that map creates a new array as compared to forEach.

```javascript
arr.map(callbackFunction(value, index, array))

let newArr = arr.map((val) => {
    return val * 2;
});
```

# FILTER METHOD

It creates a new array of elements that give true for a condition. If we want to filter out anything then we use filter methods.

```javascript
let newArr = arr.filter((val) => {
    return val % 2 == 0;
});
```

# REDUCE METHOD

When there are lots of inputs and there is only one value in the output. Example: sum, average.

```javascript
arr.reduce((result, current) => {
    return result + current;
});
```


# DOM Manipulation in JavaScript

DOM manipulation in JavaScript refers to the process of using JavaScript to interact with and modify the Document Object Model (DOM) of a webpage. The DOM is a representation of the structure of a webpage, where each element is an object that can be accessed and modified. This allows developers to dynamically change the content, structure, and style of a webpage in response to user actions or other events.

Here are some common tasks involved in DOM manipulation:

## 1. Selecting Elements

Accessing elements in the DOM using methods such as `getElementById`, `getElementsByClassName`, `getElementsByTagName`, `querySelector`, and `querySelectorAll`.

```javascript
// Select an element by ID
const element = document.getElementById('myElement');

// Select elements by class name
const elements = document.getElementsByClassName('myClass');

// Select elements by tag name
const elements = document.getElementsByTagName('div');

// Select the first element that matches a CSS selector
const element = document.querySelector('.myClass');

// Select all elements that match a CSS selector
const elements = document.querySelectorAll('.myClass');
```

## 2. Changing Content

Modifying the content of elements using properties like `innerHTML`, `textContent`, and `value`.

```javascript
// Change the inner HTML of an element
element.innerHTML = '<p>New Content</p>';

// Change the text content of an element
element.textContent = 'New Text';

// Change the value of an input element
inputElement.value = 'New Value';
```

## 3. Changing Styles

Modifying the styles of elements using the `style` property or by adding/removing classes.

```javascript
// Change the style of an element
element.style.color = 'red';

// Add a class to an element
element.classList.add('newClass');

// Remove a class from an element
element.classList.remove('oldClass');
```

## 4. Adding/Removing Elements

Dynamically adding or removing elements from the DOM using methods like `appendChild`, `insertBefore`, `removeChild`, and `replaceChild`.

```javascript
// Create a new element
const newElement = document.createElement('div');
newElement.textContent = 'New Element';

// Append the new element to a parent element
parentElement.appendChild(newElement);

// Remove an element from the DOM
parentElement.removeChild(childElement);

// Replace an existing element with a new element
parentElement.replaceChild(newElement, oldElement);
```

## 5. Event Handling

Adding event listeners to elements to respond to user actions like clicks, key presses, and form submissions.

```javascript
// Add an event listener to an element
element.addEventListener('click', function(event) {
    // Handle the click event
    console.log('Element clicked!');
});
```

These are just a few examples of how JavaScript can be used to manipulate the DOM. DOM manipulation is a powerful tool for creating dynamic and interactive web applications.


# CONSTRUCTOR

- Rule 1: Constructor has the same name as that of a class.
- Rule 2: Constructor is somewhat like a method but not exactly a method.
- Rule 3: Constructor does not return anything, not even void, it only returns an instance of the class.
- Rule 4: There are basically two types of constructors in Java: parameterized and non-parameterized.
- Rule 5: There is a special kind of constructor provided by Java that is the default constructor. If you are not creating any constructor in your class then Java Virtual Machine is going to provide you a default constructor.
- Rule 6: There is a mechanism of constructor chaining which every constructor does.
- Rule 7: When you create an object of a class then the constructor is automatically invoked.
- Rule 8: If you want to call a constructor from another constructor inside the same class then you have to use `this` keyword. For this, `this` should be the first statement inside the constructor.
