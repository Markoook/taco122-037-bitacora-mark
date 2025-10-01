# Clase 03

## Sintesis de esta clase
- Exploraron Arduino.
- Exploraron funcion de subir imagenes.
- No tengo material de clase ya que no contaba con medio para la clase.
- Ttrabajo desde casa lo visto en clase.

## Encargos de la class
1. Escribir el texto elejido en morse.
### Entrega.
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
