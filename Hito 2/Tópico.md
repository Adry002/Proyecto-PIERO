# Desarrollo de elementos necesarios y su programación; SIMSCAPE
## _PROGRAMACIÓN_
Se basa en programacióm MATLAB y contiene constructos conceptos adicionales específicos para el modelado físico
## _BIBLIOTECA FOUNDATION_
Aquí se encuentra los bloques de elementos físicos básicos y bloques de construcción, así como fuentes y sensores, se basan en componentes textuales creados con el lenguaje de Simscape.
Puede utilizar estos archivos de origen como base para componentes personalizados
## _BIBLIOTECA UTILITIES_
Contiene bloques del entorno esenciales para crear modelos de redes físicas.
## _COMO CREAR BIBLIOTECAS DE BLOQUES PERSONALIZADAS_
Simscape tiene una biblioteca de ejemplo que se encuentra en el suiguiente directorio **matlabroot /toolbox/physmod/simscape/supporting_files/example_libraries/+Condensadores**.
Despues de copiar los archivos cambiamos el nombre de +Condensadores al que queramos.Finalmente para construir la biblioteca se escribe **ssc_build**
## _BLOQUES_
**-Bloque de componente (ssc_component)** - Al principio este bloque no tiene ningún puerto y el icono de bloque indica que sí Unspecified. Abrimos la carpeta y buscamos el archivo
del componente de lenguaje Simscape deseado y lo abrimos.                                                                                               
**-El bloque Solver Configuration** - Contiene parámetros relacionados con algoritmos numéricos para simulaciones de Simscape. Cada diagrama de Simscape (o cada red física distinta 
topológicamente en un diagrama) debe contener un bloque Solver Configuration.                                                                                  
**-El bloque Simulink-PS Converter y el bloque PS-Simulink Converter** - Para conectar los bloques de Simscape y Simulink®. Se tiliza el bloque Simulink-PS Converter para conectar los
puertos de salida de Simulink a los puertos de entrada de Physical Signals y el bloque PS-Simulink Converter para conectar los puertos de salida de Physical Signals a los puertos 
de entrada de Simulink.                                                               
**-El bloque Probe** - Que permite seleccionar variables de otro bloque de Simscape en el modelo y generarlas como señales de Simulink.
## _CONTROL_
-Posición                                          
-Velocidad                                        
-Controlador PI


https://github.com/user-attachments/assets/f4d2829a-7091-4988-b168-f9259db9ebba

