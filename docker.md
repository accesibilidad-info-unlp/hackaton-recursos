# Docker

Docker permite empaquetar una aplicación junto con sus dependencias para que pueda ejecutarse de forma consistente en distintos entornos.

Es especialmente útil para compartir proyectos entre integrantes del equipo y simplificar el despliegue.

## Dockerfile básico para Node.js

Permite ejecutar una aplicación Node dentro de un contenedor.

```dockerfile
FROM node:22-alpine

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

EXPOSE 3000

CMD ["npm", "start"]
```

## Construir imagen

```bash
docker build -t mi-app .
```

## Ejecutar contenedor

```bash
docker run -p 3000:3000 mi-app
```

## Docker Compose básico

Ideal para comenzar proyectos rápidamente.

```yaml
services:
  app:
    build: .
    ports:
      - "3000:3000"
```

## Iniciar servicios

```bash
docker compose up
```

## Detener servicios

```bash
docker compose down
```

## Ver logs

```bash
docker compose logs
```

