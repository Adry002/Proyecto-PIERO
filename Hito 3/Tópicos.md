# Tipos de controladores y su implementación con Simulink 
## _¿QUÉ ES UN CONTROLADOR?_
Compara el valor real de la salida de una planta con la entrada de referencia, determina la desviación o error, 
y produce una señal de control que reducirá la velocidad a 0 ó a un valor pequeño
## _TIPOS DE CONTROLADOR_
- P
- I
- PI
- PD
- PID
## _P, CONTROLADOR PROPORCIONAL_
Multiplica el error; es el controlador más simple.
## _I, CONTROLADOR INTEGRAL_
Disminuye y/o elimina el error en el estado estacionario. Eltiempode respuesta es más lento que los P. Se usan cuando 
las variables deben permanecer dentro de un rango muy estrecho y requieren de control de ajuste fino.
## _PI, CONTROLADOR PROPORCIONAL INTEGRAL_
Combina el comportamiento de los dos anteriore.
Kp, entra instantaneamente.
Ki, entra con retardo y anula por completo el error.
## _PD, CONTROLADOR PROPORCIONAL DERIVATIVO_
Toma la derivada del error con repecto al tiempo y la multiplicacion por una constante.
## _PID, CONTROLADOR PROPORCIONAL INTEGRAL-DERIVATIVO_
Calcula la desviación o error entre un valor medido y el que se quiere obtener para aplicar una acción que ajuste el proceso. 
Aprovecha las ventaja de cada uno de los controladores de acciones básicas. Ofrece una respuesta muy rápida y una compesación
de la señal de error inmediata, sin embargo este sistema es muy propenso a oscilar. Los parámetros son dificiles de ajustar.
## _TÉCNICA USADA PARA LA IMPLEMENTACIÓN EN SIMULINK_
- PRECOMPENSACIÓN; Se corrige la perturbación antes de que llegue realmente a las variables controladas.
- RETROALIMENTACIÓN; 
## _BOTONES_
- "PARAMETERS", para ajustar los valores de las ganancias y otros parámetros.
- "OPTIONS", configura opciones avanzadas.
- "BOTONES", ejecuta simulaciones.
