# subasta-salvaje-public

Fotos públicas de las **partidas del sistema** de [Subasta Salvaje](https://github.com/ElMaxter99/subasta-salvaje), servidas por [jsDelivr](https://www.jsdelivr.com/).

> **Este repositorio lo rellena la aplicación.** El superadmin arrastra imágenes en `/admin/plantillas` y la app las sube aquí con la API de contenidos de GitHub. No edites ni borres archivos a mano salvo para retirar una imagen que ya no se use.

## Estructura
```
plantillas/<slug-de-la-plantilla>/<tipo>-<nombre>-<hash>.webp
```
- `<tipo>`: `cover` (portada de la tarjeta, ≤ 1200×630), `scene` (casa inicial, ≤ 1536×1024) o `item` (foto de un elemento del catálogo, ≤ 768×768).
- `<hash>`: los 12 primeros caracteres del SHA-256 del contenido. Misma imagen = mismo nombre: no se duplica y un archivo **nunca cambia** de contenido.
- Todas son **WebP** en el *formato interno* de la aplicación (sin metadatos EXIF/GPS; ver `docs/IMAGEN-INTERNA.md` del proyecto principal).

## Cómo se enlazan
La app guarda enlaces **fijados al commit**, que se sirven al instante y no caducan:

```
https://cdn.jsdelivr.net/gh/ElMaxter99/subasta-salvaje-public@<commit>/plantillas/<slug>/<archivo>.webp
```
Evita enlazar `@master`: jsDelivr cachea las ramas durante horas.

## Configuración de la app (Vercel)
```
GITHUB_ASSETS_REPO=ElMaxter99/subasta-salvaje-public
GITHUB_ASSETS_BRANCH=master        # la rama por defecto de este repositorio
GITHUB_ASSETS_TOKEN=…              # token FINO de GitHub, solo para este repositorio, permiso «Contents: Read and write»
```
El token es un secreto: solo en Vercel, nunca en este repositorio.

## Reglas del contenido
- Solo imágenes **propias, con licencia o generadas** para el proyecto.
- **Sin fotos de personas** ni datos personales.
- Todo lo que se sube aquí es **público** y lo sirve un tercero (jsDelivr).

## Autoría y licencia
Autor: [ElMaxter99](https://github.com/ElMaxter99). La licencia de las imágenes **está por decidir por el propietario**; hasta entonces no se concede ninguna licencia adicional más allá de su uso dentro de Subasta Salvaje.
