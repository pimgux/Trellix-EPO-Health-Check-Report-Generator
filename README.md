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
Tambien vamos a necesitar tener instalado en la ePO Trellix la extencion y recopilando informacion por un periodo de tiempo. 
-  ePO Server Health (https://docs.trellix.com/es-ES/bundle/trellix-epolicy-orchestrator-on-prem-5.10.0-product-guide/page/UUID-ce1ef548-2ba5-8858-e1a6-4444631d8b82.html)
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
  -  https://10.106.13.1:8443/rest/hcrs/healthcheckresults/index?start=0&limit=25&includeManual=false   
- healthcheckresults.txt: Contiene los resultados del health check, incluyendo el estado y las recomendaciones.
  -  https://X.X.X.X:8443/rest/hcrs/healthcheckresults/index?start=4655&limit=1000&includeManual=false
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
