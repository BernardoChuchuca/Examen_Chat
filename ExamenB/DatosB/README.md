# Examen_Interciclo_Chuchuca_Torres
Este proyecto es una aplicación Angular servida con Apache, ejecutada en un contenedor Docker basado en Debian.

## Requisitos

- Docker
- Node.js y npm (opcional, si quieres construir el proyecto en tu máquina local)

## Configuración de la Aplicación Angular

La aplicación Angular está configurada para mostrar el mensaje "¡Bienvenido a mi servidor Docker con Angular!" en la página principal.

## Pasos para Construir y Ejecutar el Proyecto

### 1. Clonar el repositorio

Clona este repositorio en tu máquina local:

```bash
git clone https://github.com/BernardoChuchuca/ExamenChuchucaFrank.git
cd ExamenChuchucaFrank
```
### 2. Construcción de la Imagen Docker
Para construir la imagen Docker, asegúrate de estar en el directorio del proyecto y luego ejecuta el siguiente comando:
```bash
docker build -t bnachoxt/pruebac .  
```
### 3. Ejecución del Contenedor Docker
Ejecuta el siguiente comando para iniciar el contenedor Docker con tu aplicación Angular servida por Apache y tambien creamos un el volumen para que al actualizar 
el codigo en la carpeta dist, se pueda ver reflejado los cambios  en la aplicacion sin necesidad de volver a contruir la imagen nuevamente.
```bash
docker run -d -p 80:80 -v ${PWD}/DatosB/dist/datos-b/browser:/var/www/html --name examen bnachoxt/pruebac
```
4. Acceso a la Aplicación
Una vez que el contenedor esté ejecutándose, abre un navegador web y ve a :
```bash
http://localhost
```

6. Publicación en DockerHub
Si deseas publicar esta imagen en DockerHub:

Inicia sesión en DockerHub:

``` bash
docker login
```
Etiqueta la imagen

```bash
docker tag bnachoxt/pruebac
```
Sube la imagen:

```bash

docker push bnachoxt/pruebac:latest    
```
