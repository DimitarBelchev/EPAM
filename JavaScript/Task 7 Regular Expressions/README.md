# JS Regular Expressions

## Practivce regular expressions in JavaScript

## Before we start

1. This practical task will be verified automatically with tests on **the Autocode platform**.
2. Please put all `JavaScript` code in the `src/script.js` file. If you use any other file, it cannot be verified.
3. Please don't change the page structure if this is not required. It may affect the tests.

## Run JavaScript code in RunJS application

`RunJS` is a JavaScript and TypeScript playground for desktop operating systems. It runs code as it's written and displays formatted results in the output panel on the right.

![RunJS application in work](https://gitlab.com/gap-bs-front-end-autocode-documents/autocode-documents/-/raw/main/images/runjs-intro.png)

RunJS is available on macOS, Windows, and Linux operating systems.

Here are detailed instructions on installing and using it: [RunJS documentation](https://runjs.app/docs).

## Task Requirements

Every function should be in its file with export. Please, use the file names mentioned in the requirements to pass the tests.

When creating a function, you must use Function Declaration, or it will not be able to be verified. How to use Function Declaration: javascript.info: [Function Declaration](https://javascript.info/function-basics#function-declaration).

**Please, note:**

- If task requirement says: _Function should **return** <something>_, it means it should deliberately return expected value. If instead of returning a value, you will show it in the console, it will not pass the check. More about function returning value: [Returning a value](https://javascript.info/function-basics#returning-a-value).

1. **Function "hasDigit"**

Write a function `hasDigit` which checks with regular expression if input string contains digits.

In the `src` folder create the `hasDigit.js` file. This file should export function `hasDigit`:

```js
export function hasDigit(str) {
  // Your code
}
```

This function takes one parameter:
`str` - any string element or `null` or `undefined`.

1. The function should return `true` if there at least on digit in the `str` parameter.
2. The function should return `false` if `str` is `null`.
3. The function should return `false` if `str` is `undefined`.

Usage example:

```js
hasDigit("SomeSome"); // false
hasDigit("Some7Name"); // true
hasDigit("44"); // true
hasDigit(); // false
hasDigit(null); // false
```

2. **Function "isValidPhoneNumber"**

Write a function `isValidPhoneNumber` which checks with regular expression if input string is a valid number in format `555-555-5555`.

In the `src` folder create the `isValidPhoneNumber.js` file. This file should export function `isValidPhoneNumber`:

```js
export function isValidPhoneNumber(str) {
  // Your code
}
```

This function takes one parameter:
`str` - any string element or `null` or `undefined`.

1. The function should return `true` if it's format strickly corresponds to `555-555-5555`.
2. The function should return `false` if it's format doesn't correspond to `555-555-5555`. For example: `444.444.4444`, `333-33-33`, `55555555555`, `343434`, `555 555 55555` etc.
3. The function should return `false` if `str` is `null`.
4. The function should return `false` if `str` is `undefined`.

Usage example:

```js
isValidPhoneNumber("444-444-4444"); // true
isValidPhoneNumber("222 222 2222"); // false
isValidPhoneNumber("2222"); // false
isValidPhoneNumber(null); // false
isValidPhoneNumber(); // false
```

3. **Function "isValidEmail"**

Write a function `isValidEmail` which checks with regular expression if input string is valid email address.

In the `src` folder create the `isValidEmail.js` file. This file should export function `isValidEmail`:

```js
export function isValidEmail(str) {
  // Your code
}
```

This function takes one parameter:
`str` - any string element or `null` or `undefined`.

1. The function should return `true` if `str` is valid email.
2. The function should return `false` if `str` is not valid email.
3. The function should return `false` if `str` is `null`.
4. The function should return `false` if `str` is `undefined`.

**Note:**
An email is a string (a subset of ASCII characters) separated into two parts by `@` symbol. a `"personal_info"` and a domain, that is `personal_info@domain`. The length of the `personal_info` part may be up to 64 characters long and domain name may be up to 253 characters.

The `personal_info` part contains the following `ASCII`characters:

- Uppercase (`A-Z`) and lowercase (`a-z`) English letters.
- Digits (`0-9`).
- Characters **! # $ % & ' \* + - / = ? ^ \_ ` { | } ~**
- Character `.` (period, dot or fullstop) provided that it is not the first or last character and it will not come one after the other.
- The domain name [for example `com`, `org`, `net`, `in`, `us`, `info`] part contains letters, digits, hyphens, and dots.

Example of valid email:

- `mysite@ourearth.com`
- `my.ownsite@ourearth.org`
- `mysite@you.me.net`

Usage example:

```js
isValidEmail("mysite@gmail.com"); // true
isValidEmail("some.name@itpu.uz"); // true
isValidEmail("some-name@itpu.uz"); // true

isValidEmail("user"); // false
isValidEmail("user@com"); // false
isValidEmail("gmail.com"); // false

isValidEmail(null); // false
isValidEmail(); // false
```

4. **Function "filterArrayContainsString"**

Write a function `filterArrayContainsString` which filters Array items if they contain a string.

In the `src` folder create the `filterArrayContainsString.js` file. This file should export function `filterArrayContainsString`:

```js
export function filterArrayContainsString(array, str) {
  // Your code
}
```

This function takes two parameters:
`array` - array of strings
`str` - any string element.

1. The function should return array filtered from input `array`, and contain only items that have `str` as a substring in it.
2. The function should return return empty array, if input `array` items don't contain `str` as a substring.
3. The function should return array with the same items as input `array` if `str` is `null` of `undefined`.

Usage example:

```js
let arr = ["apple", "pineapple", "orange", "lemon"];

filterArrayContainsString(arr, "ap"); // ['apple', 'pineapple']
filterArrayContainsString(arr); // ['apple', 'pineapple', 'orange', 'lemon']
filterArrayContainsString(arr, "ppp"); // []
```

5. **Function "replaceASymbol"**

Write a function `replaceASymbol` will find all words starting and ending with the letter `a`, and replace each of them with `!`. Between the letters `a` can be any character (except `a`).
For example: string `aba accca azzza wwwwa` should give result with `! ! ! wwwwa`

In the `src` folder create the `replaceASymbol.js` file. This file should export function `replaceASymbol`:

```js
export function replaceASymbol(str) {
  // Your code
}
```

This function takes one parameters:
`str` - any string element or `null` or `undefined`.

1. The function should return new string with replaced `a` character with `!` sign in all words starting and ending with the letter `a`
2. The function should return new string that is equal to input `str` if no words starting and ending with letter `a` found.

Usage example:

```js
replaceASymbol("aba accca zzz wwaww"); // "! ! zzz wwaww"
replaceASymbol("zzz wwaww"); // "! ! zzz wwaww"
```
