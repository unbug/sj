<img src="https://user-images.githubusercontent.com/799578/41671640-51642072-74ea-11e8-8bf2-7588062eed70.png" width="300">

# Swift and JavaScript comparison snippets
Well, I think the most easy way to learn Swift and JavaScript in the same time is read the code, just the code!

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


## Resources
[The swift programming language guide](https://docs.swift.org/swift-book/LanguageGuide/TheBasics.html)