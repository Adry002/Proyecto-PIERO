# Control continuo (Bucle cerrado)
Nuestro Control continuo esta formado por dos subsisemas ,el ya presentado en el Hito 2 "PieroAdry" ó como esta de moda ahora 
llamarlo "Gemelo digital" y por un nuevo subsistema "ControladorBC"
![resumen1](https://github.com/user-attachments/assets/f41ecc90-3b24-4e49-b0e2-50f2cc612b09)


## ControladoBC
Formado, como se puede ver en la imagen, por dos bloques "PID controller" los cuales debemos de configurar corrrectamente
entrando en el propio bloque y dandole al boton tune. Una vez dentro del tune solo debemos ir moviendo las guias superiores hasta 
obtener los valores que se buscaban
![resumen2](https://github.com/user-attachments/assets/324ab45f-5372-4c29-af8e-2782988889c8)


Bloque "PID controller" sintonizado para la rueda izquierda
![resumen3](https://github.com/user-attachments/assets/815d2c8e-17f3-498b-ae7f-6892728a7d9f)



Bloque "PID controller" sintonizado para la rueda derecha
![resumen4](https://github.com/user-attachments/assets/683eca3e-cb0b-4fae-b823-f250eaadbb7c)



## Video corrección de trayectoria

https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/3d2e7d8c-4bfe-4461-8774-259f5c0f9ffe

# Test Cinemático
A continución mostraremos el modelo test cinemático formado por 4 subsistemas que son "MCI" "MCD" "Odometría" y "PieroControladoS".Este modelo lo usaremos para hacer un circulo en 10 segundos.
![resumen5](https://github.com/user-attachments/assets/466ec182-4d8f-4474-aee9-fb50a150875a)


## MCI
![resumen6](https://github.com/user-attachments/assets/1f4f518a-31c8-4b22-b405-d890475596eb)


## MCD
![resumen7](https://github.com/user-attachments/assets/4e25b138-93b6-419b-b196-99600ec39345)


## PieroControladoS
Es básicamente nuestro Control continuo (Bucle cerrado)
![resumen8](https://github.com/user-attachments/assets/fc06159d-4767-42e6-9126-02bda80218f9)


## Odometría
La usaremos para ver en una gráfica XY la trayectoria teórica que debería hacer nuestro Piero
![resumen9](https://github.com/user-attachments/assets/f473d5a3-9577-44d8-9830-4c9017ab12a9)


Gráfica XY trayectoria circulo en 10 segundos
![resumen10](https://github.com/user-attachments/assets/297949df-0bd7-46d5-96bd-40253b8335df)


## Video realizando el circulo en 10 segundos
Mi Piero hace el circulo en 10 segundos pero no se detiene. Para que se detenga debemos introducirle un swicht y ponerle una condición


https://github.com/user-attachments/assets/710a4b7f-31f9-4f7f-962a-96212df8bf42



