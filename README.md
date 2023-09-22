> Exposición de sensores
<div id="header" align="center"> 
<h1> Sensor de temperatura analógico:</h1>
<h3>Termistor NTC (coeficiente de temperatura negativo). </h3>



<br><br><img src= "https://github.com/KarimeIsabel/SistemasProgramables/assets/60378108/1d75c0d4-a003-4e74-aaf0-fb388539ab8e"> 
<div/>
  
# Nombre de los pines

| Nombre |         Descripccion        |
+--------+-----------------------------+
|   VCC  |    Alimentación positiva    |
+--------+-----------------------------+
|   OUT  | Señal de salida (analógica) |
+--------+-----------------------------+
|   GND  |            Tierra           |
+--------+-----------------------------+

# Atributos
|    Nombre   |           Descripccion           | Valor por defecto |
|-------------|----------------------------------|-------------------|
| Temperatura |   Valore de temperatura inicial  | ¨24¨              |
|     Beta    | El coeficiente beta del termisor | ¨3950¨            |

# Leer la Temperatura

``` Python
const float BETA = 3950; // should match the Beta Coefficient of the thermistor
int analogValue = analogRead(A0);
float celsius = 1 / (log(1 / (1023. / analogValue - 1)) / BETA + 1.0 / 298.15) - 273.15;
```

Ejemplo de simulación

https://wokwi.com/projects/299330254810382858
