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

- @aliabdulhadi_8 C5 (REPETIDO) — media_id 18106163105051464 — https://www.instagram.com/p/DbEivZVm9_7/ — INCIDENCIA: progreso.json estaba desactualizado (seguia en ali_s8t=4/hoy.ali_s8t=2 pese a que C3, C4 y C5 ya estaban publicados hoy segun este log). Esta corrida calculo clave c05 con el contador viejo y republico el mismo contenido de C5 (mismo caption, mismo carrusel), creando un post duplicado nuevo (media_id distinto del original 17924569731390908). Se corrigio el estado a ali_s8t=5 y hoy.ali_s8t=4 (cuota de hoy ahora completa) para que la proxima corrida tome c06 sin saltarselo. Revisar por que las corridas de C3/C4/C5 no dejaron progreso.json actualizado.
