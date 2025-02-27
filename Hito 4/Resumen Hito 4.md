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
![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/e1b7e558-4dfb-4c2c-bfa8-90354f5d2df1)

"PID-controller" sintonizado para la rueda derecha
![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/6c7f5bab-dd64-4b3b-8255-f29f6735fbcd)

## Odometría
Se desvía 0,005 ,es prácticamente recto
![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/b3465377-f67f-4c83-8ba0-6f7e9ca56364)


## Video 1 metro

https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/bd560af3-231a-4e6b-9666-56c0800800ba

# H42_Circulo10s
Compuesto por un "PID-controller" exterior y 4 subsistemas, 3 que ya conocemos "MCD" "MCI" "OdometríaZ" y uno nuevos "PieroControladoZ" compesto por "PieroAdryZ" y "ControladorBCz"

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/aa9a8d62-02b2-44a3-b3ec-5074f0bfade8)

## Sintonización "PID-controller" exterior

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/55a0fedd-325f-426a-b8d6-4fa47c3694cf)

## PieroControladoZ

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/f97b3ff0-632b-43b7-a7e6-ec2c8ff9cf1b)

## ControladorBCz

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/ba304284-2a7d-4478-bb80-ced46a9749f2)

Sintonización "PID-controller" rueda izquierda

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/83712c7f-30a4-4814-a54a-54513a689ed8)

Sintonización "PID-controller" rueda derecha

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/1f12c18f-4343-4060-be41-d2209d1ecd08)

## Odometría

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/bc82fa46-931b-4097-b20c-bbecc23a895a)

# H43_Giro360P
![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/aacad46d-ec89-4b7c-8a46-f0f9b71264cd)

Sintonización "PID-controller" exterior

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/ac3f4d6f-5878-45b8-9d5b-c7ac21a2f224)

## Scope
![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/0e9033f1-4ff9-44cf-92d6-1207a7172217)

## Odometría

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/4b6c5e97-80a5-4c11-8f16-162abf29aff8)

## Video 360P

https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/58ad197e-9a68-4a2b-8072-3dc831812160

# H34_Giro360PI

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/1512c0ed-8323-426a-9779-26658498e7b4)

Sintonización "PID-controller" exterior

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/b8bcf4d2-40d1-4e78-b678-dc92de53f652)

## Scope
![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/1d6e4465-38b5-4b0d-bc5e-468efe525e52)


## Odometría
![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/ba4e7123-b403-4c53-9aba-3fdac56249ba)

## Video 360PI

https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/15122a67-c4be-4913-8b38-5d7e4366de57

# H44_SalidaClase
Se usa dos señales de entrada unapara la velocidad lineal y otra para los angulos de giro

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/4d766ff3-1d79-4595-b978-01d498763953)

## Señal "Vlineal" usada
En la carpeta "Datos" de este repostorio la podras encontrar como "Vlineal.mat", usada para la veocidad lineal

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/2e33f149-f35c-46de-98ac-023270b8144b)

## Señal "Theta" usada
En la carpeta "Datos" de este repostorio la podras encontrar como "Theta.mat", usada para los ángulos de giro

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/018a1923-1b66-4cbb-b4c1-2beda8662772)

## Odometría
![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/fe33fda2-3b17-4659-8c27-f3e12ea5f8b8)

## Video saliendo de clase

https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/e854a85f-7133-4757-98af-18ea2ec2d977



