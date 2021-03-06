## Learning
Programs become really useful when we can have them do things like math for us.
The basic math operations you should learn right away are:

```
+    Basic addition.

-    Basic subtraction.

*    Basic multiplication.

/    Division. This can get a little tricky. When used with float type
	 variables, we get a float type result (Ex: 5.0 / 2.0 = 2.5); with int
	 types, we get the integer division result, which discards the
	 fractional part (Ex: 5 / 2 = 2).

%    Modulo. Gives us the remainder part of an integer division. Remember
	 long division? If 5 / 2 = 2 R 1, then 5 % 2 = 1.

++   This means "increment by 1". Ex:
     '''
       sheep_count++; // sheep_count is now 1 larger
     '''
     There is also '--'.

+=   Increment by the given amount. Ex:
	 '''
	   sheep_count += 5; // sheep_count is now 5 larger
	 '''
	 There is also '-=', '*=', '/=', and '%='.

()   Basic parentheses.
```

float or int? We should also be aware of what types of numbers we are working
with. With variables, it is easy because we had to state the type. With
literals, we have to be more careful. '1' is an int type, but '1.0' is a float
type, for example. Adding the decimal point ('.') automatically makes a number
a float.

Challenges
----------
1. Write a program that stores the result of a math expression in a variable.
   It could be '2 + 2', or something more creative like '2 + 2 * 48 / 2'.
   Have your program print out the result. Do the math by hand to make sure
   your program gets it right.

2. Write a program that stores the result of a math expression using variables
   in another variable.

3. Write a program that uses one of the '+=' kind of operators. Use it 3 times,
   printing the variable's value after each usage of a '+=' kind of operator.

4. `(Extra)` Write a program that can solve for the c in a^2 + b^2 = c^2 when
   a and b are known. Note that in C/C++, '^' is not the "power" operator,
   you might need to do some Google Fu to find out how to compute powers of
   numbers or how to get the square root of a number (although you should
   do as much algebra as you can by hand first).
