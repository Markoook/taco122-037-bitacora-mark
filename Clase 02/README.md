# Clase 02
## Sintesis de esta clase
- Niveles de programacion.
- Aprendimos algunos terminos de programacion.
- Processing.

## Encargos de la class
1. Usar processing para usar el texto del encargo y movimiento.

### Entrega.
1. Aquí
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
