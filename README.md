# Vanilla JS


## DOM manipulation

### Getting elements in the DOM

To get elements in the DOM (Document Object Model) with JavaScript, you can use the **`document`** object and its various methods. Here are a few common ways to get elements:

1. **`getElementById()`**: This method returns the element with the specified ID. For example:

```jsx
const myElement = document.getElementById("myId");
```

1. **`getElementsByClassName()`**: This method returns an array-like object of all elements with the specified class name. For example:

```jsx
const myElements = document.getElementsByClassName("myClass");
```

1. **`getElementsByTagName()`**: This method returns an array-like object of all elements with the specified tag name. For example:

```jsx
const myElements = document.getElementsByTagName("div");
```

1. **`querySelector()`**: This method returns the first element that matches the specified CSS selector. For example:

```jsx
const myElement = document.querySelector(".myClass");
```

**`querySelectorAll()`**: This method returns a NodeList of all elements that match the specified CSS selector. For example:

```jsx
const myElements = document.querySelectorAll(".myClass");
```

Once you have obtained a reference to an element using one of these methods, you can manipulate its properties, attributes, and content using JavaScript.

### Looping through arrays and objects

To loop through arrays and objects in JavaScript, you can use various loop constructs such as **`for`** loop, **`while`** loop, **`for...in`** loop, and **`for...of`** loop. Here's an overview of how to use each loop construct:

- **`for`** loop: You can use a **`for`** loop to iterate over each element in an array. Here's an example:

```jsx
const myArray = ["apple", "banana", "orange"];
for (let i = 0; i < myArray.length; i++) {
	console.log(myArray[i]);
}
```

- **`while`** loop: You can use a **`while`** loop to iterate over each element in an array or object. Here's an example:

```jsx
const myArray = ["apple", "banana", "orange"];
let i = 0;
while (i < myArray.length) {
	console.log(myArray[i]);
	i++;
}
```

- **`for...in`** loop: You can use a **`for...in`** loop to iterate over the properties of an object. Here's an example:

```jsx
const myObj = { name: "John", age: 30, city: "New York" };
for (let key in myObj) {
	console.log(`${key}: ${myObj[key]}`);
}
```

- **`for...of`** loop: You can use a **`for...of`** loop to iterate over the elements in an array or values of an object. Here's an example:

```jsx
const myArray = ["apple", "banana", "orange"];
for (let value of myArray) {
	console.log(value);
}

const myObj = { name: "John", age: 30, city: "New York" };
for (let value of Object.values(myObj)) {
	console.log(value);
}
```

### Getting, setting, and removing classes

In JavaScript, you can manipulate the classes of HTML elements using the **`classList`** property of an element. The **`classList`** property provides methods to add, remove, toggle, and check if an element has a particular class.

Here are some examples:

- Adding a class:

To add a class to an element, you can use the **`add()`** method of the **`classList`** property. For example, to add the class "active" to an element with an ID of "myElement", you can do the following:

```jsx
var elem = document.getElementById("myElement");
elem.classList.add("active");
```

- Removing a class:

To remove a class from an element, you can use the **`remove()`** method of the **`classList`** property. For example, to remove the class "active" from the same element as above, you can do the following:

```jsx
var elem = document.getElementById("myElement");
elem.classList.remove("active");
```

- Toggling a class:

