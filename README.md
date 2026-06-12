# Extracción del conocimiento de Base de Datos - Desempeño 1er Parcial

## Datos del Alumno
* **Nombre:** Mauricio Medel de Jesús
* **Universidad:** Universidad Tecnológica del Centro de Veracruz (UTCV)
* **Carrera:** Ingeniería en Gestión de Software
* **9;A**

## Descripción General
Crear un portafolio en GitHub que documente el ciclo completo de análisis sobre un conjunto de datos de dominio público. El proyecto abarcará las fases de preprocesamiento, evaluación estadística descriptiva y creación de visualizaciones, con el propósito de interpretar los hallazgos y aplicar la pirámide DIKW (Datos, Información, Conocimiento, Sabiduría) para extraer valor real.

## Objetivo
Desarrollar y automatizar un pipeline de datos que permita extraer información de operaciones diarias de un restaurante, normalizarla creando una dimensión de tiempo, calcular métricas de ventas y almacenar los resultados en una base de datos PostgreSQL para su posterior visualización y análisis de rendimiento regional y de productos.

## Datasets Utilizados
Se simularon fuentes de datos locales mediante tres archivos estructurados:
* `productos1.csv`: Catálogo de productos, categorías y precios unitarios.
* `sucursales1.csv`: Catálogo de ubicaciones físicas del negocio.
* `operaciones_diarias1.csv`: Archivo transaccional con el detalle de las ventas diarias por sucursal y producto.

## Herramientas Utilizadas
* **Lenguaje:** Python 3
* **Entorno de Desarrollo:** Jupyter Notebook
* **Librerías de manipulación y análisis:** `pandas`
* **Librerías de visualización:** `matplotlib`
* **Conexión a Base de Datos:** `sqlalchemy`, `psycopg2`
* **Motor de Base de Datos:** PostgreSQL

## Instrucciones de Ejecución General
Para reproducir este proyecto localmente, sigue estos pasos:
1. Clonar este repositorio en tu máquina local.
2. Asegurarte de tener instalado Python y las dependencias listadas (`pip install pandas matplotlib sqlalchemy psycopg2-binary`).
3. Crear una base de datos vacía en PostgreSQL llamada `dw_restaurante`.
4. Abrir el archivo Jupyter Notebook principal.
5. En la celda de conexión a la base de datos, modificar las credenciales (`USUARIO` y `CONTRASENA`) para que coincidan con tu entorno local de PostgreSQL.
6. Ejecutar las celdas en orden secuencial (Opción de menú: *Kernel -> Restart & Run All*).



## Conclusiones Generales
La integración de Python con PostgreSQL mediante SQLAlchemy demostró ser altamente eficiente para automatizar procesos ETL. Al estructurar la información transaccional cruda en un modelo dimensional (dimensiones y hechos), logramos reducir la complejidad de las consultas analíticas. Las visualizaciones obtenidas comprueban que el almacenamiento estructurado facilita la identificación rápida de patrones de consumo, lo cual es vital para la toma de decisiones estratégicas, como el reabastecimiento de inventario para los productos con mayor rotación (entradas) o la asignación de presupuesto por sucursal.