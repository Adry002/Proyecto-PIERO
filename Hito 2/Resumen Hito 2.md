# Estudio de las "zonas muertas" y de las "zonas de saturacion"
Para determinar tanto las zonas muertas como las zonas de saturación se hará uso de un modelo llamado "Toma datos". Este modelo hace uso de un subsistema "PieroAdry_HW",compuesto a su vez por dos subsistemas más uno es el subsistema "Motores" ya presentado en el hito 1 y otro denominado "EncoderAdryVel"
## PieroAdrY_HW
![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/d17956ef-355a-4acf-968d-5f8863ba2a65)

## EncoderAdryVel
![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/d5f5c630-76b6-49c6-aad7-4e67f8ce2ae9)

## Toma datos
![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/5610a7fd-55dc-41bd-95a6-44479e205b69)

## Señal "Rampa" usada
![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/a9b79369-8f0d-4b8f-bbfa-1e6bcd8b7fd7)

## Scope y tabla de datos obtenida
Como se puede obserbar en el scope al principio tiene un retraso en la respuesta, dos picos de saturación tanto por arriba como por abajo, y una pequeña inercia al finalizar la respuesta

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/4bcb2ea2-a9fa-447e-8179-6b0a9af31270)

Esto es una captura de una pequeña parte de la tabla de Datos obtenida ,para poder ver los 1001 datos del muestreo lo único que debes hacer es ir a la carpeta datos de este repositorio con el nombre "ZonaMuerta.mat" y ahí la encontrarás completa

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/cbbd86bb-6c74-4d1a-9d79-2886c688e73f)

# Control en Bucle Abierto
El control Bucle abierto hace uso de dos subsistemas "PieroAdry_HW" el cuál ya conocemos y "ControladroBA"
## ControladoBA
Para el controladorBA usaremos dos bloques llamados "Lookup with Linear Lagrange Interpolation" que usaremos tanto para la rueda derecha como izquierda. Para configurarlo correctamente se pincha en el bloque y le damos en el apartado "Edit table and breakpoints..." una vez dentro se irá introduciendo valores desde -255 hasta 255  de nuestra tabla "ZonaMuerta.mat". En este caso como se verá a continuación hemos cogido valores de 50 en 50.

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/e03717fd-aa6f-4709-b84e-1c03c742ec36)

-Rueda Izquierda

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/af8f821e-da15-4a7e-8a21-b4cfcbf6a692)

-Rueda Derecha

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/9ad3b9dd-87fb-4a57-a0e0-2741e41051a3)
# Extraer datos para la identificación a partir de un Pulso
Para extraer los datos de identificación se volverá ha hacer uso del modelo "Toma datos".Pero esta vez introduciremos una señal llamada "Pulso" 
## Toma datos

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/34a898a1-87dd-443b-9164-8be2e6f6a5be)

## Señal "Pulso" usada

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/b376a255-b8bd-4540-b4c5-d8a3fbc2aef6)

## Scope y tabla de datos obtenida
![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/a51c6b32-3a3a-4cf8-abf5-656b2932d4dd)

Al igual que pasaba con la rampa esto es una captura de una pequeña parte de la tabla de Datos obtenida ,para poder ver los 1001 datos del muestreo lo único que debes hacer es ir a la carpeta datos de este repositorio con el nombre "Datos101.mat" y ahí la encontrarás completa

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/4bd761f7-9d33-460a-9e3e-911759d1e61f)


## Sistem identification
Importamos nuestros datos del tipo "Time-domain-signal" y procesamos la señal para eliminar el punto de inercia del final

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/f2ac56f6-b6a7-4af8-9b08-25f9500d89b7)

Vamos introduciendo valores de polos y ceros

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/364bde0c-6be6-40ad-980c-e30d56f7e148)

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/3069493f-172a-4429-ae43-b72269182bae)

Comparamos y nos quedamos con la función de transferencia que tenga menor error

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/fca8969c-8b09-4886-8780-6d15514b3be8)

Para finalmente obtener nuestras funciones de transferencia tanto de la rueda derecha como de la izquierda

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/78e68545-3046-4399-b8c2-de1aa5e0faa9)

Función transferencia derecha, la podemos encontrar completa en la carpeta "Datos" de este repositorio con el nobre de "TFd10.mat"

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/4267f673-8580-4506-8a23-defcd4fbdf3f)

Función transferencia izquierda, la podemos encontrar completa en la carpeta "Datos" de este repositorio con el nobre de "TFi10.mat"

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/7bb9dfef-296f-456d-b00e-5c807d01aa9c)

# GEMELO DIGITAL
Por ultimo crearemos nuestro gemelo digital, hecho a partir de nuestras funciones de transferencias y se llamará "PieroAdry", nuestro gemelo digital ó PieroAdry como lo quieras llamar estara constituido por dos subsistemas el primero es el ya presentado "PieroAdry_HW" y el otro es uno nuevo llamado "PieroAdry_Model" que esta formado por nuestras funciones de transferencias

## PieroAdry

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/732bfb06-cf33-4203-819d-7479613bc65f)

## PieroAdry_Model

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/6e4bc5aa-520a-49fb-852d-3869354f5cad)
