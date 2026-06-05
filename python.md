# Python

## Entorno Virtual (venv)

Permite aislar las dependencias de un proyecto Python para evitar conflictos con otras aplicaciones instaladas en el sistema.

Es una práctica recomendada para cualquier proyecto que utilice bibliotecas externas.

Muchas aplicaciones Python requieren instalar dependencias adicionales (Flask, FastAPI, Pandoc, OpenCV, etc.), por lo que se recomienda trabajar dentro de un entorno virtual.

## Verificar instalación

```bash
python --version
```

## Crear entorno virtual

```bash
python -m venv .venv
```

## Activar entorno

### Linux / macOS

```bash
source .venv/bin/activate
```

### Windows

```cmd
.venv\Scripts\activate
```

## Instalar dependencias

```bash
pip install flask
```

## Ver dependencias instaladas

```bash
pip list
```

## Guardar dependencias

```bash
pip freeze > requirements.txt
```

## Instalar desde requirements.txt

```bash
pip install -r requirements.txt
```

## Desactivar entorno

```bash
deactivate
```

