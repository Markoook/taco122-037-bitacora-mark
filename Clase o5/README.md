# Clase 05
No traje la pantalla OLED porque estaba agotada pero un compañero me compartió la suya para los ejercicios practicos.
## Sintesis de la clase:
- Aprendimos sobre los array y ciclos for.
- Usamos biblioteca/libreria para la pantalla.
# Encargos de la class:
1. Usar la pantalla OLED (en mi caso usé el simulador) para mostrar una oracion o frase, utilicé la misma cita de siempres.
   (Me atrasé con la entrega de este encargo pero mas vale tarde que nunca)
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
