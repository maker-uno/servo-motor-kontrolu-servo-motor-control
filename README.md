#include <Servo.h>  // Servo kütüphanesini projemize ekledik.
Servo servoM;  // Servo nesnemizi oluşturduk, ismini servoM yaptık.
int pos = 0;    // pos değişkenini oluşturup 0’a eşitledik.
void setup() {
  servoM.attach(9);  // Servoyu 9nolu pin’e bağladığımızı belirttik.
}
void loop() {
  for (pos = 0; pos <= 180; pos += 1) { // For döngüsü ile 0 ile 180 derece arası gitmesini sağladık.
                                        // her bir adımda 1 derece artacak şekilde ayarladık.
    servoM.write(pos);              // Servo açı değeri olarak belirlediğimiz pos değişkenini servoya yazdırdık.
    delay(15);                       // servonun hedeflenen açıya gidebilmesi için 15 ms bekleme ekledik.
  }
  for (pos = 180; pos >= 0; pos -= 1) { // for döngüsü ile 180 ile 0 derece arası gitmesini sağladık.
    servoM.write(pos);              // Servo açı değeri olan pos değişkenini servo’ya yazdırdık.
    delay(15);                       // Servonun açı değerine gidebilmesi için 15 ms. bekleme ekledik.
  }
}
