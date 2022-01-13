# Lab-2-Uni-2
1. Objetivos

1.1 Objetivo General

Analizar y armar el circuito, mediante el uso de una herramienta digital y de conceptos principal para comprobar por medio del experimento el Teoema de Thévenin en un circuito resistivo .

1.2 Objetivos Específicos

Identificar los componentes principal del circuito  para poder armarlo y realizar las medidas correspondientes. 

Conocer los conceptos principales sobre el teorema de Thévenin para analizar adecuadamente el circuito.

Realizar los calculos adecuados para comprobar con los datos que se obtuvieron el experimento. 

2. Marco teórico

![image](https://user-images.githubusercontent.com/94153604/149265727-35503b4f-8f62-43ce-a860-c626bce7353e.png)

3. Requisitos previos

![image](https://user-images.githubusercontent.com/93958596/149264615-6466199d-bd8c-463d-9de9-03f6dfadf934.png)
![image](https://user-images.githubusercontent.com/93958596/149264640-8e4da11c-7d10-4674-b86b-e285b0a6908b.png)
![image](https://user-images.githubusercontent.com/93958596/149264655-2970c138-43d8-48cb-b226-f5951c3cd2f7.png)
![image](https://user-images.githubusercontent.com/93958596/149264671-06522569-6bff-4138-9475-bc74d9a4a297.png)
![image](https://user-images.githubusercontent.com/93958596/149264690-a8ae95b3-8a77-4ca1-92bf-9957f079872e.png)

4. Materiales y equipos requeridos

![image](https://user-images.githubusercontent.com/93958596/149257619-92364683-4e8f-4eec-a16e-9650ee2d8aa5.png)

5. Respuestas a interrogantes y calculo de error

Para calcular la resistencia de Thevenin se deben anular las fuentes de voltaje

![image](https://user-images.githubusercontent.com/93958596/149266392-c411ba14-ee2d-4880-925a-7d0a2a952b72.png)

R1 y R2 se encuentran en paralelo

    1/Req1 = 1/R1 + 1/R2 = 1/0.56 kΩ + 1/4.7 kΩ = 2 kΩ
    Req1 = 1/2 kΩ = 0.5 kΩ

Req1 y R3 se encuentran en paralelo

    1/Req2 = 1/Req1 + 1/R3 = 1/0.5 kΩ + 1/0.33 kΩ = 5.03 kΩ
    Req1 = 1/5.03 kΩ = 0.2 kΩ

Req2 y R4 se encuentran en serie

    RTH = Req2 + R4 = 0.2 kΩ + 0.1 kΩ = 0.3 kΩ = 300 Ω

Para calcular el voltaje de Thevenin se debe quitar R5 y dejar en cortocircuito

![image](https://user-images.githubusercontent.com/93958596/149266513-414dbd07-7c27-4a30-bd5a-b0728bc1fb00.png)

El voltaje que circula por R3 es igual a VTH

![image](https://user-images.githubusercontent.com/93958596/149266540-1b106bbe-495a-455c-b160-9c0d5d854ba5.png)

En el primer lazo:

    R1*I1 + R2*I1 – R2*I2 = 12 V
    560 I1 + 4700 I1 – 4700 I2 = 12 
    5260 I1 – 4700 I2 = 12 	(1)

En el segundo lazo:

    R3*I2 + R2*I2 – R2*I1 = 12 V
    330 I2 + 4700 I2 – 4700 I1 = 2
    5030 I2 – 4700 I1 = 2	  (2)

Despejamos I1 de la primera ecuación y lo reemplazamos en la segunda ecuación:

    I1 = (12 + 4700 I2) / (5260)
    5030 I2 – 4700 * (12 + 4700 I2) / (5260) = 2
    5030 I2 – 0.89 * (12 + 4700 I2) = 2
    5030 I2 – 10.68 – 4183 I2 = 2
    847 I2 = 12.68
    I2 = 0.015 A 

La corriente que pasa por R3 es I2 por lo que, usando la ley de Ohm se puede hallar el voltaje en R3

    VR3 = R3*I2 = 330 Ω * 0.015 A = 4.95 V

Quedando el circuito de Thevenin de la siguiente manera

![image](https://user-images.githubusercontent.com/93958596/149266653-eac24f92-841e-4b4d-8073-1bebc25f55da.png)

Hallamos la intensidad en R5, la cual es igual a la intensidad total porque es un circuito en serie

    I5 = IT = 4.95 V / 1300 Ω = 0.0038 A = 3.8 mA

Y el voltaje en R5 es:

    VR5 = 3.8 mA * 1 kΩ = 3.8 V
 
 Resultados de las tablas:

![image](https://user-images.githubusercontent.com/93958596/149266717-18278973-d2c8-4b25-a7d2-4ec9185d79b5.png)
![image](https://user-images.githubusercontent.com/93958596/149266727-18bcbdb0-a93c-4a2c-b383-99bf2a20dac5.png)

6. Video

https://www.youtube.com/watch?v=SRS8Fgav-JA

7. Conclusiones

Para armar el respectivo cicuito se necesita dos fuentes de voltaje cd, 5 ressitencias y multimetros para posterior mente medir el volataje del cicuito principal y despues del voltaje VTH y la resistencia RTH cuando esta abierto el circuit , por ello  los valores para la forma general del circuito de thevenin es VTH = 5.06 V y RTH = 299 ohmios los cuales se coloca en el respectivo circuito en serie. 

El metodo de Thevenin se lo considera util para facilitar el análisis de circuitos complejos, puesto que esta compuesto por el VTH y la RTH los cuales por general en el circuito de thevenin el vaoltaje se ebcuentra en serie con la resisencia , sin embargo se puede manifertar que el circuito equivalente de thevenin no es el mismo que el circuito general y cabe recalcar que para obtener el valores que se necesitan no existen formulas específicas sino que se debe realizar el respectivo analisis. 

Para obtener el VTH y la RTH se debe analizar la manera en la cual se encuentran las resistencias ya sea en serie o en paralelo como R1 y R2 estan en paralelo al igual que R1 y R3, estan en serie R2 y R4  y para calcular el VTH se debe quitar R5 y dejarlo en corto cuircuito , después se procede a obtener un sistema de ecuaciones para obtener el valor de la corriente y con el uso de la ley de Ohm se puede hallar el valor de VR3 el cual es igual al VTH y con ello se arma el respectivo circuito equivalente, cabe recalcalcar que el analisis de cada circuito es diferente. 

8. Bibliografía

Floyd, T. (2007). Principio de Circuitos Eléctricos. Pearson, Prentice Hall

