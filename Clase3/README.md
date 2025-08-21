# Clase 03 / 21.08.2025
## Resumen
Comenzamos la clase con un peueño recordatorio y resolución de preguntas sobre la utilización de Github, en su mayoría son cosas que ya tengo aprendidas deste andes ya que no es mi primera vez en Github.
Principalente recordamos como crear carpetas, archivos README y pegar fotografías en estos últimos.

La siguiente parte de la clase se trató principalmente de exploraciones primarias con ARDUINO, cómo yo no traje el dispositivo, utilizaré [Tinker Card](https://www.tinkercad.com/things/1jfkEjWRtGt/editel), una página web para poder hacer circuitos de forma virtual.

![Tinkercad](ImagenesClase03/TinKerCad.png)

Antes de comenzar con el codigo de ARDUINO, Maty explicó sobre el paradigma entre lo análogo y lo digital. 
El universo digital es conocido como el universo "discrteto", donde solo existe el estado binario cómo on/off, 1-0, High/Low.
Por otra parte, el Universo análogo o "Continuo" son gradientes, existen maticez complejos, ejemplo es que entre 0 y 1 existe infinitos números decimales.

### Arduino experimentación Básica

Ya comenzando con los ejercicios de hoy, Maty enseña a realizar un blink con el Led integrado de la targeta en forma manual. 
El codigo utilizado es:
```cpp
//Primer Ejercicio 21.08.2025
int ledPin = 13;
//Aqui combertimos el pin en una varieble que puedo 
//cambiar siempre que quieras
int tiempoOn = 100;
int tiempoOff = 100;
//Aquí convertimos el tiempo el delay como variables igual que el 
//Pin

void setup()
{
  pinMode (ledPin,OUTPUT); 
  //El pinMode define que hacen el Pin nombrado
  //si es output o input
  Serial.begin (9600);
    //9600 es un baudio, número de datos por segundo
}

void loop()
{
  digitalWrite (ledPin, HIGH);
  //"digitalWrite" se utiliza para ordenar el quehacer del pin 
  //en comportamiento digital, o séa 1 o 0
  Serial.println ("Prendio");
  //Serial.println es para que el monitor serial nos diga
  //que está sucediendo en nuestro código.
  delay (tiempoOn);
  //Paralizar el código en milisegundos
  
  digitalWrite (ledPin, LOW);
  Serial.println ("Apagao"); 
  delay (tiempoOff);
}
```
Esto es materia que ya he revisado en años anteriores con la profesora Mónica Bate en Taller Instruental el año 2023 y Taller Central 1-2 el año 2024, pero estos ejercicios me sirven para refrescar la memoria y comenzar a imaginar que haré respecto a obra.

El siguiente paso del ejercicio de hoy será escribir la letra A en Morse utilizando principalmente las ordenes "int" y "digitalWrite".

```cpp
//Hablar en Morce Ejercicio DOS 21.08.2025
int ledPin = 13;
//Siempre es el pin 13 si queremos utilizar el 
//Led adjunto a la placa
int tiempoPunto = 1000;
int separador = 500;
int tiempoRaya = 2000;
int finCaracter = 500;
//Hay 4 tiempos, el encendido del punto y raya
//El separador entre raya y punto y el fin del caracter
void setup()
{
  pinMode (ledPin,OUTPUT); 
  
  Serial.begin (9600);
    
}

void loop()
{
  digitalWrite (ledPin, HIGH);
  Serial.println ("Punto");
  delay (tiempoPunto);

  digitalWrite (ledPin, LOW);
  Serial.println ("separador"); 
  delay (separador);
  
  digitalWrite (ledPin, HIGH);
  Serial.println ("Raya");
  delay (tiempoRaya);
  
  digitalWrite (ledPin, LOW);
  Serial.println ("finCaracter"); 
  delay (separador);
}
```

Para agilizar acciones repetitiva podemos utilizar el termino "void x", donde una serie de acciones pueden reducirse a una sola indicación en el "void loop".

## Encargo 3

Escribir con Morse los texto escogido en la Clase 01 con la luz adjunta al Arduino.
