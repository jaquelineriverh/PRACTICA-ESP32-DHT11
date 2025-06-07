# PRACTICA-ESP32-DHT11
ESTE REPOSITORIO MUESTRA COMO PROGRAMAR UNA ESP32 CON SENSOR DE DHT11
## INTRODUCCION

### DESCRIPCION

La Esp32 la utilizamos en un entorno de adquision de datos, lo cual en esta practica ocuparemos un sensor (DTH11) para adquirir temperatura y humedad del entorno; Cabe aclarar que esta practica se usara un simulador llamado WOKWI.

## MATERIAL NECESARIO

Para realizar esta practica necesitas lo siguiente:

-[WOKWI](https://wokwi.com/)

-Tarjeta ESP 32

-Sensor DHT11

## INSTRUCCIONES

### Requisitos previos

Para poder usar este repositorio necesitas entrar a la plataforma [WOKWI](https://wokwi.com/)

### Instrucciones de preparación de entorno

1.Abrir la terminal de programación y colocar la siguente programación:

```
#include "DHTesp.h"

const int DHT_PIN = 15;
DHTesp dhtSensor;


void setup() {

  Serial.begin(115200);
  dhtSensor.setup(DHT_PIN, DHTesp::DHT22);
}

void loop() {

  TempAndHumidity  data = dhtSensor.getTempAndHumidity();
  Serial.println("Temp: " + String(data.temperature, 1) + "°C");
  Serial.println("Humidity: " + String(data.humidity, 1) + "%");
  Serial.println("---");
  delay(1000);
}
```


2.Instalar la libreria de DHT sensor library for ESPx como se muestra en la siguente imagen


![](https://github.com/jaquelineriverh/PRACTICA-ESP32-DHT11/blob/main/DHT.jpg)



3.Hacer la conexion de DHT11 con la ESP32 como se muestra en la siguente imagen.

![](https://github.com/jaquelineriverh/PRACTICA-ESP32-DHT11/blob/main/CONEXION%20DE%20DHT11.png)


### Instrucciónes de operación
1.Iniciar simulador.

2.Visualizar los datos en el monitor serial.

3.Colocar la temperatura y humedad dando doble click al sensor DHT11

## Resultados

Cuando haya funcionado, verás los valores dentro del monitor serial como se muestra en la siguente imagen.


![]()





