# Scope

*Scope* is the visibility of a variable--where they can be seen, accessed, and used.

Most popular languages use *block* scope--a variable is defined in a block, and its scope is limited to that block unless you modify it.

JavaScript has _function_ scope--a variable's scope is the function it was created in. 

Starting with ES6, you can also define block scope in JavaScript using the `let` operator.

## About the "scope chain"

The scope chain: Scopes can nest. A nested variable can look "upward"--every inner level can access levels outside it. The scope chain is defined "lexically"--that is, functions run in the scope where they're defined, not the scope they're called from. 

For example: a function *called* inside another function, and attempting to use a variable inside the calling function, will return an error. A function *nested* inside another function, and using a variable in that calling function, will work.

Understanding scope is critical to working with JavaScript, because much of JavaScript programming is concerned with defining and manipulating scope.


## More Reading:
[You Don't Know JS: Scope and Closures](https://github.com/getify/You-Dont-Know-JS/blob/master/scope%20%26%20closures/ch3.md)