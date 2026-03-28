Proyecto MLOps – Despliegue de Modelo de Machine Learning
Descripción

Este proyecto muestra cómo llevar un modelo de Machine Learning a una aplicación web para que pueda ser utilizado por cualquier usuario. El modelo fue entrenado previamente y luego se integró en una aplicación web donde el usuario puede ingresar datos y obtener una predicción.

¿Cómo funciona?

El funcionamiento del proyecto es el siguiente:

Se entrena un modelo de Machine Learning.
El modelo se guarda en un archivo.
La aplicación web carga ese modelo.
El usuario ingresa datos en la página web.
El modelo genera una predicción y muestra el resultado.
Docker permite empaquetar todo el proyecto para que funcione en cualquier computador sin problemas de dependencias.

En pocas palabras, el usuario ingresa datos en la web, la aplicación usa el modelo entrenado y devuelve una predicción.

Estructura del proyecto
app.py: aplicación web
deployment_20231111.pkl: modelo entrenado
templates: archivos de la página web
static: estilos de la página
requirements.txt: librerías necesarias
Dockerfile: archivo para crear el contenedor Docker
Cómo ejecutar el proyecto
Ejecutar localmente
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
python app.py

Luego abrir en el navegador:
http://127.0.0.1:5000

Ejecutar con Docker
docker build -t mlops-app .
docker run -p 5000:5000 -it mlops-app

Luego abrir:
http://localhost:5000

Conclusión

Este proyecto es un ejemplo básico de MLOps, donde un modelo de Machine Learning se pone en producción mediante una aplicación web y un contenedor Docker para que pueda ejecutarse en cualquier entorno.
