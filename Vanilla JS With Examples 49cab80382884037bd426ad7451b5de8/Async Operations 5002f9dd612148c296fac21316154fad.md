# Async Operations

Asynchronous operations are a fundamental part of JavaScript programming. They allow you to execute code in a non-blocking manner, which means that other code can continue to execute while the asynchronous operation is running. Here are some examples of how to perform asynchronous operations in JavaScript:

1. Using Promises

Promises provide a way to handle asynchronous operations in JavaScript. A promise represents a value that may not be available yet, but will be at some point in the future. You can use the **`then`** method of a promise to handle the value when it becomes available.

```jsx
function fetchData() {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      resolve('Data received');
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
      resolve('Data received');
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