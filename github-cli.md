# Guía de GitHub CLI (`gh`)

`gh` es la herramienta oficial de línea de comandos de GitHub que te permite gestionar repositorios, pull requests, issues y más directamente desde tu terminal.

---

## 1. Instalación

### Linux

Instala `gh` usando el gestor de paquetes de tu distribución:

**Ubuntu / Debian**

```bash
sudo apt update && sudo apt install gh
```

**Fedora / RHEL / CentOS**

```bash
sudo dnf install gh
```

**Arch Linux**

```bash
sudo pacman -S github-cli
```

### Windows

Abri la terminal (PowerShell o CMD) y ejecuta:

```powershell
winget install --id GitHub.cli
```

*(También podes descargar el instalador gráfico `.msi` desde [cli.github.com](https://cli.github.com)).*

---

## 2. Iniciar sesión (Autenticación)

Configura tus credenciales para conectarte a GitHub:

```bash
gh auth login
```

*Segui las instrucciones: elige `GitHub.com`, selecciona `HTTPS` o `SSH`, y completa la autenticación web o mediante token.*

Verificar el estado de tu sesión activa:

```bash
gh auth status
```

---

## 3. Trabajar con repositorios

Clonar un repositorio de GitHub:

```bash
gh repo clone organizacion/proyecto
```

Crear un nuevo repositorio público en GitHub:

```bash
gh repo create mi-proyecto --public
```

---

## 4. Pull Requests (PR)

Crear una propuesta para integrar los cambios de tu rama a `main`:

```bash
gh pr create --title "Título corto" --body "Detalles de los cambios"
```

*Consejo: Podes ejecutar solo `gh pr create` para rellenar los campos de manera interactiva paso a paso en la terminal.*

Listar los PRs activos del repositorio:

```bash
gh pr list
```

Traer la rama de un PR de un compañero para probarla localmente:

```bash
gh pr checkout <numero_de_PR>
```

Fusionar el PR actual en la rama principal:

```bash
gh pr merge
```

---

## 5. Issues (Tareas)

Crear una nueva tarea o reporte de bug:

```bash
gh issue create --title "Título de la tarea" --body "Descripción"
```

Ver las tareas que tienes asignadas:

```bash
gh issue list --assignee "@me"
```

---

## 6. Flujo habitual de trabajo

```text
Crear rama local y hacer commits
↓
Subir cambios a GitHub: git push
↓
Crear el Pull Request: gh pr create
↓
Fusionar el código tras aprobarlo: gh pr merge
```

---

## 7. Computadoras compartidas

Si estás usando un equipo público o del aula, asegúrate de borrar tu sesión al finalizar la jornada:

```bash
gh auth logout
```
