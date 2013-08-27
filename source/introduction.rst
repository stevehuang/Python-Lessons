.. highlight:: ectosh


==========================
Lesson 1- Introduction
==========================

----------
Syllabus 
----------

1. Introduction and goals
2. Statement, expressions, and variables
3. Functions, logic, conditions
4. Data types 
5. Loops
6. Data type - Objects
7. Event-driven programming
8. local and global variables, buttons, and input fields
9. The canvas, static drawing, timers, interactive drawing
10. Lists, keyboard input, motion, positional/velocity control
11. Mouse input, most lists, dictionaries, images
12. Deep dive classes, tiled images
13. Acceleration and friction, spaceship class, sprite class, sound
14. sets, groups of sprites, collisions, sprite animation

-------------------
Introduction 
-------------------

Coding seems to be the popular trend today. The everyone should
learning coding “meme” trend has really taken off. Even NYC major
Bloomberg has been advocating programming (link found `here
<https://twitter.com/MikeBloomberg/status/154999795159805952>`_). While
coding is trendy, it involves more than just typing away at your
computer. These lessons and notes aim to provide a bases to start
becoming a not just a programmer, but a problem solver. 

The goal of these lessons is to introduce Python and basic programming
and computer science ideas to high school level students & readers. It
is assumed that no programming and only basic math skills are needed
for these lessons. The lessons cover general concepts and gently
introduces Python syntax and usage to students with an emphasis on
examples.

The first half of the lessons covers basic syntax and introduces
general programming constructs. After each topic, exercise problems
are encouraged to be done. Some exercises extend on the topics covered
in the lessons, while others build upon previous lessons.

There are a few ongoing mini projects to help reinforce concepts and
also motivate and encourage readers to try out different things. Some
of the mini projects are more open-ended in order to expound the idea
there is no one solution to solve a problem.

The second half of the lessons focus on how to use Python for game
development and introduces more computer science ideas. We use a game
library called PyGame which is written for Python to expedite game
development. As the reader gets more accustomed to the programming
language, the problems will shift mode towards problem solving rather
than just reiterating a certain topic.

One of the key things to recognize is that learning to program & code
is more than just knowing how to write a certain programming
language. It involves researching, designing, understanding,
communicating before you even write code. We'll try to practice an
touch upon those skills through these lessons. 

-----------
Setup
-----------

Before we start with the lessons, we need to setup your computer with
Python. The lessons can be done on Windows OS or Mac OsX. We provide
online links to the setup instructions. These instructions are written
by Python community developers. Much of the lessons were written with
Python version 2.7.5. 

**Setting up on MacOsX**

- Python 2.7.x for Mac OsX link `here <http://www.python.org/download/releases/2.7.5/>`_ 

- Python install instructions `here <http://babydatajournalism.tumblr.com/post/20704018450/how-i-installed-python-april-2012-mac-os>`_

Python downloads (for other OSes) found `here
<http://www.python.org/download/>`_

An editor is a program that allows you to edit code. There are
graphical user interface (GUI) editors tailored for programming
languages. For these lessons, we use Eclipse, which is an open source
GUI. Eclipse is more than just an editor though. It is called an
integrated development environment (IDE). 

The instructions are provided here:

Installing Eclipse editor for Mac OsX `here <http://www.eclipse.org/downloads/?osType=macosx>`_

To get python development environment you need to download the PyDev
Plugin. The instructions are found `here
<http://pydev.org/manual_101_root.html>`_. A video tutorial can be
found `here <http://www.youtube.com/watch?v=gCapULV-tPE>`_

Visual Python (`link <http://pythontutor.com/visualize.html>`_) is an
online tool that is very useful for visualizing how your code
works. Some of the lessons will use this as a way to help your understanding. 

----------------------------
Writing your first Program
----------------------------

What is a computer program? When you write a program, you write in a
language which can be executed by the computer. For python you write
the code in a file with the extension ".py". The code is a series of
statements that are executed in order. Then you 

Let's write our first Python program.

Create a new file in a folder. Call it "hello.py".

Type the following code

.. code-block:: python
   :linenos:

   # set the variable hello to "Hello World"
   hello = "Hello world"
   # printing out hello variable
   print(hello)

Save the file and then run it using the terminal on Mac OsX. Type in
the terminal::

  % python hello.py 

You printed out the text "Hello World". You can think of Python code
being executed one line at a time.  Each set of instructions tell the
computer exactly what to do. 

Line 1 is a comment. When the line of code starts with the character
`#`, it means comments. Comment is some text, you can write that
describe what you are doing in the code.  When the code is running,
the comments are skipped and not executed.

Line 2 is a variable. We'll discuss more about variables later. Just
know that the variable `hello` is set to the string "Hello World". 

Line 3 is another comment.

Line 4 is a function which prints the text of the variable
`hello`. The function is called `print`. This is a special procedure
that is called that tells the copmuter to display the text to the
screen.

You can even write the code in a Python shell. Just type python at
your terminal. You will see something like this::

  % python
  Python 2.7.3 (default, Apr 10 2013, 06:20:15) 
  [GCC 4.6.3] on linux2
  Type "help", "copyright", "credits" or "license" for more information.
  >>> 

You can type the lines in from the program, like this::

  % python
  Python 2.7.3 (default, Apr 10 2013, 06:20:15) 
  [GCC 4.6.3] on linux2
  Type "help", "copyright", "credits" or "license" for more information.
  >>> 
  >>> hello="Hello World"
  >>> print(hello)
  Hello World
  >>> 

Type ``quit()`` to exit Python shell. 

-------------------------- 
Source code and examples
--------------------------

Source code and examples are posted publicly on github. The link is https://github.com/stevehuang/Python-Exercises.

---------------
Other comments
---------------

These lessons and notes were written for some programming lessons that
I was teaching my nephew. As a results, some of the notes may seem
incomplete. My goal was to find what worked for him. I've included
links to videos and tutorials that we reviewed. I've credited the
authors/creators whenever possible.

There are no plans to keep these notes or links updated. Python is a
language that keeps evolving. There are plenty of resources devoted to
documenting changes. I've documented some good resources used for
these lessons.

**Resources**

- `Python.org <http://www.python.org>`_ - official programming language website
- `Visual Python <http://pythontutor.com/visualize.html>`_ - an online python visiual code execution tool
- `Eclipse.org <http://www.eclipse.org/>`_ - Offical Eclipse Project Page
