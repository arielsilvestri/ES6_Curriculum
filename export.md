## Export: One of Import's siblings.

### Challenge Description.
>In the previous challenge, you learned about `import` and how it can be leveraged to import small amounts of code from large files. In order for this to work, though, we must utilize one of the statements that goes with `import`, known as `export`. When we want some code-a function, or a variable-to be usable in another file, we must `export` it in order to `import` it into another file. 

>The following is what we refer to as a `named export`. With this, we can `import` any code we `export` into another file with the `import` syntax you learned in the last lesson. Here's an example:

>```javascript
const capitalizeString = (string) => {
  return string.charAt(0).toUpperCase() + string.slice(1);
} 

export { capitalizeString } //How to export functions.
export const foo = "bar"; //How to export variables.
```

>Alternatively, if you would like to compact all your export statements into one line, you can take this approach:

>```javascript
const capitalizeString = (string) => {
  return string.charAt(0).toUpperCase() + string.slice(1);
}

const foo = "bar";

export { capitalizeString, bar }
```

>Either approach is perfectly acceptable.

### Instructions
>Below are two variables that I want to make available for other files to use. Utilizing the first way I demonstrated `export`, `export` the two variables.

### Challenge Seed
```javascript
const foo = "bar";
const boo = "far";
```

### Challenge Tests
```javascript
assert(code.match(/export\s+const\s+foo\s+=+\s"bar"/ig)
assert(code.match(/export\s+const\s+boo\s+=+\s"far"/ig))
```

### Challenge Solutions
```javascript
export const foo = "bar";
export const boo = "far";
```
