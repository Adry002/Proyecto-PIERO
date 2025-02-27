# Estudio de las "zonas muertas" y de las "zonas de saturacion"
Para determinar tanto las zonas muertas como las zonas de saturación se hará uso de un modelo llamado "Toma datos". Este modelo hace uso de un subsistema "PieroAdry_HW",compuesto a su vez por dos subsistemas más uno es el subsistema "Motores" ya presentado en el hito 1 y otro denominado "EncoderAdryVel"
## PieroAdrY_HW

![resumen1](https://github.com/user-attachments/assets/07489620-a7b0-4e96-ad7e-ac228b04d2eb)

## EncoderAdryVel

![resumen2](https://github.com/user-attachments/assets/9af5b01b-7586-4079-a0c4-749dd376ebb5)

## Toma datos

![resumen3](https://github.com/user-attachments/assets/5a296919-eb42-469b-9420-4c8a046352d8)

## Señal "Rampa" usada

![resumen4](https://github.com/user-attachments/assets/c0fc7727-0706-404a-b269-b94782d24968)

## Scope y tabla de datos obtenida
Como se puede obserbar en el scope al principio tiene un retraso en la respuesta, dos picos de saturación tanto por arriba como por abajo, y una pequeña inercia al finalizar la respuesta
![resumen5](https://github.com/user-attachments/assets/b5b4cceb-0145-4a16-8601-3c32af65cc6d)



Esto es una captura de una pequeña parte de la tabla de Datos obtenida ,para poder ver los 1001 datos del muestreo lo único que debes hacer es ir a la carpeta datos de este repositorio con el nombre "ZonaMuerta.mat" y ahí la encontrarás completa
![resumen6](https://github.com/user-attachments/assets/84b467f0-052c-46e7-b26c-6f4449cfe030)



# Control en Bucle Abierto
El control Bucle abierto hace uso de dos subsistemas "PieroAdry_HW" el cuál ya conocemos y "ControladroBA"
## ControladoBA
Para el controladorBA usaremos dos bloques llamados "Lookup with Linear Lagrange Interpolation" que usaremos tanto para la rueda derecha como izquierda. Para configurarlo correctamente se pincha en el bloque y le damos en el apartado "Edit table and breakpoints..." una vez dentro se irá introduciendo valores desde -255 hasta 255  de nuestra tabla "ZonaMuerta.mat". En este caso como se verá a continuación hemos cogido valores de 50 en 50.


![resumen7](https://github.com/user-attachments/assets/bde8a3ef-82fc-4771-96bf-d4f6287e23cc)

-Rueda Izquierda
![resumen8](https://github.com/user-attachments/assets/51eb0d9d-6378-4141-a768-e44e8e80bd11)



-Rueda Derecha
![resumen9](https://github.com/user-attachments/assets/19ed623a-50a0-4443-8cc9-9b0ececd8435)

# Extraer datos para la identificación a partir de un Pulso
Para extraer los datos de identificación se volverá ha hacer uso del modelo "Toma datos".Pero esta vez introduciremos una señal llamada "Pulso" 
## Toma datos
![resumen10](https://github.com/user-attachments/assets/7584bf8f-b374-4945-b8a2-8007c165d5f7)


## Señal "Pulso" usada
![resumen11](https://github.com/user-attachments/assets/a1fca16c-d491-4757-b603-c6f7877297c7)


## Scope y tabla de datos obtenida

![resumen12](https://github.com/user-attachments/assets/d6873c00-cefb-4ab1-8eca-48b8647d2c54)

Al igual que pasaba con la rampa esto es una captura de una pequeña parte de la tabla de Datos obtenida ,para poder ver los 1001 datos del muestreo lo único que debes hacer es ir a la carpeta datos de este repositorio con el nombre "Datos101.mat" y ahí la encontrarás completa


![resumen13](https://github.com/user-attachments/assets/ec28bbea-8eae-4afe-8892-9dc53e477156)


## Sistem identification
Importamos nuestros datos del tipo "Time-domain-signal" y procesamos la señal para eliminar el punto de inercia del final


![resumen14](https://github.com/user-attachments/assets/15fd2ba9-c94b-464d-bfd3-2f0ab58e8a88)

Vamos introduciendo valores de polos y ceros


![resumen15](https://github.com/user-attachments/assets/aa9d5fd6-c264-45ab-a45d-4b4a5ec94761)

![resumen16](https://github.com/user-attachments/assets/4d80366e-d6e1-4fba-b957-26c388286e67)

Comparamos y nos quedamos con la función de transferencia que tenga menor error

![resumen17](https://github.com/user-attachments/assets/5735adf4-77e2-41e8-a2d4-6387b527daaf)

Para finalmente obtener nuestras funciones de transferencia tanto de la rueda derecha como de la izquierda

![resumen18](https://github.com/user-attachments/assets/d8f68f42-a704-48ba-ac68-fca0d02344fc)

Función transferencia derecha, la podemos encontrar completa en la carpeta "Datos" de este repositorio con el nobre de "TFd10.mat"
![resumen19](https://github.com/user-attachments/assets/73f5b1f5-5d62-4610-be0f-5c18cd70f2a2)


Función transferencia izquierda, la podemos encontrar completa en la carpeta "Datos" de este repositorio con el nobre de "TFi10.mat"

![resumen20](https://github.com/user-attachments/assets/01f584d1-b1b6-44a6-9d82-1740c7dae13f)

# GEMELO DIGITAL
Por ultimo crearemos nuestro gemelo digital, hecho a partir de nuestras funciones de transferencias y se llamará "PieroAdry", nuestro gemelo digital ó PieroAdry como lo quieras llamar estara constituido por dos subsistemas el primero es el ya presentado "PieroAdry_HW" y el otro es uno nuevo llamado "PieroAdry_Model" que esta formado por nuestras funciones de transferencias

## PieroAdry

![resumen21](https://github.com/user-attachments/assets/baed964c-90f0-4b74-beff-204cecf608ab)

## PieroAdry_Model
![resumen22](https://github.com/user-attachments/assets/1ceab4d7-0f43-4fe8-bf68-00dc1c494fc5)

