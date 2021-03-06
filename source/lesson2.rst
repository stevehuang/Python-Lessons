============
Lesson 2 - expressions, statements, and variables
============

One of the first things to learn in a programming language is the
syntax and grammar. These are the rules that defines how you write
your code and how your code is executed. We’ll focus on the “how you
write your code” topic for these lessons.

Lesson 2 covers expressions, statements, variables and writing and
executing python code.

----------
Expression
----------

An expression in a programming language is a combination of explicit
values, constants, variables, operators, and functions.

For example, a value can be a number or a string.::

 numbers - 4, 3.14
 string - “How are you?”

A variable can be like::

 x,y,z
 bigVariableName
 special_123

Operators can be like::

 +, -, *, /, *= 

And finally, functions can be like::

 HelloWorld()
 Factorial(5)

----------
Statements
----------

A statement is a composition of keywords and expressions.  A simple
statement comprises of a single logical line.

Here is are examples of an assignment statements::

 x = 5
 y = 10
 string = “Hello World”

Another useful statement is the print statement. The function outputs

Here are some examples::

  print(“Hello World”)
  
There are keywords in Python language to perform certain operations. They are listed here::

 and      assert   break    class    continue def      del      elif   
 else     except   exec     finally  for      from     global   if 
 import   in       is       lambda   not      or       pass     print 
 raise    return   try      while    yield

For more details about statements, you can go to this reference.

http://docs.python.org/2/reference/simple_stmts.html

**Compound Statements**

Compound statements contain (groups of) other statements. They affect
or control the execution of those other statements in some way. In
general, compound statements span multiple lines.

Here are some examples of compound statements. Don't worry about
trying to understand them. We'll go over them in other lessons.

If statement::

  x=10 
  if x > 5:
    print(“x is greater than 10”)

While statement::

  x = 0 
  while x < 10:
    x += 1 
    print(“x is “, x)

For statement::

  for x in range(10):
    print (“x is “, x)

Try statement::

 try: 
  x = 1/0 
 finally:
  x = 42 

A whole compound statement may be contained in one line. For example,
you can write the For statement above like this::

For statement in one line::

  for x in range(10): print ("x is", x)

However you can imagine that if there is a lot of code, then writting
everything in one line looks confusing. Generally, it is not a good
practice to write all the code in a line.

reference: http://docs.python.org/2/reference/compound_stmts.html

---------
Variables
---------

Earlier, we saw assignment statements, like ``x =5`` or ``string = “Hello World”``

A variable is the name that is left of assignment. The right-hand stide is the value.
Think of a variable as a placeholder, a bucket which can be used later. Like a math
equation, where you replace the variable with the assigned value. You
can change the variables value directly, like::

 x = 5
 x = x + 2
 print x

A variable can be named with any lettter, the special character "_" and every
number. You cannot start a variable name with a number though.

Variable numbers in Python are case-sensitive. This means a variable
name like ``variable_name`` is different than ``Variable_Name``.

Variables cannot be the same name as keywords in Python.

Similar a calculator and simple algebric equations, you can use
variables and assignments to compute answers. 

Some simple examples you can try out are::

  x = 10
  y = 20
  print (x+y)
  print (x*y)
  print (x*0)
  print (y*2)
  print (x/y)

What’s the answer to each example? Remember, just subsitute the x and
y variables with the values. Now try::

  print x/0

An error occurred. Dividing by 0 in Python, and in many other
programming languages, is considered an error. 

Try out the following::

  x+y*10

Did you notice it follows the order of precedence? First 10 is
multiply with ``y`` and then the result is added to ``x``. Python code follows
the order of precedence like math. Below is a table describing the order. 

+-------------------+----------------------------------------+
|Operator           | Description                            |
+-------------------+----------------------------------------+
|``+``, ``-``       | Addition, Subtraction                  |
+-------------------+----------------------------------------+
|``*``, ``/``, ``%``| Multiplication, Division, Remainder    |
+-------------------+----------------------------------------+
|``+x``, ``-x``     | Positive, Negative                     |
+-------------------+----------------------------------------+
|``**``             | Exponential                            |
+-------------------+----------------------------------------+

