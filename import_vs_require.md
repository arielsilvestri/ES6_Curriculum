## Import vs. Require: What's the difference?

### Challenge Description
>In the past, you may or may not have used `require()` to bring in code from an external file or to load a module. It is commonly used in Node to load up and establish a connection to a database:

>```javascript
var pg = require('pg') //This loads PostgreSQL into the current file```

>With the above code, we now have access to all the functions associated with the PostgreSQL module. While this works fine, it introduces a potential problem: Some modules are very robust, and we may only need a few of its functions for a given scope.

>ES6 gives us a very handy tool known as `import`. With it, we can choose which parts of a module or file to load in a given scope, saving time and memory. 

>Let's draw out an example. Say I have a file, `math_array_functions` with twenty functions. One of those functions, `countItems,` will count the number of items in an array. I really need this function in another file, `counting_array_items`, which is in the same directory, but I don't want to load all twenty functions. That's where `import` becomes handy! See below for how we do this:

>```javascript
import { countItems } from "math_array_functions"```

>And just like that, we can use our `countItems` function in `counting_array_items` without loading the other 19 functions.

### Instructions
>In the code below, there are two require statements in a file, `proper_name` that are loading code from two other files in the same directory. One of the files, `string_functions`, has a few hundred functions that do something to a string. The other file, `proper_name_functions`, has 15 functions that are designed to work with proper name. With this information, determine which file should be fully loaded and which file you should import a specific function, `capitalizeString`, from.

>Hint: Compare the file names to determine this.

### Challenge Seed
```javascript
  var string_functions = require("string_functions")
  var proper_name_functions = require("proper_name_functions")
```

### Challenge Tests
```javascript
  // Test capitalizeString is defined
  // Test capitalizeString is a function
  // Test capitalizeString is inside of curly brackets
  // Test proper_name_functions is defined
  // Test proper_name_functions is a require statement
```

### Challenge Solution
```javascript
  import { capitalizeString } from "string_functions"
  var proper_name_functions = require("proper_name_functions")
```
