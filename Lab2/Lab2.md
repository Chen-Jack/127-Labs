This is meant to be a supplement to https://stjohn.github.io/teaching/csci127/f18/lab2.html

## Type/Variables Refresher
Remember that we were introduced to two Python types so far:

**Integers** (Whole Numbers)
```python
x = 5 # Remember that comments start with a hashtag. This will be ignored by Python.
y = -12323232354353
someVariableName = 12
age = 24

positiveNumber = -1 
# Remember that variable names are just names. 
# Just cause the name is "positiveNumber", doesnt mean it HAS to be positive.
# However, it's up to you as the programmer to use variable names properly.

```
**Strings** (Collection of symbols/letters) </br>
```python

# All strings must be surrounded by quotation marks (Single or double quotes don't matter)

name = "Jack"
school = "Hunter College"

# A single letter can count as a string
y = "a"

 # Strings can just be symbols, letters are not required
x = "!?!###"

 # A space counts as a symbol. Thus, this is also a string
myVariable = " "

 # Your string can actually be empty. Technically this is a string with nothing inside it.
someValue = ""
```

### Type Operations
Integers have access to the typical math operations.
```python
x = 1
y = 2

print(x + y) # Output is 3 (Addition)
print(x - y) # Output is -1 (Subtraction)
print(x * y) # Output is 2 (Multiplication)
print(x / y) # Output is 0.5 (Division)
```

Strings have access to an operation called concatenation. (String Addition) </br>
This is done by using the "+" operation.
```python
print("ABC" + "DEF") # Output is "ABCDEF"
print("Hey" + "There") # Output is "HeyThere". Spaces are not automatically inserted
print("Hey " + "There") #There is is a space at the end of "Hey ". Output is "Hey There"
print("Hello" + "!!!!") # Output is "Hello!!!!"


firstName = "Jack"
lastName = "Chen"
fullName = "Jack" + " " + "Chen" # Adding my first Name, a space, and my last name
print(fullName) # Output is "Jack Chen"


x = "1" # Remember this is a string because its surrounded by quotes. 
y = "2" 
print( x + y )  # Output is "12". Not 3

print (1 + 1 ) #Output is 2. Because the inputs are not surrounded by quotes. Therefore they are integers
print ("1" + "1") #Output is "11"

```

# Lab 2
## A new type, Lists (Also called Arrays)
```python
# Lists are created by using square brackets [].

# Lists can have anything inside them.
variable = [1,4,5,2] # A list of integers

anotherList = ["1", "a", "Hello", "Goodbye", "", " ", "?" ] # A list of strings

y = [1, 5, "wow", "this is a string haha", -5] # A list containing a mixture of integers and strings

finalListExample = [ "1", 4, [ "a", "b", "c"], 0 , "hello"] # A mixed list, containing another list inside it

simpleList = [1,2,3] 
mixedList = [ simpleList, 3, "a"] # This list also contains another list inside it.
```
One important property is the ability to access things inside the list.
```python
# To access a spot inside your list, do the following

myList = [5, "hello", "a", 123, -5] 

# Accessing the 2nd index of myList. Remember that we start counting from 0. 
item = myList[2]  
print(item) # Output is "a"

item = myList[0] # Remember we can reassign variables. 
print(item) # Output is 5, because the index starts at 0.

item = myList[1]
print(item) # Output is "hello"

item = myList[9999999]
print(item) # Error. myList only has 5 things inside it. There is no 999999th index.

```

## How do Loops work?
Remember that to do something multiple times, we followed this general template
```python
# Remember that x is just a variable name, we can call it whatever we want

# Prints "Hello" 5 times
for x in range(5):
  print("Hello") 
  
# Prints "No" 10 times
for i in range(10):
  print("No")
  
# Prints "Yes" 50 times
for dsfdsfdsfsd in range(50): # Again, dsfdsfdsfds is just a variable
  print("Yes")
```
So what does the variable do?
