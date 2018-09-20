# Lab 4

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


