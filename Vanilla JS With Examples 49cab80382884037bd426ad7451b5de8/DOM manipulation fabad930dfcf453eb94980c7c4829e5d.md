# DOM manipulation

## Getting elements in the DOM

To get elements in the DOM (Document Object Model) with JavaScript, you can use the **`document`** object and its various methods. Here are a few common ways to get elements:

- **`getElementById()`**: This method returns the element with the specified ID. For example:

```jsx

const myElement = document.getElementById("myId");

```

- **`getElementsByClassName()`**: This method returns an array-like object of all elements with the specified class name. For example:

```jsx

const myElements = document.getElementsByClassName("myClass");

```

- **`getElementsByTagName()`**: This method returns an array-like object of all elements with the specified tag name. For example:

```jsx

const myElements = document.getElementsByTagName("div");

```

- **`querySelector()`**: This method returns the first element that matches the specified CSS selector. For example:

```jsx

const myElement = document.querySelector(".myClass");

```

**`querySelectorAll()`**: This method returns a NodeList of all elements that match the specified CSS selector. For example:

```jsx

const myElements = document.querySelectorAll(".myClass");

```

Once you have obtained a reference to an element using one of these methods, you can manipulate its properties, attributes, and content using JavaScript.

`Project:`

- Create another file called `index.html`

```jsx
<!DOCTYPE html>
<html>
<head>
	<title>DOM Elements Example</title>
</head>
<body>
	<h1 id="heading">Hello, World!</h1>
	<p class="content">This is a paragraph.</p>
	<button id="btn">Click me</button>

	<script src="app.js"></script>
</body>
</html>
```

- In your `app.js` file:

```jsx
// Get the h1 element by ID
const heading = document.getElementById('heading');
console.log(heading);

// Get the p element by class name
const content = document.getElementsByClassName('content');
console.log(content[0]);

// Get the button element by tag name
const btn = document.getElementsByTagName('button');
console.log(btn[0]);
```

- To run the application, open the HTML file in your web browser by double-clicking on the file or right-clicking and selecting "Open With" and choosing your preferred browser. You can see the `console.log()` output by opening the developer tools.

In this example, we have an HTML document that contains an **`h1`** element with an **`id`** of "heading", a **`p`** element with a **`class`** of "content", and a **`button`** element with an **`id`** of "btn". In the JavaScript code, we use the **`document.getElementById()`**, **`document.getElementsByClassName()`**, and **`document.getElementsByTagName()`** methods to get the elements from the DOM by their respective selectors. We then log the elements to the console.

When running this code, you should see the **`h1`**, **`p`**, and **`button`** elements logged to the console.

## Looping through arrays and objects

To loop through arrays and objects in JavaScript, you can use various loop constructs such as **`for`** loop, **`while`** loop, **`for...in`** loop, and **`for...of`** loop. Here's an overview of how to use each loop construct:

- **`for`** loop: You can use a **`for`** loop to iterate over each element in an array.

`Project:`

- Try out the code below & feel free to change the values.

```jsx
const myArray = ["apple", "banana", "orange"];
for (let i = 0; i < myArray.length; i++) {
  console.log(myArray[i]);
}

```

- **`while`** loop: You can use a **`while`** loop to iterate over each element in an array or object.

`Project:`

- Try out the code below & feel free to change the values.

```jsx

const myArray = ["apple", "banana", "orange"];
let i = 0;
while (i < myArray.length) {
  console.log(myArray[i]);
  i++;
}

```

- **`for...in`** loop: You can use a **`for...in`** loop to iterate over the properties of an object.

`Project:`

- Try out the code below & feel free to change the values.

```jsx

const myObj = { name: "John", age: 30, city: "New York" };
for (let key in myObj) {
  console.log(`${key}: ${myObj[key]}`);
}

```

- **`for...of`** loop: You can use a **`for...of`** loop to iterate over the elements in an array or values of an object.

`Project:`

- Try out the code below & feel free to change the values.

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

## Getting, setting, and removing classes

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

To check if an element has a particular class, you can use the **`contains()`** method of the **`classList`** property. For example, to check if the same element as above has the class "active", you can do the following:

```jsx
var elem = document.getElementById("myElement");
if (elem.classList.contains("active")) {
  // do something
}
```

`Project:`

- Try out the code below & feel free to change the values.
- `index.html`

```jsx
<!DOCTYPE html>
<html>
<head>
	<title>DOM Classes Example</title>
	<style>
		.active {
			background-color: green;
			color: white;
		}

		.inactive {
			background-color: red;
			color: white;
		}
	</style>
</head>
<body>
	<div id="box">This is a box.</div>
	<button id="activate">Activate</button>
	<button id="deactivate">Deactivate</button>

	<script src="app.js"></script>
</body>
</html>
```

- `app.js`

```jsx
const box = document.getElementById('box');
const activateBtn = document.getElementById('activate');
const deactivateBtn = document.getElementById('deactivate');

// Get the current class of the box
const currentClass = box.className;
console.log(currentClass);

// Add the 'active' class to the box
box.classList.add('active');

// Remove the 'active' class from the box and add the 'inactive' class
activateBtn.addEventListener('click', () => {
  box.classList.remove('active');
  box.classList.add('inactive');
});

// Remove the 'inactive' class from the box and add the 'active' class
deactivateBtn.addEventListener('click', () => {
  box.classList.remove('inactive');
  box.classList.add('active');
});
```

## Manipulating styles

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

`Project:`

- `index.html`

```jsx
<!DOCTYPE html>
<html>
<head>
  <title>Manipulating Styles with JavaScript</title>
  <style>
    button {
      background-color: blue;
      color: white;
      padding: 10px;
      border-radius: 5px;
    }
  </style>
</head>
<body>
  <button id="myButton">Click me!</button>

  <script src="app.js"></script>
</body>
</html>
```

