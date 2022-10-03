#include <Servo.h>

Servo myservo;  // create servo object to control a servo

int pos = 0;
void setup() {
  myservo.attach(9);  // attaches the servo on pin 9 to the servo object
  myservo.write(pos);
  delay(100);
}

void loop() {
for (pos = 0; pos< 180;pos+=5){
  myservo.write(pos);
  delay(20);
}
delay(50);
  for (pos = 180; pos>0;pos-=5){
  myservo.write(pos);
  delay(20);
  }
  delay(50);
}
