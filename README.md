# Strings Lab 1

## Instructions for lab submission

1. Fork the assignment repo
1. Clone your Fork to your machine
1. Complete the lab
1. Push your changes to your Fork
1. Submit a Pull Request back to the assignment repo
1. Paste a link to of your Fork on Canvas and submit

## Question 1

Write code that prints out all the numbers from 1 to 10 as a single string.
(Hint: the `String()` function can convert an Int to a String)
```swift
var single = ""
for a in 1...10 {
single = single + " \(a)"  
}
print(single)
```
***
## Question 2

Write code that prints out all the even numbers from 5 to 51 as a single string.
```swift
var single = ""
for a in 5...51 where a % 2 == 0 {
single = single + " \(a)"
}
print(single)
```

***
## Question 3

Write code that prints out every number ending in 4 between 1 and 60 as a single string.
```swift
var single = ""
for a in 1...60 where a % 5 == 0 && a % 10 != 0 {
single = single + " \(a - 1)"
}
print(single)
```
***
## Question 4

Print each character in the string `"Hello world!"`
```swift
var stringQ4 = "Hello world!"
for a in stringQ4 {
print(a)
}
```
***
## Question 5

Print out the last character in the string below.  You cannot use the Character literal "!" (i.e you must access `myStringSeven`'s characters).
```swift
`let myStringSeven = "Hello world!"`
let myStringSeven = "Hello world!"
print(myStringSeven.last)
```
***
## Question 6

Write code that switches on a string, given the following conditions:
- If the string's length is even, print out every character.
- If the string's length is odd, print out every other character.
``` swift
var stringQ6 = "anythings"
stringQ6.enumerated()
for (a, b) in stringQ6.enumerated() {
if stringQ6.count % 2 == 0 {
print(b)
} else if a % 2 == 0 {
print(b)
}
}
```
***
## Question 7

Initialize a String with a character. Show that it is a Character, and not another String, that you're using to initialize it.
```swift
var q7 = Character("a")
var qq7 = String("a")
print(qq7 == q7)
```

***
## Question 8

Build five pairs of **canonically equivalent** strings, the first of each being a pre-composed character and the second being one that uses combinable unicode scalars. Show that they are equivalent.
```swift
let p = "\u{00A2}"
let q = "¢"
print(p == q)

let a = "\u{00A3}"
let b = "£"
print(a == b)

let c = "\u{00A9}"
let cr = "©"
print(c == cr)

let s = "\u{00A7}"
let t = "§"
print(s == t)

let i = "\u{30D11}"
let j = "𰴑"
print(i == j)
```

***
## Question 9

**Using only Unicode**, print out `"HELLO WORLD!"`
```swift
print("\u{0048}\u{0045}\u{004C}\u{004C}\u{004F}\u{0020}\u{0057}\u{004F}\u{0052}\u{004C}\u{0044}")
```
***
## Question 10

**Using only Unicode**, print out your name.
```swift
print("\u{0041}\u{004E}\u{0047}\u{0045}\u{004C}\u{0041}")
```
***
## Question 11

**Using only Unicode**, print out `"HELLO WORLD!"` in another language.
```swift
print("\u{3053}\u{3093}\u{306B}\u{3061}\u{306F}\u{4E16}\u{754C}")
```
***
## Question 12

Print the below flower box using the following information.

- The unicode number for ⚘ is U-2698
- The top and bottom of the box are represented by dashes and the rows are |
- Use the terminator argument in your print statements to print on the same line.
- Hint: It may be useful to try printing out a box of just one character to start then work your way from there.

```swift
Flower Box:
- - - - - - - - - - -
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
- - - - - - - - - - -
let dashes = "- - - - - - - - - - - "
let flower = "| \u{2698} | \u{2698} | \u{2698} | \u{2698} | \u{2698} |"

for a in 0...8 {
if a == 0 || a == 8 {
print(dashes)
} else {
print(flower)
}
}
```

***
## Question 13

Write a program that sets up a chess board using Unicode.

```swift
Chess Board:
♖ ♘ ♗ ♕ ♔ ♗ ♘ ♖
♙ ♙ ♙ ♙ ♙ ♙ ♙ ♙




♟ ♟ ♟ ♟ ♟ ♟ ♟ ♟
♜ ♞ ♝ ♛ ♚ ♝ ♞ ♜

var whiteRow1 = "\u{2656} \u{2658} \u{2657} \u{2655} \u{2654} \u{2657} \u{2658} \u{2656}"
var whiteRow2 = "\u{2659} \u{2659} \u{2659} \u{2659} \u{2659} \u{2659} \u{2659} \u{2659}"
var blackRow1 = "\u{265F} \u{265F} \u{265F} \u{265F} \u{265F} \u{265F} \u{265F} \u{265F}"
var blackRow2 = "\u{265C} \u{265E} \u{265D} \u{265B} \u{265A} \u{265D} \u{265E} \u{265C}"
for a in 1...8 {
if a == 1 {
print(whiteRow1)
} else if a == 2 {
print(whiteRow2)
} else if a == 7 {
print(blackRow1)
} else if a == 8 {
print(blackRow2)
} else {
print("")
}
}
```

***
## Question 14

You are given a string stored in the variable `aString`. Create new string named `replacedString` that contains the characters of the original string with all the occurrences of the character `"e"` replaced by `"\*"`.

```swift
var aString = "Replace the letter e with \*"

print(aString.replacingOccurrences(of: "e", with: "*"))

 ```

Example:

Input:
`var aString = "Replace the letter e with *"`

Expected values:
`replacedString = "R*plac* th* l*tt*r * with *"`

***
## Question 15

You are given a string stored in variable `aString`. Create a new string called `reverse` that contains the original string in reverse order. Print the reversed string.

```swift
var aString = "this string has 29 characters"
var reverse = ""

var aString = "this string has 29 characters"
var reverse = ""
for a in aString {
reverse = "\(a)" + reverse
}
print(reverse)
```

Example:
Input:
`var aString = "Hello"`

Output:
`"olleH"`

***
## Question 16

You are given a string stored in variable `aString`. Print `true` if `aString` is a palindrome, and `false` otherwise. A **palindrome** is a string which reads the same backward or forward.

```swift
let aString = "anutforajaroftuna"

let aString = "anutforajaroftuna"
var reverse = ""
for a in aString {
reverse = "\(a)" + reverse
}
if aString == reverse {
print("true")
} else {
print("false")
}

```

Example 1:
Input:
`var aString = "anutforajaroftuna"`

Output:
`true`

Example 2:
Input:
`var aString = "Hello"`

Output:
`false`

***
## Question 17

You are given a string stored in variable `problem`. Write code so that you print each word of the string on a new line.

```swift
var problem = "split this string into words and print them on separate lines"

for a in problem.components(separatedBy: " ") {
print("\(a)")
}
```

Example:
Input:
`var problem ="split this string into words and print them on separate lines"`

Output:
```swift
split
this
string
into
words
and
print
them
on
separate
lines
```

***
## Question 18

You are given a string stored in variable `problem`. Write code that prints the longest word in the string.

```swift
var problem = "find the longest word in the problem description"

var wordsArray = problem.components(separatedBy: " ")
var longestWord = wordsArray.max(by: {$1.count > $0.count})
print(longestWord!)

```

Example:
Input:
`var problem = "find the longest word in the problem description"`

Output:
`description`

Hint: Keep track of the longest word you encounter and also keep track of its length.

***
## Question 19

Given a string in English, create a tuple containing the number of vowels and consonants.

```swift
let vowels = "aeiou"
let consonants = "bcdfghjklmnpqrstvwxyz"
let input = "Count how many vowels I have!"

var vowelCount = 0
var consonantCount = 0
for a in input {
for b in vowels {
if b == a {
vowelCount += 1
}
}
for c in consonants {
if c == a {
consonantCount += 1
}
}
}
var tuple = (vowels: vowelCount, consonants: consonantCount)

```

***
## Question 20

Given a string of words separated by a `" "`. Write code that prints out the length of the last word.

If there is no last word print out `"No last word"`.
```swift
var sample = "a sample of words"
print(sample.components(separatedBy: " ").last!.count)
```
Example:
Input: `"How are you doing this Monday?"`

Output: `7`

***
