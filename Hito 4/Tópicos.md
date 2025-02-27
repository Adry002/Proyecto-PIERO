# COMPARATIVA ENTRE SISTEMAS CONTINUOS Y DISCRETOS
## ¿Qué son?
CONTINUOS: Son aquellos cuyas variables evolucionan continuamente con el tiempo.           
DISCRETO: Aquel que cambia su estado en intervalos de tiempo variado y no de forma constante
## Tipo de señales
Un _Sistema continuo_ tiene como entrada señales continuas, o lo que viene a ser lo mismo señales analógicas 
convirtiendola en señales continuas de salida, mientras que un _Sistema discreto_ tiene como entrada señales 
discretas, o lo que viene a ser lo mismo señales digitales convirtiendola en señales discretas de salida.
## ¿Como se describen?
Los _Sistemas continuos_ se describen típicamente mediante ecuacioness diferenciales, ya sean ordinarias o en 
derivadas parciales. Los _Sistemas discretos_ hay dos tipos los estático o sin memoria (depende de la entrada
en ese mismo instante) y los dinámicoso con memoria(tiene en cuenta muestras pasadas o futuras).Pueden ser invariantes 
en el tiempo ó variante en el tiempo. Y tambien tenemos sistemas lineales o no lineales(los que no cumplan la propiedad
multiplicatiba o aditiva).
## Función de transferencia sistema continuo
En un sistema SISO (única entrada,única salida), la función de transferenciase puede calcular de varias formas:
proceso de linelización (modelo lineal ó incremental);Aplicando transformadas de laplace(modelo lineal ó incremental);
diagramas de bloques(serie,paralelo,retroalimentado),el retroalimentado tiene una condición de diseño.

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/6931f0ca-8245-47f0-9365-511e6532701a)

## Función de transferencia sistema discreto
Se utiliza la transformada Z, que viene definida por la siguiente fórmula.

![image](https://github.com/Escuela-de-Ingenierias-Industriales/RegulacionAutomatica23-Adry009/assets/145486042/20648ee0-0e07-4df3-bd7b-d8a1f58edc3a)

## Método Ruth-Hurwitz(estabilidad de un sistema de tiempo discreto lineal)
El teorema proporciona un criterio capaz de determinar en cuál semiplano (izquierdo o derecho) del plano complejo están 
localizadas las raíces del denominador de la función de transferencia de un sistema; y en consecuencia, conocer si dicho 
sistema es estable o no.
También se utiliza para el trazado del lugar de las raíces. Su objetivo es determinar el límite en el que los polos del 
sistema en bucle cerrado pasan al semiplano derecho complejo y por lo tanto el sistema se vuelve inestable.Los resultados
obtenidos quedarán en función dela ganancia de k.
## Método Jury 
El criterio de estabilidad de Jury es un método para determinar la estabilidad de un sistema de tiempo discreto lineal 
mediante el análisis de los coeficientes de su polinomio característico.Es análogo al metodo de Ruth, con la diferencia
de que el criterio de estabiliddad de juryrequiere que los polos del sistema estén ubicados dentro del círculo unitario centrado
en el origen, mientras que el criterio de estabilidad de Routh-Hurwitz requiere que los polos estén en la mitad izquierda
del plano complejo
