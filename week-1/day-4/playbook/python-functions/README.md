Day 4 - Python Functions

# Functions

## SWBATs 

+ Understand N.I.C.O (Name, Input, Code, Output)
+ Declare functions with and without parameters
+ Call functions with and without passing arguments
+ Understand the concept of a return value
+ Understand local and global variable scope

## Motivation

Today we will learn about functions in Python. This is important because functions let us package code into blocks that we can reuse. It connects to what we've previously learned because we can take the code we've written before and package it into functions. This will prevent us from writing the same code over and over again. We've also been using a handful functions already and this lesson will explain how and why we've been doing that.

## Lesson Plan

### Concept

In programming, a function holds a set of actions that will only run when we call that function. This ultimately helps us control the flow of our program and allows us to easily repeat a set of actions multiple times.

If you prefer a metaphor:
A function is kind of like placing a mouse in a box and that mouse will only perform the actions he was trained to do whenever you call his name.

### Declaration

+ A python function is essentially a set of instructions that we write out and can reuse over and over again.
+ (Pick a kid in the class to call on). Joe - I want you to close your computer, stand up and walk out the door.
+ Jk, come back. These essentially are the steps that Joe would follow if he was getting ready to head out to lunch.
+ Computers need explicit step by step instructions like this because they cannot infer what you mean when you say something like go get lunch.
+ But we can essentially teach the computer what go get lunch means by wrapping up these instructions in a function called `GoGetLunch`.

+ The syntax for writing python functions is very specific. To define a function, you want to use the `def` statement:

```python
def GoGetLunch():
	print ""
```

+ The key elements here are the def statement, the parentheses and the colon at the end.
+ The instructions go inside this function as demonstrated by the indentation. Let’s print each of the steps inside of our function and try running the program.

```python
def GoGetLunch():
	print "Close Computer"
	print "Stand up"
	print "Walk out the door"
};
```
+ Nothing happened. Why is that? We declared our function - which is like adding the `GoGetLunch` function to the computer’s dictionary - but we didn’t actually tell the computer to execute the function.

### Calling a function

+ We need call a function like this `GoGetLunch()` to make it run.
+ This is the equivalent of telling the computer - do those steps in the `GoGetLunch` function. Test it out.
+ What’s up with those parentheses? Those are like a placeholder for something called an argument. 
+ Our instructions are pretty generic right now. What if we wanted to direct them towards a specific student? Like adding a step that says “hey, Joe”.

### Passing in Parameters (inputs)

```python
function GoGetLunch(student):
	print 'hey, ' + student
	print 'close your computer'
	print 'stand up'
	print 'walk out the door'
```

+ We can reuse this function and just change the name of the student we address by adding a student argument.
+ Then we can call it like this:

```python
GoGetLunch("Joe");
GoGetLunch("Jill");
GoGetLunch("Josie");
```

### Return Values

+ There is one more VERY IMPORTANT thing about functions - return values.
+ We are going to get some help explaining this concept from [Cheddar the mouse](https://docs.google.com/presentation/d/1yoZyfQbvEfw53Pp03Bd_ziY8-Ai0jqCeQ0NKy4EAce8/edit#slide=id.p60).
+ A function is kind of like placing a mouse in a box and that mouse will only perform the actions he was trained to do whenever you tell him to do a certain action.
+ Here is Cheddar in his box. We’ve trained him to `DoMath` (addition really) with two variables x and y.

```python
def DoMath(x,y):
	return x+y
```

+ Notice there is a `return` statement. We need to include `return` in order to get something back from the function. In essence if we left off the return statement Cheddar might perform the math in his head but not give us the answer. By saying return we’re telling the function give us back the answer.
+ This is important because most of the time functions don’t live all alone by themselves they rely on other functions - so getting something back is very important. Don’t forget the return! 
+ Another way to think about it is that `return` talks to the computer and `print` talks to people

### N.I.C.O

We can break down the creation of functions into four things that every function has:

+ **Name   ** - Decide an appropriate name for the function
+ **Inputs ** - Figure out what inputs, if any, are needed to accomplish what the name describes
+ **Code   ** - Put the code inside the function to be run when it is called
+ **Outputs** - A value that the function can return though it can be `undefined`

### Variable Scope

Another thing that is important to understand about python functions is variable scope. 
	
+ When you declare a variable outside of a function it will also be available inside of the function. For example:

```python
milkType = "whole milk"
def IsWholeMilk():
	if (milkType == "whole milk”):
		return true
	else:
		return false
```
+ If I run `IsWholeMilk();` we’ll get back true. The function `IsWholeMilk` has access to the variable milkType that was declared outside of the function.
+ BUT if you declare a variable inside of a function it will only be available inside of the function.
+ Here is an example:
```python
def milkTheCow():
  bessyCow = 'milked'  # local var
  return bessyCow;

print bessyCow  # Throws an error, since the variable is local to the function 'milkTheCow'

print milkTheCow()  # Prints correctly since we are printing the returned value now
```
+ If we type `bessyCow` we’ll get an error. We are trying to access `bessyCow` from outside of the function and she only exists inside of the function.
+ The only way you can get access to `bessyCow` is if you run the function. Then `bessyCow` will be returned - like when Cheddar tossed out the answer to those math equations - and we’ll be able to see the value that way.

+ *Variable scope* - and not being able to access variables outside of a function - seems annoying but it’s really important and helpful because you will know exactly what your variable is equal to - it can only be set from within your function so it can only be equal to the value that you set within your function.

### Lists as inputs

Functions can accept lists as inputs:
 
```python
def GetMaximumLength(list_of_strings):
    lengths = []
    for item in list_of_strings:
        lengths.append(len(item))
    return max(lengths)

print GetMaximumLength(['hello', 'from', 'cssi', 'at', 'google'])
```

And functions can return lists:

```python
def GetDigits(my_string):
    digits = []
    for letter in my_string:
        if letter.isdigit():
            digits.append(letter)
    return digits

print GetDigits('It is 71 degrees today')
```

Functions can modify their arguments:

```python
def SwapEnds(some_list):
    some_list[0] = some_list[-1]


def MessWithList(my_list):
    SwapEnds(my_list)
    my_list.append(5)


a_list = [1, 2, 3, 4]
print a_list
MessWithList(a_list)
print a_list
```

## Conclusion / So What?

Functions are the building block of any developer. They let you create little machines (mice) that you can use and re-use from other parts of your code. This can make life a lot easier and save a ton of typing!

## Hints and Hurdles

+ Syntax is important! In Python the indentation defines what is inside and outside of a function/method. Miss a tab somewhere and your code could have some really weird behavior.
	+ On a related now be very careful not to mix spaces and tabs in a file. If you do python might not recognize some of them
+ Function names should be descriptive and helpful. Trust me, 'future you' who doesn't remember your code at all will thank you.

