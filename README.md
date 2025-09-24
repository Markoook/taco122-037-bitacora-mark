# taco122-037-bitacora-mark
apuntes y proyects de electronica

## Clase 1
introduccion 
#### tarea
referentes generales 
referente literario Oscar Wilde
"La única manera de librarse de la tentación es caer en ella"

## Clase 2
#### tarea
```
String mensaje = "La única manera de librarse de la tentación es caer en ella";  // El texto que se repetirá
float ang = 0;     
float rot = 0;      

void setup() {
  size(600, 600);
  textSize(16);
  textAlign(CENTER, CENTER);
  fill(255);
}

void draw() {
  background(255,0,0);
  translate(height/2,width/2);
  rotate(rot);

  int i = 0; // índice de letra
  
  for (float a = 11; a < TWO_PI*4.55; a += 0.3) { // control de separación de letras
    float r = a/2 * a/2;
    float y = cos(a + ang) * r;
    float x = sin(a + ang) * r;

    char letra = mensaje.charAt(i % mensaje.length()); 
    text(letra, x, y); // dibuja la letra en la espiral

    i++;
  }

  ang += 0.02;
  rot += 0.00;
}
```
## Clase 3
### tarea
```
int ledPin=13;
int tiempoPunto=400;
int separador=400;
int tiempoRaya=1200;
int timeEspacio=2800;
int timeFin=5000;
void setup ()
{
  pinMode(ledPin,OUTPUT);
  Serial.begin(9600);
}
void loop (){
// de aqui en mas escribo la cita de oscarito
  L();
  A();
  ESP();
  U();
  N();
  I();
  C();
  A();
  ESP();
  M();
  A();
  N();
  E();
  R();
  A();
  ESP();
  D();
  E();
  ESP();
  L();
  I();
  B();
  E();
  R();
  A();
  R();
  S();
  E();
  ESP();
  D();
  E();
  ESP();
  L();
  A();
  ESP();
  T();
  E();
  N();
  T();
  A();
  C();
  I();
  O();
  N();
  ESP();
  E();
  S();
  ESP();
  C();
  E();
  D();
  E();
  R();
  ESP();
  A();
  N();
  T();
  E();
  ESP();
  E();
  L();
  L();
  A();
 fin();
}
void punto (){
  digitalWrite(ledPin,HIGH);
  Serial.println(".");
  
  delay(tiempoPunto);
  digitalWrite(ledPin,LOW);
  Serial.println(" ");
  delay(separador);
}
void raya(){
  digitalWrite(ledPin,HIGH);
  Serial.println("_");
  
  delay(tiempoRaya);
  digitalWrite(ledPin,LOW);
  Serial.println(" ");
  delay(separador);
}
void fin (){
  digitalWrite(ledPin,LOW);
  Serial.println("fin");
  
  delay(timeFin);
}
void A(){
  punto();
  raya();
}
        
void B(){
  raya();
  punto();
  punto();
  punto();
}
void C(){
  raya();
  punto();
  raya();
  punto();
}
void D(){
  raya();
  punto();
  punto();
}
void E (){
  punto();
}
void efe(){
  punto();
  punto();
  raya();
  punto();
}
void G(){
  raya();
  raya();
  punto();
}
void H(){
  punto();
  punto();
  punto();
  punto();
}
void I(){
  punto();
  punto();
}
void J(){
  punto();
  raya();
  raya();
  raya();
}
void K(){
  raya();
  punto();
  raya();
}
void L(){
  punto();
  raya();
  punto();
  punto();
}
void M(){
  raya();
  raya();
}
void N(){
  raya();
  punto();
}
void O(){
  raya();
  raya();
  raya();
}
void P(){
  punto();
  raya();
  raya();
  punto();
}
void Q(){
  raya();
  raya();
  punto();
  raya();
}
void R(){
  punto();
  raya();
  punto();
}
void S(){
  punto();
  punto();
  punto();
}
void T(){
  raya();
}
void U(){
  punto();
  punto();
  raya();
}
void V(){
  punto();
  punto();
  punto();
  raya();
}
void W(){
  punto();
  raya();
  raya();
}
void X(){
  raya();
  punto();
  punto();
  raya();
}
void Y(){
  raya();
  punto();
  raya();
  raya();
}
void Z(){
  raya();
  raya();
  punto();
  punto();
}
//segun mi amado internet el espacio entre palabras dura siente veces un punto
//dentro del mismo letra hay un punto de distancia entre rayas y puntos
//entre dos letras distintas hay tres
//entre palabras distintas la distancia es de siente
//y la raya son tres vces lo que dura un punto
void ESP(){
  digitalWrite(ledPin,LOW);
  Serial.println("esp");
  delay(timeEspacio);
}
```
# Clase ...
(ante lo tardio y mediocre de esta entrega me disculpo, no es mucho pero es trabajo honesto)
## Evaluacion 1 
### si me da tiempo la pretendo alterar...
```
#include <Wire.h>
#include <Adafruit_GFX.h>
#include <Adafruit_SSD1306.h>

#define ANCHO_PANTALLA 128
#define ALTO_PANTALLA 64


#define OLED_ADDR 0x3C  


Adafruit_SSD1306 pantallita(ANCHO_PANTALLA, ALTO_PANTALLA, &Wire);

int posicionVertical= 0;

void setup() {
  
  if(!pantallita.begin(SSD1306_SWITCHCAPVCC, OLED_ADDR)) {
    Serial.begin(9600);
    Serial.println(F("No se encontró pantalla SSD1306"));
    for(;;); 
  }

  
}

void loop() {
  posicionVertical++;

 pantallita.clearDisplay();             
  pantallita.setTextSize(1);            
  pantallita.setTextColor(SSD1306_WHITE);
  pantallita.setCursor(1, posicionVertical);          
  pantallita.println("La unica manera");     
  pantallita.display();                  

  pantallita.setTextSize(1);          
  pantallita.setTextColor(SSD1306_WHITE);
  pantallita.setCursor(1, posicionVertical+10);        
  pantallita.println("De liverarse de ");     
  pantallita.display();                  

  pantallita.setTextSize(1);           
  pantallita.setTextColor(SSD1306_WHITE);
  pantallita.setCursor(1, posicionVertical+20);        
  pantallita.println("la tentacion ");     
  pantallita.display();               
 
  pantallita.setTextSize(1);           
  pantallita.setTextColor(SSD1306_WHITE);
  pantallita.setCursor(1, posicionVertical+30);          
  pantallita.println("ceder ante ella");     
  pantallita.display();                  
  delay(300);

}
```
