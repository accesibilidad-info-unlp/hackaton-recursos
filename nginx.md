# Nginx

Es un servidor web liviano y de alto rendimiento.

Puede utilizarse para servir archivos estáticos o actuar como proxy inverso frente a aplicaciones desarrolladas con Node.js, Python, PHP u otras tecnologías.

## Configuración básica

Servidor web simple que entrega archivos estáticos desde el directorio por defecto.

```nginx
server {
    listen 80;
    server_name localhost;

    root /usr/share/nginx/html;
    index index.html;
}
```

## Configuración de proxy inverso

Redirige las solicitudes hacia una aplicación ejecutándose en el puerto 3000.

```nginx
server {
    listen 80;
    server_name localhost;

    location / {
        proxy_pass http://app:3000;

        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
    }
}
```

## Uso habitual:

```text
Cliente
↓
Nginx
↓
Aplicación Node / React / API
```

