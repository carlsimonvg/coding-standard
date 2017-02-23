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

### Determining if a string matches a search string
To check if a search string exists in a string check the index for that item.
If the index is greater than -1 then the substring is present in the string
example:

```
const isPresent = "hello world".indexOf("wo") > -1;
```

if you are doing a case insensitive search search the string in it's lowercase form.

example:

```
const isPresent = "Hello World".toLowerCase().indexOf("wo") > -1;
```

## Closing
There are a number of [string functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) in javascript;  
If a string function exists as a rule, that is the function you should use.
Please familiarise yourself with the functions that already exist in javascript.

