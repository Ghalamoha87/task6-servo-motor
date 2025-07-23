# 🤖 6-Servo Motor Control Project with Arduino

## Description
This project controls six servo motors using an Arduino board.  
Each servo moves from 0° to 180° and back, either in sequence or simultaneously.  
It’s ideal for robotics, mechanical arms, or animatronics.

---

## Objectives
- Control 6 servo motors using Arduino
- Learn how to use the Servo library
- Understand servo movement via software

---

## Components Used
- Arduino Uno
- 6x Servo Motors (SG90 or similar)
- Breadboard
- Jumper Wires
- (Optional) External 5V Power Supply

---

## preview 
<img width="1180" height="571" alt="image" src="https://github.com/user-attachments/assets/fc8fbbb0-bfbc-4811-97f8-2d30b542d0dd" />

---

## 💻 Code

```cpp
#include <Servo.h>

Servo myservo1, myservo2, myservo3, myservo4, myservo5, myservo6;

void setup() {
  myservo1.attach(3);
  myservo2.attach(4);
  myservo3.attach(5);
  myservo4.attach(6);
  myservo5.attach(7);
  myservo6.attach(8);
}

void loop() {
  for (int pos = 0; pos <= 180; pos++) {
    myservo1.write(pos);
    myservo2.write(pos);
    myservo3.write(pos);
    myservo4.write(pos);
    myservo5.write(pos);
    myservo6.write(pos);
    delay(15);
  }

  for (int pos = 180; pos >= 0; pos--) {
    myservo1.write(pos);
    myservo2.write(pos);
    myservo3.write(pos);
    myservo4.write(pos);
    myservo5.write(pos);
    myservo6.write(pos);
    delay(15);
  }
}
```

## Algorithm
```
Step-by-step logic of the servo control:

Initialize 6 Servo objects

Attach each servo to a unique digital pin

In the main loop:

Move all servos from 0° → 180° with small delay

Then move them from 180° → 0° again


```
