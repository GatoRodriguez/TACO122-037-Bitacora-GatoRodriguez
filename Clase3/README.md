# Clase 3
## Resumen
Comenzamos la clase con un peueño recordatorio y resolución de preguntas sobre la utilización de Github, en su mayoría son cosas que ya tengo aprendidas deste andes ya que no es mi primera vez en Github.
Principalente recordamos como crear carpetas, archivos README y pegar fotografías en estos últimos.

La siguiente parte de la clase se trató principalmente de exploraciones primarias con ARDUINO, cómo yo no traje el dispositivo, utilizaré [Tinker Card](https://www.tinkercad.com/things/1jfkEjWRtGt/editel), una página web para poder hacer circuitos de forma virtual.

![Tinkercad](ImagenesClase03/TinKerCad.png)

Antes de comenzar con el codigo de ARDUINO, Maty explicó sobre el paradigma entre lo análogo y lo digital. 
El universo digital es conocido como el universo "discrteto", donde solo existe el estado binario cómo on/off, 1-0, High/Low.
Por otra parte, el Universo análogo o "Continuo" son gradientes, existen maticez complejos, ejemplo es que entre 0 y 1 existe infinitos números decimales.

## Arduino experimentación Básica

Ya comenzando con los ejercicios de hoy, Maty enseña a realizar un blink con el Led integrado de la targeta en forma manual. 
El codigo utilizado es:
```cpp
//Primer Ejercicio 21.08.2025 Blink manual
int ledPin = 13;
//Aqui combertimos el pin en una varieble que puedo 
//cambiar siempre que quieras
void setup()
{
  pinMode (ledPin,OUTPUT); 
  //El pinMode define que hacen el Pin nombrado
  //si es output o input
}

void loop()
{
  //"digitalWrite" se utiliza para ordenar el quehacer del pin 
  //en comportamiento digital, o séa 1 o 0
  digitalWrite (ledPin, HIGH);
  delay (1000);
    //Paralizar el código en milisegundos
  digitalWrite (ledPin, LOW);
  delay (1000);
}
```
Esto es materia que ya he revisado en años anteriores con la profesora Mónica Bate en Taller Instruental el año 2023 y Taller Central 1-2 el año 2024, pero estos ejercicios me sirven para refrescar la memoria y comenzar a imaginar que haré respecto a obra.
En lo personal, me interesa la posibilidad en que el código aparezca en la obra, que no se oculten necesariamente, esto ya que el lenguaje de programación al caracterizarse por ser ordenado y no intuitivo de leer para las peronas que no conocen en profundidad sobre computación. Junto a esto, exponer el código permite es como hacerle la autopsia a un archivo.
