#Pasos realizados para la creacion de base de datos en Big Query de google cloud 

1. Crear el proyecto y habilitar servicios
Entra a Google Cloud Console.

Crear el Proyecto Destileria 1823

Habilita las APIs necesarias:
Cloud Storage API
BigQuery API

2. Crear un Bucket en Cloud Storage
Ve a Storage > Buckets.
Haz clic en Create Bucket.

Asigna un nombre único global (ej. Inevtario General).

Selecciona la región donde estará alojado.
Define nivel de acceso (público o privado — suele ser privado).
Configura el control de versiones si quieres preservar cambios.
Finaliza la creación.

3. Subir archivos CSV al Bucket
Dentro del bucket, haz clic en Upload Files.
Selecciona los archivos CSV desde tu computadora.
Verifica que se subieron correctamente.

4. Crear el Dataset en BigQuery
Ve a BigQuery > SQL Workspace.
En el panel izquierdo haz clic derecho en tu proyecto y selecciona Create Dataset.
Asigna un nombre (ej. base_de_datos_inventario).
Define localización geográfica (debe coincidir con tu bucket si es posible).
Configura caducidad si aplica.

Guarda.
5. Crear tablas desde los archivos CSV
Ahora vas a importar cada archivo CSV como una tabla.

🔹 Método Manual (UI):

Dentro del dataset, haz clic en Create Table.

Fuente: Google Cloud Storage.

Escribe la ruta: gs://ingesta-datos-inventatario/Inventariofinal.csv

Formato de archivo: CSV.

Nombre de tabla: ej. Inventario Final

Esquema:

Puede ser detectado automáticamente (Auto detect) o lo defines tú.

Verifica delimitadores, encabezados y tipos de datos.

Opciones avanzadas: configura codificación, separador de campos, etc.

Clic en Create Table

Enlace del proyecto: [destileria-1823.base_de_datos_inventario](https://console.cloud.google.com/bigquery?hl=es&inv=1&invt=Ab2LLQ&project=destileria-1823)

Video explicativo de la automatizacion: 

https://github.com/user-attachments/assets/c2b4868d-2c98-4be5-94a9-e2bdca81ce57
