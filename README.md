> Exposición de sensores
<div id="header" align="center"> 
<h1> Sensor de temperatura analógico:</h1>
<h3>Termistor NTC (coeficiente de temperatura negativo). </h3>

Un termistor NTC (coeficiente de temperatura negativo) es un tipo de sensor de temperatura que utiliza un material semiconductor cuya resistencia eléctrica disminuye a medida que aumenta la temperatura. 

<br><br><img src= "https://github.com/KarimeIsabel/SistemasProgramables/assets/60378108/1d75c0d4-a003-4e74-aaf0-fb388539ab8e"> 
<div/>
  
# Nombre de los pines
<br><br><img src= "https://github.com/KarimeIsabel/SistemasProgramables/assets/60378108/02539091-3942-48cb-bc80-c5ea3e1c6216">


# Atributos
<br><br><img src= "https://github.com/KarimeIsabel/SistemasProgramables/assets/60378108/4e0024b8-2008-4a95-819c-93f44f181c10">


# Leer la Temperatura

``` Python
const float BETA = 3950; // should match the Beta Coefficient of the thermistor
int analogValue = analogRead(A0);
float celsius = 1 / (log(1 / (1023. / analogValue - 1)) / BETA + 1.0 / 298.15) - 273.15;
```

Ejemplo de simulación

https://wokwi.com/projects/299330254810382858
