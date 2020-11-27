# parlor-tricks-js
A list of random JavaScript parlor tricks.  See also [parlor-tricks-py](https://github.com/spaceaardvark/parlor-tricks-py/).

### Regex: tokenize repeating characters in a string

```javascript
const test = "1101000000101";
const regex = /(\w)\1*/g

const tokens = test.match(regex);

console.log(tokens); 
// => [ '11', '0', '1', '000000', '1', '0', '1' ]
```

Tags: regex, string, sequence, repeating, characters, binary gap, run-length encoding

### Array: `slice` vs. `splice`

- `slice` **copies** the array segment \[*startIndex*, *endIndex*).
- `splice` performs surgey on the the array, cutting out \[*startIndex*, *startIndex* + *deleteCount*) and optionally inserting *item1*, *item2*, ...

Bonus: `xs.slice()` makes a quick shallow copy of the array.

Tags: array, slice, splice, inclusive, exclusive, copy

### Array: `sort`

- sort **numbers** with `xs.slice().sort((a, b) => a - b)`.
- sort everything else with `xs.slice().sort()`.

### Binary: *n* bits will all *1*s

16 bits = `Math.pow(2, 17) - 1`
n bits = `Math.pow(2, n) - 1`

This is a shortcut derived from the [sum of the first n terms of a geometric series](https://en.wikipedia.org/wiki/Geometric_series#Formula).

Tags: binary, shift, bits, geometric series

