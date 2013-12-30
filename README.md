# Variadic

Return a function that accepts a variable number of arguments as the last parameter.

## Installation

```
npm install variadic --save
```

## Usage

```javascript
var variadic = require('variadic');

var fn = variadic(function (args) {
  return args;
});

fn(); //=> []
fn('a'); //=> ['a']
fn('a', 'b') //=> ['a', 'b'];

var fn = variadic(function (a, b, args) {
  return { a: a, b: b, args: args };
});

fn(); //=> { a: undefined, b: undefined, args: [] }
fn('a'); //=> { a: 'a', b: undefined, args: [] }
fn('a', 'b', 'c', 'd', 'e'); //=> { a: 'a', b: 'b', args: ['c', 'd', 'e'] }
```

## License

MIT