- `app.js`

```jsx
// Get the button element
const myButton = document.getElementById('myButton');

// Add a click event listener to the button
myButton.addEventListener('click', () => {
  // Change the button's background color
  myButton.style.backgroundColor = 'red';

  // Change the button's text color
  myButton.style.color = 'black';

  // Change the button's padding
  myButton.style.padding = '20px';

  // Change the button's border radius
  myButton.style.borderRadius = '10px';
});
```

This code defines a simple HTML document that contains a button element, CSS styles that define the button's initial appearance, and JavaScript code that modifies the button's styles when it's clicked.

## Getting and setting attributes

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

`Project:`

- Within your folder, add two images named `image.jpg` & `new-image.jpg`
- `index.html`

```jsx
<!DOCTYPE html>
<html>
<head>
  <title>Getting and Setting Attributes with JavaScript</title>
</head>
<body>
  <img id="myImage" src="image.jpg" alt="My Image">

  <button id="getAttributeButton">Get Image Source</button>
  <button id="setAttributeButton">Set Image Source</button>

  <script src="app.js"></script>
</body>
</html>
```

- `app.js`

```jsx
// Get the image element
const myImage = document.getElementById('myImage');

// Get the "Get Image Source" button
const getAttributeButton = document.getElementById('getAttributeButton');

// Add a click event listener to the "Get Image Source" button
getAttributeButton.addEventListener('click', () => {
  // Get the "src" attribute of the image element
  const src = myImage.getAttribute('src');

  // Log the value of the "src" attribute to the console
  console.log(`The image source is ${src}`);
});

// Get the "Set Image Source" button
const setAttributeButton = document.getElementById('setAttributeButton');

// Add a click event listener to the "Set Image Source" button
setAttributeButton.addEventListener('click', () => {
  // Set the "src" attribute of the image element to a new value
  myImage.setAttribute('src', 'new-image.jpg');

  // Log a message to the console to indicate that the image source has been changed
  console.log('The image source has been changed!');
});
```

In this example, we have an **`img`** element with an **`id`** of **`myImage`**. We also have two buttons: one to get the current value of the **`src`** attribute of the image element, and another to set the **`src`** attribute to a new value.

We use JavaScript to get a reference to the image element and the two buttons, and then add click event listeners to the buttons. When the "Get Image Source" button is clicked, we use the **`getAttribute`** method to get the current value of the **`src`** attribute and log it to the console.

When the "Set Image Source" button is clicked, we use the **`setAttribute`** method to set the **`src`** attribute of the image element to a new value, and log a message to the console to indicate that the image source has been changed.

## Listening for events in the DOM

In JavaScript, you can listen for events in the DOM (Document Object Model) using event listeners. Event listeners are functions that are executed when a specific event occurs, such as a click, keypress, or mouse movement.

To add an event listener to an element in the DOM, you first need to select the element using its ID or class name. You can do this using the **`document.getElementById()`** or **`document.getElementsByClassName()`** methods.

Once you have selected the element, you can add an event listener to it using the **`addEventListener()`** method. This method takes two arguments: the name of the event you want to listen for (such as 'click' or 'keypress'), and the function that should be executed when the event occurs.

Here's an example of how to add a click event listener to a button element with an ID of "myButton":

```jsx

const myButton = document.getElementById("myButton");

myButton.addEventListener("click", function() {
  alert("Button clicked!");
});

```

In this example, the **`addEventListener()`** method is used to add a click event listener to the **`myButton`** element. When the button is clicked, the anonymous function passed as the second argument is executed, which displays an alert message saying "Button clicked!".

You can also remove event listeners using the **`removeEventListener()`** method. This method takes the same two arguments as **`addEventListener()`**: the name of the event you want to remove the listener for, and the function that was originally passed as the listener.

```jsx

myButton.removeEventListener("click", myFunction);

```

In this example, the **`removeEventListener()`** method is used to remove the click event listener that was added previously. The **`myFunction`** function is the function that was originally passed as the listener.

`Project:`

- `index.html`

```jsx
<!DOCTYPE html>
<html>
  <head>
    <title>Event Listener Example</title>
  </head>
  <body>
    <button id="myButton">Click Me!</button>
    <script src="app.js"></script>
  </body>
</html>
```

- `app.js`

```jsx
const myButton = document.getElementById('myButton');

function handleClick() {
  alert('Button clicked!');
}

myButton.addEventListener('click', handleClick);

// remove the event listener after 5 seconds
setTimeout(function() {
  myButton.removeEventListener('click', handleClick);
}, 5000);
```

In the above JavaScript, we use the **`document.getElementById()`** method to get a reference to the button with an ID of "myButton". We then define a function called **`handleClick()`** that will be called when the button is clicked.

We then use the **`addEventListener()`** method to add a click event listener to the button. The first argument to **`addEventListener()`** is the name of the event we want to listen for ('click' in this case), and the second argument is the function that will be called when the event is triggered (**`handleClick`** in this case).

Finally, we use the **`setTimeout()`** method to wait 5 seconds, and then we use the **`removeEventListener()`** method to remove the click event listener from the button. We pass in the same function (**`handleClick`**) as the second argument to **`removeEventListener()`** to ensure that we remove the correct event listener.

In our example, we simply show an alert message when the button is clicked, and we remove the event listener after 5 seconds.

You can test this example by adding it to a new HTML file, opening the file in your web browser, and clicking on the "Click Me!" button. You should see an alert message appear that says "Button clicked!", and then after 5 seconds, clicking on the button will no longer trigger the alert message.