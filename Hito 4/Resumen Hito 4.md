# Cambio de variable Continua a discreta 
En este Hito 4 trabajaremos con variables discretas en vez de continuas para ello debemos de hacer  cambios en algunos subsistemas y 
a partir de estos cambios crear nuevos subsistemas. Este hito se podría decir que está compuesto por 4 partes:
# H41_1 metro
Para esta parte debemos de crear un subsistema que llamaremos "PieroContolado1mZ" compuesto por "PieroAdryZ" y "ControladoPos1mZ"
![resumen1](https://github.com/user-attachments/assets/9a975c5a-d29c-4593-88ae-dcfd0cfe751d)

## PieroContolado1mZ
![resumen2](https://github.com/user-attachments/assets/483cb51c-0487-498b-8f19-5c6064c8d6eb)


## PieroAdryZ
PieroAdryZ esta formado por el subsistema "PieroAdry" que hemos estado usando desde el Hito 1 y por uno nuevo "PieroAdry_modelZ"
que tiene un cambio, y es nada más y nada menos que las nuevas funcines de transferencia para los valores en discreta
![resumen3](https://github.com/user-attachments/assets/f4845abc-f30d-4f91-a741-62eba1f87e46)



Para  __PieroAdry_modelZ__ como he dicho hay que buscar sus nuevas funciones de transferencias, y la verdad es que es muy sencillo simplemente
tenemos realizar el mismo proceso que hicimos para buscar las funciones de tranferencia en continua
![resumen4](https://github.com/user-attachments/assets/4b467a11-94cc-44aa-88bd-b514f2a1c30e)



Una vez hemos comparado en el _Sistem identification_ cojemos la función con polos y ceros que tenga el menor error. 
Función de transferencia para la rueda derecha, como se ha dicho ya en varias ocasiones, esto es una captura de la función
de transferencia para verla completa simplemente en la carpeta "Datos" de este repositorio la encontraras como "TFdz21.mat"
![resumen5](https://github.com/user-attachments/assets/28a8455b-1cc0-408d-aa00-36358d6e9934)



captura de la función de transferencia  de la rueda izquierdapara verla completa simplemente en la carpeta "Datos" de
este repositorio la encontraras como "TFiz20.mat"
![resumen6](https://github.com/user-attachments/assets/1760f56d-8935-4f96-adc2-884cd8e1c594)

![resumen7](https://github.com/user-attachments/assets/f4323594-7d65-4085-b2bd-854472073238)


## ControladorPos1mZ
El controlador esta formado po dos bloques "PID-controller" el cual debemos poner en discreta y sintonizarlos correctamente con el boton tune
![resumen8](https://github.com/user-attachments/assets/1a2a9024-ad09-45d4-9f30-ed537c6f1993)


Cambiamos a discreto
![resumen9](https://github.com/user-attachments/assets/4b77c89d-8210-4441-87f5-b31b4b7f11a9)


"PID-controller" sintonizado para la rueda izquierda
![resumen10](https://github.com/user-attachments/assets/545984f6-d4cf-4fca-b718-f788933125c7)

"PID-controller" sintonizado para la rueda derecha

![resumen11](https://github.com/user-attachments/assets/a550226b-b7ac-49ff-a402-bce722aaa963)

## Odometría
Se desvía 0,005 ,es prácticamente recto

![resumen12](https://github.com/user-attachments/assets/ceed6020-8aff-41f7-ab4f-857968bd64ba)


## Video 1 metro

https://github.com/user-attachments/assets/bca78580-1029-4793-9c85-71a24d33c82e


# H42_Circulo10s
Compuesto por un "PID-controller" exterior y 4 subsistemas, 3 que ya conocemos "MCD" "MCI" "OdometríaZ" y uno nuevos "PieroControladoZ" compesto por "PieroAdryZ" y "ControladorBCz"
![resumen13](https://github.com/user-attachments/assets/461685a1-a4e8-4c86-afc5-4f9f29bd3315)


## Sintonización "PID-controller" exterior
![resumen14](https://github.com/user-attachments/assets/13780d07-6976-4562-a110-4d5930b31561)


## PieroControladoZ
![resumen15](https://github.com/user-attachments/assets/286f6c4a-2dbc-4f0c-95fb-f28986d62848)


## ControladorBCz
![resumen16](https://github.com/user-attachments/assets/ab0432aa-b811-4dfd-b3e6-2ade872115c3)


Sintonización "PID-controller" rueda izquierda
![resumen17](https://github.com/user-attachments/assets/0117a3fc-08c5-4d74-999c-cb15b72786d2)


Sintonización "PID-controller" rueda derecha
![resumen18](https://github.com/user-attachments/assets/5649a361-44d1-45ad-9480-16a7ac232933)

## Odometría
![resumen19](https://github.com/user-attachments/assets/aaa309bf-53a2-4d27-ba87-2dca08deb4fb)


# H43_Giro360P
![resumen20](https://github.com/user-attachments/assets/ccf0b432-04a9-4ebe-8942-27620a9b5fd2)

Sintonización "PID-controller" exterior
![resumen21](https://github.com/user-attachments/assets/e65d9294-1c14-4d66-85f1-80e58dcf3531)


## Scope
![resumen22](https://github.com/user-attachments/assets/f771806b-62c1-4167-9dfb-6507e54933b3)

## Odometría
![resumen23](https://github.com/user-attachments/assets/9d3b9872-f929-4241-b46d-7ba30fb0e269)

## Video 360P


https://github.com/user-attachments/assets/573c30f9-a7b6-4022-8c99-c8438e882fd5


# H34_Giro360PI
![resumen24](https://github.com/user-attachments/assets/f5e43938-495d-4315-81bf-006c7f7bc51a)


Sintonización "PID-controller" exterior
![resumen25](https://github.com/user-attachments/assets/2ce02e94-cdd4-4bbb-906c-41f92a28c0e7)

## Scope
![resumen26](https://github.com/user-attachments/assets/16fcbb62-6e25-4667-b8dc-41cef571479f)

## Odometría
![resumen27](https://github.com/user-attachments/assets/da3fec3d-48c6-43a9-89ec-f11019df7e2c)

## Video 360PI
https://github.com/user-attachments/assets/f6be1a74-5202-4caa-bd81-d99c827cc362


# H44_SalidaClase
Se usa dos señales de entrada unapara la velocidad lineal y otra para los angulos de giro
![resumen28](https://github.com/user-attachments/assets/1e7a509e-fdea-4049-93cf-5c0c56ce48d7)


## Señal "Vlineal" usada
En la carpeta "Datos" de este repostorio la podras encontrar como "Vlineal.mat", usada para la veocidad lineal
![resumen29](https://github.com/user-attachments/assets/dec9d8a1-c157-40f6-94f0-6e75f0a7cdf0)

## Señal "Theta" usada
En la carpeta "Datos" de este repostorio la podras encontrar como "Theta.mat", usada para los ángulos de giro
![resumen30](https://github.com/user-attachments/assets/89d10936-fb11-4f04-8fd0-65ba267066ef)


## Odometría

![resumen31](https://github.com/user-attachments/assets/96e5cce4-a567-4ec8-97ec-c8d88e5285df)

## Video saliendo de clase

https://github.com/user-attachments/assets/7b211dc7-f33b-4e05-b492-2925748adc9a




