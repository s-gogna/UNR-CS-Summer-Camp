## Learning
Sometimes, we want our program to make a choice between several actions. We can
accomplish this with an `else if`. `else if` works like an extra `if`. You
can follow an `if` with as many `else if`s as you'd like. When you are done
adding `else if`s, you can end the chain with an `else` if you'd like. Once
the condition for any of the `if`s is met, only that code block will execute
and the rest will be skipped.

Example:
```
/**
 * This example prints something different based on if a number is a multiple
 * of 3, 5, both, or neither.
 */

int g_number = 0;

void setup() {
    Serial.begin(9600);
}

void loop() {
    if (g_number % 3 == 0 && g_number % 5 == 0) {
        Serial.println("wubba lubba dub dub!");
    } else if (g_number % 3 == 0) {
        Serial.println("fizz");
    } else if (g_number % 5 == 0) {
        Serial.println("buzz");
    } else {
        Serial.println(".");
    }

    g_number += 1;
}
```

## Challenges
1. Write a simple program that tests a variable "grade" using an
   "if - else if - else" chain and prints out if the grade is an
   A, B, C, D, or F.
2. Write a program that says that a number is "good" if the number is between
   2 and 6, that the number is bad if it is between 12 and 14, and says nothing
   otherwise. (Yes this is a repeat, but you can do it in a better way now.)
3. Write a program that stores a number in a variable. The program should
   control 3 LEDs. The program should turn on a number of LEDs equal to the
   number held by the variable. If the number is greater than 3, just turn
   all of the LEDs on.
4. `(Extra)` Make one up!
