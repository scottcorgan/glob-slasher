# glob-slasher

Prefix an object (key/values) of globs with a slash and normalize. Supports negated globs too. Glob version of slasher module

## Install

```
npm install glob-slasher --save
```

## Usage

```js
var slasher = require('glob-slasher');

// Strings
var pathname = '!**/something';
console.log(slasher(pathname)); // OUTPUTS: '!/**/something'

// Arrays
var globs = ['!**/something', '/here'];
console.log(slasher(globs)); // OUTPUTS: ['!/**/something', '/here']

// Objects
var globs = {
  '**/some/route': 'index.html'
};
console.log(slasher(globs));

// OUTPUTS:
{
  '/**?some/route': '/index.html'
}
```

## Run Tests

```
npm install
npm test
```
