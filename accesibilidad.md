# Accesibilidad Web - Guía rápida

## Idioma del documento

Permite que lectores de pantalla y navegadores interpreten correctamente el idioma principal del contenido.

```html
<html lang="es">
```

## Título descriptivo

```html
<title>Mapa Accesible de la Facultad</title>
```

## Configuración para dispositivos móviles

```html
<meta
  name="viewport"
  content="width=device-width, initial-scale=1">
```

## Estructura HTML semántica básica

Utilizar etiquetas semánticas ayuda a que lectores de pantalla, motores de búsqueda y otras tecnologías comprendan mejor la estructura del contenido.

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta
    name="viewport"
    content="width=device-width, initial-scale=1">

  <title>Mapa Accesible de la Facultad</title>
</head>

<body>

  <header>

    <nav>
        <ul>
          <li><a href="#entradas">Entradas</a></li>
          <li><a href="#rutas">Rutas</a></li>
        </ul>
  </nav>

  </header>

  <main>
    <h1>Mapa Accesible</h1>

    <section id="entradas">
      <h2>Entradas</h2>

      <article>
        <h3>Entrada Principal</h3>
        <p>Información sobre accesibilidad.</p>
      </article>
    </section>

    <section id="rutas">
      <h2>Rutas</h2>

      <article>
        <h3>Ruta Norte</h3>
        <p>Descripción de la ruta.</p>
      </article>
    </section>

  </main>

  <footer>
    <p>Facultad de Ingeniería</p>
  </footer>

</body>
</html>
```

## Estructura de encabezados

```html
<h1>Mapa Accesible</h1>

<h2>Entradas</h2>

<h2>Rutas</h2>

<h3>Ruta Norte</h3>
```

## Imágenes con texto alternativo

```html
<img
  src="rampa.jpg"
  alt="Rampa de acceso principal a la Facultad">
```

## Formularios etiquetados

```html
<label for="email">
  Correo electrónico
</label>

<input
  id="email"
  type="email">
```

## Botones descriptivos

```html
<button>
  Descargar PDF accesible
</button>
```

## Enlaces descriptivos

```html
<a href="/mapa">
  Ver mapa accesible
</a>
```

## Contraste suficiente

WCAG recomienda:

```text
Texto normal: 4.5:1 o superior

Texto grande: 3:1 o superior
```

## Revisar contraste con DevTools

```text
F12
↓
Inspect
↓
Seleccionar texto
↓
Styles
↓
Color Picker
↓
Contrast Ratio
```

## Navegación con teclado

Verificar:

```text
Tab
Shift + Tab
Enter
Espacio
```

## Foco visible

Las personas que navegan con teclado deben poder identificar claramente dónde se encuentra el foco.

```css
:focus {
  outline: 2px solid currentColor;
}
```

## Zoom

Comprobar al menos:

```text
200%
```

sin pérdida significativa de funcionalidad.

## Mensajes claros

Ejemplos:

```text
Correo electrónico obligatorio.

La contraseña debe tener al menos 8 caracteres.
```

## Auditoría rápida

```text
F12
↓
Lighthouse
↓
Accessibility
↓
Generate report
```

## Checklist antes de la demo

```text
✓ lang="es"
✓ title descriptivo
✓ viewport configurado
✓ encabezados organizados
✓ imágenes con alt
✓ formularios etiquetados
✓ botones descriptivos
✓ enlaces descriptivos
✓ contraste suficiente
✓ navegación con teclado
✓ foco visible
✓ zoom al 200%
```