The operators are listed from lowest to highest precedence
(row-wise). Operators in the same box have the same precedence. You
have to perform the operations from left to right for the same group.

For example ``x=10**2+5*2-5`` is computed as follows:

1. First, ``10**2`` is calculated because Exponential is the highest
   precedence in the table above. ``10**2`` means 10 to the power of 2
   ("10 squared"), which is 100.

2. So the result would be ``100+5*2-5``. Then multiplication would
   take precedence. So ``5*2`` would be calculated.

3. Next the result would be ``100+10-5``. Since addition and
   subtraction are in the same group, we can just calculate from left
   to right. The final answer would be ``105``.

Another example is ``x=10%3**3``. Here ``3**3`` is performed first,
followed by the remainder operation ``%``. So it would be
``10%27``. The remainder would be ``10``.

You can find the detailed table for the order of precedence here
including other expressions that we have not covered.

http://docs.python.org/2/reference/expressions.html#operator-precedence

---------
Exercises
---------

1. **Statements.**  Try printing out some expressions
 Open the command shell or terminal. Type the statements::

  print “Hello World”
  print 3.14
  print x		

 What happened here? Why didn’t the last statement work?
2. **Assignment.** 
 Try the following assignments::

  name = “John Doe”
  print “My name is “, name
  name2 = “Wendy Doe”
  print “My name is”, name2
  print “Their names are “ + name + “ and “ + name2
  name = name2
  print “My name changed to”, name

 Notice that the ``name`` variable is changed to be the same as ``name2``. 
3. **Variables and Assignments.** 
 Try out the following code::

  x = 10
  y = 20
  x = y
  y = 12

 What is ``x``?
4. These series of exercises go more examples of how arithmetic works
   in Python.  First print out some numbers in Python. 
 Try::
 
  print 3
  print -1
  print 3.0
  print 3.1415
  print -3.3333

 Notice that the number 3 is printed out like that instead of
 3.0. This is because 3 is an integer and 3.0 is a floating point
 number. We'll cover this more in the data types lesson. We can
 convert data types and make the integer 3 into the floating number
 3.0 by running this command::

  print float(3)

 You can also convert a floating point number to an integer by running
 something like this::

   print int(3.0)
5. The previous exercise shows how we can explicitly convert to
   floating point or integer numbers. You can also do it implicitly
   through arithmetic calculations. For example::

     print (1.0*3)
     print (1*3)
   If one operand is a floating number, then the result will be one
   also.
   If both operands are integers like ``1*3``, then the result is an
   integer.
6. There are 5280 feet in a mile. Write a Python statement that
   calculates and prints the number of feet in 13 miles.
7. The perimeter of a rectangle is 2w+2h, where w and h are the
   lengths of its sides. Write a Python statement that calculates and
   prints the length in inches of the perimeter of a rectangle with
   sides of length 4 and 7 inches. (Try to use variables)
8. The distance between two points (x0,y0) and (x1,y1) is
   (x0−x1)2+(y0−y1)2. Write a Python statement that calculates and
   prints the distance between the points (2,2) and (5,6).
9. Given the variables x0, y0, x1, and y1, write an assignment
statement that defines a variable distance whose values is the
distance between the points (x0,y0) and (x1,y1).
10. Heron's formula states the area of a triangle is s(s−a)(s−b)(s−c)
where a,b and c are the lengths of the sides of the triangle and s=12,
(a+b+c) is the semi-perimeter of the triangle.

Given the variables x0, y0, x1,y1, x2, and y2, write a Python program
that computes a variable area whose value is the area of the triangle
with vertices (x0,y0), (x1,y1) and (x2,y2). (Hint: our solution uses
five assignment statements.)

More exercises:

