# Plan Estratégico InBeck SRL — Gantt (estilo RIA)

Tablero estático (HTML/CSS/JS, sin backend) que muestra el Gantt del plan estratégico
2026-2027 de InBeck SRL, con la misma paleta e identidad visual del sistema interno
**RIA** (gestión de proyectos, Gantt y certificación).

Pensado para presentarse de forma remota: no depende de que RIA esté corriendo en
una máquina local, es 100% navegable desde el navegador una vez publicado.

## Contenido

- `index.html` — el tablero (lee los datos de `assets/data.json`)
- `assets/data.json` — los 2 ejes estratégicos, 8 iniciativas y sus acciones
- `assets/logo-inbeck.png` — logo de InBeck SRL

Click en cualquier barra del Gantt para desplegar el detalle de la iniciativa
(descripción, resultados esperados, recursos y acciones con responsable y fechas).

## Cómo publicarlo en GitHub Pages

1. Creá un repositorio nuevo en GitHub (por ejemplo `plan-estrategico-inbeck`), público.
2. Subí el contenido de esta carpeta a la rama `main`:

   ```bash
   cd ruta/a/esta/carpeta
   git init
   git add .
   git commit -m "Plan estratégico InBeck - Gantt estilo RIA"
   git branch -M main
   git remote add origin https://github.com/TU-USUARIO/plan-estrategico-inbeck.git
   git push -u origin main
   ```

   (Esta carpeta ya viene con un repo git inicializado y el primer commit hecho —
   solo hace falta el paso de `git remote add` y `git push`.)

3. En GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a
   branch → Branch: `main` / `/(root)`** → Save.
4. En un minuto queda publicado en:
   `https://TU-USUARIO.github.io/plan-estrategico-inbeck/`

## Actualizar datos

Todo el contenido del Gantt sale de `assets/data.json`. Para modificar fechas,
responsables o acciones, editá ese archivo (es JSON plano) y volvé a hacer
`git add . && git commit -m "actualizo datos" && git push`.
