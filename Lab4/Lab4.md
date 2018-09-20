# Lab 4
## New Types
### Floats
Floats are decimal numbers. 
```python
x = 4.2 # This is a float
y = 0.2222 # This is a float
z = 1/3 # This will become a float
a = 1 # This is not a float, this is an integer
b = 1.0 # This is a float, because it is a decimal
```

### Booleans
Booleans are types that are either True or False.
```python
x = True # This is a boolean
y = False # This is a boolean
z = "true" # This is a string
```


## Type Conversion/Casting

#### int()
You can convert a string into an integer using int(), but only if the string looks like an integer

```python
x = "4" # This is a string because it has quotes.
# Adding two strings will concatenate the strings.
print( x + x ) # Prints out 44.

# Convert 'x' into an integer, and stores the new version inside the variable 'y'
y = int(x) # y is 4, not "4"

print( y + y ) # Prints out 8.


# Another Example
a = "10"
print( a + a ) # Prints out "1010"

print( int(a) + int(a) ) #prints out 20


# One more example
n = "hello"
print( int(n) ) # ERROR, CANNOT TURN "HELLO" INTO AN INTEGER

# Last example
f = "12.1"
print( int(f) ) #ERROR. You cannot turn "12.1" into an integer, because 12.1 is not a whole number.

```

#### float()
Recall that before, we have been working with integers, which are a data type that includes only whole numbers. But what about decimal numbers? They are called floats. To convert a string or integer into a float, using float().

```python
# Remember that this failed before
x = "12.1"
print( int(x) ) # ERROR, "12.1" can not become an integer whole number.

# However, this will work
x = "12.1"
print( float(x) ) # Prints out 12.1, not "12.1"

# Another example
money = "100.25"
money = float(money) # Convert money into a float, and store the value in the variable "money"
print( money * 2 ) # Prints out 200.50


# Small example
x = 2 # x is an integer.
y = float(2) # y is a float.
print( y ) # Prints 2.0, not 2

```
#### Is there really a big difference between between a integer and float?
Yes. Even though you can do most basic math with either of them, there are certain scenarios where they differ. Not only that,
an integer and float is very different in the perspective of a computer.

#### str()
Just like how you can convert a string into an integer or float, you can also do the opposite. To convert
an integer or float into a string, use str()
```python
age = 24 # This is an integer
print( age + age ) # Prints out 48

age = str(age) # Convert age into a string, and store the converted version inside the variable "age"
print( age + age ) # Prints out "2424"

# This also works on decimal numbers.
debt = 0.50 # This is a float
debt = str(debt) # Turn debt into a string, and store it inside "debt"
print( debt + debt ) # Prints out "0.500.50", not 1.0

# Another example
n = 14.24 # This is a float
print( str(n) + str(n) ) # Prints out "14.2414.24"

```

## Applying int() and float() with input()

#### Remember that when you use input(), everything you enter will become a string, even if you enter a number
```python
# Assume for the following input, you type 2 and hit enter,
print("Enter something into x")
x = input()   
print( x + x ) # Prints out "22", not 4
```

### When you use input() and want to do some math problems, you will typically need to convert.

#### [Example] Ask the user for their age, and print out how old they will be in 5 years.
Wrong solution
```python
# First, we need to ask for the user to enter their age through input.
print("Please enter your age")
age = input() # Remember this is a string.
print( age + 5 ) # ERROR, adding a string into an integer
```
Correct solution
```python
# First, we need to ask for the user to enter their age through input.
print("Please enter your age")
age = input() # Remember this is a string. So let us convert it into an integer
age = int(age) # Convert age into an integer, and store it inside the variable 'age'.
print( age + 5 ) # VALID, integer + integer.

```

#### [Example] Ask the user for two float numbers, then add them.
Solution
```python
# Since we are asking for two numbers, we need to call input twice.
print("Enter first number")
num1 = input()

print("Enter second number")
num2 = input()

# Since num1 and num2 are strings, then convert them to floats
num1 = float(num1)
num2 = float(num2)

# Now that num1 and num2 are numbers, in this case floats, we can add them properly.
print( num1 + num2 )

```

## Decisions (if-else statements)
When you want to things conditionally in your code, you use if-else statements. What do I mean by conditionally? It lets your program run and have different outcomes.

### Conditions
First, let us talk about conditions. Conditions are commands that evaluate to a boolean (either true of false). Let us look at all the comparison operators.
``` python
## == , this checks if they are the same value, do not confuse this with a single equal sign.
print( 2 == 2 ) # True
print( "1" == 1 ) # False, they are not the same type.
print( int("1") == 1 ) # True

## > , < , Less than or greater than. It works the same way as in math
print( 1 < 2 ) # True
print( 100 < 0 ) # False
print( 10 > 1 ) # True

## <=, >= , Less than or equal to. Greater than or equal to.
print( 1 <= 2 ) # 1 is less than or equal to 2. True
print( 2 <= 2 ) # 2 is less than or equal to 2. True
print( 4 >= 8 ) # 4 is greater than or equal to 8. False
```

