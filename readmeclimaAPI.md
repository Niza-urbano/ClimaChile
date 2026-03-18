App Clima

Descripción
App Clima es una aplicación web que permite ver el clima actual y el pronóstico semanal de varias ciudades de Chile.  
La interfaz muestra temperatura (máx y mín), estado del clima (soleado,parcialmente nublado, nublado, lluvioso), pronóstico por día con emojis representativos, y estadísticas semanales.  
La aplicación utiliza Bootstrap para un diseño moderno y es responsive.

Estructura de clases

"LugarClima"
- Representa una ciudad con su información de clima.
- Propiedades principales:
  - "id" → identificador único
  - "nombre" → nombre de la ciudad
  - "emoji" → icono representativo del estado del clima
  - "tempActual" → temperatura actual
  - "estadoActual" → estado del clima actual
  - "pronosticoSemanal" → arreglo con los días de pronóstico
- Métodos:
  - "calcularEstadisticas()"" → analiza "pronosticoSemanal" y devuelve:
    - Temperatura mínima y máxima de la semana
    - Promedio de temperatura máxima
    - Mensaje resumen sobre el clima de la semana.

API de clima utilizada

- Nombre: Open-Meteo  
- URL base: `https://api.open-meteo.com/v1/forecast`  
- Documentación: [https://open-meteo.com/](https://open-meteo.com/)  
- Datos obtenidos:
  - `current_weather.temperature` → temperatura actual
  - `current_weather.weathercode` → código del estado del clima
  - `daily.temperature_2m_max` → máximas diarias
  - `daily.temperature_2m_min` → mínimas diarias
  - Se utiliza `latitude` y `longitude` de cada ciudad para la consulta.

---

Cálculo de estadísticas

1. Se recorre el arreglo `pronosticoSemanal` de cada `LugarClima`.
2. Se calculan:
   - `min` → mínima de todos los días
   - `max` → máxima de todos los días
   - `prom` → promedio de las temperaturas máximas
3. Se cuentan los días según su estado (`Soleado`, `Lluvioso`, `Nublado`) para generar un mensaje resumido de la semana:
   - Mayoría de soleado → "Semana mayormente soleada."
   - Mayoría de lluvias → "Semana con varias lluvias."
   - Mezcla → "Semana con clima variable."

  Github: https://github.com/Niza-urbano/ClimaChile.git