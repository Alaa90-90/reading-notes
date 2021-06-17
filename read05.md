# Logical operators
Logical operators are typically used with Boolean (logical) values; when they are, they return a Boolean value. However, the && and || operators actually return the value of one of the specified operands, so if these operators are used with non-Boolean values, they may return a non-Boolean value. The logical operators are described in the following table.

## Logical operators

| Logical AND (&&)  | expr1 && expr2      | Returns expr1 if it can be converted to false; otherwise, returns expr2. Thus, when used with Boolean values, && returns true if both operands are true; otherwise, returns false.            |
| Logical OR (||)   | expr1 || expr2      | Returns expr1 if it can be converted to true; otherwise, returns expr2. Thus, when used with Boolean values, || returns true if either operand is true; if both are false, returns false.   |
| Logical NOT (!)   |	!expr             | Returns false if its single operand that can be converted to true; otherwise, returns true.|

|----|----|----|
|    |    |    |
|    |    |    |

	
The following code shows examples of the && (logical AND) operator.

var a1 =  true && true;     // t && t returns true
var a2 =  true && false;    // t && f returns false
var a3 = false && true;     // f && t returns false
var a4 = false && (3 == 4); // f && f returns false
var a5 = 'Cat' && 'Dog';    // t && t returns Dog
var a6 = false && 'Cat';    // f && t returns false
var a7 = 'Cat' && false;    // t && f returns false
Copy to Clipboard
The following code shows examples of the || (logical OR) operator.

var o1 =  true || true;     // t || t returns true
var o2 = false || true;     // f || t returns true
var o3 =  true || false;    // t || f returns true
var o4 = false || (3 == 4); // f || f returns false
var o5 = 'Cat' || 'Dog';    // t || t returns Cat
var o6 = false || 'Cat';    // f || t returns Cat
var o7 = 'Cat' || false;    // t || f returns Cat
Copy to Clipboard
The following code shows examples of the ! (logical NOT) operator.

var n1 = !true;  // !t returns false
var n2 = !false; // !f returns true
var n3 = !'Cat'; // !t returns false
Copy to Clipboard
Short-circuit evaluation
As logical expressions are evaluated left to right, they are tested for possible "short-circuit" evaluation using the following rules:

false && anything is short-circuit evaluated to false.
true || anything is short-circuit evaluated to true.
The rules of logic guarantee that these evaluations are always correct. Note that the anything part of the above expressions is not evaluated, so any side effects of doing so do not take effect.

Note that for the second case, in modern code you can use the new Nullish coalescing operator (??) that works like ||, but it only returns the second expression, when the first one is "nullish", i.e. null or undefined. It is thus the better alternative to provide defaults, when values like '' or 0 are valid values for the first expression, too.