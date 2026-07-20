# s8-carruseles-cdn

Estado en la nube del pipeline de publicacion en Instagram (S8Tracker + Academia Seccion 8).
Existe para que las tareas programadas NO dependan de archivos en la Mac de Ali.

## Archivos

- `urls.json` — 90 claves (`c01`..`c60` = S8Tracker, `a01`..`a30` = deck propio AS8). Cada valor es la lista de IDs de catbox EN EL ORDEN DE LOS SLIDES. La URL completa se arma como `https://files.catbox.moe/{id}.jpg`. 680 imagenes, todas verificadas a 1080x1350.
- `captions.json` — el caption de cada carrusel, misma clave. Los `\n` son saltos de linea reales.
- `progreso.json` — contadores. `datos`/`software`/`as8_propio`/`as8_s8t`/`ali_s8t` = ultimo carrusel publicado de cada serie. El bloque `hoy` lleva la cuota del dia y se resetea cuando cambia `fecha`.
- `log.md` — bitacora de publicaciones e incidencias.

## Reglas

- 1 carrusel por corrida, nunca dos.
- Los contadores SOLO suben si el publish fue exitoso; si falla, no se tocan y la siguiente corrida reintenta el mismo carrusel.
- Cuotas diarias: @s8tracker 2, @academiaseccion8 3, @aliabdulhadi_8 4.
