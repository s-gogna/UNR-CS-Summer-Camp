BUTTON
======

Description
-----------
Buttons are the most basic sensor. They only provide 2 output values: high or
low. You can read from them with digital or analog pins.

Pin-out
-------

out           out
   \         /
    \-------/
     |     |
     |  O  |
     |     |
    /-------\
   /         \
 in           in

The pins across from each other are tied together (in is directly connected
to in), the pins on the same side of the package are connected through the
button. The signal is passed through when the button is pressed.

Notes
-----
It is good to mention to the motivated student that you don't _have_ to connect
the button to a program. You can actually use it to pass signal through a
circuit and avoid writing some code. Sometimes, an elegant circuit makes for
the most elegant code.
