## This is meant to be a suppliment to https://stjohn.github.io/teaching/csci127/f18/lab3.html. Make sure you read through the Professor's Lab beforehand.


# Lab 3

## New Turtle Commands
Recall that we went through the following commands.

#### import turtle
```python
# Remember that turtle is not available to Python. 
# To use it, we must download the extension/module on the computer and import it.
import turtle
```

#### turtle.Turtle()
Similiar to integers, strings and lists, turtle.Turtle() creates a type that we will refer to as a turtle type.
So like all other types, we can store the turtle as a variable.
```python
# Again. When we use turtle commands, we MUST import turtle
import turtle

#Now, we have access to turtle.Turtle()

x = turtle.Turtle() # We created a turtle and put it in the variable "x".
myOtherTurtle = turtle.Turtle() # We created a second turtle and put it in variable "myOtherTurtle".

```

#### .forward(integer)
You can make your turtle move by using forward(). This is done by telling a specific turtle (stored in a variable),
to move forward a specific amount of distance.
```python
import turtle

x = turtle.Turtle() # We created a turtle and put it in the variable "x".
myOtherTurtle = turtle.Turtle() # We created a second turtle and put it in variable "myOtherTurtle".

x.forward(50) #This will make the turtle we stored in "x", to move forward 50 units.
myOtherTurtle.forward(100) # This will make the turtle we stored in "myOtherTurtle", to move forward 100 units
```

#### .left(integer) and .right(integer)
Makes your turtle rotates left or right. The integer you put inside left() or right() is the angle of rotation.



## Finished reading this entire document?
Click on the link and read through lab one more time.
https://stjohn.github.io/teaching/csci127/f18/lab3.html

If you understand everything in the Professor's Lab, you are ready to move on.
