---
layout: project
type: project
image: images/arduino uno.jpg
title: Arduino Fire Alarm System
permalink: projects/arduino
# All dates must be YYYY-MM-DD format!
date: 2018-08-20
labels:
  - Robotics
  - Arduino
  - C++
summary: My partner and I designed a fire alarm system that allows users to trigger a buzzer and an LED indicating a fire is present with a push button.
---

<div class="Arduino Circuit">
  <img class="ui image" src="../images/arduino circuit.png">
</div>

What is an Arduino UNO? An Arduino UNO is a programmable microcontroller circuit board. The Arduino code syntax is similar with C++ and the Arduino IDE is used to connect and program the UNO board with your computer.

For the project, at first, my partner and I attached a flame sensor for temperature detecting. However, we encountered problems with the testing of the circuit board. My partner and I decided to replace the sensor with a normal switch that will serve as a sensor or fire alarm switch. Turning on the switch will trigger a positive voltage across the circuit board and while the switch is on, the buzzer will begin to make a synchronous noise. At the same time, the Arduino IDE console will also output a "Flame Detected!" message if the switch is turned on and "No flame detected!" if the switch is turned off.

Here is the code overview:

```c++
int buzzer = 8;
int LED = 7;
int flame_sensor = 4;
int flame_detected;

void setup()
{
  Serial.begin(9600);
  pinMode(buzzer, OUTPUT);
  pinMode(LED, OUTPUT);
  pinMode(flame_sensor, INPUT);
}
void loop()
{
  flame_detected = digitalRead(flame_sensor);
  if (flame_detected == 1)
  {
    Serial.println("Flame detected! Please take proper action.");
    digitalWrite(buzzer, HIGH);
    tone(buzzer, 1000, 500);
    digitalWrite(LED, HIGH);
    delay(200);
    digitalWrite(LED, LOW);
    delay(200);
  }
  else
  {
    Serial.println("No flame detected! Temperature is normal.");
    digitalWrite(buzzer, LOW);
    digitalWrite(LED, LOW);
  }
 delay(1000);
}
```