### If statement
When writing an if statement, you must specify a condition that is True or False
```python
# Example
if( 1 == 1 ):  # 1 == 1 is a condition, that evalutes to True
  print("Hello")


# Another Example
if( 2 < 2 ): # 2 < 2 is a condition, that evalutes to True
  print("Yes")

```

#### The commands under the if statement ONLY EXECUTE when the condition is TRUE.
```python
# The output is "equal", because the condition is true.
if( 100 == 100 ):  # 1 == 1 is a condition, that evalutes to True
  print("equal")

# There is no output. Since A == B is false, the commands inside the if statement is ignored.
if( "A" == "B"):
  print("WILL THIS RUN?")

# There is no output. Since the condition is false, the commands inside the if statement is ignored.
if( 2 < -2 ): # 2 < 2 is a condition, that evalutes to True
  print("Yes")
  
# Output is "It works", since the condition 0 >= 0 is true.
if( 0 >= 0 ):
  print("It works")
  
```

### If-Else
We can expand the if statement with an else statement. The else statement will execute by default, ONLY when the if statement is False. Since the else statement will run by default, it does not need a condition.


```python
# When the if condition is true, then the else statement is ignored and vice-versa.

# The output is "Hello". Since 1 == 1 is true, the if statement is executed and the else statement is ignored.
if(1 == 1):
  print("Hello")
else:
  print("Goodbye")

# The output is "No". Since 1 > 2 is false, the if statement is ignored, and the else statement occurs.
if(1 > 2):
  print("Yes")
else:
  print("No")

# The output is "A". Since 2 <= 2 is true, the if statement is executed and the else statement is ignored.
if(2 <= 2 ):
  print("A")
else:
  print("B")
```

#### [Example] Ask the user to input their name. Print whether their name is Michael.
```python
# Let us ask for input and store the answer inside a variable called name.
print("Enter your name")
name = input()

# Use if-else statement. Remember that the if portion needs to have a condition that is either True or False.
if(name == "Michael"): # Use == to check if they are the same, not =
  print("HEY MICHAEL")
else:
  print("Hey, NOT michael...")

```

#### [Example] Ask the user to input their age. Print whether or not they are old enough to order at a bar.
```python
# First, we need to ask for input. So let us do so and store inside a variable called age.
print("How old are you")
age = input() 

# Remember that input() is always a string, so let us convert it into an integer.
age = int(age)

# Now let us use our if else statement. Remember that the if portion needs to have a condition
if( age > 21 ): # This is a condition, since age > 21 is either True or False.
  print("You are old enough! Have a pint!")
else:
  print("Uh. Here's some milk")
```

### if,elif, else
Before with if-else, we had two outcomes. Now, lets expand it to have as many outcomes as possible. To do so, we use "elif".
```python
# Just like if, you need to put a condition that is either true or false inside the elif statement.
if(1 < 1): # 1 < 1 is a condition
  print("A")
elif(1 > 1): # 1 > 1 is a condition
  print("B")
else:       # else will execute when everything else is False
  print("E")
  
  
# You can add as many elif statements as you want
if(1 < 1): 
  print("A")
elif(1 > 1): 
  print("B")
elif(2 == 2): 
  print("C")
elif( 0.5 < 2 ):
  print("D")
else:       # else will execute when everything else is False
  print("C")
```

#### Note that if-elif-else statements will stop at the first condition that is true.
```python
x = 100;

# This will output "A".
# Even though x > 5 is true, x > 0 occurs first, therefore it will stop immediately.
if(x > 0): # This is true
  print("A")
elif( x > 5 ): # This is also true
  print("B")
else:
  print("C")


# Even though though multiple statements are true, only the first will will count.
# The output is "You can drink"
age = 24;
if(age > 70): # False
  print("You can retired")
elif(age > 21): # True
  print("You can drink")
elif( age > 18): # True
  print("You can smoke")
elif( age > 13 ): # True
  print("You can work")
else:
  print("You're a kid")

```


### You MUST start with an if statement. elif and else is optional. 
```python
# Example
else:   # WRONG, you can't have an else statement by itself.
  print("a")
  
# Example
elif ( 1 == 1):  # WRONG, you MUST start with an if statement.
  print("a")

# Example
if( 1 == 1 ):  # This is okay, you can have a single if.
  print("a")
  
# Example
if( 1 == 1 ):  # This is okay, you don't need to have an else statement.
  print("A")
elif( 1 <= 1 ):
  print("B")
elif( 1 >= 1):
  print("C")

# Example
elif( 1 == 1):   # WRONG, you still MUST start with an if statement.
  print("A")
else:
  print("B")

```

### Using multiple if statements just creates multiple if-elif-else statements.
```python
# Since each condition is an if statement. They can all be evaluted individually without influencing each other.
# The output is "You can drink", "You can smoke", "You can work".
age = 24;
if(age > 70): # False
  print("You can retired")
if(age > 21): # True
  print("You can drink")
if( age > 18): # True
  print("You can smoke")
if( age > 13 ): # True
  print("You can work")
else:
  print("You're a kid")

```



