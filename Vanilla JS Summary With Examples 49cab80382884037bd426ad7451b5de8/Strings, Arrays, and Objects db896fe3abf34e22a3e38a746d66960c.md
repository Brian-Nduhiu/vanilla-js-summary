# Strings, Arrays, and Objects

## **Removing whitespace from a string**

In Javascript, you can remove whitespace from a string using several methods:

- Using the **`trim()`** method: This method removes whitespace from both ends of a string. It does not modify the original string, but returns a new string without the whitespace.

`Project:`

- Try out the code below & feel free to change the values.

```jsx

const str = "    Hello World!    ";
const trimmedStr = str.trim();
console.log(trimmedStr); // "Hello World!"
```

- Using regular expressions: You can use regular expressions to replace whitespace characters with an empty string. This method removes all whitespace from the string, including whitespace in the middle of the string.

`Project:`

- Try out the code below & feel free to change the values.

```jsx
const str = "    Hello World!    ";
const trimmedStr = str.replace(/\s/g, '');
console.log(trimmedStr); // "HelloWorld!"
```

In the regular expression **`/ \s /g`**, **`\s`** matches any whitespace character (including spaces, tabs, and line breaks) and **`g`** is a flag that indicates a global search (i.e., it replaces all matches, not just the first one).

- Using **`split()`** and **`join()`**: You can split the string into an array of words, remove any empty strings (which would be created if there was whitespace between words), and then join the array back into a string.

`Project:`

- Try out the code below & feel free to change the values.

```jsx
const str = "    Hello World!    ";
const trimmedStr = str.split(' ').filter(Boolean).join('');
console.log(trimmedStr); // "HelloWorld!"
```

In this method, **`split(' ')`** splits the string into an array of words (using space as the separator), **`filter(Boolean)`** removes any empty strings from the array, and **`join('')`** joins the remaining words back into a string with no spaces.

## Transforming text to uppercase and lowercase

To transform text to uppercase and lowercase in JavaScript, you can use the built-in **`toUpperCase()`** and **`toLowerCase()`** methods.

`Project:`

- Try out the code below & feel free to change the values.

```jsx

let myString = "Hello, World!";
let upperCaseString = myString.toUpperCase();
let lowerCaseString = myString.toLowerCase();

console.log(upperCaseString); // Outputs "HELLO, WORLD!"
console.log(lowerCaseString); // Outputs "hello, world!"

```

In this example, we create a string called **`myString`** and assign it the value "Hello, World!". We then use the **`toUpperCase()`** method to create a new string called **`upperCaseString`**, which contains the uppercase version of the original string. Similarly, we use the **`toLowerCase()`** method to create a new string called **`lowerCaseString`**, which contains the lowercase version of the original string.

## Converting strings to integers

In JavaScript, you can convert a string to an integer using the built-in **`parseInt()`** function. 

`Project:`

- Try out the code below & feel free to change the values.

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

## Replacing a portion of text with different text

In JavaScript, you can replace a portion of text with different text using the **`replace()`** method. 

`Project:`

- Try out the code below & feel free to change the values.

```jsx

let myString = "Hello, World!";
let newString = myString.replace("World", "Universe");

console.log(myString); // Outputs "Hello, World!"
console.log(newString); // Outputs "Hello, Universe!"

```

In this example, we create a string called **`myString`** and assign it the value "Hello, World!". We then use the **`replace()`** method to replace the word "World" with "Universe", and assign the result to a new variable called **`newString`**.

We can then log both **`myString`** and **`newString`** to the console using the **`console.log()`** method. We can see that **`myString`** remains unchanged, while **`newString`** contains the modified text.

The **`replace()`** method takes two arguments: the first argument is the text to be replaced, and the second argument is the text that will replace it. If the text to be replaced appears multiple times in the string, only the first instance will be replaced. To replace all instances, you can use a regular expression with the global flag (**`/g`**). 

`Project:`

- Try out the code below & feel free to change the values.

```jsx
let myString = "Hello, World! Hello, World!";
let newString = myString.replace(/World/g, "Universe");

console.log(myString); // Outputs "Hello, World! Hello, World!"
console.log(newString); // Outputs "Hello, Universe! Hello, Universe!"

```

In this example, we use a regular expression (**`/World/g`**) to replace all instances of "World" with "Universe". The **`g`** flag indicates that the replacement should be global, meaning all instances will be replaced.

## Getting a portion of a string

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

`Project:`

- Try out the code below & feel free to change the values.

```jsx
const str = "Hello World!";
const subStr1 = str.substring(0, 5); // "Hello"
const subStr2 = str.substring(6); // "World!"
const subStr3 = str.slice(0, 5); // "Hello"
const subStr4 = str.slice(6); // "World!"
const subStr5 = str.slice(-6); // "World!"

console.log(subStr1);
console.log(subStr2);
console.log(subStr3);
console.log(subStr4);
console.log(subStr5);
```

In this example, we have a string "Hello World!". We use the **`substring()`** method to extract the first 5 characters of the string and the remaining characters starting from index 6. We also use the **`slice()`** method to do the same thing, with an additional example of extracting the last 6 characters of the string using a negative index.

## Splitting a string into an array based on a character

To split a string into an array based on a character in JavaScript, you can use the **`split()`** method. This method takes a delimiter as an argument, and it returns an array containing the substrings between the delimiters.

`Project:`

- Try out the code below & feel free to change the values.

```jsx

const str = "apple,banana,orange";
const arr = str.split(",");
console.log(arr); // ["apple", "banana", "orange"]

```

