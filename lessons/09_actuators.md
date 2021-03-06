## Learning
Actuators are components that do something in the physical world. They help
make our projects interesting. Actuators could be anything from LEDs to motors
to lasers (we have a small set of actuators in our kits). You should already
have experience with an LED from "hello world".

Some actuators are special and will require different code, but for many basic
actuators we connect them to one of the Arduino's pins. For actuators that can
only be turned "on or off", we can attach the actuator to any pin and use
the `digitalWrite()` function. For actuators that can accept many values, we
connect them to one of the PWM (!) pins and use the `analogWrite()` function.
Be sure to initialize the pin for writing with the `pinMode()` function in
the setup. It is also a good idea to initialize the pin to a known value in the
setup.

Keep in mind that you can only use values 0 to 255 when using `analogWrite()`.

It is often worth checking out the data sheet for an actuator if there is one
so that you can be well-informed about how to use it.

Example:
```
/**
 * THIS CODE DOES NOT HAVE A CIRCUIT! If you try and run this code,
 * it probably won't work. This is "abstract" code meant to compare and contrast
 * digital sensors and analog sensors. If you want to, you can try and
 * create your own circuit with some actuators, you can make this code work.
 */

#define DIGITAL_ACTUATOR_PIN 8
#define ANALOG_ACTUATOR_PIN 3

void setup() {
    pinMode(DIGITAL_ACTUATOR_PIN, OUTPUT);
    digitalWrite(DIGITAL_ACTUATOR_PIN, LOW);

    pinMode(ANALOG_ACTUATOR_PIN, OUTPUT);
    analogWrite(ANALOG_ACTUATOR_PIN, 0);
}

void loop() {
    digitalWrite(DIGITAL_ACTUATOR_PIN, HIGH);
    analogWrite(ANALOG_ACTUATOR_PIN, 100);
    delay(300);

    digitalWrite(DIGITAL_ACTUATOR_PIN, LOW);
    analogWrite(ANALOG_ACTUATOR_PIN, 30);
    delay(300);
}
```

## Challenges
1. Learn how to control LEDs using analog write. Write your own blink program
   that uses `analogWrite` to make the LED alternate between being dim and
   bright.
2. Learn how to use a servo motor.
3. Learn how to use the piezo buzzer to play tones.
4. `(Extra)` Pick another actuator you find interesting and learn about it.
