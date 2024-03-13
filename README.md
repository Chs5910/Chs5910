#include <Servo.h>// Import library

Servo myservo;
int led = 13;

Servo myservo1;
int led1 = 12;

void setup()
{
pinMode(led, OUTPUT);
myservo.attach(9); // Attach servo to pin 9

pinMode(led1, OUTPUT);
myservo1.attach(10); // Attach servo to pin 10
}

void loop()
{
// Rotate Servo 1 by 90 degrees
myservo.write(90);
delay(10);

digitalWrite(led, HIGH);
delay(8000);
digitalWrite(led, LOW);

myservo.write(0);
delay(1000);

// Rotate Servo 2 by 90 degrees
myservo1.write(90);
delay(10);

digitalWrite(led1, HIGH);
delay(8000);
digitalWrite(led1, LOW);

myservo1.write(0);
delay(1000);
}
