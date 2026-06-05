# Git

Git es un sistema de control de versiones que permite registrar cambios en el código, colaborar con otras personas y recuperar versiones anteriores del proyecto.

## Clonar un repositorio

Descarga una copia local del repositorio.

```bash
git clone https://github.com/organizacion/proyecto.git
```

## Configurar nombre y correo

Después de clonar el repositorio, configura tu identidad para que los commits queden asociados correctamente a tu cuenta.

```bash
git config user.name "Tu Nombre"
git config user.email "tucorreo@ejemplo.com"
```

Verificar la configuración actual:

```bash
git config --list
```

## Ver estado

Muestra archivos modificados y cambios pendientes.

```bash
git status
```

## Agregar cambios

Prepara todos los archivos modificados para el próximo commit.

```bash
git add .
```

Agregar un archivo específico:

```bash
git add archivo.txt
```

## Crear commit

Guarda un conjunto de cambios en el historial.

```bash
git commit -m "Descripción de los cambios"
```

## Obtener cambios remotos

Descarga cambios desde GitHub.

```bash
git pull
```

## Enviar cambios

Publica cambios en GitHub.

```bash
git push
```

## Ver historial

Muestra los commits realizados.

```bash
git log --oneline
```

## Flujo habitual

```text
Modificar archivos
↓
git add
↓
git commit
↓
git push
```

## Computadoras compartidas

Si estás utilizando una computadora del aula o un equipo que no te pertenece, se recomienda utilizar GitHub desde el navegador o autenticación temporal.

Evita guardar credenciales permanentes o tokens personales en equipos compartidos.

Al finalizar la jornada:

- Cierra sesión en GitHub.
- Elimina credenciales almacenadas.
- Elimina claves SSH temporales si fueron creadas para el evento.