To toggle a class on an element (i.e., add it if it doesn't exist and remove it if it does), you can use the **`toggle()`** method of the **`classList`** property. For example, to toggle the class "active" on the same element as above, you can do the following:

```jsx
var elem = document.getElementById("myElement");
elem.classList.toggle("active");
```

- Checking if an element has a class:

To check if an element has a particular class, you can use the **`contains()`** method of the **`classList`** property. For example, to check if the same element as above has the class "active", you can do the following:var elem = document.getElementById("myElement");
if (elem.classList.contains("active")) {
// do something
}

```jsx
var elem = document.getElementById("myElement");
if (elem.classList.contains("active")) {
	// do something
}
```

### Manipulating styles

In JavaScript, you can manipulate the style of an HTML element using the **`style`** property of the element. The **`style`** property provides access to the inline style of the element and allows you to set or modify individual style properties.

Here are some examples:

- Setting a style property:

To set a style property of an element, you can use the property name as a string and set it equal to a value. For example, to set the background color of an element with an ID of "myElement" to red, you can do the following:

```jsx
var elem = document.getElementById("myElement");
elem.style.backgroundColor = "red";
```

- Modifying a style property:

To modify a style property of an element, you can access it through the **`style`** property and change its value. For example, to change the font size of the same element as above to 16 pixels, you can do the following:

```jsx
var elem = document.getElementById("myElement");
elem.style.fontSize = "16px";
```

- Setting multiple style properties:

To set multiple style properties of an element, you can chain property assignments using the **`style`** property. For example, to set the background color and font size of the same element as above, you can do the following:

```jsx
var elem = document.getElementById("myElement");
elem.style.backgroundColor = "red";
elem.style.fontSize = "16px";
```

- Getting a style property:

To get the value of a style property of an element, you can access it through the **`style`** property. For example, to get the font size of the same element as above, you can do the following:

```jsx
var elem = document.getElementById("myElement");
var fontSize = elem.style.fontSize;
```

Note that this will only work for inline styles, and not for styles defined in a stylesheet. To get the computed style of an element, including styles defined in stylesheets, you can use the **`getComputedStyle()`** method. For example, to get the computed font size of the same element as above, you can do the following:

```jsx
var elem = document.getElementById("myElement");
var computedStyle = getComputedStyle(elem);
var fontSize = computedStyle.fontSize;
```

### Getting and setting attributes

In JavaScript, you can get and set attributes of an HTML element using the **`getAttribute()`** and **`setAttribute()`** methods of the element.

Here are some examples:

- Getting an attribute:

To get the value of an attribute of an element, you can use the **`getAttribute()`** method. For example, to get the value of the **`src`** attribute of an **`img`** element with an ID of "myImage", you can do the following:

```jsx
var elem = document.getElementById("myImage");
var src = elem.getAttribute("src");
```

- Setting an attribute:

To set the value of an attribute of an element, you can use the **`setAttribute()`** method. For example, to set the value of the **`src`** attribute of the same **`img`** element as above, you can do the following:

```jsx
var elem = document.getElementById("myImage");
elem.setAttribute("src", "path/to/image.jpg");
```

- Removing an attribute:

To remove an attribute from an element, you can use the **`removeAttribute()`** method. For example, to remove the **`src`** attribute from the same **`img`** element as above, you can do the following:

```jsx
var elem = document.getElementById("myImage");
elem.removeAttribute("src");
```

- Checking if an attribute exists:

To check if an element has a particular attribute, you can use the **`hasAttribute()`** method. For example, to check if the same **`img`** element as above has a **`src`** attribute, you can do the following:

```jsx
var elem = document.getElementById("myImage");
if (elem.hasAttribute("src")) {
	// do something
}
```

### Listening for events in the DOM

In JavaScript, you can listen for events in the DOM (Document Object Model) using event listeners. Event listeners are functions that are executed when a specific event occurs, such as a click, keypress, or mouse movement.

To add an event listener to an element in the DOM, you first need to select the element using its ID or class name. You can do this using the **`document.getElementById()`** or **`document.getElementsByClassName()`** methods.

Once you have selected the element, you can add an event listener to it using the **`addEventListener()`** method. This method takes two arguments: the name of the event you want to listen for (such as 'click' or 'keypress'), and the function that should be executed when the event occurs.

Here's an example of how to add a click event listener to a button element with an ID of "myButton":

```jsx
const myButton = document.getElementById("myButton");

myButton.addEventListener("click", function () {
	alert("Button clicked!");
});
```

In this example, the **`addEventListener()`** method is used to add a click event listener to the **`myButton`** element. When the button is clicked, the anonymous function passed as the second argument is executed, which displays an alert message saying "Button clicked!".

You can also remove event listeners using the **`removeEventListener()`** method. This method takes the same two arguments as **`addEventListener()`**: the name of the event you want to remove the listener for, and the function that was originally passed as the listener.

```jsx
myButton.removeEventListener("click", myFunction);
```

In this example, the **`removeEventListener()`** method is used to remove the click event listener that was added previously. The **`myFunction`** function is the function that was originally passed as the listener.

## **Strings, Arrays, and Objects**

### **Removing whitespace from a string**

In Javascript, you can remove whitespace from a string using several methods:

- Using the **`trim()`** method: This method removes whitespace from both ends of a string. It does not modify the original string, but returns a new string without the whitespace.

```jsx
const str = "    Hello World!    ";
const trimmedStr = str.trim(); // "Hello World!"
```

- Using regular expressions: You can use regular expressions to replace whitespace characters with an empty string. This method removes all whitespace from the string, including whitespace in the middle of the string.

```jsx
const str = "    Hello World!    ";
const trimmedStr = str.replace(/\s/g, ""); // "HelloWorld!"
```

In the regular expression **`/ \s /g`**, **`\s`** matches any whitespace character (including spaces, tabs, and line breaks) and **`g`** is a flag that indicates a global search (i.e., it replaces all matches, not just the first one).

- Using **`split()`** and **`join()`**: You can split the string into an array of words, remove any empty strings (which would be created if there was whitespace between words), and then join the array back into a string.

```
javascriptCopy code
const str = "    Hello World!    ";
const trimmedStr = str.split(' ').filter(Boolean).join(''); // "HelloWorld!"

```

In this method, **`split(' ')`** splits the string into an array of words (using space as the separator), **`filter(Boolean)`** removes any empty strings from the array, and **`join('')`** joins the remaining words back into a string with no spaces.

### Transforming text to uppercase and lowercase

To transform text to uppercase and lowercase in JavaScript, you can use the built-in **`toUpperCase()`** and **`toLowerCase()`** methods.

Here's an example of how to use them:

```jsx
let myString = "Hello, World!";
let upperCaseString = myString.toUpperCase();
let lowerCaseString = myString.toLowerCase();

console.log(upperCaseString); // Outputs "HELLO, WORLD!"
console.log(lowerCaseString); // Outputs "hello, world!"
```

In this example, we create a string called **`myString`** and assign it the value "Hello, World!". We then use the **`toUpperCase()`** method to create a new string called **`upperCaseString`**, which contains the uppercase version of the original string. Similarly, we use the **`toLowerCase()`** method to create a new string called **`lowerCaseString`**, which contains the lowercase version of the original string.

### Converting strings to integers

In JavaScript, you can convert a string to an integer using the built-in **`parseInt()`** function. Here's an example:

```jsx
let myString = "42";
let myNumber = parseInt(myString);

console.log(typeof myString); // Outputs "string"
console.log(typeof myNumber); // Outputs "number"
console.log(myNumber); // Outputs 42
```

In this example, we create a string called **`myString`** and assign it the value "42". We then use the **`parseInt()`** function to convert the string to an integer, and assign the result to a new variable called **`myNumber`**.

We can then use the **`typeof`** operator to check the data type of both **`myString`** and **`myNumber`**, and we can see that **`myString`** is a string and **`myNumber`** is a number. We can also log the value of **`myNumber`** to the console and see that it is equal to 42.

Note that **`parseInt()`** can also take a second argument that specifies the base of the number system used in the string being parsed. For example, **`parseInt("101", 2)`** would parse the binary string "101" and return the decimal value 5. If the second argument is not provided, **`parseInt()`** assumes a base of 10.

### Replacing a portion of text with different text

In JavaScript, you can replace a portion of text with different text using the **`replace()`** method. Here's an example:

```jsx
let myString = "Hello, World!";
let newString = myString.replace("World", "Universe");

console.log(myString); // Outputs "Hello, World!"
console.log(newString); // Outputs "Hello, Universe!"
```

In this example, we create a string called **`myString`** and assign it the value "Hello, World!". We then use the **`replace()`** method to replace the word "World" with "Universe", and assign the result to a new variable called **`newString`**.

We can then log both **`myString`** and **`newString`** to the console using the **`console.log()`** method. We can see that **`myString`** remains unchanged, while **`newString`** contains the modified text.

The **`replace()`** method takes two arguments: the first argument is the text to be replaced, and the second argument is the text that will replace it. If the text to be replaced appears multiple times in the string, only the first instance will be replaced. To replace all instances, you can use a regular expression with the global flag (**`/g`**). For example:

```jsx
let myString = "Hello, World! Hello, World!";
let newString = myString.replace(/World/g, "Universe");

console.log(myString); // Outputs "Hello, World! Hello, World!"
console.log(newString); // Outputs "Hello, Universe! Hello, Universe!"
```

In this example, we use a regular expression (**`/World/g`**) to replace all instances of "World" with "Universe". The **`g`** flag indicates that the replacement should be global, meaning all instances will be replaced.

### Getting a portion of a string

To get a portion of a string in JavaScript, you can use the **`substring()`** or **`slice()`** method. Both methods return a new string containing the extracted characters.

The **`substring()`** method takes two arguments: the starting index and the ending index (optional). If the ending index is not specified, the method extracts characters to the end of the string.

Here's an example:

```jsx
const str = "Hello World!";
const subStr1 = str.substring(0, 5); // "Hello"
const subStr2 = str.substring(6); // "World!"
```

In the example above, **`subStr1`** contains the first 5 characters of the string (**`"Hello"`**), and **`subStr2`** contains all characters starting from the 7th index (the character "W") to the end of the string (**`"World!"`**).

The **`slice()`** method works similarly, but it can also take negative indices as arguments, which count from the end of the string. Here's an example:

```jsx
const str = "Hello World!";
const subStr1 = str.slice(0, 5); // "Hello"
const subStr2 = str.slice(6); // "World!"
const subStr3 = str.slice(-6); // "World!"
```

In the example above, **`subStr1`** and **`subStr2`** are the same as in the previous example. **`subStr3`** contains the last 6 characters of the string, starting from the end of the string (**`"World!"`**).

### Splitting a string into an array based on a character

To split a string into an array based on a character in JavaScript, you can use the **`split()`** method. This method takes a delimiter as an argument, and it returns an array containing the substrings between the delimiters.

Here's an example:

```jsx
const str = "apple,banana,orange";
const arr = str.split(",");
console.log(arr); // ["apple", "banana", "orange"]
```

In the example above, the **`split()`** method is called on the **`str`** variable, with the comma (",") delimiter as an argument. This splits the string into an array of three elements, each element containing a fruit name.

If the delimiter is not found in the string, the **`split()`** method will return an array containing the entire string as its only element. Here's an example:

```jsx
const str = "hello world";
const arr = str.split(",");
console.log(arr); // ["hello world"]
```

In the example above, the **`split()`** method is called on the **`str`** variable with a comma (",") delimiter, but since the delimiter is not found in the string, the method returns an array containing the entire string as its only element.

### Adding items to an array or object

In JavaScript, you can add items to an array or object using different methods.

To add an item to an array, you can use the **`push()`** method, which adds an element to the end of the array. For example:

```jsx
let myArray = [1, 2, 3];
myArray.push(4);
console.log(myArray); // Output: [1, 2, 3, 4]
```

Alternatively, you can use the bracket notation to replace an item in a specific position in the array. For example:

```jsx
let myArray = [1, 2, 3];
myArray[2] = 4;
console.log(myArray); // Output: [1, 2, 4]
```

To add a new property to an object, you can use the dot notation or bracket notation. For example:

```jsx
let myObject = { name: "John", age: 30 };
myObject.gender = "male"; // using dot notation
myObject["hobby"] = "reading"; // using bracket notation
console.log(myObject); // Output: { name: 'John', age: 30, gender: 'male', hobby: 'reading' }
```

In both cases, you are simply assigning a value to a specific property of the object.

### Merging two or more arrays or objects together

In JavaScript, you can merge two or more arrays or objects using different methods.

Merging Arrays:

- Using the **`concat()`** method: This method returns a new array that concatenates two or more arrays. For example:

```jsx
let arr1 = [1, 2, 3];
let arr2 = [4, 5, 6];
let arr3 = arr1.concat(arr2);
console.log(arr3); // Output: [1, 2, 3, 4, 5, 6]
```

- Using the spread operator (**`...`**): This operator can be used to spread the elements of one array into another. For example:

```jsx
let arr1 = [1, 2, 3];
let arr2 = [4, 5, 6];
let arr3 = [...arr1, ...arr2];
console.log(arr3); // Output: [1, 2, 3, 4, 5, 6]
```

Merging Objects:

- Using the **`Object.assign()`** method: This method copies the properties of one or more source objects to a target object. For example:

```jsx
let obj1 = { a: 1, b: 2 };
let obj2 = { c: 3, d: 4 };
let obj3 = Object.assign({}, obj1, obj2);
console.log(obj3); // Output: { a: 1, b: 2, c: 3, d: 4 }
```

Note that the first argument of **`Object.assign()`** is an empty object **`{}`** which is used as the target object.

- Using the spread operator (**`...`**): This operator can be used to spread the properties of one object into another. For example:

```jsx
let obj1 = { a: 1, b: 2 };
let obj2 = { c: 3, d: 4 };
let obj3 = { ...obj1, ...obj2 };
console.log(obj3); // Output: { a: 1, b: 2, c: 3, d: 4 }
```

Note that if there are properties with the same name in both objects, the property from the second object will overwrite the property from the first object.

### map, filter, reduce

**`map()`**, **`filter()`**, and **`reduce()`** are higher-order array methods in JavaScript that allow you to manipulate and transform arrays in various ways.

- **`map()`** method:

The **`map()`** method creates a new array by applying a function to each element in the original array. It returns a new array with the same length as the original array but with each element transformed according to the function provided. For example:

```jsx
const numbers = [1, 2, 3, 4];
const doubled = numbers.map((num) => num * 2);
console.log(doubled); // Output: [2, 4, 6, 8]
```

In this example, the **`map()`** method multiplies each element of the **`numbers`** array by 2 and returns a new array containing the transformed elements.

- **`filter()`** method:

The **`filter()`** method creates a new array with all elements that pass the test provided by a function. It returns a new array containing only the elements for which the function returns **`true`**. For example:

```jsx
const numbers = [1, 2, 3, 4, 5, 6];
const evenNumbers = numbers.filter((num) => num % 2 === 0);
console.log(evenNumbers); // Output: [2, 4, 6]
```

In this example, the **`filter()`** method creates a new array containing only the even numbers from the **`numbers`** array.

- **`reduce()`** method:

The **`reduce()`** method applies a function to each element in the array to reduce it to a single value. It takes two parameters: a function to execute on each element of the array, and an initial value to start with. The function takes two arguments: an accumulator and the current value. The function returns a new value that becomes the accumulator for the next iteration. The final result is the value of the accumulator after the last iteration. For example:

```jsx
const numbers = [1, 2, 3, 4, 5];
const sum = numbers.reduce(
	(accumulator, currentValue) => accumulator + currentValue,
	0
);
console.log(sum); // Output: 15
```

In this example, the **`reduce()`** method adds all the values in the **`numbers`** array and returns the final sum of 15.

These three methods are very powerful and can be used in combination to perform complex operations on arrays in a concise and elegant way.

## **DOM Injection**

### Detecting when the DOM is ready

Detecting when the DOM is ready in JavaScript is an essential step before manipulating the document's elements dynamically. One of the most common ways to detect when the DOM is ready is to use the **`DOMContentLoaded`** event. This event fires when the browser has finished parsing the HTML and constructing the DOM tree. Here's an example of how you can use it:

```jsx
document.addEventListener("DOMContentLoaded", function () {
	// Your code to manipulate the DOM goes here
});
```

Alternatively, you can use the **`window.onload`** event to detect when the entire page, including images and stylesheets, has finished loading. However, keep in mind that using **`window.onload`** may cause delays in the page loading, so it's not always the best choice.

```jsx
window.onload = function () {
	// Your code to manipulate the DOM goes here
};
```

Finally, if you're using a JavaScript library like jQuery, you can use its ready() method to detect when the DOM is ready:

```jsx
$(document).ready(function () {
	// Your code to manipulate the DOM goes here
});
```

Whichever method you choose, make sure to place your code inside the callback function to ensure that the DOM is ready before attempting to manipulate it.

### Adding text and HTML to an element

You can add text and HTML to an element in several ways using JavaScript. Here are some examples:

- Using the innerHTML property: The innerHTML property sets or returns the HTML content (inner HTML) of an element. You can use it to add text or HTML to an element:

```jsx
// Get the element
const element = document.getElementById("my-element");

// Add text to the element
element.innerHTML = "Hello World!";

// Add HTML to the element
element.innerHTML = "<h1>Hello World!</h1>";
```

- Using the textContent property: The textContent property sets or returns the text content of an element:

```jsx
// Get the element
const element = document.getElementById("my-element");

// Add text to the element
element.textContent = "Hello World!";
```

- Using the createElement and appendChild methods: You can create a new element and append it to an existing element:

```jsx
// Get the element
const parent = document.getElementById("parent-element");

// Create a new element
const newElement = document.createElement("p");

// Set the text content
newElement.textContent = "Hello World!";

// Append the new element to the parent element
parent.appendChild(newElement);
```

- Using the insertAdjacentHTML method: You can insert HTML at a specified position relative to the element:

```jsx
// Get the element
const element = document.getElementById("my-element");

// Insert HTML after the element
element.insertAdjacentHTML("afterend", "<p>Hello World!</p>");

// Insert HTML before the element
element.insertAdjacentHTML("beforebegin", "<p>Hello World!</p>");

// Insert HTML at the beginning of the element
element.insertAdjacentHTML("afterbegin", "<p>Hello World!</p>");

// Insert HTML at the end of the element
element.insertAdjacentHTML("beforeend", "<p>Hello World!</p>");
```

### Creating new elements

In JavaScript, it is not possible to create new elements in the same way that you can create new objects or functions. However, you can dynamically create and add elements to the DOM (Document Object Model) using JavaScript.

Here is an example of how you can create a new element (in this case, a paragraph element) using JavaScript and add it to the DOM:

```jsx
// create a new paragraph element
var newParagraph = document.createElement("p");

// set the text content of the paragraph element
newParagraph.textContent = "This is a new paragraph created with JavaScript!";

// get a reference to the parent element where you want to add the new paragraph
var parentElement = document.getElementById("myParentElement");

// add the new paragraph to the parent element
parentElement.appendChild(newParagraph);
```

In this example, **`document.createElement()`** creates a new paragraph element, **`newParagraph.textContent`** sets the text content of the element, **`document.getElementById()`** gets a reference to the parent element where we want to add the new paragraph, and **`parentElement.appendChild()`** adds the new paragraph to the parent element.

### Removing elements from the DOM

Removing elements from the DOM (Document Object Model) can be done using the **`removeChild()`** method or the **`remove()`** method. Here are examples of both methods:

- Using **`removeChild()`** method: You can remove a child element from a parent element using the **`removeChild()`** method. Here is an example:

```jsx
var parentElement = document.getElementById("myParentElement");
var childElement = document.getElementById("myChildElement");
parentElement.removeChild(childElement);
```

In this example, **`parentElement`** is the parent element and **`childElement`** is the child element that you want to remove.

- Using **`remove()`** method: You can also remove an element using the **`remove()`** method, which is a newer method and is supported in modern browsers. Here is an example:

```jsx
var childElement = document.getElementById("myChildElement");
childElement.remove();
```

This will remove the **`myChildElement`** from the DOM.

In both cases, the element is removed from the DOM, but there is a slight difference between the two methods. The **`removeChild()`** method requires you to reference the parent element, while the **`remove()`** method can be called directly on the element that you want to remove.

It is also worth noting that removing an element from the DOM will also remove any event listeners or data associated with that element, so you should be careful when removing elements from the DOM.

## **DOM Traversal**

### Climb up and down the DOM

Climbing up and down the DOM (Document Object Model) in JavaScript involves navigating through the parent, child, and sibling elements of an element.

Here are a few ways to climb up and down the DOM in JavaScript:

- Getting parent element: You can get the parent element of an element using the **`parentElement`** property. Here is an example:

```jsx
var childElement = document.getElementById("myChildElement");
var parentElement = childElement.parentElement;
```

This will get the parent element of the **`myChildElement`** element.

```jsx
var parentElement = document.getElementById("myParentElement");
var childElements = parentElement.children;
```

This will get an array of all the child elements of the **`myParentElement`** element.

1. Getting sibling elements: You can get the sibling elements of an element using the **`previousElementSibling`** and **`nextElementSibling`** properties. Here is an example:

```jsx
var childElement = document.getElementById("myChildElement");
var previousSibling = childElement.previousElementSibling;
var nextSibling = childElement.nextElementSibling;
```

This will get the previous and next sibling elements of the **`myChildElement`** element.

1. Querying the DOM: You can also query the DOM using selectors like **`querySelector()`** and **`querySelectorAll()`**. Here is an example:

```jsx
var parentElement = document.querySelector("#myParentElement");
var childElements = parentElement.querySelectorAll(".myChildElements");
```

This will get an array of all child elements of **`myParentElement`** that have the class **`myChildElements`**.

### Filter nodes by selectors

To filter nodes by selectors in JavaScript, you can use the **`querySelectorAll()`** method. This method returns a NodeList object that contains all the elements that match the specified CSS selector(s).

Here's an example:

```html
<ul>
	<li>Item 1</li>
	<li class="selected">Item 2</li>
	<li>Item 3</li>
	<li class="selected">Item 4</li>
	<li>Item 5</li>
</ul>
```

```jsx
const selectedItems = document.querySelectorAll("li.selected");
console.log(selectedItems); // NodeList [ <li class="selected">Item 2</li>, <li class="selected">Item 4</li> ]
```

In this example, we use the **`querySelectorAll()`** method to select all the **`li`** elements with the **`selected`** class. The method returns a NodeList object that contains the two selected **`li`** elements.

You can also use more complex selectors, such as:

```jsx
const selectedItems = document.querySelectorAll("ul li.selected");
console.log(selectedItems); // NodeList [ <li class="selected">Item 2</li>, <li class="selected">Item 4</li> ]
```

In this example, we use the **`querySelectorAll()`** method to select all the **`li`** elements with the **`selected`** class that are descendants of a **`ul`** element.

Once you have selected the nodes, you can manipulate them in various ways, such as changing their text content or adding/removing classes. For example:

```jsx
selectedItems.forEach((item) => {
	item.textContent += " - Selected";
	item.classList.remove("selected");
});
```

In this example, we use the **`forEach()`** method to iterate over each selected item and append the text " - Selected" to its content, and then remove the **`selected`** class.

### Detect when an element is in the viewport

To detect when an element is in the viewport in JavaScript, you can use the **`getBoundingClientRect()`** method to get the position of the element relative to the viewport, and then compare it to the dimensions of the viewport.

Here's an example:

```jsx
const element = document.getElementById("my-element");

function isInViewport() {
	const rect = element.getBoundingClientRect();
	return (
		rect.top >= 0 &&
		rect.left >= 0 &&
		rect.bottom <=
			(window.innerHeight || document.documentElement.clientHeight) &&
		rect.right <= (window.innerWidth || document.documentElement.clientWidth)
	);
}

// Call isInViewport() whenever the window is scrolled or resized
window.addEventListener("scroll", function () {
	if (isInViewport()) {
		console.log("Element is in viewport");
	} else {
		console.log("Element is not in viewport");
	}
});

window.addEventListener("resize", function () {
	if (isInViewport()) {
		console.log("Element is in viewport");
	} else {
		console.log("Element is not in viewport");
	}
});
```

In this example, we first select the element with the **`getElementById`** method. We then define a function called **`isInViewport()`** that uses the **`getBoundingClientRect()`** method to get the position of the element relative to the viewport, and checks whether it is within the bounds of the viewport.

We then add event listeners for the **`scroll`** and **`resize`** events, and call the **`isInViewport()`** function to check whether the element is currently in the viewport. If it is, we log a message to the console.

Note that the **`getBoundingClientRect()`** method returns a DOMRect object with the position of the element relative to the top-left corner of the viewport. The **`top`** and **`left`** properties represent the distance of the top and left edges of the element from the top-left corner of the viewport, while the **`bottom`** and **`right`** properties represent the distance of the bottom and right edges of the element from the top-left corner of the viewport.

Also note that the **`window.innerHeight`** and **`window.innerWidth`** properties represent the height and width of the viewport, while the **`document.documentElement.clientHeight`** and **`document.documentElement.clientWidth`** properties represent the height and width of the document's root element. We use these properties to check whether the element is within the bounds of the viewport.

### Calculate distances to the top of the bottom of the viewport

To calculate the distance of an element to the top or bottom of the viewport in JavaScript, you can use the **`getBoundingClientRect()`** method to get the position of the element relative to the viewport, and then calculate the distance based on the position and dimensions of the viewport.

Here's an example:

```jsx
const element = document.getElementById("my-element");

function distanceToTopOfViewport() {
	const rect = element.getBoundingClientRect();
	return rect.top;
}

function distanceToBottomOfViewport() {
	const rect = element.getBoundingClientRect();
	return (
		(window.innerHeight || document.documentElement.clientHeight) - rect.bottom
	);
}

// Call distanceToTopOfViewport() and distanceToBottomOfViewport() whenever needed
console.log(distanceToTopOfViewport()); // distance from element to top of viewport
console.log(distanceToBottomOfViewport()); // distance from element to bottom of viewport
```

In this example, we first select the element with the **`getElementById`** method. We then define two functions called **`distanceToTopOfViewport()`** and **`distanceToBottomOfViewport()`** that use the **`getBoundingClientRect()`** method to get the position of the element relative to the viewport, and calculate the distance from the element to the top or bottom of the viewport based on its position and dimensions.

We can then call these functions whenever we need to calculate the distance. The **`distanceToTopOfViewport()`** function returns the distance from the top of the viewport to the top of the element, while the **`distanceToBottomOfViewport()`** function returns the distance from the bottom of the element to the bottom of the viewport.

Note that the **`window.innerHeight`** and **`document.documentElement.clientHeight`** properties represent the height of the viewport, while the **`getBoundingClientRect()`** method returns a DOMRect object with the position of the element relative to the top-left corner of the viewport. We use these properties to calculate the distance from the element to the top or bottom of the viewport.

## **Browser Storage**

### Cookies

Cookies are small pieces of data that are sent by a website to a user's web browser and stored on the user's computer or device. They are typically used to store information such as user preferences, login credentials, and shopping cart items.

Cookies are sent to the web server with every subsequent request made by the user's web browser to the same website. This allows the website to recognize the user and personalize their experience, such as displaying personalized content or remembering their login status.

In JavaScript, you can work with cookies using the **`document.cookie`** property. Here are some examples of how you can create, read, update, and delete cookies:

**Creating a cookie:**

To create a cookie, you can set the **`document.cookie`** property to a string that includes the name, value, and optional attributes of the cookie. For example:

```jsx
document.cookie =
	"username=John Doe; expires=Thu, 18 Dec 2025 12:00:00 UTC; path=/";
```

This creates a cookie named **`username`** with the value **`John Doe`**, an expiration date of December 18, 2025, and a path of **`/`** (meaning the cookie is accessible on all pages within the website).

**Reading a cookie:**

To read the value of a cookie, you can access the **`document.cookie`** property and parse the string to find the value of the desired cookie. For example:

```jsx
const cookies = document.cookie.split("; ");
for (let i = 0; i < cookies.length; i++) {
	const parts = cookies[i].split("=");
	const name = parts[0];
	const value = parts[1];
	if (name === "username") {
		console.log("The value of the username cookie is: " + value);
	}
}
```

This splits the **`document.cookie`** string into an array of individual cookies, and then loops through each cookie to find the one with the name **`username`**. Once the cookie is found, its value is logged to the console.

**Updating a cookie:**

To update the value or attributes of a cookie, you can create a new cookie with the same name and updated values or attributes, and set its expiration date to the current time plus the desired duration. For example:

```jsx
const d = new Date();
d.setTime(d.getTime() + 7 * 24 * 60 * 60 * 1000); // 7 days from now
const expires = "expires=" + d.toUTCString();
document.cookie = "username=Jane Doe; " + expires + "; path=/";
```

This creates a new cookie named **`username`** with the value **`Jane Doe`**, an expiration date of 7 days from the current time, and a path of **`/`**.

**Deleting a cookie:**

To delete a cookie, you can create a new cookie with the same name and an expiration date in the past. For example:

```jsx
document.cookie = "username=; expires=Thu, 01 Jan 1970 00:00:00 UTC; path=/;";
```

This creates a new cookie named **`username`** with no value, an expiration date of January 1, 1970 (which effectively deletes the cookie), and a path of **`/`**.

### The localStorage and sessionStorage APIs

The **`localStorage`** and **`sessionStorage`** APIs are built-in browser features that allow web developers to store data on the client-side (i.e., in the user's browser). Both APIs provide a way to store key-value pairs of data, but there are some key differences between them.

- **localStorage**

The **`localStorage`** API allows you to store data with no expiration date. This means that the data will persist even after the browser window or tab is closed, and will remain available until it is explicitly deleted or cleared. Some examples of data that could be stored in **`localStorage`** include user preferences, saved game progress, or cached data.

Here's an example of how to use the **`localStorage`** API in JavaScript:

```jsx
// Store a value in localStorage
localStorage.setItem("key", "value");

// Retrieve a value from localStorage
const value = localStorage.getItem("key");

// Remove a value from localStorage
localStorage.removeItem("key");

// Clear all values from localStorage
localStorage.clear();
```

Note that the **`setItem()`** method is used to store a key-value pair in **`localStorage`**, while the **`getItem()`** method is used to retrieve the value associated with a given key. The **`removeItem()`** method is used to remove a key-value pair, and the **`clear()`** method is used to remove all key-value pairs from **`localStorage`**.

- **sessionStorage**

The **`sessionStorage`** API is similar to **`localStorage`**, but with one key difference: the data stored in **`sessionStorage`** is only available for the duration of the browser session. This means that the data will be cleared when the user closes the browser window or tab.

Here's an example of how to use the **`sessionStorage`** API in JavaScript:

```jsx
// Store a value in sessionStorage
sessionStorage.setItem("key", "value");

// Retrieve a value from sessionStorage
const value = sessionStorage.getItem("key");

// Remove a value from sessionStorage
sessionStorage.removeItem("key");

// Clear all values from sessionStorage
sessionStorage.clear();
```

Note that the methods for working with **`sessionStorage`** are identical to those for **`localStorage`**.

In general, **`localStorage`** is a good choice for storing data that needs to persist across browser sessions, while **`sessionStorage`** is better suited for storing data that is only needed for the current browser session. Both APIs can be useful for storing data that needs to be accessible across multiple pages within a website.

### Storing arrays and objects

Both **`localStorage`** and **`sessionStorage`** allow you to store arrays and objects in addition to simple strings. To store an array or object, you simply need to convert it to a string using **`JSON.stringify()`** before storing it, and then convert it back to its original form using **`JSON.parse()`** when retrieving it.

Here's an example of how to store an array in **`localStorage`**:

```jsx
const myArray = [1, 2, 3];
localStorage.setItem("myArray", JSON.stringify(myArray));
```

In this example, the **`myArray`** variable is first converted to a JSON string using **`JSON.stringify()`**, and then stored in **`localStorage`** using the **`setItem()`** method.

To retrieve the array from **`localStorage`**, you would use the **`getItem()`** method and then parse the JSON string using **`JSON.parse()`**:

```jsx
const storedArray = JSON.parse(localStorage.getItem("myArray"));
```

In this example, the **`getItem()`** method is used to retrieve the JSON string from **`localStorage`**, and then **`JSON.parse()`** is used to convert the string back to its original array form.

The same approach can be used to store and retrieve objects:

```jsx
const myObject = { name: "John", age: 30 };
localStorage.setItem("myObject", JSON.stringify(myObject));

const storedObject = JSON.parse(localStorage.getItem("myObject"));
```

In this example, the **`myObject`** variable is first converted to a JSON string using **`JSON.stringify()`**, and then stored in **`localStorage`** using the **`setItem()`** method. The **`getItem()`** method is then used to retrieve the JSON string, which is converted back to its original object form using **`JSON.parse()`**.

Note that the **`JSON.stringify()`** and **`JSON.parse()`** methods can also be used with **`sessionStorage`** in the same way.

### Expiring localStorage data

Unlike **`sessionStorage`**, data stored in **`localStorage`** has no expiration date by default. However, you can set an expiration date for your **`localStorage`** data by storing an object that includes both the data and the expiration date.

Here's an example of how you can store expiring data in **`localStorage`**:

```jsx
// Store data with an expiration date of 1 hour from now
const expirationDate = new Date().getTime() + 60 * 60 * 1000; // 1 hour from now
const data = { foo: "bar", expiration: expirationDate };
localStorage.setItem("myData", JSON.stringify(data));
```

In this example, an object is created that includes the data you want to store (**`{ foo: 'bar' }`**) and an expiration date set to 1 hour from now. The object is then stringified using **`JSON.stringify()`** and stored in **`localStorage`** using the **`setItem()`** method.

To retrieve the data and check if it has expired, you would first retrieve the object from **`localStorage`** and then check the expiration date:

```jsx
const storedData = JSON.parse(localStorage.getItem("myData"));

if (
	storedData &&
	storedData.expiration &&
	storedData.expiration > new Date().getTime()
) {
	// Data has not expired, use it as needed
	const myValue = storedData.foo;
} else {
	// Data has expired or does not exist, do something else
}
```

In this example, the **`getItem()`** method is used to retrieve the JSON string from **`localStorage`**, which is then parsed into an object using **`JSON.parse()`**. The code then checks if the stored data exists (**`storedData`** is not **`null`**), and if it has not expired (**`storedData.expiration`** is greater than the current time).

If the stored data is still valid, you can use it as needed. If the data has expired or does not exist, you can take appropriate action, such as fetching new data from the server.

Note that this approach requires you to manually check for expiration and handle expired data yourself. If you need more sophisticated expiration and caching behavior, you might consider using a library such as **`lscache`** or **`store.js`**.

### Query strings

In web development, a query string is a part of a URL that contains data that is passed to a server-side script, which can then use that data to generate a dynamic web page. Query strings are typically used to send parameters to a web page, allowing the page to display customized content based on the values of those parameters.

In JavaScript, you can manipulate the query string of a URL using the **`window.location.search`** property. This property returns the query string portion of the current page's URL, including the question mark. For example, if the current URL is **`http://example.com/index.html?name=John&age=30`**, then **`window.location.search`** would return **`?name=John&age=30`**.

To manipulate the query string, you can use the **`URLSearchParams`** API. This API provides methods for adding, modifying, and removing parameters from a query string. Here's an example:

```jsx
// Get the current query string
let searchParams = new URLSearchParams(window.location.search);

// Get the value of a parameter
let name = searchParams.get("name"); // "John"

// Set the value of a parameter
searchParams.set("age", 31);

// Remove a parameter
searchParams.delete("name");

// Add a new parameter
searchParams.append("gender", "male");

// Update the query string of the current URL
let newQueryString = searchParams.toString();
window.history.replaceState(null, null, "?" + newQueryString);
```

In this example, we create a new **`URLSearchParams`** object based on the current query string, then use its methods to modify the parameters. Finally, we update the query string of the current URL using the **`replaceState`** method of the **`window.history`** object.

## **APIs and JavaScript**

### Common HTTP methods

There are several HTTP methods used to interact with web resources. Here are the most common ones:

1. GET - retrieves a resource from the server. This method is used to request information from the server, such as a webpage or a file. When a user types a URL into their web browser, the browser sends a GET request to the server to retrieve the web page.
2. POST - submits data to the server to be processed. This method is often used to submit form data, such as user login credentials or a search query.
3. PUT - updates an existing resource on the server. This method is used to update or replace an existing resource, such as a file or a database record.
4. DELETE - removes a resource from the server. This method is used to delete an existing resource, such as a file or a database record.
5. PATCH - partially updates an existing resource on the server. This method is similar to the PUT method, but is used to update only part of a resource rather than replacing the entire resource.
6. HEAD - retrieves metadata about a resource without retrieving the resource itself. This method is used to check if a resource exists or to retrieve information about the resource, such as its size or modification date.
7. OPTIONS - retrieves information about the communication options available for a resource. This method is used to check what methods and headers are supported by the server for a particular resource.

These HTTP methods are specified in the request sent from the client to the server, and the server responds with a corresponding status code and message indicating the success or failure of the request.

### Calling API endpoints with XHR

In JavaScript, you can use the XMLHttpRequest (XHR) object to make HTTP requests to API endpoints. Here's an example of how to use XHR to call a GET endpoint:

```jsx
const xhr = new XMLHttpRequest();
xhr.open("GET", "https://api.example.com/data");

xhr.onload = function () {
	if (xhr.status === 200) {
		const response = JSON.parse(xhr.responseText);
		console.log(response);
	} else {
		console.log("Request failed. Returned status of " + xhr.status);
	}
};

xhr.send();
```

In this example, we create a new XHR object using the **`XMLHttpRequest`** constructor, and then call the **`open`** method to specify the method and URL of the API endpoint we want to call. We then set the **`onload`** event handler to process the response returned from the server.

When the response is received, the **`onload`** function is called. We check the status of the response to see if it was successful (status code 200) or if there was an error. If the response was successful, we parse the JSON data using the **`JSON.parse`** method, and then process the response data. If the response was not successful, we log an error message.

After setting up the XHR object, we call the **`send`** method to initiate the request. This method sends the request to the server, and the **`onload`** function is called when the response is received.

Note that this example uses a GET request, but you can use XHR to make other types of requests as well, such as POST, PUT, and DELETE. To do so, you would simply modify the **`open`** method to specify the desired method and any data to be sent with the request.

### Transforming API response data

When calling an API endpoint, you may need to transform the response data to match the requirements of your application. Here are some common ways to transform API response data using JavaScript:

- Parsing JSON - If the API returns data in JSON format, you can use the **`JSON.parse()`** method to convert it into a JavaScript object. For example:

```jsx
const xhr = new XMLHttpRequest();
xhr.open("GET", "https://api.example.com/data");

xhr.onload = function () {
	if (xhr.status === 200) {
		const response = JSON.parse(xhr.responseText);
		console.log(response);
	} else {
		console.log("Request failed. Returned status of " + xhr.status);
	}
};

xhr.send();
```

- Filtering data - You can filter API response data using the **`filter()`** method to return only the data that matches a certain criteria. For example, if you have an array of objects and you only want to return objects with a certain value in a certain property, you can use **`filter()`** to achieve this. For example:

```jsx
const filteredData = responseData.filter((item) => item.property === "value");
console.log(filteredData);
```

- Mapping data - You can transform the structure of API response data using the **`map()`** method to create a new array based on the existing array. For example, if you have an array of objects and you want to return an array containing only a specific property of each object, you can use **`map()`** to achieve this. For example:

```jsx
const transformedData = responseData.map((item) => item.property);
console.log(transformedData);
```

- Sorting data - You can sort API response data using the **`sort()`** method to sort the elements of an array in ascending or descending order. For example, if you have an array of objects and you want to sort them based on a specific property, you can use **`sort()`** to achieve this. For example:

```jsx
const sortedData = responseData.sort((a, b) => a.property - b.property);
console.log(sortedData);
```

These are just a few examples of how you can transform API response data using JavaScript. Depending on the requirements of your application, you may need to use additional methods or techniques to transform the data.

### API authentication js

API authentication in JavaScript typically involves sending an authentication token or credentials along with each API request. Here are the steps involved:

1. Obtain authentication credentials from the API provider. This may involve creating an account on the provider's website and generating an API key or token.
2. Store the credentials securely. This may involve using environment variables, storing the credentials in a secure file, or using a third-party secrets management tool.
3. Include the credentials in each API request. This can be done using the Authorization header in the request. For example:

```jsx
fetch("https://api.example.com/data", {
	headers: {
		Authorization: "Bearer " + authToken,
	},
});
```

1. Handle authentication errors. If the credentials are invalid or expired, the API provider may return a 401 Unauthorized status code. Your code should handle this error and prompt the user to re-enter their credentials or take other appropriate action.

Note that the specific implementation of API authentication may vary depending on the API provider and the JavaScript framework or library you are using.

### Third-party data and XSS attacks

Third-party data refers to data that is collected or processed by a third-party entity, such as an advertising network or analytics provider. Cross-Site Scripting (XSS) attacks are a type of security vulnerability that can be caused by malicious code injected into a web page.

When using third-party data, it's important to be aware of the potential for XSS attacks. Here are some best practices for mitigating this risk:

1. Use a Content Security Policy (CSP): A CSP is a security feature that allows you to define which sources of content are allowed to be loaded on your web page. By using a CSP, you can prevent unauthorized third-party scripts from running on your web page.
2. Validate third-party data: Before using third-party data on your web page, validate it to ensure that it is safe and does not contain any malicious code. This can be done using input sanitization or by using a third-party data validation tool.
3. Use a sandboxed iframe: If you need to display third-party content on your web page, such as an embedded video or map, consider using a sandboxed iframe. This will prevent the third-party content from accessing the rest of your web page.
4. Limit third-party data access: Only allow third-party entities to access the data that they absolutely need to function properly. This will reduce the risk of data breaches and other security vulnerabilities.

Overall, it's important to carefully consider the risks of using third-party data and take appropriate measures to mitigate those risks. By following best practices and staying up-to-date on the latest security trends, you can help ensure the security and integrity of your web applications.

## **Writing Plugins**

### Code structure and design

When writing plugins, it's important to follow good coding practices to ensure that your code is maintainable, scalable, and easy to use. Here are some tips for structuring and designing your plugin code:

1. Use a modular structure: Divide your code into modules that handle different functionality. This will make it easier to maintain and debug your code.
2. Keep your code simple: Write your code in a way that is easy to understand and maintain. Avoid complex logic or over-engineering.
3. Use appropriate design patterns: Design patterns are common solutions to recurring problems in software development. Choose the appropriate design patterns for your plugin to make it more scalable and maintainable.
4. Provide configuration options: Allow users to customize the behavior of your plugin by providing configuration options. This will make your plugin more flexible and easier to use.
5. Use meaningful variable and function names: Use descriptive names for your variables and functions to make your code more readable and easier to understand.
6. Provide clear documentation: Write clear and concise documentation for your plugin that explains how to use it and what it does.
7. Use a consistent coding style: Use a consistent coding style throughout your plugin code to make it easier to read and maintain.
8. Test your code: Write automated tests to ensure that your plugin code works as expected and to catch any bugs or errors.

By following these best practices, you can create a well-structured and maintainable plugin that is easy to use and provides value to your users.

### Settings and user options

Settings and user options are important considerations when developing software or applications. Here are some tips for designing and implementing them effectively:

1. Identify the key settings and options: Determine which settings and options are most important to the user and necessary for the software's functionality. Limit the number of settings and options to avoid overwhelming the user.
2. Organize settings and options: Group settings and options logically, and use clear and consistent labels to make it easy for the user to understand and find what they're looking for.
3. Use default values: Set sensible default values for each setting or option. This makes it easier for users to get started with the software, and reduces the number of decisions they have to make.
4. Allow customization: Allow users to customize the software to meet their needs by providing options to change settings or enable/disable features. This increases the software's flexibility and usability.
5. Provide clear explanations: Provide clear explanations and context for each setting or option so that users can understand what it does and how it affects the software's behavior.
6. Save settings and options: Save user preferences and options so that they persist across sessions. This reduces the amount of work users have to do to set up the software each time they use it.
7. Test settings and options: Test settings and options thoroughly to ensure that they work as expected and don't introduce bugs or errors.

By following these guidelines, you can design and implement settings and user options that enhance your software's usability and flexibility, while minimizing confusion and errors.

### Events and callbacks

Events and callbacks are important concepts in JavaScript that allow developers to write code that is responsive and interactive. Here's a brief overview of how events and callbacks work:

- Events:

Events are actions that occur within a web page, such as a user clicking on a button or a page finishing loading. JavaScript can listen for these events and respond to them by executing code.

For example, you might write a function that changes the color of a button when it's clicked:

```jsx
const button = document.querySelector("button");

button.addEventListener("click", function () {
	button.style.backgroundColor = "red";
});
```

In this example, the **`addEventListener`** method is used to listen for the **`click`** event on the **`button`** element. When the event occurs, the anonymous function provided as the second argument is executed, which changes the button's background color to red.

- Callbacks:

A callback is a function that is passed as an argument to another function and executed when that function has completed. This allows for asynchronous code execution, where the program can continue running while a long-running task (such as fetching data from a server) is carried out in the background.

For example, you might write a function that fetches data from a server using the **`fetch`** method and passes a callback function to be executed when the data is returned:

```jsx
function fetchData(callback) {
	fetch("https://example.com/data")
		.then((response) => response.json())
		.then((data) => {
			// execute the callback function with the fetched data
			callback(data);
		});
}

// call the fetchData function with a callback function
fetchData(function (data) {
	// do something with the fetched data
	console.log(data);
});
```

In this example, the **`fetchData`** function takes a callback function as an argument and executes it when the data is returned from the server. This allows the calling code to continue running while the data is being fetched, and then respond to the data when it becomes available.

Overall, events and callbacks are essential concepts in JavaScript that allow developers to write responsive and interactive code. By mastering these concepts, you can write more complex and powerful programs that provide a better user experience.

### JS Modules

JavaScript modules are a way to organize and reuse code in a modular fashion. Modules allow developers to break down their code into small, reusable pieces that can be imported into other parts of the codebase as needed.

JavaScript modules were introduced in ECMAScript 6 (ES6) as a way to address the problem of code organization and reusability in large codebases. Prior to ES6, developers would use various patterns such as IIFE (Immediately Invoked Function Expression) and CommonJS to achieve modularity in their code.

To define a module in JavaScript, you use the **`export`** keyword to specify which parts of the module should be exposed to other parts of the codebase. You can export functions, variables, classes, and more. Here's an example of a simple module that exports a function:

```jsx
// my-module.js
export function myFunction() {
	console.log("Hello from myFunction!");
}
```

To use this module in another part of your codebase, you use the **`import`** keyword to bring in the exported parts of the module. Here's an example of how to use the **`myFunction`** function from the **`my-module`** module:

```jsx
// main.js
import { myFunction } from "./my-module.js";

myFunction(); // logs "Hello from myFunction!"
```

Modules can also be used to create private variables and functions within a module that are not exposed to other parts of the codebase. This helps to keep your code organized and prevent naming collisions with other parts of your codebase.

In summary, JavaScript modules provide a way to organize and reuse code in a modular fashion, making it easier to manage large codebases and prevent naming collisions.

## Async Operations

Asynchronous operations are a fundamental part of JavaScript programming. They allow you to execute code in a non-blocking manner, which means that other code can continue to execute while the asynchronous operation is running. Here are some examples of how to perform asynchronous operations in JavaScript:

1. Using Promises

Promises provide a way to handle asynchronous operations in JavaScript. A promise represents a value that may not be available yet, but will be at some point in the future. You can use the **`then`** method of a promise to handle the value when it becomes available.

```jsx
function fetchData() {
	return new Promise((resolve, reject) => {
		setTimeout(() => {
			resolve("Data received");
		}, 2000);
	});
}

fetchData().then((data) => {
	console.log(data);
});
```

In this example, the **`fetchData`** function returns a promise that resolves after 2 seconds. The **`then`** method is used to log the data when it becomes available.

1. Using Async/Await

Async/await is a newer syntax for handling asynchronous operations in JavaScript. It allows you to write asynchronous code that looks and behaves like synchronous code.

```jsx
function fetchData() {
	return new Promise((resolve, reject) => {
		setTimeout(() => {
			resolve("Data received");
		}, 2000);
	});
}

async function getData() {
	const data = await fetchData();
	console.log(data);
}

getData();
```

In this example, the **`getData`** function is declared as **`async`** to allow the use of the **`await`** keyword. The **`fetchData`** function returns a promise that resolves after 2 seconds, and the **`await`** keyword is used to wait for the promise to resolve before logging the data.

Using Callbacks

Callbacks are a common way to handle asynchronous operations in JavaScript. A callback is a function that is passed as an argument to another function and is called when the asynchronous operation is complete.

```jsx
scssCopy code
function fetchData(callback) {
  setTimeout(() => {
    callback('Data received');
  }, 2000);
}

fetchData((data) => {
  console.log(data);
});

```

In this example, the **`fetchData`** function accepts a callback function as an argument. The callback function is called with the data after 2 seconds, and the data is logged to the console.

## Event Loop

The Event Loop is a key concept in JavaScript that enables asynchronous programming. It's a mechanism for managing the execution of code in a non-blocking way, so that the application can continue to process user input and perform other tasks while it's waiting for certain operations to complete.

In a simplified way, the Event Loop works by continuously checking the call stack (the stack of functions being executed), the task queue (the queue of functions waiting to be executed), and the microtask queue (the queue of promises waiting to be resolved). If the call stack is empty, the Event Loop picks up the next task or microtask in the corresponding queue and adds it to the call stack for execution.

Here's a more detailed explanation of how the Event Loop works:

1. Whenever an operation is started in JavaScript, it's added to the call stack. This includes function calls, variable assignments, and other statements.
2. If an operation involves an asynchronous task, such as fetching data from a server or waiting for a user input, it's moved out of the call stack and into the task queue or microtask queue, depending on the type of task.
3. When the call stack is empty, the Event Loop picks up the next task or microtask in the corresponding queue and adds it to the call stack for execution.
4. Once the task or microtask is complete, any callbacks or promises associated with it are added to the corresponding queue, and the Event Loop continues to check for tasks and microtasks to process.

This process repeats continuously, allowing the application to handle multiple tasks and events simultaneously without blocking the main thread. It's important to note that long-running tasks should be handled in a way that doesn't block the Event Loop, such as by delegating them to a web worker or breaking them into smaller, non-blocking operations.

In summary, the Event Loop is a mechanism that enables non-blocking, asynchronous programming in JavaScript. It works by continuously checking the call stack and queues for tasks and microtasks to execute, allowing the application to handle multiple tasks and events simultaneously.

## Observables

In JavaScript, observables are objects that allow you to subscribe to events and receive notifications whenever those events occur. They are a part of the Reactive Programming paradigm and are commonly used in modern front-end frameworks like Angular and React.

Observables are similar to promises in that they both represent a value that may be available at some point in the future. However, observables are more powerful than promises because they can emit multiple values over time, whereas promises only emit a single value.

To use observables in JavaScript, you need to first create an observable object using a library like RxJS. Here's an example of how to create an observable that emits a sequence of numbers:

```jsx
import { Observable } from "rxjs";

const observable = new Observable((subscriber) => {
	subscriber.next(1);
	subscriber.next(2);
	subscriber.next(3);
	subscriber.complete();
});
```

In this example, we're creating an observable that emits the numbers 1, 2, and 3 in sequence, and then completes. To subscribe to this observable and receive its values, we can use the **`subscribe`** method:

```jsx
observable.subscribe({
	next: (value) => console.log(value),
	complete: () => console.log("Observable completed"),
});
```

In this code, we're subscribing to the observable and passing an object with two methods: **`next`** and **`complete`**. The **`next`** method is called each time the observable emits a value, and the **`complete`** method is called when the observable has completed emitting values.

Observables are a powerful tool for handling asynchronous events in JavaScript, and they can be used in a variety of scenarios, including network requests, user input, and more.

[An intro to Observables and how they are different from promises](https://www.freecodecamp.org/news/what-are-observables-how-they-are-different-from-promises/)
