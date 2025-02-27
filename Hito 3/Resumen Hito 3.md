# Control continuo (Bucle cerrado)
Nuestro Control continuo esta formado por dos subsisemas ,el ya presentado en el Hito 2 "PieroAdry" ó como esta de moda ahora 
llamarlo "Gemelo digital" y por un nuevo subsistema "ControladorBC"

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/2b2fbf3d-7a74-4f84-8d5f-ad903b5c65e0)

## ControladoBC
Formado, como se puede ver en la imagen, por dos bloques "PID controller" los cuales debemos de configurar corrrectamente
entrando en el propio bloque y dandole al boton tune. Una vez dentro del tune solo debemos ir moviendo las guias superiores hasta 
obtener los valores que se buscaban

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/0d59ca75-ffbb-46fd-b745-550592a9941d)

Bloque "PID controller" sintonizado para la rueda izquierda

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/43c2e7da-c189-4849-8d1c-ec3bfd3bb647)

Bloque "PID controller" sintonizado para la rueda derecha

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/ab5d255e-f1f4-411a-94ed-f4fbfb5355b8)

## Video corrección de trayectoria

https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/3d2e7d8c-4bfe-4461-8774-259f5c0f9ffe

# Test Cinemático
A continución mostraremos el modelo test cinemático formado por 4 subsistemas que son "MCI" "MCD" "Odometría" y "PieroControladoS".Este modelo lo usaremos para hacer un circulo en 10 segundos.

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/10841457-1d2f-41b9-a5b0-fa7978d55a2f)

## MCI

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/4fcb4bdb-a534-425e-a8ae-46c5c99743ac)

## MCD

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/18a5d34a-d7e3-42c5-9078-56bc14da3556)

## PieroControladoS
Es básicamente nuestro Control continuo (Bucle cerrado)

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/9cd6fa16-02d8-45b1-88a6-541c28ba8d2a)

## Odometría
La usaremos para ver en una gráfica XY la trayectoria teórica que debería hacer nuestro Piero

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/230122d6-9162-4d37-ad03-fb03daa806f0)

Gráfica XY trayectoria circulo en 10 segundos

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/2c2f101a-89d3-41c7-ab77-6999b35f5a1d)

## Video realizando el circulo en 10 segundos
Mi Piero hace el circulo en 10 segundos pero no se detiene. Para que se detenga debemos introducirle un swicht y ponerle una condición

https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/2cc6d4b9-3919-4834-ac9a-05849a7edd53
