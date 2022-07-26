# servo-motor-stepper---motor-brushless---motor
 1//servo motor//
   هو نوع من المحركات تستخدم للتطبيقات  التي تحتاج الي الدوران     مثل  مفاصل الروبوت   اجنحة الطائرات  مفاصل  الابواب 
      توجد  صور توضح  طريقة عمل   servo-motor   نرجو  مراجعتها     وهنا   في   الرابط circuit    المستخدمه لتحريك servo motor  
     وهنا  توجد  الدائرة  لتحريكه 
 
      https://www.tinkercad.com/things/kxyo69Vylkz
     
 2//stepper- motor

    هو  يستخدم   في  الآلات  الصغيره     مثل  الطابعه   وقاطع الليزر    وبعض  الروبوتات  

اهم  مميزاته  :    
يمكن  التحكم   في   عدد   وسرعة دوراته    وزاوية التوقف  بدقة  


يمكن  النظر  الي  الصور  المرفقة  وملاحظه    الدائوة المستخدمة   لتحريكه والموجوده  في  الرابط   
https://www.tinkercad.com/things/bNpK4U1AQFh
الكود  البرمجي  

Stepper_Motor
 * محرك محرك السائر لتحقيق الأمام والعكس
 */
void setup() {
  // put your setup code here, to run once:
  for (int i = 2; i < 6; i++) {
    pinMode(i, OUTPUT);
  }
}

void clockwise(int num)
{
  for (int count = 0; count < num; count++)
  {
    for (int i = 2; i < 6; i++)
    {
      digitalWrite(i, HIGH);
      delay(3);
      digitalWrite(i, LOW);
    }
  }
}

void anticlockwise(int num)
{
  for (int count = 0; count < num; count++)
  {
    for (int i = 5; i > 1; i--)
    {
      digitalWrite(i, HIGH);
      delay(3);
      digitalWrite(i, LOW);
    }
  }
}

void loop() {
  // put your main code here, to run repeatedly:
  clockwise(512);
  delay(10);
  anticlockwise(512);
}
