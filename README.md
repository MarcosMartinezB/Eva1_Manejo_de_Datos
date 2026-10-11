Procesamiento de Datos Masivos y Flujos ETL con KNIME y MySQL

Resumen del Proyecto

Este repositorio contiene el desarrollo completo de la Evaluación Sumativa N°1 para la asignatura de Manejo de Datos en INACAP. El objetivo principal del proyecto fue aplicar procesos de extracción, transformación y carga (ETL), así como la generación de reportes y visualizaciones analíticas a partir de dos fuentes de información de diferente escala: un archivo masivo CSV con datos de ventas de productos de Amazon y la base de datos relacional Northwind alojada en MySQL.

Casos Prácticos y Desarrollo

Caso Práctico 1: Procesamiento de Datos de Amazon

El dataset de Amazon, debido a su elevado volumen de información, presentaba problemas de lectura y rendimiento al intentarse abrir en hojas de cálculo convencionales. Mediante KNIME Analytics Platform se construyó un flujo de trabajo capaz de procesar el archivo completo sin restricciones de columnas.

Se utilizaron nodos como CSV Reader, GroupBy, Sorter y Math Formula para resolver tres análisis clave:

Valoraciones de Usuarios: Análisis de la distribución de calificaciones en estrellas. Se identificó una alta concentración de productos sin valoración registrada (892.728 registros), mientras que el resto de los productos presentó una tendencia predominantemente positiva.

Cantidad de Productos por Categoría: Comparación de la densidad del catálogo mediante gráficos de barras horizontales. Las categorías de Bebés y Electrónicos lideran la oferta con más de 30.000 productos cada una, en contraste con secciones especializadas como lanzamientos o bronceadores.

Precio Promedio por Categoría: Cálculo de promedios combinando funciones de conteo y suma para obtener el valor medio por categoría. Los productos tecnológicos y computadores mostraron los promedios más altos, observándose un decrecimiento progresivo hacia artículos digitales de bajo costo y e-books.

Caso Práctico 2: Conexión Relacional y Reportes Northwind

Para el segundo caso práctico se configuró un servidor local mediante XAMPP y phpMyAdmin para alojar la base de datos MySQL de Northwind. La conexión se estableció en KNIME a través del nodo MySQL Connector.

A través del nodo DB Query Reader se ejecutaron consultas SQL avanzadas para responder a tres requerimientos corporativos:

Volumen de Ventas por Ciudad: Identificación de las ciudades con mayor cantidad de órdenes procesadas, destacando Londres, Río de Janeiro, Boise y São Paulo. Los resultados se exportaron automáticamente a un archivo CSV mediante el nodo CSV Writer.

Monto Total Vendido por Ciudad: Integración de tablas de órdenes, detalles de pedidos y clientes para calcular los ingresos monetarios totales. Este análisis reveló que la cantidad de pedidos no necesariamente equivale al volumen de dinero generado, siendo ciudades como Cunewalde, Boise y Graz las de mayor recaudación.

Top Categorías de Productos Más Vendidas: Consulta relacional entre múltiples tablas para agrupar las ventas por categoría. Mediante los nodos Sorter y Top k Row Filter se aislaron las 5 categorías principales (Lideradas por Bebidas y Lácteos), graficando la tendencia en un diagrama de líneas y exportando el reporte procesado.

Documentos e Insumos Incluidos

El repositorio incluye el archivo con el flujo de trabajo exportado de KNIME (.knwf) que contiene todos los nodos y transformaciones aplicadas, junto con el informe académico en formato PDF presentado para INACAP. Por motivos de tamaño y límites de almacenamiento, el dataset CSV original de Amazon no se incluye en el repositorio.

Tecnologías Aplicadas

Herramientas ETL y Analítica: KNIME Analytics Platform.
Bases de Datos Relacionales: MySQL, XAMPP, phpMyAdmin y lenguaje SQL.
Gestión de Archivos y Reportes: Exportación automatizada a archivos CSV e informes técnicos en PDF.

Big Data Processing and ETL Workflows using KNIME and MySQL

Project Overview

This repository contains the complete development of the Summative Evaluation 1 for the Data Management course at INACAP. The main objective of the project was to implement Extraction, Transformation, and Loading (ETL) processes, as well as generate analytical reports and data visualizations from two distinct data sources: a massive CSV dataset containing Amazon product sales and the Northwind relational database hosted on MySQL.

Practical Cases and Implementation

Case Study 1: Amazon Data Processing

Due to its large data volume, the Amazon dataset caused reading errors and performance issues when loaded into standard spreadsheet software. Using KNIME Analytics Platform, a workflow was built to process the full dataset without column constraints.

Nodes such as CSV Reader, GroupBy, Sorter, and Math Formula were implemented to solve three core requirements:

User Ratings: Analysis of star rating distributions. A large concentration of unrated products was detected (892,728 records), whereas rated items showed a predominantly positive user perception.

Product Quantity by Category: Catalog density comparison using horizontal bar charts. The Baby and Electronics categories led the offering with over 30,000 items each, contrasting with niche categories like new releases or tanning products.

Average Price by Category: Computation of average prices by combining count and sum aggregations. Desktop computers and tech equipment registered the highest average prices, exhibiting a steady decrease toward low-cost digital goods and e-books.

Case Study 2: Relational Connection and Northwind Reporting

For the second case study, a local environment was configured using XAMPP and phpMyAdmin to host the Northwind MySQL database. The connection was established in KNIME using the MySQL Connector node.

Using the DB Query Reader node, advanced SQL queries were executed to fulfill three business requirements:

Sales Volume by City: Identification of cities with the highest number of processed orders, led by London, Rio de Janeiro, Boise, and São Paulo. Results were automatically exported to CSV using the CSV Writer node.

Total Revenue Sold by City: Integration of sales orders, order details, and customer tables to calculate total monetary revenue. The analysis revealed that order volume does not directly correlate with total revenue, as cities like Cunewalde, Boise, and Graz generated the highest income.

Top Product Categories by Sales: Relational query combining multiple tables to aggregate sales by product category. Using Sorter and Top k Row Filter nodes, the top 5 performing categories were isolated (led by Beverages and Dairy Products), visualized through a line plot, and exported into CSV format.

Included Files and Artifacts

This repository includes the exported KNIME workflow file (.knwf) containing all configured nodes and data transformations, alongside the official academic report in PDF format submitted to INACAP. Due to file size constraints, the raw Amazon CSV dataset is excluded from the repository.

Technologies Applied

ETL & Analytics Tools: KNIME Analytics Platform.
Relational Databases: MySQL, XAMPP, phpMyAdmin, and SQL querying.
Data Management & Reporting: Automated CSV exports and technical PDF documentation.