In the example above, the **`split()`** method is called on the **`str`** variable, with the comma (",") delimiter as an argument. This splits the string into an array of three elements, each element containing a fruit name.

If the delimiter is not found in the string, the **`split()`** method will return an array containing the entire string as its only element. 

`Project:`

- Try out the code below & feel free to change the values.

```jsx

const str = "hello world";
const arr = str.split(",");
console.log(arr); // ["hello world"]

```

In the example above, the **`split()`** method is called on the **`str`** variable with a comma (",") delimiter, but since the delimiter is not found in the string, the method returns an array containing the entire string as its only element.

## Adding items to an array or object

In JavaScript, you can add items to an array or object using different methods.

To add an item to an array, you can use the **`push()`** method, which adds an element to the end of the array. 

`Project:`

- Try out the code below & feel free to change the values.

```jsx

let myArray = [1, 2, 3];
myArray.push(4);
console.log(myArray); // Output: [1, 2, 3, 4]

```

Alternatively, you can use the bracket notation to replace an item in a specific position in the array. 

`Project:`

- Try out the code below & feel free to change the values.

```jsx
let myArray = [1, 2, 3];
myArray[2] = 4;
console.log(myArray); // Output: [1, 2, 4]

```

To add a new property to an object, you can use the dot notation or bracket notation.

`Project:`

- Try out the code below & feel free to change the values.

```jsx
let myObject = { name: 'John', age: 30 };
myObject.gender = 'male'; // using dot notation
myObject['hobby'] = 'reading'; // using bracket notation
console.log(myObject); // Output: { name: 'John', age: 30, gender: 'male', hobby: 'reading' }

```

In both cases, you are simply assigning a value to a specific property of the object.

## Merging two or more arrays or objects together

In JavaScript, you can merge two or more arrays or objects using different methods.

Merging Arrays:

- Using the **`concat()`** method: This method returns a new array that concatenates two or more arrays.

`Project:`

- Try out the code below & feel free to change the values.

```jsx
let arr1 = [1, 2, 3];
let arr2 = [4, 5, 6];
let arr3 = arr1.concat(arr2);
console.log(arr3); // Output: [1, 2, 3, 4, 5, 6]

```

- Using the spread operator (**`...`**): This operator can be used to spread the elements of one array into another.

`Project:`

- Try out the code below & feel free to change the values.

```jsx

let arr1 = [1, 2, 3];
let arr2 = [4, 5, 6];
let arr3 = [...arr1, ...arr2];
console.log(arr3); // Output: [1, 2, 3, 4, 5, 6]

```

Merging Objects:

- Using the **`Object.assign()`** method: This method copies the properties of one or more source objects to a target object.

`Project:`

- Try out the code below & feel free to change the values.

```jsx
let obj1 = { a: 1, b: 2 };
let obj2 = { c: 3, d: 4 };
let obj3 = Object.assign({}, obj1, obj2);
console.log(obj3); // Output: { a: 1, b: 2, c: 3, d: 4 }

```

Note that the first argument of **`Object.assign()`** is an empty object **`{}`** which is used as the target object.

- Using the spread operator (**`...`**): This operator can be used to spread the properties of one object into another.

`Project:`

- Try out the code below & feel free to change the values.

```jsx
let obj1 = { a: 1, b: 2 };
let obj2 = { c: 3, d: 4 };
let obj3 = { ...obj1, ...obj2 };
console.log(obj3); // Output: { a: 1, b: 2, c: 3, d: 4 }

```

Note that if there are properties with the same name in both objects, the property from the second object will overwrite the property from the first object.

## map, filter, reduce

**`map()`**, **`filter()`**, and **`reduce()`** are higher-order array methods in JavaScript that allow you to manipulate and transform arrays in various ways.

- **`map()`** method:

The **`map()`** method creates a new array by applying a function to each element in the original array. It returns a new array with the same length as the original array but with each element transformed according to the function provided. 

`Project:`

- Try out the code below & feel free to change the values.

```jsx

const numbers = [1, 2, 3, 4];
const doubled = numbers.map(num => num * 2);
console.log(doubled); // Output: [2, 4, 6, 8]

```

In this example, the **`map()`** method multiplies each element of the **`numbers`** array by 2 and returns a new array containing the transformed elements.

- **`filter()`** method:

The **`filter()`** method creates a new array with all elements that pass the test provided by a function. It returns a new array containing only the elements for which the function returns **`true`**. 

`Project:`

- Try out the code below & feel free to change the values.

```jsx
const numbers = [1, 2, 3, 4, 5, 6];
const evenNumbers = numbers.filter(num => num % 2 === 0);
console.log(evenNumbers); // Output: [2, 4, 6]

```

In this example, the **`filter()`** method creates a new array containing only the even numbers from the **`numbers`** array.

- **`reduce()`** method:

The **`reduce()`** method applies a function to each element in the array to reduce it to a single value. It takes two parameters: a function to execute on each element of the array, and an initial value to start with. The function takes two arguments: an accumulator and the current value. The function returns a new value that becomes the accumulator for the next iteration. The final result is the value of the accumulator after the last iteration. 

`Project:`

- Try out the code below & feel free to change the values.

```jsx
const numbers = [1, 2, 3, 4, 5];
const sum = numbers.reduce((accumulator, currentValue) => accumulator + currentValue, 0);
console.log(sum); // Output: 15

```

In this example, the **`reduce()`** method adds all the values in the **`numbers`** array and returns the final sum of 15.

These three methods are very powerful and can be used in combination to perform complex operations on arrays in a concise and elegant way.