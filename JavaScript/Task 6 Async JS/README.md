# Async JS

## Write functions to work with asynchronous code

## Before we start

1. This practical task will be automatically verified with tests on the Autocode platform.
2. Please, don't change the page structure, if it is not required for a task. It may affect tests.

## Run JavaScript code in RunJS application

`RunJS` is a JavaScript and TypeScript playground for desktop operating systems. It runs code as it's written and displays formatted results in the output panel on the right.

![RunJS application in work](https://gitlab.com/gap-bs-front-end-autocode-documents/autocode-documents/-/raw/main/images/runjs-intro.png)

RunJS is available on macOS, Windows, and Linux.

Here are detailed instructions on how to install and use it: [RunJS documentation](https://runjs.app/docs).

## Task Requirements

Every function should be in its file with export. Please, use the file names mentioned in the requirements to pass the tests.

**Please, note:**

- If task requirement says: _Function should **return** <something>_, it should deliberately return expected value. If it is displayed in the console instead of returning a value, it will not pass verification. More about function returning value: [Returning a value](https://javascript.info/function-basics#returning-a-value).

1. **The function "mocker"**

Write the function `mocker` that returns a new function. This new function should create a Promise which resolves with delay 1s.

```js
function mocker(data) {
  // your code...
}
```

This function takes one parameter:
`data` - an array or object with the users data.

1. The function should return new function.
2. This new function creates a Promise object.
3. The Promise resolves in 2 seconds.
4. The new function defined by `mocker` returns the Promise object.

**An example of using the function:**

```js
const getUsers = mocker([{ id: 1, name: "User1" }]);
getUsers().then((users) => {
  // Will fire after 1 second.
  console.log(users); // [{id: 1, name: 'User1'}];
});
```

2. **The function "summarize"**

Write the function `summarize` that receives array of promises and returns promise with sum of their values.

```js
function summarize(args) {
  // your code...
}
```

This function takes one parameter `args` these arguments are expected to be array of Promises

1. The function should return a Promise.
2. The function takes array of resolved values from each of the input Promises.
3. Incoming promises always go into the resolved state and resolve to a number.
4. Use the Promise.all() method, which takes in an array of Promises.
5. Sum up all the resolved values into a single value.

**An example of using the function:**

```js
const promise1 = Promise.resolve(4);
const promise2 = new Promise((resolve) => resolve(2));
summarize(promise1, promise2).then((sum) => {
  console.log(sum);
}); // 6
```

3. **The function "getAllData"**

Write the function `getAllData`. This is an asynchronous function that retrieves data from a database and outputs it after a delay of 1 second.

```js
const database = [
  { name: "John", age: 25, city: "New York" },
  { name: "Alice", age: 30, city: "Los Angeles" },
  { name: "Bob", age: 35, city: "Chicago" },
];

function getAllData(database) {
  // your code...
}
```

The function takes a database parameter, which is an array of objects containing data.

1. A function returns a Promise that resolves with an array of objects.
2. This Promise use method that takes an array of promises as its argument
3. Inner promise will resolve with the database parameter after a delay of 1 second

**An example of using the function:**

```js
const database = [
  { name: "John", age: 25, city: "New York" },
  { name: "Alice", age: 30, city: "Los Angeles" },
  { name: "Bob", age: 35, city: "Chicago" },
];

getAllData(database).then((result) => {
  console.log(result);
});
//{ name: "John", age: 25, city: "New York" },
//{ name: "Alice", age: 30, city: "Los Angeles" },
//{ name: "Bob", age: 35, city: "Chicago" }
```

4. **The function "getFriendNames"**

Write the function `getFriendNames` that makes an API call to retrieve data about a user, and then uses that data to make a second API call to retrieve more information about the user's friends. The function should return an array of the user's friend names.

To accomplish this task, you will need to use the async/await syntax to make asynchronous API calls and handle the returned data.

```js
async function getFriendNames(userId) {
  // your code...
}
```

1. The function takes a single parameter, userId is number
2. The function makes a call to the endpoint `https://example.com/users/${userId}/friends` using the fetch function.
3. The await keyword is used to wait for the response to be returned before continuing.
4. The response is returned as a JSON object
5. The function should extract the friend names from the JSON object.
6. The function should return an array of friend names.

**An example of using the function:**

```js
getFriendNames(1);
```
