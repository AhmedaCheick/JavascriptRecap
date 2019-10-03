# JS Recap
## Agenda 
---
### Types, Operators and Values

```javascript
// numbers 
7.43

// Very small/big numbers can be represented using exponents (e)
2.4e8 // same as 240000000

+ // addition
* // multiplication 
- // subtraction 
% // remainder or modulo

// Creful using these two
Infinity // + infinity 
-Infinity // - infinity 

NaN // not a number 

// As long as the the quotes at the start and the end of the string match
// String can be represented in 3 ways
"I am  a string"
'This is another string'
`Me too, but I am special` // template literals, allow for value-embedding

`5+5 is ${5+5}` // code 
"5+5 is 10" // output 

// Unary operator 
typeof 4; // code
"number" // output 

typeof "S" // code
"string" // output 
```
### Comparison:
#### Numeric: So far so good
```javascript
3 < 2 // less than
false // output

1.01 > 1 // greater than
true 
```
#### Strings: *This is where JS fails the sanity check* 

```javascript
"z" > "a" // is "z" greater than "a"
true // output
```
Strings are ordered alphabetically. "a" being the 'smallest' to "z" the 'largest'.
```javascript
"Z" > "a" // is capital "Z" greater than "a"?
false // output 
```
Well, with the exception of a upper cases. uppercase letters are always “less” than lowercase ones.  