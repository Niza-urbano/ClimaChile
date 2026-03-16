App Clima 

Descripción
Esta es una App de Clima desarrollada con HTML, CSS y JavaScript puro.  
Permite consultar el estado del tiempo actual y el pronóstico semanal de distintas ciudades de Chile, mostrando información como temperatura mínima, máxima, promedio y un resumen de la semana.  

Modelado de Datos
La app utiliza un arreglo de objetos llamado "lugares".  
Cada objeto representa una ciudad y contiene:

- "nombre": Nombre de la ciudad.
- "emoji": Emoji que representa el clima actual.
- "tempActual": Temperatura actual en grados Celsius.
- "estadoActual": Estado del clima (Soleado, Lluvioso, Nublado y Parcialmente Nublado.).
- "pronosticoSemanal": Un arreglo con objetos que describen el clima de cada día:
  - "dia": Nombre del día de lunes a domingo.
  - "min": Temperatura mínima.
  - "max": Temperatura máxima.
  - "estado": Estado del clima de ese día.

Este modelado permite recorrer los datos fácilmente y generar dinámicamente tanto la visualización principal como las estadísticas.

Estadísticas Calculadas
La app calcula automáticamente, a partir del pronóstico semanal:

- Mínima de la semana: el valor más bajo de temperatura mínima.  
- Máxima de la semana: el valor más alto de temperatura máxima.  
- Promedio de temperatura máxima: promedio de las temperaturas máximas de los 7 días y un mensaje que dice:  
  - Semana mayormente soleada, ideal para actividades al aire libre.  
  - Semana fría con varias lluvias, no olvides tu paraguas.  
  - Semana con clima variable y cielos parcialmente cubiertos.

 Uso
1. Selecciona una ciudad en el menú desplegable.  
2. La app mostrará:
   - Clima actual con emoji y temperatura.  
   - Pronóstico semanal en cápsulas interactivas.  
   - Estadísticas calculadas y mensaje resumen.  

Enlace al repositorio
Puedes ver el código completo en GitHub: 
