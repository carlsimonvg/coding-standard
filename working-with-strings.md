# Working with strings
This document will define how to perform common tasks when working with strings.

## Concatenation
There are different scenarios where you want to do string concatenation. 
It can either be single or multi line text.

### Single Line
if you want to concatenate a string from different variables use the [es6 string interpolation](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Template_literals).  
example: '`${variable1} ${varialbe2}`'

### Single Line from Loop
The best way to concatenate a string in a loop is to populate an array with the values and then join the array when you are done.  

```
const result = [];
for(let i = 0; i < 1000; i++) {
    result.push(`string number ${i}`);
}
return result.join(" ");
```

### Multiline
When constructing multiline text you also use array joining.

```
const result = [];
result.push("line 1");
result.push("line 2");
result.push("line 3");
return result.push("\n");
```

## String find and replace
To replace values in a string you split the string into an array and rejoin it again.  
example:

```
"item1 and item2".spilt("and").join("or");
```

will result in `item1 or item 2`