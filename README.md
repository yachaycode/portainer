# Portainer Community Edition (CE)

## Instalación Rápida

1. **Prerequisitos**: Asegúrate de tener Docker instalado. [Guía de instalación de Docker](https://docs.docker.com/get-docker/).

2. **Crear `docker-compose.yml`**:
   Crea un archivo `docker-compose.yml` con el siguiente contenido:

   ```yaml
   version: '3.8'

   services:
     portainer:
       image: portainer/portainer-ce:latest
       container_name: portainer
       restart: always
       ports:
         - "9000:9000"
       volumes:
         - /var/run/docker.sock:/var/run/docker.sock
         - portainer_data:/data

   volumes:
     portainer_data:
   ```

3. **Levantar Portainer**:
   Ejecuta el siguiente comando en la terminal:

   ```bash
   docker-compose up -d
   ```

4. **Acceder a la Interfaz**:
   Abre tu navegador y ve a: [http://localhost:9000](http://localhost:9000)

## Detener Portainer

Para detener el servicio, ejecuta:

```bash
docker-compose down
```

## Más Información

Visita la [documentación de Portainer](https://docs.portainer.io/) para más detalles.
