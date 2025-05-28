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
git clone https://github.com/BernardoChuchuca/Examen_Chat.git
cd ExamenChuchucaFrank
```
### 2. Construcción de la Imagen Docker
Para construir la imagen Docker, asegúrate de estar en el directorio del proyecto y luego ejecuta el siguiente comando:
```bash
docker build -t bnachoxt/ejemplo .  
```

4. Acceso a la Aplicación
Una vez que el contenedor esté ejecutándose, abre un navegador web y ve a :
```bash
http://localhost
```

6. Publicación en DockerHub
Si deseas publicar esta imagen en DockerHub:

docker push bnachoxt/ejemplo:tagname
  
```
