## Export Default

### Challenge Description
>In the `export` lesson, you learned about the syntax referred to as a `named export`. This allowed you to make multiple functions and variables available for use in other files.

>There is another `export` syntax you need to know, known as `export default`. Usually you will use this syntax if only one value is being exported from a file. It is also used to create a fallback value for a file or module.

>Here is a quick example of `export default`:

>```javascript
export default const add = (x,y) => {
  return x + y;
}
```

>There is a one major feature of `export default` you must never forget-since it is used to declare a fallback value for a module or file, **you can only have one value be a default export in each module or file**. 

### Instructions
>The following function should be the fallback value for the module. Please add the necessary code to do so.

### Challenge Seed
```javascript
const subtract = (x,y) => {return x - y;}
```

### Challenge Tests
```javascript
assert(code.match(/export\s+default\s+const\s+subtract\s+=\s+\(x,y\)\s+=>\s+{return\s+x\s-\s+y;}/ig))
```

### Challenge Solution
```javascript
export default const subtract = (x,y) => {return x - y;}
```