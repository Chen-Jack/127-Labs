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
Lastly, you have the ability to access a specific symbol of a string.
```python

example = "Hello There" #This is a string because it has quotes around it

# To access the first symbol of a string, we write
print( example[0] ) #Will print the first symbol in example. Output is "H"

#Remember that indexs start at 0

print( example[3] ) #Will print the 4th symbol. Output is "l"

print( example[5] ) #Will print the 6th symbol. Output is " ". A space character

print (example[4353543] ) # Will cause an error. Our string does not have that many symbols in it.

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
Just like strings, you have the ability access things inside the list.
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



## Loop Refresher
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
## How do Loops work, why is the variable important?
Loops work by traveling through something called an iterable. An iterable can be simply understood as ...
> A data type that has a order to it.
```python

# This is an iterable cause there is an order.
x = [5 , 1, 5] # First value is 5, next is 1, last value is 5.

# This is also an iterable
name = "Jack"  # First value is "J", then "a", "c", last value is "k".

# Thus, we should know that
a = [1,2,3] # LISTS ARE ITERABLE
b = "A sentence" #STRINGS ARE ITERABLE
c = 3 # A single integer is NOT iterable.
d = [3] # A list containing a single integer is iterable

```

# Loops work by having a variable assign itself to each value of an iterable on each step (IMPORTANT)
```python
# This is an oversimplification, but this depicts the essence of what is happening

#Note that the variable is called i.
for i in range(5):
 print(i)
 
#First, range(5) will "basically" return a list starting from 0, up to but not including 5.
# Aka range(5) = [0,1,2,3,4]

#So when we say
for i in range(5):
 print(i)
 
#It logically becomes.
for i in [0,1,2,3,4]:
 print(i)

# Therefore. i start at 0 on the first step, and will reassign itself on each step.
for i in [0,1,2,3,4]:  # First output is 0, then 1, then 2, then 3, and then 4.
 print(i)
 
# Further proof.
for number in [5,2,1]: #First output is 5, then 2, and then 1.
 print(i)
 
# This works with strings because strings are also iterable (Has an order)
for letter in "WOW": # First output is "W", then "O", and then "W"
 print(letter)

# Examples.
# Question 1) Print all numbers from 0 to 10.
# We know that range(11) will "basically" return the list of numbers [0,1,2,3,4,5,6,7,8,9,10]. 
# Remember range(11) starts at 0, and stops, but does not include 11.

for number in range(11): # Since we are actually using the numbers inside range(11), lets use a meaningful variable name
 print(number)
 
# Question 2) Print hello 3 times.
# We will use range(3) because we want something to happen 3 times.
for whocares in range(3): #Since we aren't using the numbers directly in range(3), we can use any variable name.
 print(number)

```

## Extra Range() Uses
As we just talked about, range(n) basically returns a List of numbers from 0 to n (but not including n)
```python
range(3) basically becomes [0,1,2]
range(5) basically becomes [0,1,2,3,4]
range(2) basically becomes [0,1]
```
Range has extra uses, for example range(start, stop). When you specify two numbers in range, it basically does the same thing as before, but you can choose where the values start.
```python
#range(5) basically becomes [0,1,2,3,4]
#range(2,5) starts at 2, and stops (but doesn't include) 5. So it becomes [2,3,4]

#range(10) basically becomes [0,1,2,3,4,5,6,7,8,9]
#range(3,10) will do the same as range(10), but start at 3. [3,4,5,6,7,8,9]

#Example. Print all numbers from 5 to 20
# Normally, if we use range(21), (Again, not range(20) because range(20) does not include the number 20),
# it would start at 0. Since we want to start at 5, we use range(5,21):

for value in range(5,21): #Output is all numbers from 5 to 20
 print(value)
 
for i in range(1,11): # Prints all numbers from 1 to 10, not including 0
 print(i)
```
The other use case is range(start, stop, step). When you specify 3 numbers, it works like range(start,stop), but you can specify the change between each value.
```python
# range(2,11)  =>  [2,3,4,5,6,7,8,9,10]  #Stops at 11, but does not include it.
# range(2,11,2)  Does the same thing as range(2,11), but now each number jumps by 2
# So it logically becomes, [2,4,6,8,10]

# range(1,11,3) => [1, 4, 7, 10] #Values start at 1, stops at 11, but not including it, and each number jumps by 3

# range(0, 10, 2) => [0,2,4,6,8] #Remember! Stops, but does not include the last number.

# Example, Print all even numbers from 0 to 100.
# We use range(0,101, 2) because we start at 0, stop at 101 (but not including 101), and increases by 2 each time.
for evenNumber in range(0,101,2):
 print(evenNumber)
```

#### Is there a way to go from 0 to 100, and jump by 2's using range(start,step)?
No, if you want to do steps, you have to specify 3 numbers. Even if you start at 0. </br>
So use range(0,101,2).

## Final Loop Review
```python

for i in range(3): # Prints 0, 1, 2
 print(i)

for letter in range(3): # Prints 0, 1, 2.  Variables are just names, don't let them fool you
 print(letter)
 
word = "Hello"
for x in word: # Prints, "H", "e", "l", "l", "o"
 print(x)

myList = [4, 1, "ah"]
for item in myList: #Prints 4, 1, "ah"
 print(item)
 
for i in 3:  # Error, 3 is not iterable. You can't traverse numbers
 print(i)
 
for i in [3]: # Prints 3.   Lists are iterable though, even if has a single value
 print(i)
 
for letter in "": #Prints nothing, because "" has nothing inside it. Note, this is not an error. This is expected
 print(letter)
 
for letter in : # Error, didn't specify something to loop through
 print(letter)
 
for item in []: #Prints nothing, because the list has nothing inside it. Note this is not an error.
 print(item)
 
for num in range(2,5): # Prints 2, 3, 4
 print(num)
 
for ok in range(2,7,2): # Range(2,7,2) becomes [0,2,4,6]. Prints 0, 2, 4, 6
 print(ok)
 
#The values start at 10, and stops at -1, but not including -1. So it actually ends at 0.
for countdown in range(10,-1, -1): #Prints 10,9,8,7,6,5,4,3,2,1,0. 
 print(countdown)

```

## Inputs
print() allows the code to send a message to the user. input() is the opposite, and allows the user to send a message to the code.
```python
# Note, input() is a command. You won't see the effects of it in the code side, only when it is being run.

#When I execute this, you should be prompted on the OTHER window, to enter a value.
print("Enter a number")
x = input()
print("You entered, x)
```