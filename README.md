> Hola
> Exposición de sensores

<div id="header" align="center"> 

***Sensor de temperatura analógico:***

_Termistor NTC_ <sub> (coeficiente de temperatura negativo). <sub/>

![image](https://github.com/KarimeIsabel/SistemasProgramables/assets/60378108/1d75c0d4-a003-4e74-aaf0-fb388539ab8e)
<div/>
  

# Leer la Temperatura
```
const float BETA = 3950; // should match the Beta Coefficient of the thermistor
int analogValue = analogRead(A0);
float celsius = 1 / (log(1 / (1023. / analogValue - 1)) / BETA + 1.0 / 298.15) - 273.15;
```
Ejemplo de simulación
https://wokwi.com/projects/299330254810382858
