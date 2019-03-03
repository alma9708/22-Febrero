int b1=3;
int b2=4;
int b3=5;
int rojo=7;
int azul=8;
int verde=9;
bool e1;
bool e2;
bool e3;
void setup() {
  // put your setup code here, to run once:
Serial.begin (9600); 
pinMode(b1, INPUT_PULLUP);
pinMode(b2, INPUT_PULLUP);
pinMode(b3, INPUT_PULLUP);
pinMode(rojo, OUTPUT);
pinMode(verde, OUTPUT);
pinMode(azul, OUTPUT);

}

void loop() {
  // put your main code here, to run repeatedly:
  e1=digitalRead(b1);
  e2=digitalRead(b2);
  e3=digitalRead(b3);
 
  if(e1 == 0 && e2 == 1 && e3 == 1){
    digitalWrite(rojo, HIGH);
    digitalWrite(azul, LOW);
    digitalWrite(verde, LOW);
  } 
  if(e1 == 1 && e2 == 0 && e3 == 1){
    digitalWrite(rojo, LOW);
    digitalWrite(azul, HIGH);
    digitalWrite(verde, LOW);
  }
  if(e1 == 1 && e2 == 1 && e3 == 0){
    digitalWrite(rojo, LOW);
    digitalWrite(azul, LOW);
    digitalWrite(verde, HIGH);
  }
