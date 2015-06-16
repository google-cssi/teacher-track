# Python - Variables

## Objectives

+ Interact with the Python Interpreter
+ Understand how and when to use comments
+ Explain what an integer is and why it's used
+ Use common mathematical operations with integers
+ Understand the difference between Integers and Floats
+ Use typical methods like to_f and to_s to mutate integers

## Motivation / Why Should You Care?


## Lesson Plan

There are 2 main ways to interact with Python - through a *script* and through the *interactive mode*.

### Running a Python Script

In a previous lecture we saw how to write a Python script and run it. The command is as follows:

python <filename>

Example:

python test.py

A few things to note here:
You need to be in the same directory as the python script to do this (otherwise, run the script with a relative/absolute path...python hw1/hw1/hw1_2/hw11.py
Python scripts are lines of code executed from top to bottom

Interactive Mode

Python also sports an interactive mode that allows you to run individual lines of Python code one at a time or in a conditional block(more on that later). For now, all you need to know is that if you invoke the command python, it will open up the interactive mode and allow you to run individual lines.

panicker-macbookpro:~ panicker$ python
Python 2.5.1 (r251:54863, Jun 17 2009, 20:37:34) 
[GCC 4.0.1 (Apple Inc. build 5465)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> print 'hello world'
hello world
>>>

A few things to note here:
The moment you close the prompt (Hold Control and Hit D) the code you ran is lost and not saved anywhere
The three carrots >>> are the python prompt - you enter lines of python at this prompt
The interactive mode should be used for testing purposes only
All exercises submitted needs to come in the form of a script not as lines from your interactive mode

The Basics of Python

Python is a powerful programming language. We'll talk about some of the basic pieces of this language in this page. You can get more details via the official Python site.

Comments

A comment is a note that a programmer can leave in the program to explain it. Comment syntax is different in every language, but in python, single line comments are delimited with a #. Try adding this:

# This won’t print!


Comments can span multiple lines:

# This program was built to allow a user to easily
# access data files associated with registration
# and person information. It is the best program
# ever written. It is loved and adored by millions.

Variables

Variables -- names we give to data -- are the bread and butter of programming:

x = 2
y = 3
z = x + y

print z

Unlike in mathematics, where = signals an equation, in programming = means assignment. The key difference is that in math, equations all apply at the same time; in programming, there's an order to these assignment statements -- and that order matters.

You declare variable names and associate them with values that you can perform operations upon. In Python, variables can not only represent simple data types (primitives) like integers but also more complex objects or collections of objects. For instance a variable, my_dog can point to a dog object that can do things like bark(), roll_over(), wag_tail(), etc. More on that later.

Primitives

Primitives are some of the most basic ways of representing data in a computer program. They are the fundamental building blocks of more complex representations and are a great place to start learning programming. From your every-day life, you already know about 2 primitives:
text: this is called str in Python (short for "string").
number: this is called int in Python (short for "integer").

Assignment

The assignment operator, written =, is used to give meaningful names to pieces of data. This should already be a familiar concept to you.

What will happen when you run this program?

my_str = 'hello, world!'
print my_str

What about now?

my_str = 'hello, world!'
my_str2 = 'hello there!'
my_str = 'hello, albert!'
print my_str

A name can only refer to one thing at a time. When you assigned "hello, albert!" to my_str, it forgot its old value of "hello, world!".
Integers

Most of you should be familiar with the concept of an integer. Try running a few of these operations below:
int1 = 3; int2 = 4; int3 = int1 + int2; print int3
int1 = 3; int2 = 4; int3 = int1 * int2; print int3
int1 = 3; int2 = 4; int3 = int1 + 10; print int3
int1 = 5; int1 += 3; int1 *= 2; print int1


## Conclusion / So What?


## Hints and Hurdles

+ 