=========================================
Lesson 3 - functions, logic, conditionals
=========================================

---------
Function
---------

A function is a relation between a set of inputs and one
output. Imagine a function as a black box that you give inputs
to. It'll perform it's operations on them and come up with an
output. Like in math, you can have a function with multiple inputs and
one answer.

For example, in math, the formula

.. math::

  2x+3y &= z \\
  (x,y) &=   \\
  (0,0) &= 0 \\
  (1,1) &= 2+3 = 5 \\
  (2,2) &= 4+6 = 10 \\
  (3,3) &= 6+9 = 15

The variable ``z`` can be expressed as a function, where inputs are ``x``, ``y``. The function can be writting as ``f(x,y)`` like this:

.. math::

  z= f(x,y) = 2x+3y

In Python, we declare functions::

  def z(x,y):
    z = 2*x+3*y
    return (z)

The function we declared is reusable.  With the example above, we can try::

  z(0,0)
  z(1,1)

Go ahead and type this in to a file and run python to try it out. The code is

.. code-block:: python
   :linenos:

   def z(x,y):
     z = 2*x+3*y
     return (z)
   answer = z(0,0)
   print "The answer for input (0,0) is " + answer
   answer = z(1,1)
   print "The answer for input (1,1) is " + answer

This function is doing the same thing as the equation we first
described. A function definition is a compound statement consisting of
a header and a body. It’s a way of grouping instructions and reusing
the same code!

In line 1, the declaration includes the keyword ``def``, the name of the function, a
sequence of parameters enclosed by parentheses, followed by a colon ``:``.

The body (lines 2,3) consists of a sequence of statements, all
indented and aligned with each other. Lines 2,3 is a block of code. 

Functions may return a value using the keyword ``return``.  To
evaluate a function call, replace the function's parameters in the
body of the function by their associated values in the call and
execute the body of the function.

Here is another example of **declaring** a function::

  # This function prints out the name
  def MyNameIs(name):
    print “my name is “, name

And this is how to **call** the function::

  MyNameIs(“Katie”)
  MyNameIs(“Francis”)

Scope of variables

Variables have something called 'scope', which dictates where they can
be referred to. There are two types of scope: global and local. Global
variables can be referred to at any point in the program, while local
variables can only be referenced within the segment of code (for
example, a function) where they appear.

You can define a global variable as
  global variable_name

here global is a keyword. It means that within a python script/file, you can make a reference to variable_name within a function or outside of a function.

Example:

global a_name="Global"

def print_something():
    a_name = "Local"
    print a_name


Which variable was printed? Why? Comment out the line a_name = "Local".  Now which variable is printed?


more examples:
http://www.codeskulptor.org/#examples-more-1b_functions-scope.py
more details:
http://docs.python.org/2/tutorial/classes.html#python-scopes-and-namespaces

----------------------------
Logic & Relational operators
----------------------------

A boolean value can be: ``True`` or ``False``. What does true or false
mean? It pretty much means what is stated. 

Is 1 equal to 1? **True!**

Is 1 equal to 2? **False!**

With Python you can write code that evaluates if a statement is either true or false. 

Try the following in the Python shell::

  1 == 1
  1 == 2
  15 < 10
  15 > 10


What were the results? With Python you can check if the relations
between different numbers. But it doesn't have to be just numbers. For
example you can do ``True == False``. The keywords ``==``, ``<``,
``>`` are called relational operators. In Python, the operators have
to evaluate to true or false. 

There are a host of other operators too::

  <    >    >=   <=
  ==   !=   and  or

.. Remember unions and intersections?
.. An intersection is a set of elements in common. 
..  A list [1 , 2 , 3,  5 ]
..  B list [6, 7, 8, 1]
..  1 is in A and B
.. A union is the set of all the elements 
..  A list [1 , 2 , 3,  5 ]
..  B list [6, 7, 8, 1]
..  6 is in A or B

You can use logical operators like and, or to make decisions in code.

False AND False = False
False AND True = False
True AND False = False
True AND True = True
False OR False = False
False OR True = True
True OR False = True
True OR True = True

NOT (False) = True
NOT (True) = False


if statements
How do we make decisions in code? Use logic statements. One way to do that is with if statements.
a) “If you are not busy, then fold the bed”
b) “If you are not busy and you are not tired, then fold the bed”

Can you do something like this in code? 

Yes!  
a) 
if (not busy):
  FoldBed()

b)
if (not busy) and (not tired):
  FoldBed()


What about this: 
“if you are my friend, I will give you 10 dollars or else if you are my cousin I will give you 20 dollars”

Examples:

friend= False
Cousin = False

if (friend==True) and (Cousin==False):
  money = money + 10
elif (friend == False) and (Cousin==True):
  money = money + 20


