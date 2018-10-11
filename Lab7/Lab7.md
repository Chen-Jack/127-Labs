# Functions

## Why?
There are many reasons to use functions, but there is a main reason for using functions; Reusability and Modularity. Functions let us write code in a manner so that we can easily reuse it. They also allow us to break down large blocks of codes into many smaller blockers.

## What does a function look like?
They have a name and parenthesis. Here are some examples that you may have seen before.
```python
print()
input()
range()
int()
float()
str()
upper()
lower()
len()
forward()
left()
right()
color()
 # Alot more 
```

# What does a function do?
Functions let you define a set of predefined instructions. By executing a function, you will execute all the predefined instructions aswell.

## Defining a basic function
To define a function, the following syntax is used.
```python
#The function is called foo
def foo():
  # Command 1
  # Command 2
  ...
  # Command 3

```

## Executing a function (aka Calling a function)
To execute a function, use the following syntax.
```python
# Defined a function called foo that will print "Hello" when executed. However, defining is not the same as executing
def foo():
  print("Hello")

# To call a function, just use the name, followed by a pair of parenthesis.
foo() # Executes the function foo. This will result in a print statement, "Hello"

```

## Examples of simple functions 
Let us look as some example functions that have no inputs.
```python

# A function called sayHello. The function prints 'Hello'. And then prints "Goodbye"
def sayHello():
  print("Hello")
  print("Goodbye")

# A function called printNurseryRhyme(). Prints out the lyrics from "Twinkle Twinkle Little Star"
def printNurseryRhyme():
  print("Twinkle Twinkle Little Star")
  print("How I wonder what you are.")
  print("Up above the world so high")
  print("Like a diamond in the sky")
  print("Twinkle, twinkle little star")
  print("How I wonder what you are")
```

## How to send something inside a function?
What about functions like len() and print()? Can't you put stuff inside those functions? How do I do that with my own functions?

### This leads us to the concept of arguments.
Arguments are things that you can "pass" into a function. Let us look at an example function called add().

```python
# The two arguments in this function are called x,y. We can now pass things inside to the function.
def add(x,y):
  print(x + y)
  
# We are calling add, but we are also passing in two values, 2 and 3.
add(2,3) # This will print 5
```

### How do arguments work?
Arguments are essentially variables, so...
```python
def add(x,y):
  print(x + y)
  
# We will call add() and we will pass in 2 and 5 as our arguments.
add(2,5) # According to the definition of add, x = 2 and y = 5.
```


#### More examples
```python
# Defining a function called greet(). This has one argument called name.
def greet(name):
  print("Hello", name)
  
# Calling greet, and passing in "Jack" as the first argument
greet("Jack") # According to the definition of greet(), name = "Jack"
```

```python
# The same if-else statement we used before in another one of my notes, but now in function for.
# The function is called checkAge(), and it prints whether you are old enough to buy alchohol.
def checkAge(age):
  if(age >= 21):
    print("Here's a pint of beer")
  else:
    print("Here's milk...")
  
# Executing the function checkAge()
checkAge(24) //According to the definition, age = 24.

```


### [REMEMBER THIS, OR ELSE!] A function should not know what happens outside it's definition!
```python
x = 5 # This is a variable with the value 5

# Bad style
def foo():
  print("Hello, World")
  print( x + 5 )        # BAD, DO NOT USE VARIABLES OUTSIDE THE FUNCTION DIRECTLY

foo()
```
```python
x = 5 # This is a variable with the value 5

# Better style
def foo(n):
  print("Hello, World")
  print(n + 5)      # Good. You can access the variable outside by passing it inside the function.

foo(x)

```

### [IMPORTANT!!!!!!!!!!!!!!], the variables inside a function are different from outside it.
```python
a = 123 # This is a variable called 123

# Let us define a function called foo, that takes one argument called "a".
# Remember that a function should not know what happens outside it!
def foo(a): #This "a", is not the same "a" outside it.
  print(a)

# Executing foo(), and passing the value 4 inside it.
foo(4) # This will print 4, not 123

```

### [ALSO REMEMBER THIS] You should be able to write functions seperate from everything else!
Since a function should not know what happens outside of its definition, you can write functions without context to the rest of the program. 
```python
# Example. Write a program that will check if a number is greater than 20.

# Since I am writing a function, I do not care what number they pass in. I do not care what the variable they pass in is called. I can just write my function seperately.
# I create a argument variable called x. I don't know what number x will be, but that doesn't matter. You can write
# the function assuming that it is a number.
def isGreaterThan20(x): 
  if(x > 20):
    prints("True")
  else
    prints("False")


# Now I can use the function in any manner I want, for any number i want.
isGreaterThan20(434) # prints True

isGreaterThan20(-1) # prints False

x = 11 # REMEMBER. THIS x IS NOT THE SAME x AS THE ONE DEFINED IN THE FUNCTION
isGreaterThan20(x) # prints False

n = 123
isGreaterThan20(n) # prints True

```

 
## Sending something outside of the function.
We recalled that to send something inside the function, we used arguments. To send something out, we the "return" keyword. 
```python
def foo():
  print("I will now send out the value 3")
  return 3
  
# Executing foo().
foo() # you might notice that nothing happened regarding 3.

# Executing foo() again, but we can capture the return value inside a variable
x = foo() # foo() will return 3. Therefore, x = 3

# Executing foo() again again, but we are using it inside print().
print( foo() ) # foo() will return 3. Therefore, this leads to print(3).

```
### REMINDER, the function automatically ends when the "return" keyword is used.
```python
# A function that takes two arguments, x and y. The function will add the two and return the sum.
def add(x,y):
  sum = x + y
  return sum   # return was used. The function ends here.
  print("The sum is", sum)  # This command will not execute since return was already called.
  

# Calling add()
n = add(4,4) # Note that the print statement is not executed because of the way the function was defined

```
