# Registro de cambios de soinea.ch

| Fecha | Qué | Quién lo pidió |
|---|---|---|
| 2026-08-24 | Texto **À propos** corregido por Andrea (incluye su diploma en reprogramación postural global, principios de 2026, y las plantillas ortopédicas). Ilustraciones propias de posturología en SVG. Botón de reserva de Posturología apuntando a su prestación real. | Andrea, WhatsApp del 20/08/2026 |
| 2026-08-17 | Fuera masajes y CrossFit Poya. En su sitio, **Posturologie** (`posturologie.html`). Un solo lugar: Physio Cuennet MIC, Marly. Horario **Lu · Ma · Me 8h – 19h** (fuera el sábado) en toda la web. | Andrea, WhatsApp del 12/08/2026 |

## Detalle del 17/08/2026

- `massages.html` borrada; redirección 301 de `/massages.html` a `/posturologie.html`
  en `vercel.json` para no perder lo que Google ya tenía indexado.
- Menú, pie de página, sitemap y datos estructurados actualizados en las 7 páginas.
- El horario y los precios reales los lleva Andrea en su agenda de `agenda.ch`.
  Lo que hay en la web es solo el rótulo del horario; el botón de reserva de
  Posturología apunta a la raíz de su agenda (`companyId=18640`), no a un grupo
  concreto, porque ella aún no ha creado la prestación allí.
- La foto de Posturología es provisional (`/assets/podologie-cabinet.webp`):
  falta una suya.
- `?v=` de `styles.css` y `motion.js` subido a `20260817`; sin eso el navegador
  serviría el CSS y el JS viejos durante un año (`vercel.json` los marca
  `immutable`).

## Detalle del 24/08/2026

- **À propos** (`index.html`): sustituido por el texto que envió Andrea el 20/08 ya corregido.
  Entra su diploma en reprogramación postural global (principios de 2026) y las plantillas
  ortopédicas a medida, que no estaban.
- **Ilustraciones propias, en SVG vectorial** (`assets/posture-*.svg`), dibujadas con la paleta
  de la web. Sustituyen a la foto provisional del gabinete. Andrea había mandado capturas de
  Google Imágenes como referencia: tienen derechos, no se podían publicar.
  - `posture-card.svg` — silueta sobre fondo oscuro, para la tarjeta de la portada.
  - `posture-axes.svg` — comparativa desequilibrio / alineación, para pantalla ancha.
  - `posture-axes-mobile.svg` — la misma, apilada, para móvil (`.posture-wide` /
    `.posture-tall` conmutan en `max-width:820px`). En una sola imagen lado a lado el
    móvil no dejaba leer nada.
- Sección nueva **«Ce que veut dire être aligné»** (`#principe`) en `posturologie.html`,
  con los SVG en línea para que hereden la tipografía de la web.
- **Botón de reserva** de Posturología: ahora apunta a la prestación que Andrea ya tiene
  creada, *Étude de la marche* (60 min, 130 CHF, grupo PODOLOGIE):
  `book.agenda.ch/services/pick/group/15023/111216?companyId=18640`.
  El registro del 17/08 decía que aún no existía; comprobado contra su agenda, sí existe.
  Si ella prefiere una prestación aparte «Posturologie», se cambia el enlace y ya está.
- FAQ y datos estructurados de `posturologie.html`: pregunta nueva sobre quién realiza el
  bilan, con su titulación.
- `?v=` subido a `20260824` en las 7 páginas.

## 24/08/2026 · versión v2 (propuesta, NO publicada como principal)

Rediseño en archivos aparte: `*-v2.html` + `styles-v2.css`. La web que ve el
público (`soinea.ch`) **no se ha tocado**. Las v2 llevan `noindex` para que
Google no las tome como contenido duplicado.

Qué cambia:

- **Hero.** La foto del gabinete es azulada y fría y chocaba con el crema de la
  marca: se calienta por CSS (`filter`). Velo rehecho con viñeta, que el titular
  competía con la silla. El logo «soinea» era ilegible sobre la foto: ahora es
  claro mientras el header va encima del hero (acotado con `:has(.hero)`, porque
  en las páginas interiores el fondo es crema).
- **El subtítulo y los botones del hero dependían de que el JS pusiera `.hero.in`.**
  Si el JS tarda, el hero se queda sin llamada a la acción. Ahora entran con
  animación CSS propia y son visibles aunque el JS no llegue.
- **Barra de reserva fija en móvil** (`Prendre rendez-vous` + `Appeler`). Es un
  negocio de citas: en el móvil el botón debe estar siempre a mano.
- **Tarjetas de servicio:** el velo oscuro subía demasiado y apagaba la foto.
- **La tarjeta «Parlons-en» era una 4ª tarjeta huérfana** en su propia fila:
  pasa a banda ancha con teléfono.
- **Años de experiencia: 18 → 7.** El texto de la propia Andrea dice que ejerce
  desde 2019.
- **Fuera los avis inventados.** Eran tres testimonios con nombres falsos
  («Marie L.», «Thomas B.», «Christine M.») y fotos de stock de Pexels,
  presentados como pacientes reales del cantón. En Suiza eso es competencia
  desleal (LCD). En su lugar, «Comment ça se passe»: tres pasos reales de una
  sesión. Si Andrea quiere reseñas, que sean las suyas de Google.
- Foco visible en teclado, sombras y radios afinados.
