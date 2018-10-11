# Functions

## Why?
There are many reasons to use functions, but there is a main reason for using functions; Reusability. Functions let us write code
in a manner so that we can easily reuse it 

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
#Defined a function called foo that will print "Hello" when executed. However, defining is not the same as executing
def foo():
  print("Hello")

# To call a function, just use the name, followed by a pair of parenthesis.
foo() # Executes the function foo. This will result in a print statement, "Hello"

```

## Example functions (Without arguments)
Let us look as some example functions that have no inputs.
```python

# A function called sayHello. The function prints 'Hello'.
def sayHello():
  print("Hello")

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
What about functions like len() and print()? You can put stuff inside it? How do I do that?

### This leads us to the concept of arguments.
Arguments are things that you can pass inside a function. Let us look at an example function called add().

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
  
# When we call add(), we passed in 2 and 5.
add(2,5) # According to the definition of add, x = 2 and y = 5.
```


#### More examples
```python
# Defining a function called greet(). This has one argument called name
def greet(name):
  print("Hello", name)
  
# Calling greet, and passing in "Jack" as the first argument
greet("Jack") # According to the definition of greet(), name = "Jack"
```

```python
# The same if-else statement we used before, but now in function for.
# The function is called checkAge(), and it prints whether you are old enough to buy alchohol.
def checkAge(age):
  if(age >= 21):
    print("Here's a pint of beer")
  else:
    print("Here's milk...")
  
# Executing the function checkAge()
checkAge(24) //According to the definition, age = 24.

```


### REMEMBER, a function should not know what happens outside it's view
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

### REMEMBER, the variables inside a function are different from outside it.
```python
a = 123 # This is a variable called 123

# Defining a function called foo, that takes one argument called "a".
# Remember what we talked about 10 lines ago. A function should not know what happens outside it
def foo(a): #This "a", is not the same "a" outside it.
  print(a)

# Executing foo(), and passing the value 4 inside it.
foo(4) # This will print 4, not 123

```
 
