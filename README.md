# Fire Alarm Using Arduino

## Project Image

(Project image will be added soon.)

## Project Overview

This project demonstrates how an Arduino can detect fire and activate an alarm system.

The system uses a flame sensor to detect the presence of fire. When fire is detected, the Arduino activates a buzzer and an LED to alert nearby people.

## Learning Objectives

- Understand how flame sensors work.
- Learn how Arduino processes sensor inputs.
- Build a basic safety and alert system.
- Explore real-world fire detection technology.

## Components Required

| Component | Quantity |
|------------|----------|
| Arduino UNO | 1 |
| Flame Sensor | 1 |
| LED | 1 |
| Buzzer | 1 |
| 220Ω Resistor | 1 |
| Breadboard | 1 |
| Jumper Wires | As Required |

## Working Principle

1. The flame sensor continuously monitors the surroundings.
2. Arduino reads the sensor value.
3. When fire is detected, the sensor sends a signal.
4. Arduino turns ON the buzzer and LED.
5. The alarm remains active until the fire is removed.

## Circuit Connections

- Flame Sensor OUT → Digital Pin 2
- LED Positive → Digital Pin 13
- LED Negative → GND
- Buzzer Positive → Digital Pin 8
- Buzzer Negative → GND

## Arduino Code

```cpp
int flamePin = 2;
int ledPin = 13;
int buzzerPin = 8;

void setup() {
  pinMode(flamePin, INPUT);
  pinMode(ledPin, OUTPUT);
  pinMode(buzzerPin, OUTPUT);
}

void loop() {
  int flame = digitalRead(flamePin);

  if (flame == LOW) {
    digitalWrite(ledPin, HIGH);
    digitalWrite(buzzerPin, HIGH);
  }
  else {
    digitalWrite(ledPin, LOW);
    digitalWrite(buzzerPin, LOW);
  }
}
```

## Applications

- Home safety systems
- School laboratory safety
- Industrial monitoring
- Fire detection systems

## Future Improvements

- Send mobile notifications.
- Add GSM alerts.
- Connect to IoT dashboards.
- Add smoke detection.

## Author

AnanyaLabs
