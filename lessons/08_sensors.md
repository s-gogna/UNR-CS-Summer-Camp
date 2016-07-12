## Learning
Programs can be kind of boring if they can't take input from the outside
world. This is why we use sensors! We won't be able to go over all of
the sensors we will use here.

Some sensors are special and will require different code, but for many basic
sensors we connect them to one of the Arduino's pins. For sensors that can
only register "on or off", we can attach the sensor to any pin and use
the `digitalRead()` function. For sensors that can give many values, we must
connect them to one of the A0-A5 pins and use the `analogRead()` function.
Be sure to initialize the pin for reading with the `pinMode()` function in
the setup.

It is often worth checking out the data sheet for a sensor if there is one
so that you can be well-informed about how to use it.

Example:
```
#define DIGITAL_SENSOR_PIN 8
#define ANALOG_SENSOR_PIN A0

void setup() {
    Serial.begin(9600);
    pinMode(DIGITAL_SENSOR_PIN, INPUT);
    pinMode(ANALOG_SENSOR_PIN, INPUT);
}

void loop() {
    bool digital_sensor_reading = digitalRead(DIGITAL_SENSOR_PIN);
    int analog_sensor_reading = analogRead(ANALOG_SENSOR_PIN);

    if (digital_sensor_reading == true) {
        Serial.println("Digital sensor activated.");
    } else {
        Serial.println("Digital sensor inactive.");
    }

    Serial.print("Analog sensor reading: ");
    Serial.println(analog_sensor_reading);

    delay(300);
}
```

## Challenges
1. Learn to use a button in a program.
2. Learn to use a light sensor in a program.
3. Learn to use a piezo buzzer as a sensor in a program.
4. `(Extra)` Pick another sensor you find interesting and learn about it.