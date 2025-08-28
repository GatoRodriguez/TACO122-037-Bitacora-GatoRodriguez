# Clase 04 / 28.08.2025
## Resumen
## Arduino
```cpp
int ledPin = 7;
int potPin = A0; 
int intervalo = 1000;
int valorPot = 0;
int potMapeado = 0;
bool estadoLed = 0;

unsigned long tiempoActual = 0;
unsigned long tiempoAnterior = 0;

void setup() 
{
  pinMode (ledPin, OUTPUT);
  Serial.begin(9600);  
}

void loop ()
  {
  
  tiempoActual = millis();
  
  valorPot = analogRead(potPin);
  //aquí me faltan cosas
  
  if (tiempoActual - tiempoAnterior > intervalo) {
  estadoLed = !estadoLed;
  Serial.println("se cumplió el if");
  tiempoAnterior = tiempoActual;
   }
  digitalWrite(ledPin,estadoLed);
 }
```
