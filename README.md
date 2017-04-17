# Reaktionsspiel
//Hier beginnt der Code:
// Variabeln
unsigned long Zufallszahl;
int Punktestand;
int Highscore;
// Pinbelegung
const int Taster1=22; // Taster 1 hat Pin 22 usw.
const int Taster2=23; //const int bedeutet Wert kann nicht verändert werden
const int Taster3=24;
const int Taster4=25;
const int LED1=26;
const int LED2=27;
const int LED3=28;
const int LED4=29;

//Ausgangsstatus
int LED1status= LOW;
int LED2status= LOW;
int LED3status= LOW;
int LED4status= LOW;
int Taster1status; //Vorliegender Status
int Taster2status;
int Taster3status;
int Taster4status;
int letzterTasterstatus1= LOW;// der vorherige Status des Tasters
int letzterTasterstatus2= LOW;
int letzterTasterstatus3= LOW;
int letzterTasterstatus4= LOW;


void setup() {
  // put your setup code here, to run once:
pinMode(Taster1,INPUT); // Taster als eingebend festlegen
pinMode(Taster2,INPUT); 
pinMode(Taster3,INPUT); 
pinMode(Taster4,INPUT);
pinMode(LED1,OUTPUT); // LEDs werden als Ausgänge definiert
                      // Pin mit Anode verbinden
pinMode(LED2,OUTPUT); 
pinMode(LED3,OUTPUT); 
pinMode(LED4,OUTPUT); 
digitalWrite(LED1,LED1status); // Weise den LEDs ihren Status zu
digitalWrite(LED2,LED2status);
digitalWrite(LED3,LED3status);
digitalWrite(LED4,LED4status);
randomSeed(analogRead(0)); /* randomseed erzeugt lange Zahl und
analogRead von pin 0 (unbelegt!) erzeugt durch durch rauschen 
verursachte Spannungsschwankung zufälligen Startpunkt innerhalb dieser Zahl */


}

void loop() {
  // put your main code here, to run repeatedly:

Zufallszahl=random(5000);
switch (Zufallszahl%4){
  case 0: {digitalWrite(LED1,HIGH);
}
}
