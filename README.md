# 🚀Trellix-EPO-Health-Check-Report-Generator
Este proyecto automatiza la generación de informes de Health Check para la plataforma **Trellix EPO**, permitiendo extraer, procesar y formatear los resultados de los archivos JSON de health check (`healthcheckresults.txt`) y la información del servidor (`serverinfo.txt`) en un documento de Word.

## ✨Características
- Carga de archivos JSON con los resultados del health check y la información del servidor.
- Generación automática de un documento de Word estructurado que incluye:
  - Resumen Ejecutivo.
  - Estado de la plataforma.
  - Equipos analizados.
  - Puntos de revisión, con descripciones y recomendaciones.
  - Análisis detallado de la información de la consola Trellix EPO y sus servidores.
  - Recomendaciones basadas en los resultados.
- Traducción automática al español de las descripciones en inglés utilizando Google Translate.
- Personalización del cliente mediante la entrada del nombre durante la ejecución.

## ⚙️Requisitos
Para ejecutar este proyecto, necesitarás instalar las siguientes librerías de Python:

```bash

pip install python-docx googletrans==4.0.0-rc1
```
## 🖱️Uso
Coloca los archivos serverinfo.txt y healthcheckresults.txt en la carpeta raíz del proyecto.
Ejecuta el script principal de Python:
- bash
- python generate_report.py
- Ingresa el nombre del cliente cuando se te solicite.
- Selecciona una opción de "runOn" para generar el informe basado en ese dataset.
- El informe será generado automáticamente en un archivo Word, con el nombre del cliente en el archivo de salida.

## 📂Archivos de entrada
- serverinfo.txt: Contiene información del servidor y la base de datos.
- healthcheckresults.txt: Contiene los resultados del health check, incluyendo el estado y las recomendaciones.

## 📄Ejemplo de salida
- El archivo de salida será un documento Word que contiene:
- Una portada con el cliente y la fecha.
- Un resumen ejecutivo del estado de la plataforma.
- Un análisis detallado de los servidores, bases de datos y servicios.
- Tablas de indicadores con su respectiva traducción al español.
- Recomendaciones para mejorar la plataforma.

## 🤝Contribuciones
Este proyecto fue desarrollado para automatizar la creación de informes de Trellix EPO Health Check. Si deseas contribuir o mejorar el proyecto, no dudes en hacer un pull request.
## 👨‍💻Autor
Matias Perez
