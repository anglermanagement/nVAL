# nVAL : not Very Accurate Language

Immutable Piece of Sh*t.

## Core Concept

1. Everything is **immutable** and **pure**.

2. ...But you **don't** get to choose.

3. Enjoy the outcome.

## Values and Functions

### Value Declaration

Simply, use the keyword `nval`.

```c
nval myFirstValue = 31;
print myFirstValue; // will NEVER print 31, but somewhere around 31.
```

Outcome may vary.

### Reassignment

You wish.

```c
nval mySecondValue = 42;
mySecondValue = 90; // Error! You cannot re-assign a value.
```

### Function Declaration

Must be a pure mathematical function.
Just like the `nval`s, you cannot assign anything inside a function.

```c
func myFirstFunc(myThirdValue, myFifthIMeanFourthValue) {
  // myThirdVariable = myThirdValue * myFifthIMeanFourthValue; // Error! You cannot re-assign a value.
  nval myFifthValue = myThirdValue;
  return myFifthValue * myFifthIMeanFourthValue;
  // return myThirdValue * myFifthIMeanFourthValue; // This is legal too.
}
```

If your function has a `side-effect`, you have to put `@impure`

```c
@impure
func mySecondFunc(mySixthValue) {
  print mySixthValue;
}
```

A value and a function can be used interchangably.

```c
func add(a, b) {
  return a + b;
}
// This is the same as :
// nval add = (a, b) => a + b; 
```

```c
func fourOfAKind(str) {
  nval strstr = str::str; // concat.
  return (str, str, str, strstr);
}
// This is the same as :
// nval fourOfAKind = (str) => { nval strstr = str::str; (str, str, str, strstr); }
```

## Statement

### Bool

* `a == b` when they are _about_ the same.
* `>` and `<` work like you think they would.
* There is no such thing as `!=`, `>=`, `<=`.

The followings are always false : 
- false

The followings are always true : 
- true
- (s,o,me,e,1,e,me,nts)
- 17717711
- **0**

### while

Sorry, no `if` or `for` loops. They serve no purpose in this language.

```c
nval bigNumber = 50;
while(bigNumber) { // repeats about 50 times
  print bigNumber; // prints 50ish numbers
}
```
