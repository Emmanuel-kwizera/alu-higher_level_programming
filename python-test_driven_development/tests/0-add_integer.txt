Using `add_integer` function:

Import `add_integer` from the `0-add_integer` module:

    >>> add_integer = __import__('0-add_integer').add_integer

Test cases:

Test with no arguments:

   >>> add_integer()
   Traceback (most recent call last):
   TypeError: add_integer() missing 1 required positional argument: 'a'

Test with one argument:

   >>> add_integer(1)
   99

Test with two integer arguments:

   >>> add_integer(3, 2)
   5

Test with a float and an integer:

   >>> add_integer(1.5, 3)
   4

   >>> add_integer(5, 0.0)
   5

Test with two floats:

   >>> add_integer(1.8, 2.3)
   3

Test with float overflow:

   >>> add_integer(float('inf'), float('inf'))
   Traceback (most recent call last):
   OverflowError: cannot convert float infinity to integer

   >>> add_integer(-float('inf'), -float('inf'))
   Traceback (most recent call last):
   OverflowError: cannot convert float infinity to integer

Test with float NaN:

   >>> add_integer(float('nan'), 3.1)
   Traceback (most recent call last):
   ValueError: cannot convert float NaN to integer

Test with non-integer or float arguments:

   >>> add_integer("This", 1)
   Traceback (most recent call last):
   TypeError: a must be an integer

Test with one integer and one non-integer argument:

   >>> add_integer(4, "Not")
   Traceback (most recent call last):
   TypeError: b must be an integer

   >>> add_integer((1, 4), 5)
   Traceback (most recent call last):
   TypeError: a must be an integer

Test with one float and one non-integer argument:

   >>> add_integer(4.6, "Not")
   Traceback (most recent call last):
   TypeError: b must be an integer

   >>> add_integer((1, 4), 5.3)
   Traceback (most recent call last):
   TypeError: a must be an integer

Test with two negative integers:

   >>> add_integer(-5, -3)
   -8

Test with two negative floats:

   >>> add_integer(-3.1, -2.9)
   -5

Test with one negative float and one negative integer:

   >>> add_integer(-7.1, -3)
   -10

Test with one positive and one negative argument:

   >>> add_integer(10, -5.2)
   5

Test with two zeros:

   >>> add_integer(0, 0.0)
   0
