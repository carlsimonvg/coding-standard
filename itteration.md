# Introduction
There are a number of ways to loop through collections. This document will provide some guidance around that.

## Itterators
Itterators have it's place but is not a substitute for normal looping.
Itterators are to be used for async actions where the next item request is not nessisarily a sequencial action.

## For Loops
NEVER use for-in loops.  
By default for loops to use are [for of](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Statements/for...of) loops.

