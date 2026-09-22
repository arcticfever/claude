# Arctic Fever · Memoria del estudio

Este repo es la memoria de trabajo de Arctic Fever (AF Estudio Creativo), estudio de branding y diseño estratégico en San Pedro Garza García. Lo usa Esteban Villarreal (founder) para que cada sesión arranque con el contexto del estudio sin tener que explicarlo otra vez.

Antes de cualquier tarea de propuestas, cotizaciones o clientes, lee lo que aplique de aquí abajo.

## Dónde está cada cosa

| Archivo | Qué contiene |
|---|---|
| `catalogo/odoo_productos.csv` | Lista de servicios de Odoo con precio de venta (export del 22 sep 2026). Es la única fuente válida de servicios y precios. |
| `referencias/precios.md` | Propuestas anteriores con montos, estructura y resultado. Sirve para calibrar precio. |
| `clientes/*.md` | Un archivo por cliente: contactos, historia, qué se propuso, montos, pendientes. |
| `.claude/skills/propuesta/SKILL.md` | Proceso completo para armar una propuesta: análisis, Figma, Odoo y correo. |

## Equipo

- **Esteban Villarreal**, Founder. Firma las cartas de las propuestas.
- **Paola Méndez Gutiérrez**, Studio Manager / Operaciones. Socia con 20%. Captura y envía cotizaciones en Odoo.
- **Frida González**, lleva juntas de descubrimiento con clientes (por ejemplo Cleber).

## Herramientas

- **Figma Slides**, archivo de propuestas: `DwUyxMm9NaePTXl0wmOfmW` ("Arctic Fever_Propuesta de Inversión"). Una fila por cliente, la más reciente arriba. Detalles de edición en la skill `propuesta`.
- **Odoo**, `arctic-fever.odoo.com`, compañía AF ESTUDIO CREATIVO. No hay conector de Odoo en las sesiones: las cotizaciones se capturan a mano con el texto que se prepara aquí. La importación por archivo falló una vez; no volver a intentarla sin revisar nombres exactos de cliente y producto.
- Conectores disponibles normalmente: Figma, Gmail, Google Drive, Google Calendar, Slack.

## Reglas que no cambian

1. **Solo se ofrecen servicios del catálogo de Odoo**, con su nombre y precio de lista. Se puede adaptar la descripción al cliente, no inventar servicios ni paquetes.
2. **Precios sin IVA** en las slides; IVA 16% en el desglose. En tarjetas se redondea a "$ 25.9 K"; en el desglose van los centavos exactos.
3. **Cliente recurrente**: descuento de -5% o -10%, mostrado como línea naranja entre Sub-total y Total. Así se aceptaron propuestas anteriores.
4. **Iguala / retainer** = productos Partners o partidas mensuales. Siempre en cotización separada de los proyectos en Odoo, con Plan recurrente Mensual.
5. **Escritura**: español directo, sin em dashes, sin "no es X, es Y", sin frases cortas de efecto, sin preámbulos ni cierres que repiten la idea. Suena a nota de founder, no a marketing. Las preferencias completas de Esteban viven en su perfil de claude.ai y aplican siempre.
6. **Correos a clientes, no WhatsApp**, salvo que Esteban diga otra cosa.

## Mantener esta memoria

Al terminar una sesión donde cambió algo de un cliente (propuesta enviada, precio, decisión, contacto nuevo), actualiza `clientes/<cliente>.md` y `referencias/precios.md`, haz commit y push. Si Esteban sube un export nuevo de productos de Odoo, regenera `catalogo/odoo_productos.csv`.
