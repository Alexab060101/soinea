# Registro de cambios de soinea.ch

| Fecha | Qué | Quién lo pidió |
|---|---|---|
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
