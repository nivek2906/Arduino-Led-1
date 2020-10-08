# Arduino-Led-1
Octubre 8 del 2020 - Biomedica


int ledPin = 6;
boolean estadoLed = false;

void setup(){
Serial.begin(9600);
pinMode(ledPin, OUTPUT);
digitalWrite(ledPin,estadoLed);
pinMode(LED_BUILTIN, OUTPUT);}

void loop(){
digitalWrite(LED_BUILTIN, HIGH);  
delay(2000);                       
digitalWrite(LED_BUILTIN, LOW);    
delay(1000);                       

if (Serial.available()){
char Letra = Serial.read();
if (Letra== 'a'){
estadoLed= !estadoLed;}
digitalWrite(ledPin,estadoLed);}}
