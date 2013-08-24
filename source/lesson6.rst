============
Lesson 6 - Data Objects
============

A data type that we have not discussed is **objects**. You can think
of an object as a noun. A noun - person, place, or thing - can perform
actions. You can program objects in a similar manner. An object can
"do things" which you can program using a **method**. Yuo can also
"can describe" it. This is call an **attribute**.

In Python you can create a new type that is an object. This object can
be virtually anything you want. The object can be a ``Person``, a
``Cat``, an ``Animal``, a ``Button``, etc.

Let's go over an example of how to write an object. Imagine a
basketball video game. You can describe a player as an object. So what
are some attributes for a basketball player? It can be their name,
height, weight, position, maybe if they have the ball or not. How
about methods? This means what can the player do? What action can they
perform? A player can shoot the ball, pass the ball, dribble the ball.

Now that we have an idea of what a player object contains, how do you
translate that into code? First, you have to define an object, which
includes the attributes and methods. Then you can create a new object
in the code.

When you define a new object data type, you need to use the ``class``
keyword. Something like this::

 class BasketballPlayer:
   def __init__(self, name):
     self.name = name

Notice there is function called ``__init__``. This is a special
function that means initializer. The function is called after an
instance of a ``BasketballPlayer`` object is created.

There are two inputs to the ``__init__`` function. The first is a
special variable called ``self``. The second is an attribute we
defined called ``name``. The name is just simply the basketball
player's name.

``self`` is a special variable. It references the object, in this case
``BasketballPlayer``.  We define the attribute for the object by
defining the **fields** for the ``self`` variable. 

Let's add some more attributes::

 class BasketballPlayer:
   def __init__(self, name):
     self.name = name
     self.weight = 150   # (unit in lbs)
     self.height = 72    # (unit in inches)
     self.hasBall = False

These attributes are defaulted to certain values. What this means is
that when you create a basketball player object, after ``__init__`` is
called, the fields ``weight``, ``height``, and ``hasBall`` are set to
the values shown above. 

Let's add some actions that the player can do - dribbing, passing, and
shooting. Note, we just show a framework for the code::

 class BasketballPlayer:
   def __init__(self, name):
     self.name = name
     self.weight = 150   # (unit in lbs)
     self.height = 72    # (unit in inches)
     self.hasBall = False

   def Dribble():
     if (self.hasBall):
       print(self.name+" dribbles the ball!")

   def Pass(self, player):
     if (self.hasBall):
       print(self.name+" passes the ball to " + player.name)
       self.hasBall = False
       player.hasBall = True

   def Shoot(self):
     if (self.hasBall):
       print(self.name+ " shoots the ball")
       self.hasBall = False

The methods ``Dribble``, ``Pass``, ``Shoot`` are added to the
``BasketballPlayer`` object. The ``self`` parameter is always the
first variable in a method. When a method like ``Shoot()`` is called, 

We've defined the data type object called ``BasketballPlayer``. How do
we use the object in our code? It's similar to other data types
(string, integer, etc). We need to create and initialize a variable.

Here's an example of how to use the object::

  def example():
    player_1 = BasketballPlayer("Kobe Bryant")
    player_2 = BasketballPlayer("Michael Jordan")
    player_1.hasBall = True
    player_1.Pass(player_2)
    player_2.Shoot()

A player is created by running the command ``player_1 =
BasketballPlayer("Kobe Bryant")``. The input parameter is the name of
the player, which matches the ``__init__`` function. We can add more
parameters if we like by adding more arguments to the function.

You can change the value of the attributes by referring to the object,
like ``player_1`` and accessing the field. Just type a dot ('.')
followed by the field name like ``player_1.hasBall = True``.

To call a method, like ``Pass``, you use the variable name, followed
by a dot ('.') and then the method name with any parameters. Unlike
the definition of the method where you put ``self`` as the first input
variable, you do not have to write ``self`` as the first
parameter. Python automatically will pass that variable to the method
when called.

You can download a copy of the entire source code for this example
`here
<https://github.com/stevehuang/Python-Exercises/blob/master/basketball_objects.py>`_.


--------- 
Exercises 
---------

1. In the example for the lesson, we forgot to set the height and
   weight for the players. Opps! Add the height and weight of the
   players and print out their stats at the end of the ``example()``
   function.

2. Suppose we want to make the game **Pong**. One of objects we can
   describe is a ball. Some attributes of a ball maybe it's 

   - radius
   - position (x,y-location)
   - color

   Write a class that uses those attributes. Then add some methods
   called ``Draw``, ``Update``, and ``Reflect``. For now don't add
   anything to the methods. You can put the keyword ``pass`` in the
   method for Python to just execute no action.
