# Comparison Operators

[Full List of JavaScript Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_operators#comparison_operators)

**Equality**  
A comparison operator compares its operands and returns a logical value based on whether the comparison is true.

```javascript
let a = "9";
let b = 9;
console.log(b == a);
/*
expected output true
Data types are not compared so 9 equals the string "9" this is true.
The eqaulity operator == is asking is true, true which is true 
*/
```

**Not Equal**  
The inequality (!=) operator checks whether its two operands are not equal, returning a Boolean result.

```javascript
let a = "9";
let b = 9;
console.log(b != a);
/*
expected output false

The data types are not being compared so as far a javascript is concerned the number 9 equals the string "9". JavaScript is comparing the values javascript looks inside the string and sees that the value  9  inside the quotes, does in fact equal 9 so this is true. However your asking if true is not true which is false. 
*/
```

**Strict Equality**

```javascript
let a = "9";
let b = 9;
console.log(b === a);
/*
expected output false
 
The strict eqaulity operator === is asking are both the data and the value true. The return value is false because the number 9 does not equal the string "9". 
*/
```

**Strictly Not Equal**

```javascript
let a = "9";
let b = 9;
console.log(b !== a);
/*
expected output true

The eqaulity operator !== is asking are both the data and the value are not equal. The number 9 does not equal the string "9", so the expression evaluates to true
*/
```

**Greater Than**

```javascript
let a = 100;
let b = 9;
console.log(b > a);
/*
expected output false

The greater than operator is asking weather 9 is greater than 100. So to the JavaScript compiler point of view is that 9 is not greater than 100 and returns false.
*/
```

**Greater Than Equal To**

```javascript
let a = 9;
let b = 9;
console.log(a >= b);
/*
expected output true

The greater than equal to operator is asking weather 9 is greater or equal to 9. So from the compiler's point of  view 9 is equal to 9 and returns true.
*/
```

**Less Than**

```javascript
let a = 9;
let b = 9;
console.log(a < b);
/*
expected output false

The less than operator is asking weather 9 is less than 9. The javascript compiler's sees that it is equal but not less than so it returns false.
*/
```

**Less Than Equal To**

```javascript
let a = 9;
let b = 9;
console.log(a <= b);
/*
expected output true

The less than operator is asking weather 9 is less than 9. The javascript compiler's sees that 9 is equal to 9 and so  returns true.
*/
```
