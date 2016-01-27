##Introduction to Conditionals

##SWBAT
- use boolean operators to test a statement's boolean value
- explain the need for if/else statements in code
- implement an if statement, and if/else statement, and an if/else if/ else statement in their code

##Lesson
- Up until this point our code has executed line by line, from top to bottom. Every line of code always ran, no matter what.
- It can be useful to write code that will only execute if certain conditions are true. This kind of code is called conditional, and a well written conditional statement reads a lot like a normal sentence.
```Swift
if somethingIsTrue {
  then execute this code
}
```
- The "somethingIsTrue" part of the statement is where booleans come in. Remember that booleans can have either a true or false value. If somethingIsTrue has a value of true, then the code inside that branch will execute. If it has a value of false, nothing will happen.
```Swift
var cold = true
if cold {
  print("Don't forget to wear a coat when you go outside.")
}
//prints "Don't forget to wear a coat when you go outside."
```
```Swift
var cold = false
if cold {
  print("Don't forget to wear a coat when you go outside.")
}
//nothing happens
```
- We can even write code for both possibilities in the same block
```Swift
var cold = false
if cold {
  print("Don't forget to wear a coat when you go outside.")
} else {
  print("Wear a t-shirt! It's beautiful outside.")
}
//prints "Wear a t-shirt! It's beautiful outside."
```
- Usually though, we want to make a comparison when deciding whether or not to execute a particular block of code. For that, we use comparison operators:

symbol|description|example
:------: | :------: | :-----:
==|equal to|1 == 1   //true
!=|not equal to|12 != 12   //false
>|greater than|4.5 > 3.0   //true
>=|greater than or equal to|6 >= 6   //true
<|less than|1000000000 < 10   //false
<=|less than or equal to|-34 <= 19   //true
- We can incorporate these directly into the if statement
```Swift
var temperature = 28
if temperature < 32 {
  print("Don't forget to wear a coat when you go outside.")
} else {
  print("Wear a t-shirt! It's beautiful outside.")
}
//prints "Don't forget to wear a coat when you go outside." because temperature < 32 is true
```
- Sometimes we need to account for more than two possibilities. To account for this, we can add "else if" statements.
```Swift
var temperature = 58
if temperature < 32 {
  print("Don't forget to wear a coat when you go outside.")
} else if temperature > 70 {
  print("Wear a t-shirt! It's beautiful outside.")
} else {
  print("It's a little chilly, you should probably throw on a sweater.")
}
//prints "It's a little chilly, you should probably throw on a sweater." because temperature < 32 and temperature > 70 are both false
```