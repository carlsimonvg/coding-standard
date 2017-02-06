#Introduction
One of the more difficult things to manage in javascript is variable scope.
Applying these rules will assist in managing varialbe scope so that your code is more secure and less leaky.

## variable
Historicall declaring variables is done by using the "var" keyword.
For all intense purposes this word never existed and should under no circomstances ever be used in your code. EVER.
If you want to declare a varialbe use the keyword "let".
All evergreen browsers and nodejs support let and const, no need to ever use var.

## constants
Constants are declared using the "const" keyword. People often default to declaring varialbes but this should not be the case.
ALWAYS use constants as the default declaration unless the value changes. If the value changes use let.

## Summary
1. NEVER use var
1. ALWAYS use const as the default
1. ONLY when the value chagnes change the const to a let.