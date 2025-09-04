# Clase 05 / 04.09.2025

Para comenzar la clase de hoy Mati nos mostró 

```cpp
//Array prmite crear varias variables del mismo tipo (numeros, pines, etc) y
//optimizar espacio.
int numeroslost [ ] = {4, 8, 16, 23, 42};

void setup() {
  Serial.begin(9600);
  
  //Serial.println(numeroslost[0]);  
  //Serial.println(numeroslost[1]);
  //Serial.println(numeroslost[2]);
  //Serial.println(numeroslost[3]);  
  //Serial.println(numeroslost[4]);
  //Serial.println(numeroslost[5]);
  
  Serial.println("Hola soy un ciclo for"]);

  //Para evitar el escribir cada uno podemos usar ciclo for
  //El ciclo for es utilizado para repetir un mismo proceso de forma automatizada
  //para declarar el ciclo debemos tener claro:
  //Donde inicia = 0 = Variable local
  //Donde termina = 5 = condición de salida
  //Còmo Varia = de 1 en 1 = i++

  for (int i = 0; i <= 5; i++ ) {

    Serial.println(numeroslost[i]);

  }

  Serial.println("Adios, ya no soy un ciclo for"]);
}
void loop() {

}
```
```cpp

int numeroslost [ ] = {4, 8, 16, 23, 42};

String lineasPoemas [ ] = 
 {
  "Señor",
  "La jaula se ha vuelto pájaro",
  "y se ha volado",
  "y mi corazón está loco",
  "porque aúlla a la muerte",
  "y sonríe detrás del viento",
  "a mis delirios",
};


void setup() {
  Serial.begin(9600);

}

void loop() {
  Serial.println("Ahora un poema muy feliz");
//Este ciclo for muere cuando llegamos a 7, como son 6, se acaba
  for (int i = 0; i < 7; i++ ) {

    Serial.println(lineasPoemas [i]);
    delay (1000);

  }

}
```
## Pantalla en Arduino
Ya experimentando esto, comenzaremos a utilizar la pantalla para el día de hoy.
Una pantalla es un sistema gráfico que transmite información.
Hay diferentes tipos de pantalla, LCD Oled, la mia es de 128 x 64
Existen diferentes protocolos y puertos, como el USB, el bluethoot. Esta pantalla utiliza el i2c, es común.
Además existe un controlador para utilizaqr los diferentes led que existen en la pantalla, en mi caos es SSH1106.

Necesitamos 4 cables pata el i2c.
un ground (tierra), VCC (voltaje), SCL (clock) y SDA (data).

En los pines Analógicos del arduino uno podemos utilizar los pins "A4" (sda) y "A5" (scl).

Para aprender a utilizar esta pantalla necesitamos una biblioteca particular de arduinos (Limor Fried, fundadora de Adafruit y el LILYpad)
En mi caso, al estr utilizando una pantalla diferente al resto, debo utilizar también otro controlador, busque en los tutoriales que sube 
