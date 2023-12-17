# project510kfda
RESUMEN DEL PROYECTO:
La presentación 510(k) ante la FDA asegura que un dispositivo médico sea equivalente a uno comercializado sin requerir aprobación PMA. El proyecto analiza la API de Autorizaciones 510(k) de la FDA, detallando productos y fechas de decisiones.

PARÁMETROS DE DESARROLLO:
CONSIGNA ENTREGA 1:
Desarrollar un programa en Python que realice extracción de una API como fuente de datos, y los guarde los datos obtenidos como un DataFrame de Pandas. Deberás usar la librería requests para obtener datos de 2 o más endpoints de la misma API. Al menos uno de los endpoints debe devolver datos temporales, que se actualicen periódicamente (ya sea por hora, por dìa, etc.), como por ejemplo: valores
meteorológicos, cotizaciones de monedas o acciones de compañías, variaciones de índices económicos, estadísticas deportivas, etc, Los demás endpoints pueden ser datos estáticos o metadatos, como por ejemplo campos que describen a una estación meteorológica (nombre, coordenadas, ciudad, etc.). Deberás realizar una extracción incremental y una full, según corresponda.
Tener en cuenta que en las próximas entregas, habrá que realizar limpieza y procesamiento de los datos extraídos

CONSIGNA ENTREGA 2:

En la instancia anterior, los datos extraídos deben estar como DataFrames. En esta etapa tenés que hacer lo siguiente:
- Guardar cada DataFrame en formato parquet, cada uno en un directorio específico, como si fuese que estás trabajando en un datalake. En caso de que estés haciendo una extracción incremental, deberás particionar por cada fecha y también por hora (si corresponde). En el caso de datos relativamente estáticos, podes particionar por algún otro campo, si consideras necesario.

CONSIGNA ENTREGA 3:
Durante las tres entregas parciales desarrolladas a lo largo de la cursada, has construido progresivamente un flujo completo de ingeniería de datos, que comprende la extracción, el procesamiento y almacenamiento de los datos. En esta última instancia, se sugiere que entregues dos jupyter notebooks, o dos scripts de Python.
- La primera debe realizar la extracción de datos de la API y su almacenamientoen Parquet.
- La segunda notebook debe leer los datos almacenados del paso anterior, aplicar transformaciones y realizar la carga en la base de datos OLAP.
El propósito de tenerlo así por separado facilita el mantenimiento, el monitoreo y la detección de errores cuando el proceso se automatice.

Criterios de evaluación:
1. Calidad del código y presentación.
  a. El código de extracción debe estar bien estructurado y seguir buenas prácticas de programación en Python.
  b. El funcionamiento del código debe estar documentado de forma clara y concisa.
2. Implementación del programa de Extracción.
  a. Justificar la técnica de extracción seleccionada.
  b. El programa debe extraer los datos de la fuente seleccionada utilizando la técnica elegida.
3. Almacenamiento en Parquet.
  a. El código debe asegurar de la existencia de los directorios donde guardará los datos, sino los debe crear automáticamente
  b. El código debe pisar los datos en el directorio, o bien insertar nuevos registros según corresponda.
4. Almacenamiento de los resultados en base de datos OLAP.
