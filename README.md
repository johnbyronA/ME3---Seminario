# Documentación

## Especialización en analítica y ciencia de datos 2023 - Cohorte VI

### ME03 Seminario - John Byron Alzate, Jorge Genes Padilla

### Insumos del proyecto

Insumos del proyecto
El presente proyecto contiene los siguientes archivos de acuerdo con los lineamientos estipulados en la rúbrica:

1. bd_entrega3_entrada.csv: Fragmento del Dataset original encontrado en la página web de MEData; sin transformar, contiene 1000 filas de registros y 50 columnas.
2. Entrega_3_seminario_DESCRIPTIVA.ipynb: Archivo con el código utilizado para el análisis estadístico y transformación del dataset anterior.
3. bd_entrega3_salida.csv: Dataset transformado.

### Origen de los datos

El nombre de la base de datos es "Base de Datos SISBEN 2017", la cual proviene de la página web de MEData, repositorio de datos abiertos generados y publicados por las diferentes dependencias de la Alcaldía de Medellín.

El enlace directo al dataset es el siguiente: http://medata.gov.co/dataset/base-de-datos-sisben-2017

El dataset encontrado en la página anterior consta de más de 60 columnas y más de un millón de filas de registros; sin embargo, para el alcance del análisis para la entrega #3 de la asignatura Seminario de la Especialización en Analítica y Ciencia de Datos 2023, se tuvieron en cuenta tan solo 50 columnas y 1000 filas de datos, las cuales fueron consideradas como las más significativas para efectos de posteriores análisis estadísticos. Dicho dataset está contenido en el archivo con nombre bd_entrega3_entrada.csv


### Pasos para la ejecución del código

#### INSTRUCCIONES:

1. Ingresar a https://colab.research.google.com/
2. Dar clic en la opción "Subir", posteriormente dar clic en la opción "Explorar".
3. Ubicar el archivo "Entrega_3_seminario_DESCRIPTIVA.ipynb" dentro del PC local.
4. Dar clic en la opción "Abrir" que se encargará de cargar el archivo al servicio de Google Colab en la nube.
5. Dar clic al icono de la carpeta en la barra lateral izquierda de la pantalla.
6. Dar clic al botón con el icono de la carpeta con una flecha apuntando hacia arriba (Subir al almacenamiento de sesión).
7. Ubicar el archivo "bd_entrega3_entrada.csv" dentro del PC local, darle clic a la opción "Abrir".
8. Esperar a que el archivo cargue completamente.
9. Ejecutar todo el código presionando la combinación de teclas CTRL + F9


### Obtención de Datos transformados

Una vez aplicados los pasos expuestos en la sección INSTRUCCIONES, se procede al uso de código en lenguaje de programación Python dentro del archivo Entrega_3_seminario_DESCRIPTIVA.ipynb para obtener transformaciones en los datos. Un ejemplo de ello son las siguientes líneas de código, las cuales contienen sus respectivos comentarios explicativos (ilustrados por un símbolo # al principio de la línea) y pueden ser encontrados dentro del archivo:

```
# Categorizar la columna "EDAD" según los nuevos rangos y categorías proporcionadas

bins = [-np.inf, 17, 29, 49, 69, np.inf]
labels = ["Underage", "Young", "Adult", "Old", "Very old"]
df['AgeCategory'] = pd.cut(df['EDAD'], bins=bins, labels=labels, right=True)
```

```
# Eliminar la columna 'Puntaje' y eliminar registros duplicados.

df.drop('PUNTAJE', axis=1, inplace=True)
df.drop_duplicates(inplace=True)
```

Posteriormente, y como resultado de todas las transformaciones empleadas dentro del código, se obtendrá un archivo de salida llamado bd_entrega3_salida.csv, el cual es una transformación del dataset original con la finalidad de poder realizar los análisis solicitados en posteriores momentos evaluativos de la asignatura Seminario.

### Conclusiones finales

El presente archivo contiene la data pertinente al alcance establecido para la entrega #3 de la asignatura Seminario de la Especialización en Analítica y Ciencia de Datos 2023 - Universidad de Antioquia.

El repositorio actual es de uso público, por lo tanto, cualquier aporte, inquietud u observación será muy bien recibida y atendida por los autores a través de pull requests o comentarios generales.

¡Buen día! 
