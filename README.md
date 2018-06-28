<img src="https://user-images.githubusercontent.com/799578/41671640-51642072-74ea-11e8-8bf2-7588062eed70.png" width="300">

# Swift and JavaScript comparison snippets

**Issue and pull request are welcome, please!**

# Table of content
- [The Basics](#the-basics)
- [Basic Operators](#basic-operators)
- [Strings and Characters](#strings-and-characters)
- [Collection Types](#collection-types)
- [Control Flow](#control-flow)
- [Functions](#functions)
- [Closures](#closures)
- [Enumerations](#enumerations)
- [Structures and Classes](#structures-and-classes)
- [Properties](#properties)
- [Methods](#methods)
- [Subscripts](#subscripts)
- [Inheritance](#inheritance)
- [Initialization](#initialization)
- [Deinitialization](#deinitialization)
- [Optional Chaining](#optional-chaining)
- [Error Handling](#error-handling)
- [Type Casting](#type-casting)
- [Nested Types](#nested-types)
- [Extensions](#extensions)
- [Protocols](#protocols)

> This table of content is from [The swift programming language guide](https://docs.swift.org/swift-book/LanguageGuide/TheBasics.html)

## The Basics
### Constants and Variables
Swift

```swift
// declare a constant 
let maximumNumberOfLoginAttempts = 10

// declare a variable
var currentLoginAttempt = 0

// declare multiple constants or multiple variables on a single line, separated by commas
var x = 0.0, y = 0.0, z = 0.0
```

JavaScript
```javascript
// declare a constant 
const maximumNumberOfLoginAttempts = 10

// declare a variable
var currentLoginAttempt = 0 
// or 
let currentLoginAttempt = 0

// declare multiple constants or multiple variables on a single line, separated by commas
var x = 0.0, y = 0.0, z = 0.0

```

### Comments
Swift
```swift
// This is a comment.

/* This is also a comment
but is written over multiple lines. */

```

JavaScript
```javascript
// This is a comment.

/* This is also a comment
but is written over multiple lines. */

```

### Numeric Type Conversion

Swift
```swift
let pi = 3.14159
// Integer and Floating-Point Conversion
let integerPi = Int(pi)
```

JavaScript
```javascript
const pi = 3.14159
// Integer and Floating-Point Conversion
const integerPi = parseInt(pi)
```

### Booleans
Swift
```swift
let orangesAreOrange = true
let turnipsAreDelicious = false

if turnipsAreDelicious {
    print("Mmm, tasty turnips!")
} else {
    print("Eww, turnips are horrible.")
}
```

JavaScript
```javascript
const orangesAreOrange = true
const turnipsAreDelicious = false

if (turnipsAreDelicious) {
    console.log("Mmm, tasty turnips!")
} else {
    console.log("Eww, turnips are horrible.")
}
```

### Error Handling
Swift
```swift
func canThrowAnError() throws {
    // this function may or may not throw an error
}
do {
    try canThrowAnError()
    // no error was thrown
} catch {
    // an error was thrown
}

```

JavaScript
```javascript
function canThrowAnError() {
    // this function may or may not throw an error
}
try {
    canThrowAnError()
    // no error was thrown
} catch (e) {
    // an error was thrown
}
```
## Basic Operators
### Assignment Operator
Swift
```swift
let b = 10
var a = 5
a = b

// decomposed tuple with multiple values into multiple variables
let (x, y) = (1, 2)
print("x = \(x), y = \(y)") // x = 1, y = 2
```

JavaScript
```javascript
let b = 10
var a = 5
a = b

// object matching with destructuring assignment
const {x, y} = {x:1, y:2}
console.log(`x = ${x}, y = ${y}`) // x = 1, y = 2
// or array matching with destructuring assignment
const [x, y] = [1, 2]
console.log(`x = ${x}, y = ${y}`) // x = 1, y = 2
```
### Arithmetic Operators
- Addition (+)
- Subtraction (-)
- Multiplication (*)
- Division (/)

Swift
```swift
1 + 2       // equals 3
5 - 3       // equals 2
2 * 3       // equals 6
10.0 / 2.5  // equals 4.0
"hello, " + "world"  // equals "hello, world"
```

JavaScript
```javascript
1 + 2       // equals 3
5 - 3       // equals 2
2 * 3       // equals 6
10.0 / 2.5  // equals 4
"hello, " + "world"  // equals "hello, world"
```
### Remainder Operator
Swift
```swift
9 % 4    // equals 1
-9 % 4   // equals -1
```

JavaScript
```javascript
9 % 4    // equals 1
-9 % 4   // equals -1
```
### Unary Minus/Plus Operator
Swift
```swift
let three = 3
let minusThree = -three       // minusThree equals -3
let plusThree = -minusThree   // plusThree equals 3, or "minus minus three"

let minusSix = -6
let alsoMinusSix = +minusSix  // alsoMinusSix equals -6
```

JavaScript
```javascript
const three = 3
const minusThree = -three       // minusThree equals -3
const plusThree = -minusThree   // plusThree equals 3, or "minus minus three"

const minusSix = -6
const alsoMinusSix = +minusSix  // alsoMinusSix equals -6
```
### Compound Assignment Operators
Swift
```swift
var a = 1
a += 2 // a is now equal to 3
```

JavaScript
```javascript
let a = 1
a += 2 // a is now equal to 3
```
### Comparison Operators
- Equal to (a == b)
- Not equal to (a != b)
- Greater than (a > b)
- Less than (a < b)
- Greater than or equal to (a >= b)
- Less than or equal to (a <= b)
- Identity operators, refer to the same object instance (a === b)
- Identity operators, not refer to the same object instance (a !== b)

Swift
```swift
1 == 1   // true because 1 is equal to 1
2 != 1   // true because 2 is not equal to 1
2 > 1    // true because 2 is greater than 1
1 < 2    // true because 1 is less than 2
1 >= 1   // true because 1 is greater than or equal to 1
2 <= 1   // false because 2 is not less than or equal to 1

let name = "world"
if name == "world" {
    print("hello, world")
} else {
    print("I'm sorry \(name), but I don't recognize you")
}
// Prints "hello, world", because name is indeed equal to "world".

let p1 = Person();
let p2 = Person();
p1 === p2 // false
p1 !== p2 // true

```

JavaScript
```javascript
1 == 1   // true because 1 is equal to 1
2 != 1   // true because 2 is not equal to 1
2 > 1    // true because 2 is greater than 1
1 < 2    // true because 1 is less than 2
1 >= 1   // true because 1 is greater than or equal to 1
2 <= 1   // false because 2 is not less than or equal to 1

const name = "world"
if (name == "world") {
    console.log("hello, world")
} else {
    console.log(`I'm sorry ${name}, but I don't recognize you`)
}
// Prints "hello, world", because name is indeed equal to "world".

const p1 = new Person();
const p2 = new Person();
p1 === p2 // false
p1 !== p2 // true
```
### Ternary Conditional Operator
Swift
```swift
let contentHeight = 40
let hasHeader = true
let rowHeight = contentHeight + (hasHeader ? 50 : 20)
// rowHeight is equal to 90
```

JavaScript
```javascript
const contentHeight = 40
const hasHeader = true
const rowHeight = contentHeight + (hasHeader ? 50 : 20)
// rowHeight is equal to 90
```
### Logical Operators
- Logical NOT (!a)
- Logical AND (a && b)
- Logical OR (a || b)

Swift
```swift
let allowedEntry = false
if !allowedEntry {
    print("ACCESS DENIED")
}
// Prints "ACCESS DENIED"

let hasDoorKey = false
let knowsOverridePassword = true
let hasDoorKey = false
let knowsOverridePassword = true
if enteredDoorCode && passedRetinaScan || hasDoorKey || knowsOverridePassword {
    print("Welcome!")
} else {
    print("ACCESS DENIED")
}
// Prints "Welcome!"
```

JavaScript
```javascript
const allowedEntry = false
if (!allowedEntry) {
    console.log("ACCESS DENIED")
}
// Prints "ACCESS DENIED"

const hasDoorKey = false
const knowsOverridePassword = true
const hasDoorKey = false
const knowsOverridePassword = true
if (enteredDoorCode && passedRetinaScan || hasDoorKey || knowsOverridePassword) {
    console.log("Welcome!")
} else {
    console.log("ACCESS DENIED")
}
// Prints "Welcome!"
```

## Strings and Characters
### String Literals
Swift
```swift
let someString = "Some string literal value"

// Multiline String Literals with three double quotation marks (""")
let quotation = """
The White Rabbit put on his spectacles.  "Where shall I begin,
please your Majesty?" he asked.

"Begin at the beginning," the King said gravely, "and go on
till you come to the end; then stop."
"""

// String Mutability
var variableString = "Horse"
variableString += " and carriage"
// variableString is now "Horse and carriage"

let constantString = "Highlander"
constantString += " and another Highlander"
// this reports a compile-time error - a constant string cannot be modified
```

JavaScript
```javascript
const someString = "Some string literal value"

// Multiline String Literals back-tick (` `) 
const quotation = `
The White Rabbit put on his spectacles.  "Where shall I begin,
please your Majesty?" he asked.

"Begin at the beginning," the King said gravely, "and go on
till you come to the end; then stop."
`

// String Mutability
let variableString = "Horse"
variableString += " and carriage"
// variableString is now "Horse and carriage"

const constantString = "Highlander"
constantString += " and another Highlander"
// this reports a compile-time error - a constant string cannot be modified
```

### String Interpolation
Swift
```swift
// insert values into the string literal is wrapped in a pair of parentheses, prefixed by a backslash (\)
let multiplier = 3
let message = "\(multiplier) times 2.5 is \(Double(multiplier) * 2.5)"
// message is "3 times 2.5 is 7.5"
```

JavaScript
```javascript
const multiplier = 3
const message = `${multiplier} times 2.5 is ${multiplier * 2.5}`
// message is "3 times 2.5 is 7.5"
```

### Accessing and Modifying a String
Swift
```swift
// String Indices
let greeting = "Guten Tag!"
greeting[greeting.startIndex]
// G
greeting[greeting.index(before: greeting.endIndex)]
// !
greeting[greeting.index(after: greeting.startIndex)]
// u


// Inserting and Removing
var welcome = "hello"
welcome.insert("!", at: welcome.endIndex)
// welcome now equals "hello!"

welcome.insert(contentsOf: " there", at: welcome.index(before: welcome.endIndex))
// welcome now equals "hello there!"

welcome.remove(at: welcome.index(before: welcome.endIndex))
// welcome now equals "hello there"

let range = welcome.index(welcome.endIndex, offsetBy: -6)..<welcome.endIndex
welcome.removeSubrange(range)
// welcome now equals "hello"
```

JavaScript
```javascript
const greeting = "Guten Tag!"
greeting.slice(0, 1)
// G
greeting.slice(-1)
// !
greeting.substr(1, 1)
// u

// Inserting and Removing
let welcome = "hello"
welcome += "!"
// welcome now equals "hello!"

welcome = welcome.substr(0, welcome.length - 1) + " there" + welcome.slice(-1)
// welcome now equals "hello there!"

welcome.substr(0, welcome.length - 1)
// welcome now equals "hello there"

let index = welcome.indexOf(' ');
welcome.slice(0, index)
// welcome now equals "hello"
```

## Collection Types
## Control Flow
## Functions
## Closures
## Enumerations
## Structures and Classes
## Properties
## Methods
## Subscripts
## Inheritance
## Initialization
## Deinitialization
## Optional Chaining
## Error Handling
## Type Casting
## Nested Types
## Extensions
## Protocols


Swift
```swift
```

JavaScript
```javascript
```