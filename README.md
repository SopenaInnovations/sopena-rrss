# Social Media Tracker · Grupo Sopena

App interna para seguimiento de redes sociales (Instagram, Facebook, LinkedIn): métricas, gráficas, análisis anual, planificación de contenido con calendario, banco de ideas y exportación del plan a PDF.

## ⚠️ Sobre la seguridad del login

Esta app usa un login simple (usuario/contraseña) hecho en JavaScript del lado del cliente. Es **suficiente para evitar que alguien entre por casualidad**, pero **NO es una protección real**: cualquier persona con conocimientos básicos puede ver el usuario y contraseña abriendo el código fuente de la página (botón derecho → "Ver código fuente", o las herramientas de desarrollador del navegador).

**No subas aquí información realmente sensible** (contraseñas de otras cuentas, datos bancarios, etc.). Para una app interna de seguimiento de métricas de redes sociales, este nivel de protección es razonable.

## Cómo cambiar el usuario y contraseña

Abre `index.html`, busca estas líneas casi al principio del `<script>` final:

```js
const APP_USER = "sopena";
const APP_PASS = "rrss2026";
```

Cámbialas por lo que quieras y guarda el archivo. Vuelve a subir el cambio a GitHub (ver pasos abajo).

## Cómo publicar en GitHub Pages

### 1. Crear el repositorio
1. Ve a [github.com/new](https://github.com/new)
2. Nombre del repositorio: por ejemplo `sopena-rrss-tracker`
3. Márcalo como **privado** si quieres que el código no sea visible públicamente (aunque la web seguirá siendo accesible para quien tenga el enlace, si activas Pages)
4. Crea el repositorio sin añadir README (ya tienes uno)

### 2. Subir los archivos
Desde tu ordenador, en la carpeta donde tengas estos archivos:

```bash
git init
git add .
git commit -m "Primera versión de la app"
git branch -M main
git remote add origin https://github.com/TU_USUARIO/sopena-rrss-tracker.git
git push -u origin main
```

(Sustituye `TU_USUARIO` por tu nombre de usuario de GitHub)

### 3. Activar GitHub Pages
1. En tu repositorio, ve a **Settings** (Configuración)
2. En el menú lateral, click en **Pages**
3. En "Source", selecciona la rama `main` y la carpeta `/ (root)`
4. Guarda. En unos minutos tu app estará en:
   `https://TU_USUARIO.github.io/sopena-rrss-tracker/`

### 4. Acceder
Abre esa URL, introduce el usuario y contraseña que configuraste, y listo.

## Notas sobre los datos

- Los datos (métricas, publicaciones, ideas) se guardan en el **almacenamiento local del navegador** (`localStorage`).
- Esto significa que **los datos son distintos en cada ordenador/navegador** donde abras la app. Si entras desde el móvil y luego desde el ordenador, no verás lo mismo.
- Si borras el historial/caché del navegador, perderás los datos guardados.
- Para tener los datos sincronizados entre dispositivos haría falta una base de datos en la nube (por ejemplo Firebase, como en tu otra app de control de chapas) — dime si quieres que lo preparemos así en el futuro.

## Repositorios relacionados

Si quieres reutilizar la cuenta de Firebase que ya tienes en `sopena-chapas` para sincronizar estos datos entre dispositivos en vez de usar localStorage, es un cambio que se puede hacer más adelante.
