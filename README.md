# subasta-salvaje-public

Almacén público de **imágenes para las partidas predefinidas** de [Subasta Salvaje](https://github.com/ElMaxter99/subasta-salvaje), un juego de subastas creativas gratuito y sin ánimo de lucro.

## Para qué sirve este repositorio
Este repositorio **solo existe para alimentar las partidas del sistema**: partidas ya preparadas por el administrador, por ejemplo *«Halloween 1»*, *«Halloween 2»*, *«Casa encantada»*, *«Batido»*… Cada vez que el administrador crea o modifica una de esas partidas y arrastra sus imágenes (portada, imagen inicial de la casa y fotos de los elementos), la aplicación las sube aquí y las sirve a través de [jsDelivr](https://www.jsdelivr.com/).

- **No tiene ningún fin comercial:** el proyecto es gratuito, sin publicidad, sin ventas ni cobros de ningún tipo. No se obtiene dinero con estas imágenes.
- **Es público:** todo lo que hay aquí puede verlo cualquiera.
- **Cambia con el uso:** su contenido varía según las partidas que el administrador vaya creando, retocando o retirando. No es un archivo estable ni un recurso para reutilizar.
- **Lo escribe la aplicación:** los commits los genera la propia app al subir imágenes. No hace falta tocar nada a mano.

## Origen y derechos de las imágenes
Las imágenes **pueden proceder de terceros** (buscadores, webs, bancos de imágenes o generadas con IA) y las selecciona el administrador **para ilustrar partidas dentro del juego**.

- **No se reclama ningún derecho** sobre ellas: pertenecen a sus respectivos titulares.
- **No se concede ninguna licencia** sobre su contenido y **no se garantiza** que estén libres de derechos.
- Su uso aquí se limita a ilustrar las partidas de Subasta Salvaje; **no están pensadas para reutilizarse, copiarse ni redistribuirse**.
- Cuando se conoce la fuente o la licencia de una imagen, se anota en [`FUENTES.md`](FUENTES.md).

## Si eres titular de una imagen y quieres que se retire
Abre un *issue* en este repositorio indicando la imagen (su ruta) y que eres su titular, o escribe a [@ElMaxter99](https://github.com/ElMaxter99) por GitHub. La imagen se retirará de las partidas y del repositorio.

## Cómo están organizadas
```
plantillas/<slug-de-la-partida>/<tipo>-<nombre>-<hash>.webp
```
- `<slug-de-la-partida>`: identificador de la partida del sistema, p. ej. `halloween-1`, `casa-encantada`.
- `<tipo>`: `cover` (portada de la tarjeta), `scene` (imagen inicial de la casa) o `item` (foto de un elemento del catálogo).
- `<hash>`: huella del contenido. La misma imagen no se duplica y un archivo **nunca cambia** una vez subido.
- Todas son **WebP** reducidas por la aplicación (sin metadatos EXIF/GPS).

## Cómo se enlazan (para quien mantenga la app)
La aplicación guarda enlaces **fijados al commit**, que se sirven al instante y no caducan:

```
https://cdn.jsdelivr.net/gh/ElMaxter99/subasta-salvaje-public@<commit>/plantillas/<slug>/<archivo>.webp
```
No uses `@master`: jsDelivr cachea las ramas durante horas. Configuración en Vercel: `GITHUB_ASSETS_REPO=ElMaxter99/subasta-salvaje-public`, `GITHUB_ASSETS_BRANCH=master` y `GITHUB_ASSETS_TOKEN` (token fino de GitHub solo para este repositorio, permiso *Contents: Read and write*; es un secreto, nunca en este repositorio).

## Reglas del contenido
- **Sin fotos de personas identificables** (ni de menores) ni datos personales.
- Sin contenido ilegal, ofensivo o que infrinja derechos de forma evidente.
- Todo lo que se sube aquí es **público**.
