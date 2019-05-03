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
- [Classes](#classes)
- [Inheritance](#inheritance)

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
### Mutability of Collections: Arrays
Swift
```swift
// creata an empty array
var someInts = [Int]()
print("someInts is of type [Int] with \(someInts.count) items.")
// Prints "someInts is of type [Int] with 0 items."

// Creating an Array with a Default Value
var threeDoubles = Array(repeating: 0.0, count: 3)
// threeDoubles is of type [Double], and equals [0.0, 0.0, 0.0]
var anotherThreeDoubles = Array(repeating: 2.5, count: 3)
// anotherThreeDoubles is of type [Double], and equals [2.5, 2.5, 2.5]

var sixDoubles = threeDoubles + anotherThreeDoubles
// sixDoubles is inferred as [Double], and equals [0.0, 0.0, 0.0, 2.5, 2.5, 2.5]


// Creating an Array with an Array Literal
var shoppingList: [String] = ["Eggs", "Milk"]
// shoppingList has been initialized with two initial items


// Accessing and Modifying an Array
if shoppingList.isEmpty {
    print("The shopping list is empty.")
} else {
    print("The shopping list is not empty.")
}
// Prints "The shopping list is not empty."
shoppingList.append("Flour")
// shoppingList now contains 3 items, and someone is making pancakes
shoppingList += ["Baking Powder"]
// shoppingList now contains 4 items
shoppingList += ["Chocolate Spread", "Cheese", "Butter"]
// shoppingList now contains 7 items
var firstItem = shoppingList[0]

// firstItem is equal to "Eggs"
shoppingList[0] = "Six eggs"
// the first item in the list is now equal to "Six eggs" rather than "Eggs"

shoppingList[4...6] = ["Bananas", "Apples"]
// shoppingList now contains 6 items

shoppingList.insert("Maple Syrup", at: 0)
// shoppingList now contains 7 items
// "Maple Syrup" is now the first item in the list

let mapleSyrup = shoppingList.remove(at: 0)
// the item that was at index 0 has just been removed
// shoppingList now contains 6 items, and no Maple Syrup
// the mapleSyrup constant is now equal to the removed "Maple Syrup" string

let apples = shoppingList.removeLast()
// the last item in the array has just been removed
// shoppingList now contains 5 items, and no apples
// the apples constant is now equal to the removed "Apples" string


// Iterating Over an Array
for item in shoppingList {
    print(item)
}
// Six eggs
// Milk
// Flour
// Baking Powder
// Bananas

for (index, value) in shoppingList.enumerated() {
    print("Item \(index + 1): \(value)")
}
// Item 1: Six eggs
// Item 2: Milk
// Item 3: Flour
// Item 4: Baking Powder
// Item 5: Bananas
```

JavaScript
```javascript
// creata an empty array
let someInts = new Array()
console.log(`someInts is an array with ${someInts.length} items.`)
// Prints "someInts is an array with 0 items."

// Creating an Array with a Default Value
let threeDoubles = [0.0, 0.0, 0.0]
// threeDoubles is of type [Double], and equals [0.0, 0.0, 0.0]
let anotherThreeDoubles = [2.5, 2.5, 2.5]
// anotherThreeDoubles is of type [Double], and equals [2.5, 2.5, 2.5]

let sixDoubles = [...threeDoubles, ...anotherThreeDoubles]
// sixDoubles is inferred as [Double], and equals [0.0, 0.0, 0.0, 2.5, 2.5, 2.5]


// Creating an Array with an Array Literal
let shoppingList = ["Eggs", "Milk"]
// shoppingList has been initialized with two initial items


// Accessing and Modifying an Array
if (shoppingList.length === 0) {
    console.log("The shopping list is empty.")
} else {
    console.log("The shopping list is not empty.")
}
// Prints "The shopping list is not empty."
shoppingList.push("Flour")
// shoppingList now contains 3 items, and someone is making pancakes
shoppingList = shoppingList.concat(["Baking Powder"])
// shoppingList now contains 4 items
shoppingList = [...shoppingList, "Chocolate Spread", "Cheese", "Butter"]
// shoppingList now contains 7 items
let firstItem = shoppingList[0]
// firstItem is equal to "Eggs"
shoppingList[0] = "Six eggs"
// the first item in the list is now equal to "Six eggs" rather than "Eggs"

shoppingList.splice(4, 3, "Bananas", "Apples")
// shoppingList now contains 6 items

shoppingList.unshift("Maple Syrup")
// shoppingList now contains 7 items
// "Maple Syrup" is now the first item in the list

let mapleSyrup = shoppingList.shift()
// the item that was at index 0 has just been removed
// shoppingList now contains 6 items, and no Maple Syrup
// the mapleSyrup constant is now equal to the removed "Maple Syrup" string

let apples = shoppingList.pop()
// the last item in the array has just been removed
// shoppingList now contains 5 items, and no apples
// the apples constant is now equal to the removed "Apples" string


// Iterating Over an Array
shoppingList.forEach((item => {
    console.log(item)
})
// Six eggs
// Milk
// Flour
// Baking Powder
// Bananas

shoppingList.forEach(((item, index) => {
    console.log(`Item ${index + 1}: ${value}`)
})
// Item 1: Six eggs
// Item 2: Milk
// Item 3: Flour
// Item 4: Baking Powder
// Item 5: Bananas
```
### Sets
Swift
```swift
// Creating and Initializing an Empty Set
var letters = Set<Character>()
print("letters is of type Set<Character> with \(letters.count) items.")
// Prints "letters is of type Set<Character> with 0 items."
var favoriteGenres: Set<String> = ["Rock", "Classical", "Hip hop"]
// favoriteGenres has been initialized with three initial items


// Accessing and Modifying a Set
print("I have \(favoriteGenres.count) favorite music genres.")
// Prints "I have 3 favorite music genres."

if favoriteGenres.isEmpty {
    print("As far as music goes, I'm not picky.")
} else {
    print("I have particular music preferences.")
}
// Prints "I have particular music preferences."

favoriteGenres.insert("Jazz")
// favoriteGenres now contains 4 items

if let removedGenre = favoriteGenres.remove("Rock") {
    print("\(removedGenre)? I'm over it.")
} else {
    print("I never much cared for that.")
}
// Prints "Rock? I'm over it."

if favoriteGenres.contains("Funk") {
    print("I get up on the good foot.")
} else {
    print("It's too funky in here.")
}
// Prints "It's too funky in here."


// Iterating Over a Set
for genre in favoriteGenres {
    print("\(genre)")
}
// Classical
// Jazz
// Hip hop
```

JavaScript
```javascript
// Creating and Initializing an Empty Set
let letters = new Set()
console.log(`letters is of type Set with ${letters.size} items.`)
// Prints "letters is of type Set with 0 items."
let favoriteGenres = new set(["Rock", "Classical", "Hip hop"])
// favoriteGenres has been initialized with three initial items


// Accessing and Modifying a Set
console.log(`I have ${favoriteGenres.size} favorite music genres.`)
// Prints "I have 3 favorite music genres."

if (favoriteGenres.size == 0) {
    console.log("As far as music goes, I'm not picky.")
} else {
    console.log("I have particular music preferences.")
}
// Prints "I have particular music preferences."

favoriteGenres.add("Jazz")
// favoriteGenres now contains 4 items
const removedGenre = favoriteGenres.delete("Rock")
if (removedGenre) {
    console.log(`${removedGenre}? I'm over it.`)
} else {
    console.log("I never much cared for that.")
}
// Prints "Rock? I'm over it."

if (favoriteGenres.has("Funk")) {
    console.log("I get up on the good foot.")
} else {
    console.log("It's too funky in here.")
}
// Prints "It's too funky in here."


// Iterating Over a Set
favoriteGenres.forEach(genre => {
    console.log(genre);
})
// Classical
// Jazz
// Hip hop
```

### Dictionaries
Swift
```swift
// Creating an Empty Dictionary
var namesOfIntegers = [Int: String]()
// namesOfIntegers is an empty [Int: String] dictionary
namesOfIntegers[16] = "sixteen"
// namesOfIntegers now contains 1 key-value pair
namesOfIntegers = [:]
// namesOfIntegers is once again an empty dictionary of type [Int: String]


// Creating a Dictionary with a Dictionary Literal
var airports: [String: String] = ["YYZ": "Toronto Pearson", "DUB": "Dublin"]


// Accessing and Modifying a Dictionary
print("The airports dictionary contains \(airports.count) items.")
// Prints "The airports dictionary contains 2 items."

if airports.isEmpty {
    print("The airports dictionary is empty.")
} else {
    print("The airports dictionary is not empty.")
}
// Prints "The airports dictionary is not empty."

airports["LHR"] = "London"
// the airports dictionary now contains 3 items

airports["LHR"] = "London Heathrow"
// the value for "LHR" has been changed to "London Heathrow"

if let oldValue = airports.updateValue("Dublin Airport", forKey: "DUB") {
    print("The old value for DUB was \(oldValue).")
}
// Prints "The old value for DUB was Dublin."

if let airportName = airports["DUB"] {
    print("The name of the airport is \(airportName).")
} else {
    print("That airport is not in the airports dictionary.")
}
// Prints "The name of the airport is Dublin Airport."

airports["APL"] = "Apple International"
// "Apple International" is not the real airport for APL, so delete it
airports["APL"] = nil
// APL has now been removed from the dictionary

if let removedValue = airports.removeValue(forKey: "DUB") {
    print("The removed airport's name is \(removedValue).")
} else {
    print("The airports dictionary does not contain a value for DUB.")
}
// Prints "The removed airport's name is Dublin Airport."


// Iterating Over a Dictionary
for (airportCode, airportName) in airports {
    print("\(airportCode): \(airportName)")
}
// YYZ: Toronto Pearson
// LHR: London Heathrow

for airportCode in airports.keys {
    print("Airport code: \(airportCode)")
}
// Airport code: YYZ
// Airport code: LHR

for airportName in airports.values {
    print("Airport name: \(airportName)")
}
// Airport name: Toronto Pearson
// Airport name: London Heathrow

let airportCodes = [String](airports.keys)
// airportCodes is ["YYZ", "LHR"]

let airportNames = [String](airports.values)
// airportNames is ["Toronto Pearson", "London Heathrow"]
```

JavaScript
```javascript
// Creating an Empty Dictionary
let namesOfIntegers = {}
// namesOfIntegers is an empty dictionary
namesOfIntegers[16] = "sixteen"
// namesOfIntegers now contains 1 key-value pair
namesOfIntegers = {}
// namesOfIntegers is once again an empty dictionary of type


// Creating a Dictionary with a Dictionary Literal
let airports = {"YYZ": "Toronto Pearson", "DUB": "Dublin"}


// Accessing and Modifying a Dictionary
console.log(`The airports dictionary contains ${Object.keys(airports).length} items.`)
// Prints "The airports dictionary contains 2 items."

if (Object.keys(airports).length == 0) {
    console.log("The airports dictionary is empty.")
} else {
    console.log("The airports dictionary is not empty.")
}
// Prints "The airports dictionary is not empty."

airports["LHR"] = "London"
// the airports dictionary now contains 3 items

airports["LHR"] = "London Heathrow"
// the value for "LHR" has been changed to "London Heathrow"

const oldValue = airports["DUB"]
airports["DUB"] = "Dublin Airport"
if (oldValue)  {
    console.log(`The old value for DUB was ${oldValue}.`)
}
// Prints "The old value for DUB was Dublin."
const airportName = airports["DUB"]
if (airportName) {
    console.log(`The name of the airport is ${airportName}.`)
} else {
    console.log("That airport is not in the airports dictionary.")
}
// Prints "The name of the airport is Dublin Airport."

airports["APL"] = "Apple International"
// "Apple International" is not the real airport for APL, so delete it
airports["APL"] = null
delete airports["APL"]
// APL has now been removed from the dictionary


// Iterating Over a Dictionary
Object.keys(airports).forEach(airportCode => {
    const airportName = airports[airportCode]
    console.log(`${airportCode}: ${airportName}`)
})
// YYZ: Toronto Pearson
// LHR: London Heathrow

let airportCodes = Object.keys(airports)
// airportCodes is ["YYZ", "LHR"]
```

## Control Flow
### For-In Loops
Swift
```swift
let names = ["Anna", "Alex", "Brian", "Jack"]
for name in names {
    print("Hello, \(name)!")
}
// Hello, Anna!
// Hello, Alex!
// Hello, Brian!
// Hello, Jack!

let numberOfLegs = ["spider": 8, "ant": 6, "cat": 4]
for (animalName, legCount) in numberOfLegs {
    print("\(animalName)s have \(legCount) legs")
}
// ants have 6 legs
// cats have 4 legs
// spiders have 8 legs
```

JavaScript
```javascript
const names = ["Anna", "Alex", "Brian", "Jack"]
for (let i = 0; i < names.length; i++) {
    console.log(`Hello, ${names[i]}!`)
}
// Hello, Anna!
// Hello, Alex!
// Hello, Brian!
// Hello, Jack!

const numberOfLegs = {"spider": 8, "ant": 6, "cat": 4}
Object.keys(numberOfLegs).forEach(animalName => {
    const legCount = numberOfLegs[animalName];
    console.log(`${animalName}s have ${legCount} legs`)
})
// ants have 6 legs
// cats have 4 legs
// spiders have 8 legs
```

### While Loops
Swift
```swift
let finalSquare = 25
var board = [Int](repeating: 0, count: finalSquare + 1)
board[03] = +08; board[06] = +11; board[09] = +09; board[10] = +02
board[14] = -10; board[19] = -11; board[22] = -02; board[24] = -08
var square = 0
var diceRoll = 0
while square < finalSquare {
    // roll the dice
    diceRoll += 1
    if diceRoll == 7 { diceRoll = 1 }
    // move by the rolled amount
    square += diceRoll
    if square < board.count {
        // if we're still on the board, move up or down for a snake or a ladder
        square += board[square]
    }
}
print("Game over!")
```

JavaScript
```javascript
let finalSquare = 25
let board = []
for (let i = 0; i <= finalSquare; i++) {
    board[i] = 0;
}
board[03] = +08; board[06] = +11; board[09] = +09; board[10] = +02
board[14] = -10; board[19] = -11; board[22] = -02; board[24] = -08
let square = 0
let diceRoll = 0
while (square < finalSquare) {
    // roll the dice
    diceRoll += 1
    if (diceRoll == 7) { diceRoll = 1 }
    // move by the rolled amount
    square += diceRoll
    if (square < board.length) {
        // if we're still on the board, move up or down for a snake or a ladder
        square += board[square]
    }
}
console.log("Game over!")
```
### Conditional Statements
 Swift
```swift
var temperatureInFahrenheit = 30
temperatureInFahrenheit = 90
if temperatureInFahrenheit <= 32 {
    print("It's very cold. Consider wearing a scarf.")
} else if temperatureInFahrenheit >= 86 {
    print("It's really warm. Don't forget to wear sunscreen.")
} else {
    print("It's not that cold. Wear a t-shirt.")
}
// Prints "It's really warm. Don't forget to wear sunscreen."
```

JavaScript
```javascript
let temperatureInFahrenheit = 30
temperatureInFahrenheit = 90
if (temperatureInFahrenheit <= 32) {
    console.log("It's very cold. Consider wearing a scarf.")
} else if (temperatureInFahrenheit >= 86) {
    console.log("It's really warm. Don't forget to wear sunscreen.")
} else {
    console.log("It's not that cold. Wear a t-shirt.")
}
// Prints "It's really warm. Don't forget to wear sunscreen."
```

### Switch
Swift
```swift
let someCharacter: Character = "z"
switch someCharacter {
case "a":
    print("The first letter of the alphabet")
case "z":
    print("The last letter of the alphabet")
default:
    print("Some other character")
}
// Prints "The last letter of the alphabet"
```

JavaScript
```javascript
const someCharacter = "z"
switch (someCharacter) {
case "a":
    console.log("The first letter of the alphabet")
    break;
case "z":
    console.log("The last letter of the alphabet")
    break;
default:
    console.log("Some other character")
}
// Prints "The last letter of the alphabet"
```

## Functions
Swift
```swift
// Defining and Calling Functions
func greet(person: String) -> String {
    let greeting = "Hello, " + person + "!"
    return greeting
}
print(greet(person: "Anna"))
// Prints "Hello, Anna!"
print(greet(person: "Brian"))
// Prints "Hello, Brian!"

func greetAgain(person: String) -> String {
    return "Hello again, " + person + "!"
}
print(greetAgain(person: "Anna"))
// Prints "Hello again, Anna!"


// Function Parameters and Return Values
// Functions Without Parameters
func sayHelloWorld() -> String {
    return "hello, world"
}
print(sayHelloWorld())
// Prints "hello, world"

// Functions With Multiple Parameters
func greet(person: String, alreadyGreeted: Bool) -> String {
    if alreadyGreeted {
        return greetAgain(person: person)
    } else {
        return greet(person: person)
    }
}
print(greet(person: "Tim", alreadyGreeted: true))
// Prints "Hello again, Tim!"


// Functions Without Return Values
func greet(person: String) {
    print("Hello, \(person)!")
}
greet(person: "Dave")
// Prints "Hello, Dave!"

// Functions with Multiple Return Values
func minMax(array: [Int]) -> (min: Int, max: Int) {
    var currentMin = array[0]
    var currentMax = array[0]
    for value in array[1..<array.count] {
        if value < currentMin {
            currentMin = value
        } else if value > currentMax {
            currentMax = value
        }
    }
    return (currentMin, currentMax)
}
let bounds = minMax(array: [8, -6, 2, 109, 3, 71])
print("min is \(bounds.min) and max is \(bounds.max)")
// Prints "min is -6 and max is 109"

// Nested Functions
func chooseStepFunction(backward: Bool) -> (Int) -> Int {
    func stepForward(input: Int) -> Int { return input + 1 }
    func stepBackward(input: Int) -> Int { return input - 1 }
    return backward ? stepBackward : stepForward
}
var currentValue = -4
let moveNearerToZero = chooseStepFunction(backward: currentValue > 0)
// moveNearerToZero now refers to the nested stepForward() function
while currentValue != 0 {
    print("\(currentValue)... ")
    currentValue = moveNearerToZero(currentValue)
}
print("zero!")
// -4...
// -3...
// -2...
// -1...
// zero!
```

JavaScript
```javascript
// Defining and Calling Functions
function greet(person) {
    const greeting = "Hello, " + person + "!"
    return greeting
}
console.log(greet("Anna"))
// Prints "Hello, Anna!"
console.log(greet("Brian"))
// Prints "Hello, Brian!"

function greetAgain(person) {
    return "Hello again, " + person + "!"
}
print(greetAgain("Anna"))
// Prints "Hello again, Anna!"


// Function Parameters and Return Values
// Functions Without Parameters
function sayHelloWorld() {
    return "hello, world"
}
console.log(sayHelloWorld())
// Prints "hello, world"

// Functions With Multiple Parameters
function greet(person, alreadyGreeted) {
    if (alreadyGreeted) {
        return greetAgain(person)
    } else {
        return greet(person)
    }
}
console.log(greet("Tim", true))
// Prints "Hello again, Tim!"


// Functions Without Return Values
function greet(person) {
    console.log(`Hello, ${person}!`)
}
greet("Dave")
// Prints "Hello, Dave!"

// Functions with Multiple Return Values
function minMax(array) {
    let currentMin = array[0]
    let currentMax = array[0]
    array.forEach(value => {
        if (value < currentMin) {
            currentMin = value
        } else if (value > currentMax) {
            currentMax = value
        }
    })
    return {currentMin, currentMax}
}
const bounds = minMax([8, -6, 2, 109, 3, 71])
console.log(`min is ${bounds.min} and max is ${bounds.max}`)
// Prints "min is -6 and max is 109"

// Nested Functions
function chooseStepFunction(backward) {
    function stepForward(input) { return input + 1 }
    function stepBackward(input) { return input - 1 }
    return backward ? stepBackward : stepForward
}
let currentValue = -4
const moveNearerToZero = chooseStepFunction(currentValue > 0)
// moveNearerToZero now refers to the nested stepForward() function
while (currentValue != 0) {
    console.log(`${currentValue}... `)
    currentValue = moveNearerToZero(currentValue)
}
console.log("zero!")
// -4...
// -3...
// -2...
// -1...
// zero!
```
## Closures
Swift
```swift
// Closure Expressions
// The Sorted Method
let names = ["Chris", "Alex", "Ewa", "Barry", "Daniella"]
func backward(_ s1: String, _ s2: String) -> Bool {
    return s1 > s2
}
var reversedNames = names.sorted(by: backward)
// reversedNames is equal to ["Ewa", "Daniella", "Chris", "Barry", "Alex"]
reversedNames = names.sorted(by: { (s1: String, s2: String) -> Bool in
    return s1 > s2
})
// or
reversedNames = names.sorted(by: { (s1: String, s2: String) -> Bool in return s1 > s2 } )
```

JavaScript
```javascript
// Closure Expressions
// The Sort Method
const names = ["Chris", "Alex", "Ewa", "Barry", "Daniella"]
function backward(s1, s2) {
    return s1 < s2
}
let reversedNames = names.sort(backward)
// reversedNames is equal to ["Ewa", "Daniella", "Chris", "Barry", "Alex"]
reversedNames = names.sort((s1, s2) => {
    return s1 < s2
})
// or
reversedNames = names.sort((s1, s2) => return s1 < s2)
```
## Classes
Swift
```swift
// class definition
class Counter {
    var count = 0
    func increment() {
        count += 1
    }
    func increment(by amount: Int) {
        count += amount
    }
    func reset() {
        count = 0
    }
}

// class instance
let counter = Counter()
// the initial count value is 0
counter.increment()
// the count's value is now 1
counter.increment(by: 5)
// the count's value is now 6
counter.reset()
// the count's value is now 0

print("The count property value is \(counter.count)")

```

JavaScript
```javascript
// class definition
class Counter {
    contructor() {
        this.count = 0
    }
    function increment() {
        this.count += 1
    }
    function increment(amount) {
        this.count += amount
    }
    function reset() {
        this.count = 0
    }
}

// class instance
let counter = Counter()
// the initial count value is 0
counter.increment()
// the count's value is now 1
counter.increment(5)
// the count's value is now 6
counter.reset()
// the count's value is now 0

console.log(`The count property value is ${counter.count}`)
```

## Inheritance
Swift
```swift
// Defining a Base Class
class Vehicle {
    var currentSpeed = 0.0
    var description: String {
        return "traveling at \(currentSpeed) miles per hour"
    }
    func makeNoise() {
        // do nothing - an arbitrary vehicle doesn't necessarily make a noise
    }
}
let someVehicle = Vehicle()
print("Vehicle: \(someVehicle.description)")
// Vehicle: traveling at 0.0 miles per hour


// Subclassing
class SomeSubclass: SomeSuperclass {
    // subclass definition goes here
}
class Bicycle: Vehicle {
    var hasBasket = false
}
let bicycle = Bicycle()
bicycle.hasBasket = true

bicycle.currentSpeed = 15.0
print("Bicycle: \(bicycle.description)")
// Bicycle: traveling at 15.0 miles per hour


// Subclasses can themselves be subclassed
class Tandem: Bicycle {
    var currentNumberOfPassengers = 0
}
let tandem = Tandem()
tandem.hasBasket = true
tandem.currentNumberOfPassengers = 2
tandem.currentSpeed = 22.0
print("Tandem: \(tandem.description)")
// Tandem: traveling at 22.0 miles per hour


// Overriding
class Train: Vehicle {
    override func makeNoise() {
        print("Choo Choo")
    }
}
let train = Train()
train.makeNoise()
// Prints "Choo Choo"


// Overriding Property Getters and Setters
class Car: Vehicle {
    var gear = 1
    override var description: String {
        return super.description + " in gear \(gear)"
    }
}
let car = Car()
car.currentSpeed = 25.0
car.gear = 3
print("Car: \(car.description)")
// Car: traveling at 25.0 miles per hour in gear 3
```

JavaScript
```javascript
// Defining a Base Class
class Vehicle {
    constructor() {
        this.currentSpeed = 0.0
    }
    get description() {
        return `traveling at ${currentSpeed} miles per hour`
    }
    function makeNoise() {
        // do nothing - an arbitrary vehicle doesn't necessarily make a noise
    }
}
let someVehicle = Vehicle()
console.log(`Vehicle: ${someVehicle.description}`)
// Vehicle: traveling at 0.0 miles per hour


// Subclassing
class SomeSubclass extends SomeSuperclass {
    contructor() {
        super();
    }
    // subclass definition goes here
}
class Bicycle extends Vehicle {
    contructor() {
        super();
        this.hasBasket = false
    }
}
let bicycle = Bicycle()
bicycle.hasBasket = true

bicycle.currentSpeed = 15.0
console.log(`Bicycle: ${bicycle.description}`)
// Bicycle: traveling at 15.0 miles per hour


// Subclasses can themselves be subclassed
class Tandem extends Bicycle {
    contructor() {
        super();
        this.currentNumberOfPassengers = 0
    }
}
let tandem = Tandem()
tandem.hasBasket = true
tandem.currentNumberOfPassengers = 2
tandem.currentSpeed = 22.0
console.log("Tandem: \(tandem.description)")
// Tandem: traveling at 22.0 miles per hour


// Overriding
class Train extends Vehicle {
    contructor() {
        super();
        this.currentNumberOfPassengers = 0
    }
    function makeNoise() {
        console.log("Choo Choo")
    }
}
let train = Train()
train.makeNoise()
// Prints "Choo Choo"


// Overriding Property Getters and Setters
class Car extends Vehicle {
    contructor() {
        super();
        this.gear = 1
    }
    get description() {
        return `${super.description} in gear ${gear}`
    }
}
let car = Car()
car.currentSpeed = 25.0
car.gear = 3
console.log(`Car: ${car.description}`)
// Car: traveling at 25.0 miles per hour in gear 3
```
