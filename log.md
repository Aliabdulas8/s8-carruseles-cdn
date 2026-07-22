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

- @academiaseccion8 C03 (S8T) — media_id 18421200121199023 — https://www.instagram.com/p/DbGXxBFG3tZ/

- ⚠️ @aliabdulhadi_8 c05 (SEGUNDA VEZ, DUPLICADO) — media_id 18061639139509290 — https://www.instagram.com/p/DbGeXn4IKRT/ — INCIDENCIA GRAVE: esta corrida de ig-ali-s8t-4x siguio el PASO 1 al pie de la letra (solo leyo progreso.json/urls.json/captions.json, sin revisar log.md) y por eso no vio la discrepancia critica anotada arriba en esta misma fecha. Con progreso.json todavia en ali_s8t=4, calculo clave=c05 y publico contenido IDENTICO al que ya esta en vivo desde 2026-07-21 (@aliabdulhadi_8 C5, media_id 17924569731390908, https://www.instagram.com/p/DbEOMA-nePy/). Resultado: c05/C5 esta publicado DOS VECES en @aliabdulhadi_8. CORRECCION aplicada en esta misma corrida: progreso.json ali_s8t corregido de 4 a 5 (refleja que C1-C5 ya estan publicados), para que la proxima corrida continue en c06 y no repita ni salte un carrusel. hoy.ali_s8t = 1 (esta publicacion si cuenta para la cuota diaria, aunque el contenido sea duplicado). PENDIENTE PARA ALI: decidir si borrar manualmente una de las dos copias de c05/C5 en @aliabdulhadi_8.
- INCIDENCIA (ig-s8tracker-datos-11am): intento de publicar c03 (serie datos) en @s8tracker (ig_user_id 36983453964636633) fallo en INSTAGRAM_CREATE_CAROUSEL_CONTAINER, antes de crear el primer child container. Error Meta: code 100, subcode 33 — "Object with ID '36983453964636633' does not exist, cannot be loaded due to missing permissions, or does not support this operation". Mismo patron de error que el incidente de @aliabdulhadi_8 registrado arriba en esta misma fecha (cuenta conectada en Composio sin los permisos/tipo de cuenta correctos). Revisar en Meta Business Suite que @s8tracker (cuenta Composio "instagram_stere-gogo") siga como cuenta Business/Creator vinculada a una Pagina de Facebook, y que el token conectado en Composio tenga el permiso instagram_content_publish. Contadores de progreso.json (globales y de hoy) NO modificados por esta corrida. La siguiente corrida reintenta el mismo carrusel (c03).

- @aliabdulhadi_8 c06 (C6) — media_id 18167332672453854 — https://www.instagram.com/p/DbGy6cDnRTm/ — verificado con log.md antes de calcular clave (C1-C5 ya publicados, c06 es el siguiente correcto). ali_s8t 5->6, hoy.ali_s8t 1->2.
