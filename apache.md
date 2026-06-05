# Apache

Es uno de los servidores web más utilizados.

Puede servir sitios estáticos directamente o funcionar como proxy inverso para aplicaciones web desarrolladas con distintos frameworks y lenguajes.

## Servidor básico

Configuración mínima para servir archivos estáticos desde un directorio local.

```apache
<VirtualHost *:80>
    ServerName localhost

    DocumentRoot "/var/www/html"

    <Directory "/var/www/html">
        AllowOverride All
        Require all granted
    </Directory>
</VirtualHost>
```

Uso habitual:

```text
Cliente
↓
Apache
↓
Archivos HTML / CSS / JS
```

## Proxy inverso

Proxy inverso hacia una aplicación ejecutándose en el puerto 3000.

```apache
<VirtualHost *:80>
    ServerName localhost

    ProxyPass / http://app:3000/
    ProxyPassReverse / http://app:3000/
</VirtualHost>
```

Requiere los módulos:

```text
proxy
proxy_http
```

Uso habitual:

```text
Cliente
↓
Apache
↓
Aplicación Node / React / API
```

