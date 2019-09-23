---
marp: true
title: Intro To Functions
theme: uncover
---

<!-- backgroundColor: #393D3F -->
<!-- color: #D7FFF1-->

# An Introduction to Functions
# From Code Immersives

![w:300](https://scontent-lga3-1.xx.fbcdn.net/v/t1.0-9/67457288_2444284939180138_6392391575451729920_n.png?_nc_cat=103&_nc_oc=AQmZLB7bEGi-TWLw0PGVwUYGxQknlSNkCXmrSQLFdQKlZbBwK6Hxs6aheAkaxgfzknU&_nc_ht=scontent-lga3-1.xx&oh=b2dd9a8e2eb214237407cd69358e1831&oe=5E161CD7)

---

### Functions

![w:300](https://3.bp.blogspot.com/-42oCVxzA_qI/T1GmphVyvxI/AAAAAAAAQJw/pS1nJXrbXXc/s400/Assembly_Line.jpg)

Every part of your code should have one job! That makes it easy to separate your code, so you can:

* Run the same code whenever you need to without repeating yourself.
* Easily see what a bit of code is supposed to do.
* Figure out why it's not, in fact, doing that.

---

### What does a function look like?


```javascript
function bumpX() {
  x = x + 1;
}
```

---

### What are all those parts, though?

```javascript
function bumpX() {
  x = x + 1;
}
```

* `function` declares the function - like `let` or `const` for variables.
* `bumpX` is the name of the function.
* Everything in the curly braces is the code that runs when the function is "called".

---

### Let's see it in action!

```javascript
let x = 3;

function bumpX() {
  x = x + 1;
}
```

What is x now?

---

### We "call" a function by saying its name _with parentheses_.

```javascript
let x = 3;

function bumpX() {
  x = x + 1;
}

bumpX();
```

What is x NOW?

---

### Calling it multiple times?

```javascript
let x = 3;

function bumpX() {
  x = x + 1;
}

bumpX();
bumpX();
bumpX();
```

What is x after all those function calls?

---

### Scope - What happens in functions stays in functions.

* Inside a function, you can look at the code outside.
* But outside a function, the code inside is a black box.

---

### So `bumpX` can see `x`.

```javascript
let x = 3;

function bumpX() {
  x = x + 1;
}

bumpX();
bumpX();
bumpX();
```

---

### But code outside can't see anything in.

```javascript
let x = 3;

function bumpX() {
  x = x + 1;
  let y = 3;
}

bumpX();

y = y + 1;
```

ERROR!