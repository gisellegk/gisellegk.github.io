---
published: true
layout: post
project: mini-testbot
title: Mini Test Bot motors!
---
So we finished wiring the mini test bot's two motors. We plan on making the base interchangeable, so our first base is a simple tank drive with two motors and encoders.
<!--more-->
There is space for four victors on the electrical board, though we've only mounted 2 of them. We are using a DB25 connector between the main part and base with a bunch of pins disconnected right now but in the future we can connect up to two more motors and encoders.

I wrote some simple software to test the motors using an arduino rather than a roboRIO. Based on example Serial and Servo code from Arduino's website.

```
#include <Servo.h>

Servo myservo;
Servo myservo2;
int incomingByte = 0;

void setup() {
  myservo.attach(9, 870, 2140);  //victor 888
  myservo2.attach(10, 870, 2140);
  Serial.begin(9600);
}
void loop() {
  if (Serial.available() > 0) {
    incomingByte = Serial.read();
    Serial.print("I received: ");
    Serial.println(incomingByte, DEC);
  }

  if (incomingByte == 119){
    myservo.write(180);
    myservo2.write(0);
    delay(15);
  }
  else if (incomingByte == 97){
    myservo.write(180);
    myservo2.write(90);
    delay(15);
  }
  else if (incomingByte == 115){
    myservo.write(0);
    myservo2.write(180);
    delay(15);
  }
  else if (incomingByte == 100){
    myservo.write(90);
    myservo2.write(0);
    delay(15);
  }
  else{
    myservo.write(90);
    myservo2.write(90);
    delay(15);
  }
}
```
