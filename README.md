# LDR-with-Servo-motor

#include <Servo.h>                      
Servo servo_motor_1;

int LDR = A0;

void setup()
{
  pinMode(8,OUTPUT);
  Serial.begin(9600);
  servo_motor_1.attach(8);
}

void loop(){
  int light = analogRead(A0);
  Serial.println(light);
  if(light>600){
    servo_motor_1.write(0);}
  else if (light<600){
  servo_motor_1.write(90);
  }
}
