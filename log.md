# Log de publicaciones

## 2026-07-20 (corridas locales, antes de migrar a la nube)

- @s8tracker C1 (datos) — https://www.instagram.com/p/DbBV_M-m9VF/
- @s8tracker C31 (software) — https://www.instagram.com/p/DbB4yqznQEr/
- @academiaseccion8 A1 (propio) — https://www.instagram.com/p/DbBp0bBHWbl/
- @academiaseccion8 C1 (S8T) — https://www.instagram.com/p/DbB-UTQm0O6/
- @aliabdulhadi_8 C1 — https://www.instagram.com/p/DbBpXOsnVKM/
- @aliabdulhadi_8 C2 — https://www.instagram.com/p/DbB-VEwG3Mv/
- INCIDENCIA: primer intento de C1 en @aliabdulhadi_8 fallo (catbox caido, Meta rechazo el contenedor). Contadores intactos, reintento exitoso en la corrida siguiente.

## 2026-07-21

- @aliabdulhadi_8 C3 — media_id 18105023242869860 — https://www.instagram.com/p/DbDrx7hoPMt/
- @aliabdulhadi_8 C4 — media_id 18386506651201978  — https://www.instagram.com/p/DbD5cUNIIZO/

- @s8tracker C02 (datos) — media_id 18104151353164161 — https://www.instagram.com/p/DbD6jXJoBpr/

- @aliabdulhadi_8 C5 — media_id 17924569731390908 — https://www.instagram.com/p/DbEOMA-nePy/

- @academiaseccion8 C2 (S8T) — media_id 18025018166846587 — https://www.instagram.com/p/DbEObmOG4kM/

- @s8tracker C32 (software) — media_id 18092501363527975 — INCIDENCIA: primer intento de contenedor fallo (Meta no pudo obtener zug1wc.jpg desde catbox), reintento inmediato exitoso — https://www.instagram.com/p/DbEc7HjG9TN/

- @academiaseccion8 A2 (propio) — media_id 17935492401091709 — https://www.instagram.com/p/DbEi9XzmzhE/

## 2026-07-22

- INCIDENCIA (ig-ali-s8t-4x): intento de publicar c05 en @aliabdulhadi_8 (ig_user_id 27502321802724366) fallo en INSTAGRAM_CREATE_CAROUSEL_CONTAINER, antes de crear el primer child container. Error Meta: code 100, subcode 33 — "Object with ID '27502321802724366' does not exist, cannot be loaded due to missing permissions, or does not support this operation". Las 7 imagenes de c05 SI cargaban (HTTP 200 verificado por curl antes del intento). La cuenta conectada en Composio (alias instagram_gammer-soiled) figura con account_type PRIVATE — la API de Instagram Graph exige cuenta Business o Creator para INSTAGRAM_CREATE_CAROUSEL_CONTAINER; revisar en Meta Business Suite si @aliabdulhadi_8 sigue como Business/Creator y si el token conectado en Composio tiene el permiso instagram_content_publish.
- DISCREPANCIA CRITICA DETECTADA (no resuelta, no se toco progreso.json): progreso.json marca ali_s8t=4 (siguiente=c05), pero este mismo log.md ya registra @aliabdulhadi_8 C5 publicado el 2026-07-21 (media_id 17924569731390908, https://www.instagram.com/p/DbEOMA-nePy/). Es decir, C5 ya estaba en vivo antes de este intento — el contador global deberia estar en 5 y el siguiente carrusel real seria c06, no c05. Se requiere que Ali confirme el valor correcto de ali_s8t antes de la proxima corrida para evitar publicar contenido duplicado o saltarse un carrusel.
- Contadores de progreso.json (globales y de hoy) NO modificados por esta corrida.
