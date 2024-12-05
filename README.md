# Integración de Azure Cosmos DB con MongoDB, Spark y Databricks para PowerBI
<img width="1228" alt="cosmosdb-databricks-powerbi" src="https://github.com/user-attachments/assets/f39baec3-fadc-4da9-8b82-9c88437304f5">

Este proyecto de análisis del clima tiene como objetivo capturar datos meteorológicos utilizando la API de OpenWeather, almacenarlos en Cosmos DB y analizarlos mediante Azure Databricks y Power BI para generar visualizaciones útiles. Al proporcionar una experiencia práctica con la recolección, almacenamiento, procesamiento y visualización de datos en un entorno de nube, este proyecto facilita el estudio de los conceptos clave de análisis de datos y permite adquirir habilidades prácticas con herramientas populares en la industria, esenciales para el rol de analista de datos.

## Estructura del Proyecto

├── images/

├── powerbi/

├── script/

│   ├── weather_to_cosmo_db.py

│   └── requirements.txt

└── notebook/

- `images/`: Carpeta para guardar las imágenes.
- `powerbi/`: Carpeta que contiene los archivos generados de Power BI.
- `script/`: Carpeta que almacena el script de Python `weather_to_cosmo_db.py` y el archivo `requirements.txt`.
- `notebook/`: Carpeta para los notebooks que se usarán en Databricks para crear las tablas.

## Paso a Paso

Puedes seguir el paso a paso completo de este proyecto en el siguiente enlace de mi blog:

[Integración de Azure Cosmos DB con MongoDB, Spark y Databricks para PowerBI](https://leonardonarvaez.com/blog/detail/integracion-de-azure-cosmos-db-con-mongodb-spark-y-databricks-para-powerbi/)

## Requisitos

- **Azure Cosmos DB** con la API para MongoDB
- **Redes virtuales y subredes** en Azure
- **Azure Databricks** para procesamiento de datos
- **OpenWeather API** para la obtención de datos climáticos
- **PowerBI** para visualización de datos

## Flujo del Proyecto

1. **Crear el entorno base en Azure**:
   - Configura **Azure Cosmos DB** con la API para MongoDB.
   - Crea redes virtuales y subredes en Azure.
   - Toma nota de los nombres de la base de datos y otras credenciales necesarias.

2. **Obtener la API Key de OpenWeather**:
   - Regístrate en [OpenWeather](https://openweathermap.org/api) para obtener tu **API Key**.

3. **Preparación en la máquina local**:
   - Crea un entorno virtual:
     ```bash
     python -m venv myenv
     source myenv/bin/activate  # En Linux/Mac
     myenv\Scripts\activate  # En Windows
     ```
   - Instala los requerimientos:
     ```bash
     pip install -r script/requirements.txt
     ```
   - Actualiza las credenciales en el archivo `weather_to_cosmo_db.py` con los datos de tu entorno de Azure y la API Key de OpenWeather.

4. **Ejecutar el script en tu máquina local**:
   - Ejecuta el script `weather_to_cosmo_db.py` para guardar los datos climáticos en **Azure Cosmos DB**.

5. **Procesar los datos en Azure Databricks**:
   - Utiliza el notebook `notebook_databricks.py` para cargar los datos almacenados en Cosmos DB en un DataFrame de Spark.
   - Procesa y limpia los datos según sea necesario.
   - Guarda los datos como tablas en Databricks.

6. **Exportar a PowerBI**:
   - Conecta PowerBI a Databricks mediante **Partner Connect**.
   - Crea las visualizaciones y análisis en PowerBI.

7. **Generar las gráficas**:
   - Utiliza PowerBI para crear gráficos sobre la evolución del clima (temperatura, humedad, presión, etc.) a lo largo del tiempo.

## Tecnologías Utilizadas

- **Azure Cosmos DB**: Base de datos NoSQL para almacenamiento.
- **Azure Databricks**: Plataforma de procesamiento de datos basada en Apache Spark.
- **Python**: Lenguaje utilizado para conectarse a la API y manejar los datos.
- **OpenWeather API**: API utilizada para capturar datos climáticos.
- **PowerBI**: Herramienta de visualización de datos.

## Configuración

1. **Configuración de Azure Cosmos DB**:
   - Crea un **Grupo de recursos** en Azure.
   - Configura una instancia de **Cosmos DB** utilizando la API para MongoDB.
   - Configura redes virtuales y subredes para la seguridad de la infraestructura.

2. **Configuración de Databricks**:
   - Crea un clúster en **Azure Databricks**.
   - Accede a Databricks y configura la conexión con Cosmos DB para importar los datos.

3. **Configuración de PowerBI**:
   - Conecta **PowerBI** con **Azure Databricks** mediante Partner Connect.
   - Importa los datos procesados en Databricks para visualizarlos.

## Notas

- Asegúrate de que las credenciales y las claves de API estén actualizadas en el script de Python antes de ejecutarlo.
- La base de datos en **Cosmos DB** se actualiza de forma incremental, por lo que los nuevos datos climáticos se agregarán cada vez que se ejecute el script.
- Las visualizaciones en PowerBI pueden ser personalizadas para mostrar gráficos sobre las condiciones climáticas en diferentes intervalos de tiempo.


