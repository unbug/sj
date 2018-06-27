<img src="https://user-images.githubusercontent.com/799578/41671640-51642072-74ea-11e8-8bf2-7588062eed70.png" width="300">

# Swift and JavaScript comparison snippets
The table of content is from [The swift programming language guide](https://docs.swift.org/swift-book/LanguageGuide/TheBasics.html).

**Issue and pull request are welcome, please!**

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