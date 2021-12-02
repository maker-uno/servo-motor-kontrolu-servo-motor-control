#include <Servo.h>

// Potansiyometrenin bağlı olduğu analog pini tanımlıyoruz. int potpin = A0;

// servo isimli bir nesne oluşturuyoruz.

Servo servo;

int val = 0;

void setup()

{

servo.attach (9); }

void loop()

{ val= analogRead (potpin); val map(val, 0, 1023, 0, 179); servo.write(val);

delay(15);

}
