# SSH

SSH permite conectarse de forma segura a otros equipos y autenticarse en servicios como GitHub sin utilizar usuario y contraseña en cada operación.

## Verificar si existe una clave SSH

Linux / macOS:

```bash
ls ~/.ssh
```

Windows (PowerShell):

```powershell
dir $HOME\.ssh
```

## Generar una nueva clave SSH

```bash
ssh-keygen -t ed25519 -C "tucorreo@ejemplo.com"
```

Presionar Enter para aceptar la ubicación predeterminada.

## Iniciar el agente SSH

Linux / macOS:

```bash
eval "$(ssh-agent -s)"
```

## Registrar la clave

```bash
ssh-add ~/.ssh/id_ed25519
```

## Ver la clave pública

```bash
cat ~/.ssh/id_ed25519.pub
```

Copiar el contenido completo.

## Agregar la clave a GitHub

1. GitHub
2. Settings
3. SSH and GPG Keys
4. New SSH Key
5. Pegar la clave pública

## Probar la conexión

```bash
ssh -T git@github.com
```

Resultado esperado:

```text
Hi usuario!
You've successfully authenticated...
```

## Clonar un repositorio de GitHub usando SSH

```bash
git clone git@github.com:organizacion/proyecto.git
```

## Uso habitual

```text
Generar clave SSH
↓
Agregar clave a GitHub
↓
Probar conexión
↓
git clone
↓
git push
```

## Computadoras compartidas

Si estás utilizando una computadora del aula o un equipo que no te pertenece:

* Evita guardar claves personales permanentes.
* Considera utilizar GitHub desde el navegador.
* Considera utilizar HTTPS para la duración del evento.
* Cierra sesión al finalizar.

