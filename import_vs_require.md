## Import vs. Require: What's the difference?

### Challenge Description
>In the past, the function `require()` would be used to import the functions and code in external files and modules. While handy, this presents a problem: some files and modules are rather large, and you may only need certain code from those external resources.

>ES6 gives us a very handy tool known as `import`. With it, we can choose which parts of a module or file to load into a given file, saving time and memory.

>Consider the following example. Imagine that `math_array_functions` has about 20 functions, but I only need one, `countItems`, in my current file. The old `require()` approach would force me to bring in all 20 functions. With this new `import` syntax, I can bring in just the desired function, like so: 

>```javascript
import { countItems } from "math_array_functions"
```

>A description of the above code: 
```javascript
import { function } from "file_path_goes_here" 
```

>There are a few ways to write an `import` statement, but the above is a very common use-case. Note: the whitespace surrounding the function inside the curly braces is a best practice-it makes it easier to read the `import` statement.

### Instructions
>Add the appropriate `import` statement that will allow the current file to use the `capitalizeString` function. The file where this function lives is called "string_functions," and it is in the same directory as the current file.

### Challenge Seed
```javascript
capitalizeString("hello!");
```

### Challenge Tests
```javascript
assert(code.match(/import\s+\{\s?capitalizeString\s?\}\s+from\s+\"string_functions\"/ig)
```

### Challenge Solution
```javascript  
import { capitalizeString } from "string_functions";

capitalizeString("hello!");

```
