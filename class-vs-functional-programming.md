#Introduction

Javascript has good support for both functional programming and object orientation.
The purpose of this document is to define when to use functional vs oop and the limitations around it.

## Functional
### Try to favoid
1. avoid closures  
1. avoid potential memory leaks  
### Rules around functional use
1. Only use functional programming when for utility functions.  
1. All resources required by the function must be passed to the function.  
1. Functions can return any object type.  
1. Do not use sub functions.
1. Do not access any resources of any types outside the scope of the function unless you are calling another function.

## Classes
Classes has two type basic types.  
1. Standard class  syntax  
1. Prototype syntax

Prototypes are only used in cases where classes are required but no transpilation is available or in an environment where the ES2015 syntax is not supported.

Classes are supper usefull for resource management.  
All resources constructed should also be destructed.
Though classes don't naturally have destructors, all destructors should be named "dispose()".
All pointers accessing constructed resources or external resources must be set to null when no longer in use.
Use the dispose method on constructed resources before setting it to null.

## Object literals
1. Use object literals for construction of data units.
2. Object literals may contain functions related to properties of the object literal.
3. Object literal functions may only access and manipulate data of the object lteral.

## summary
All functions are self contained utilities.
