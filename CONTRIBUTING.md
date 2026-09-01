# Cómo colaborar — guía paso a paso

Esta guía asume que nunca usaste GitHub. Seguí los pasos en orden la primera
vez; después vas a hacerlo automático.

## 0. Una sola vez: cloná el repositorio

```bash
git clone https://github.com/ORGANIZACION/la-filiberta.git
cd la-filiberta
```

(Cambiá `ORGANIZACION` por el usuario u organización real de GitHub donde
viva el repositorio.)

## 1. Creá tu rama

Nunca trabajes directo sobre `main`. Antes de tocar cualquier archivo:

```bash
git checkout main
git pull origin main
git checkout -b equipo-nombre/seccion
```

Ejemplo: `git checkout -b equipo-rocket/galeria`

## 2. Hacé tus cambios

Editá los archivos que te tocaron (por ejemplo, `css/galeria.css` o tu
tarjeta dentro de `index.html`). Guardá seguido.

## 3. Guardá el avance con commits

```bash
git add .
git commit -m "Agrego tarjeta de proyecto del equipo Rocket"
```

Un buen mensaje de commit dice **qué** cambiaste, en pocas palabras.

## 4. Subí tu rama a GitHub

```bash
git push origin equipo-rocket/galeria
```

La primera vez, GitHub te va a dar un link para abrir el pull request
directamente en la terminal.

## 5. Abrí el Pull Request (PR)

1. Entrá al repositorio en GitHub.
2. Vas a ver un botón **"Compare & pull request"** — hacé clic.
3. Escribí un título corto y, si hace falta, una línea explicando qué hiciste.
4. Confirmá con **"Create pull request"**.

## 6. Pedí revisión

Avisale a tu equipo (o al profe) que el PR está listo. Alguien más lee los
cambios y comenta si hay que ajustar algo, antes de fusionar.

## 7. Fusioná a main

Cuando el PR está aprobado, hacé clic en **"Merge pull request"**. Recién ahí
tus cambios pasan a formar parte de la página real.

## Si aparece un conflicto

Un conflicto pasa cuando dos personas cambiaron las mismas líneas del mismo
archivo. GitHub te va a avisar en el PR. Para resolverlo:

```bash
git checkout main
git pull origin main
git checkout equipo-rocket/galeria
git merge main
```

Git va a marcar las líneas en conflicto directamente en el archivo, con algo así:

```
<<<<<<< HEAD
tu versión
=======
la versión de main
>>>>>>> main
```

Elegí qué versión (o combinación de ambas) dejar, borrá esas marcas, y volvé
a hacer commit y push:

```bash
git add .
git commit -m "Resuelvo conflicto en galeria.css"
git push origin equipo-rocket/galeria
```

## Convención de nombres de rama

`equipo-<nombre>/<seccion>` — por ejemplo:

- `equipo-rocket/galeria`
- `equipo-pixel/sustentabilidad`
- `equipo-byte/hero`

Así queda claro quién trabaja en qué, con solo mirar la lista de ramas.
