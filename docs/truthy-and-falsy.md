# Truthy and Falsy Values

In JavaScript, a truthy value is a value that is considered true when encountered in a Boolean context. All values are truthy unless they are defined as falsy.

## Falsy Values

The falsy values in javascript are as follows:

1. false
2. 0
3. ""
4. null
5. undefined
6. NaN

## Logical And

If the first operand is truthy, the logical AND operator `&&` returns the second operand. The && operator is executed before the || operator (see below ).

```javascript
console.log(4 &&  2;);
// Expected output: 2
```

If the first operand is falsy, the logical AND operator `&&` returns the first operand:

```javascript
console.log(null && 4);
// Expected output: null
```

**Logical or**
The logical OR `||` is evaluated left to right. The operator returns the value of one of the specified operands based on its truthy of falsy value.

```javascript
//  if the left side is falsy returns the right side
console.log("" || "right side");

//  if the left side is truthy returns the left side
console.log("I am the left" || null);

// if both sides are truthy then the left side is returned
console.log("left side" || "right side");

//  if both sides are falsy the right side is returned
console.log(undefined || NaN);
```
