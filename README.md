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

- `slice` **copies** the array segment \[*startIndex*, *endIndex*). `slice()` copies the entire arrary.
- `splice` performs surgey on the the array, cutting out \[*startIndex*, *startIndex* + *deleteCount*) and optionally inserting *item1*, *item2*, ...

Tags: array, slice, splice, inclusive, exclusive, copy
