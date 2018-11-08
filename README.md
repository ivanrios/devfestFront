
# devfestFront

Front end de sitio web



Crear un proyecto
https://console.cloud.google.com

Descargar el SDK de Google Cloud Platform
https://cloud.google.com/sdk/






Configurar:

**gcloud auth login**

**gcloud config set project [PROJECT]**






Validar config:

 **gcloud config list**


Clonar el repo y abrir el branch sitioWeb


Agregar permisos públicos de solo lectura

**gsutil acl ch -u AllUsers:R gs://devfestcancun **

**gsutil defacl set public-read gs://devfestcancun**


Subir archivos (sincronización)

**gsutil rsync -R . gs://devfestcancun**



Si quieres que la página responda a tu dominio, debes crear un registro CNAME en tus DNS

demo.devfestcancun.com to c.storage.googleapis.com 


Configurar archivo default

**gsutil web set -m index.html -e 404.html gs://devfestcancun**
