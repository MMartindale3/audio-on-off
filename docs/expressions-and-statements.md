# Equality Operators

## Expression

At its core, an expression is a bit of JavaScript code that produces a value. You create an expression any time you combine values, variables, and operators, which computes to a value. The computation is called an evaluation.

```js
1 → produces 1
"hello" → produces "hello"
5 * 10 → produces 50
num > 100 → produces either true or false
isHappy ? "🙂" : "🙁" → produces an emoji
[1, 2, 3].pop() → produces the number 3
```

## Statements

A JavaScript program is a sequence of statements. Each statement is an instruction for the computer to do something. Statements typically end in a semi-colon, which marks the end of the statement. The semi-colon isn't necessary for certain statements, like if statements, while loops, and function declarations.

**Example of a JavaScript statements**

```js
let taxRate = 0.05;
// or
loginButton.addEventListener("click", onLoginRequest);
//or
throw new Error("Something exploded!");
```

Think of statements as the building blocks to build a program the blank room, while expressions fill in the details a bed room with a bed coloured walls lights etc.

<div style=" width:600px; display:flex; justify-content:center; gap:0.5rem ">
<img  src="./img/blank-room.jpeg" width="300" alt="blank room">
<img src="./img/bed-room.jpg" width="300" alt="blank room">
</div>

## Slots

Statements often have "slots" for expressions. We can put any expression we like into those slots.

```js
let hi = /* some expression */;
```

For example, declaring a variable has an expression slot.  
We can use any of the expressions we saw earlier in that slot:

```js
let hi = 1;
let hi = "hello";
let hi = 5 * 10;
let hi = num > 100;
let hi = isHappy ? "🙂" : "🙁";
let hi = [1, 2, 3].pop();
```

In terms of valid syntax, expressions are interchangeable. If a statement has an expression slot, we can put any expression there, and the code will run. We won't get a syntax error.

That said, we can still run into other issues. For example, the following code is syntactically valid, but we'll crash the browser tab if we try to run it, since it causes an infinite loop:

```js
while ("hello") {
	// Because “hello” never changes, this loop will
	// run over and over until the script crashes.
	// Syntactically valid, but still problematic.
}
```

## A handy trick

If you want to know whether a chunk of JS is an expression or a statement log it out to the console.

---

If it runs, the code is an expression.  
If you get an error, it's a statement (or, possibly, invalid JavaScript syntax).

The nice thing about using the console is you can see what value an expression resolves to!  
Even as an experienced developer, I rely a ton on console.log. It's a wonderfully versatile tool!

## Functions Arguments and Expressions

When you use a function all function arguments must be expressions.
Expressions produce a value, and that value will be passed into the function.

```js
/*
    When calling a function the arguments being passed must be expressions (values).
    The expression will resolve to a value and the values are passed into the function (parameters).
*/
renderTemplate("Jane Doe", "Tracking Management");

function renderTemplate(name, department) {
	console.log(`<p>${name} ${department}</p>`);
}
```

Statements don't produce a value, and so they can't be used as function arguments.

```
console.log(/* Some chunk of JS here */);
```
