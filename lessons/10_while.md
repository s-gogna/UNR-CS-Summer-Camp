## Learning
What do you do if you want your program to wait for something? The answer
is the "while" loop! Think of it like an "if" that starts over and repeats
until the condition is false. If the condition is false to begin with, the
loop code will never execute. Also keep in mind that there should be code
in the loop that updates the condition; if there isn't, the loop code
might just run forever and never exit!

Example:
```
#define BUTTON_PIN 8

void setup() {
    Serial.begin(9600);
    pinMode(BUTTON_PIN, INPUT);
}

void loop() {
    bool button_pressed = false;

    while (!button_pressed) {
        Serial.println("...waiting for the button to be pressed...");

        button_pressed = digitalRead(BUTTON_PIN);
        delay(300);
    }

    Serial.println("The button was pressed!");
}
```

## Challenges
1. Write a program that increments a number variable and then ends once the
   variable reaches a certain value. Use print statements to indicate the
   loop's progress.
2. Write a program that waits for a different type of sensor to produce
   a reading that is a certain value or in a certain range before the loop
   exits.
3. Write a program that has an infinite loop in it (of your own creation).
4. `(Extra)` Google "Fibonacci Sequence". Write a program that prints out
   each number of the sequence using an infinite while loop.
5. `(Extra)` Google "Collatz Conjecture". Write a program that carries out the
   computation of the sequence for some number that is stored in a variable
   at the start of "setup()".
