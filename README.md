# Optionals lab

Fork and clone this repo. On your fork, answer and commit the follow questions. When you are finished, submit the link to your repo on Canvas.


## Question 1

a. Given the variable `userNameOne` below, print *"The username is Test User"*.  Use *Optional Binding* (`if let`) to print the name.

```swift

var userNameOne: String? = "Test User"

if let userName = userNameOne {
    print("The username is \(userName)")
}

```

b. Given the variable `userNameTwo` below, print *"The username is undefined"*.  Use the *nil coalescing operator* (`??`).

```swift

var userNameTwo: String? = nil

let undefinedUser = userNameTwo ?? "The username is undefined."

print(undefinedUser)



```

## Question 2

a. Given the variables `rectOneWidth` and `rectOneHeight` below, print "The area of rectOne is 50".  Use *Optional Binding* (`if let`) to print the area.

```swift

var rectOneWidth: Double? = 5
var rectOneHeight: Double? = 10

if let oneWidth = rectOneWidth, let oneHeight = rectOneHeight {
    let rectOneArea = oneWidth * oneHeight
    print("The area of rectOne is \(rectOneArea)")
} else {
    print("The area of rectOne is not able to be calculated.")
}

```

b. Given the variables `rectTwoWidth` and `rectTwoHeight` below, print "The are of rectTwo is not able to be calculated".  Use *Optional Binding* (`if let`) to print this message.

```swift

var rectTwoWidth: Double? = nil
var rectTwoHeight: Double? = nil

if let twoWidth = rectTwoWidth, let twoHeight = rectTwoHeight {
    let rectTwoArea = twoWidth * twoHeight
    print("The area of rectTwo is \(rectTwoArea)")
} else {
    print("The area of rectTwo is not able to be calculated.")
}

```

## Question 3

a. Given the variables `userOneName`, `userOneAge`, and `userOneHeight` below, write code that prints "Hello Anne!  You are 15 years old and 5.8 feet tall" (1 foot = 12 inches).  Use optional binding.


```swift

var userOneName: String? = "Anne"
var userOneAge: Int? = 15
var userOneHeight: Double? = 70

if let nameOne = userOneName, let ageOne = userOneAge, let heightOne = userOneHeight {
    let height = (heightOne / 12)
    print("Hello \(nameOne)! You are \(ageOne) years old and \(String(format:"%.2f", height)) feet tall.")
}


```

b. Given the variables `userTwoName`, `userTwoAge` and `userTwoHeight` below, write code that prints "Hello user!  You are 15 years old and I don't know how tall you are".  Use optional binding

```swift

Attempt: (Please assist me with this) - this is a formewr request but i would still like to go over this to discuss other solutions

var userTwoName: String? = nil
var userTwoAge: Int? = 15
var userTwoHeight: Double? = nil

if let nameTwo = userTwoName, let ageTwo = userTwoAge, let heightTwo = userTwoHeight {
    print("Hello \(nameTwo)! you are \(ageTwo) years old and \(heightTwo)")
} else {
    
    let nameTwo = "user"
    let heightTwo = "I dont know how tall you are."
    let ageTwo = userTwoAge ?? 15
    print("Hello \(nameTwo)! you are \(ageTwo) years old and \(heightTwo)")
}

```


## Question 4

Given  the variable `favoriteNumber`, write code that either prints "Your favorite number is " followed by the number, or "I don't know what your favorite number is"

`favoriteNumber` is of type Int? and will either be `nil` or a random number between 0 and 10.  It will change each time you run your Playground.

```swift

var favoriteNumber = Bool.random() ? Int.random(in: 0...10) : nil

if favoriteNumber != nil {
    print("the num is \(String(describing: favoriteNumber))")
} else {
    print("is nil")
}

```



## Question 5

Given the variables `numOne`, `numTwo` and `numThree`, write code that prints "The sum of all the numbers is " followed by their sum.  If a number is `nil`, don't add it to the sum.  If all numbers are `nil`, the sum is zero.

```swift
var numOne = Bool.random() ? Int.random(in: 0...10) : nil
var numTwo = Bool.random() ? Int.random(in: 0...10) : nil
var numThree = Bool.random() ? Int.random(in: 0...10) : nil
```

## Question 6

a. Given the variable `numbers` below, write code that prints "The sum of all the numbers is " followed by their sum.  If a number is `nil`, don't add it to the sum.  If all numbers are `nil`, the sum is zero.

```swift
var numbers = [Int?]()

for _ in 0..<10 {
    numbers.append(Bool.random() ? Int.random(in: 0...100) : nil)
}
```

// this code is alex's answer when we worked on it in class together.

b. Using the same variable, find the average of all non-nil values.

var messages: [String] = ["Good, Morning"]
for _ in 0..<10 {
  messages.append("Hello, Yulia") // append() - adds to array
}
print(messages.count)


// a - add only non-nil values
var numbers = [Int?]()
for _ in 0..<10 {
    numbers.append(Bool.random() ? Int.random(in: 0...100) : nil)
}

var sum = 0
for num in numbers {
  sum += num ?? 0 // nil-coalescing to unwrap num
}
print("The sum of all the numbers is \(sum)")


// b - average of non-nil values
sum = 0 // clearing sum
var nonNilValueCount = 0
for num in numbers {
  // use optional binding to unwrap num
  if let unwrappedNum = num {
    // valid integer here, increment nonNilValueCount by 1
    nonNilValueCount += 1
    sum += unwrappedNum
  }
}
print(numbers)
print("The average of the \(nonNilValueCount) non-nil values is \(sum / nonNilValueCount)")

## Extra Questions

https://github.com/joinpursuit/Pursuit-Core-iOS-Extra-Optionals-Questions/blob/master/README.md
