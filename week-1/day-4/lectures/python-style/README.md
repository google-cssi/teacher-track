# Python Style Guide

Please follow these guidelines when completing your assignments:

## Keep lines short (< 80 characters) and readable

This doesn't have to be EXACT, but for a single line of code, shorter is generally better. Use variables and extra lines instead of making one line especially long.

Bad:

```python
print 'The class diagram is the main building block' + str1 + ' ' + 'You can then use it to do the following: ' + str2.upper()
```

Good:

```python
result_str = 'The class diagram is the main building block'
result_str = result_str + str1 + ' '
result_str = result_str + 'You can then use it to do the following: ' + str2.upper()

print result_str
```

## Always add comments (comment prolifically)

Comments should be added to demarcate parts of the script and to show logical blocks of code. Adding comments allows other programmers to more easily understand what's going on in your code. ("Future You" will be one of those people)

Good:

# Part I
print 'PART I'

# Manipulate a String to demonstrate upper(), lower(), and replace()
target_str = target_str.upper()
...
print target_str

3. Use single quotes instead of double quotes for strings

Bad:

print "hello world"
greeting = "hello galaxy!'

Good:

print 'hello world'
greeting = 'hello galaxy!'


4. Naming Conventions

The official naming conventions for python at Google are:

module_name, package_name, ClassName, MethodName, ExceptionName, FunctionName, GLOBAL_VAR_NAME, instance_var_name, function_parameter_name, local_var_name.

Important Conventions for Our Class:

Python Files: module_name (ex: demo_script.py)
Variable Names: local_var_name (ex: num_employees, total_payments)
Global Variable Names: GLOBAL_VAR_NAME (ex: FREEZING_POINT_WATER)
Function Name: FunctionName (ex: DivideByTwo)
Function Parameter Name: function_parameter_name (ex. DivideByTwo(target_num))
Class Names: ClassName (ex: DogHouse)

Please follow these conventions in all your course work.


5. Variables should have LOGICAL names

The name you choose for a variable is very important because it helps readers (and you, the programmer) understand the purpose of that variable. Generic names like big_str, big_int, etc. are considered bad names (except in demonstration scripts in which they serve no practical purpose). Verbose names (variable_for_adding_integers_together) are also frowned upon.

Good variable names should depict the purpose of the variable in a concise manner and perhaps also contain some information about the type of data the variable will be holding.

Here are some examples:

 Bad	 Good
 big_str	 results_str
 albert_str	 name
 int_for_counting_the_number_of_something	 counter
 total_number_of_employees	 num_employees

