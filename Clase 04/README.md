# Clase 04
## Aprendimos sobre:
- Protoboard.
- Potenciometro.
(incerto imagen)


## Encargos de la class 
1. Traer pantalla.
2. Usar if para alterar un led con el potenciometro.

```

int ledPin = 9;
int potPin = A0; 
int valorPot = 0;
int potMapeado = 0;
int intensidadLuz = 0;

void setup() 
{
  pinMode(ledPin, OUTPUT);
  Serial.begin(9600);  
}

void loop() 
{
  valorPot = analogRead(potPin);
  potMapeado = map(valorPot, 0, 1023, 0, 255);
  intensidadLuz = potMapeado;
 
  analogWrite(ledPin, intensidadLuz);

  if (intensidadLuz>220){
    analogWrite(ledPin,0);
    delay(500);
    analogWrite(ledPin,intensidadLuz);
    delay(500);
  }
  Serial.println(intensidadLuz);
}
```
