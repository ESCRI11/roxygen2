# roxygen2 <img src="man/figures/logo.png" align="right" />
Hacky update to the [`roxygen2`](https://github.com/r-lib/roxygen2) package.

This will be able to document `R6` classes that are declared over multiple files using the `$set` method.

For this to work, the files should be named as follows:
```
.
├── R
│   ├── R6Class.R
│   ├── R6Class$method1.R
│   └── R6Class$method1.R
│   .
│   .    
.
.

```
In short:

+ Declare the `R6` class `MyClass` in a file named `MyClass.R`
+ Declare the new methods for the class `MyClass` in individual (you can have multiple `$set` on the same file, it will still work) files named `MyClass$my-method.R`

Use at your own risk
