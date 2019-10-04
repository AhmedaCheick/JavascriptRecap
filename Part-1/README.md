# JS Recap
## Agenda 
---
### `Types, Operators and Values`

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

NaN // not a number (confused)

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
### `Comparison:`
#### `Numeric:` 
```javascript
3 < 2 // less than
false // output

1.01 > 1 // greater than
true 
```
#### `Strings:` *Sanity Check* 

```javascript
"z" > "a" // is "z" greater than "a"
true // output
```
Strings are ordered **alphabetically**. "a" being the 'smallest' to "z" the 'largest'.
```javascript
"Z" > "a" // is capital "Z" greater than "a"?
false // output 
```
Well, with the exception of uppercase letters. They are always “less” than lowercase ones. 
<br>
To visually see it from "largest" to "smallest": <br>
<br>
`z > y > x > w > v > ... b > a > Z > Y > X > ... > B > A` <br>
<br>
(...) The three dots here simply indicate an intentional omission of the letters but the pattern should be clear. <br>
<br>
So, how will javascript compare **longer** strings (i.e words, sentences)? <br>
Javascript goes over the string from left to right, comparing the unicodes (characters) one by one: <br>
* Compares first characters of both words, decides whether one is greater or they're both equal. 
* When both firsts are equal, goes on to compare the next two. 
* Repeat until the end. 
* If both strings end at the same length, then they are equal. Otherwise, the longer string is greater.

#### `Other`
```javascript
>= // greatr than or equal to 
<= // less than or equal to 
!= // not equal to 
```
**Note:** There is only one value in JavaScript that is not equal to itself, and that is `NaN`. 
```javascript
console.log(NaN == NaN)
false // this is bc it's the result of nonsensical computation and that can be different every time.
``` 

#### `Logical Operators`
Applied to Boolean values. <br>
* and: `&&`
* or: `||`
* not: `!`
<br>
<strong>!</strong> flips the value behind it. 
<br>

```javascript
!true // read: not true
false // output: produces false 
```
<br>
<strong>null</strong> and <strong>undefined</strong> are empty values and the difference can be ignored. 

#### `Automatic Conversion`
Javascript tries to please everyone. There's a cost to that "openness".
```javascript
12 * null // multiplication 
0 // output 

"51" - 1 // the string "51" minus 1
50 // outputs the number 50

"5" + 1 // string "5" plus 1
"51" // outputs the string "51"

"five" * 2 // string "five" times 2
NaN // output 'Not a Number'
```
This is just Javascript being Javascript. This is called *type coercion*. JS notices an operation and tries its "best" to satisfy the instructions by quietly converting the values. <br>
In the **first case**, `null` becomes `0`. In the **second case**, it recognizes `"51"` as a string but also realizes that `-` is an operator on numerics and `1` is also a numeric value. Whereas in the **third case**, the `+` operator is used for concatinating two strings together and "5" is already a string, so it makes sense to cast `1` as a string as well. 
<br>

`==` tests whether both values are the same.<br>
`===` tests whether the type and content matches. <br>
`!==` Will return true if they're not equal in type and/or content. 
