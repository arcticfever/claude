---
name: propuesta
description: Armar una propuesta de Arctic Fever para un cliente, de principio a fin. Usar cuando Esteban pide una propuesta, cotización, "qué le ofrecemos a X", o comparte un transcript de junta, un chat de cliente o una solicitud de rediseño/branding/iguala. Cubre análisis, oferta con el catálogo de Odoo, edición del deck en Figma Slides, líneas para Odoo y correo de envío.
---

# Propuesta Arctic Fever

## 1. Entender al cliente

1. Lee el material que comparta Esteban (transcript, chat, notas) y el archivo `clientes/<cliente>.md` si existe.
2. Saca de ahí, con citas textuales cuando se pueda:
   - Qué pidió el cliente con sus palabras y cuál es el problema real detrás.
   - Quién decide y quién propone.
   - Presupuesto, ciclo de presupuesto, urgencia y fechas.
   - Proveedor actual y contra qué nos van a comparar.
   - Historia con nosotros: propuestas previas, qué se aceptó, qué se cayó y por qué.
3. Si es cliente recurrente, revisa `referencias/precios.md` para calibrar precio y tono.

## 2. Armar la oferta

1. Usa solo productos de `catalogo/odoo_productos.csv` (tipo = servicio). Nombre exacto, precio de lista.
2. Agrupa partidas en 2 o 3 etapas con nombre claro para el cliente (ej. "Mensaje y Arquitectura", "Diseño Web"). Cada etapa lista qué partidas de Odoo la componen.
3. Ofrecimientos fijos del estudio:
   - **Proyecto** (branding, web, manual de comunicación, campañas, etc.) armado con partidas.
   - **Iguala mensual** con partidas mensuales (Producción Mensual de Contenido, Newsletter, Post, Junta Quincenal) o tiers Partners (Inicial $14,352 · Transformación $28,704 · Boost $47,840).
4. Evita ofrecer lo que el cliente dijo que no le toca decidir (ej. en Cleber, arquitectura de marca era de Marketing, no de Desarrollo Organizacional).
5. Si el cliente es sensible a precio o ya se fue por una propuesta cara, propón un solo proyecto cerrado, sin iguala ni upsell.
6. Calcula: subtotal, descuento (si aplica), IVA 16% y total. Verifica la suma con Python antes de ponerla en slides.
7. Registra supuestos que no salen del material (plazos mínimos, SLA, número de piezas, herramienta) y díselos a Esteban al final para que los valide.

## 3. Deck en Figma Slides

Archivo `DwUyxMm9NaePTXl0wmOfmW`. Carga antes la skill `figma-use` y `figma-use-slides` del servidor de Figma.

**Flujo:** Esteban duplica la fila del cliente anterior y la renombra con el cliente nuevo. Tú editas esa fila en su lugar. No borres slides; si sobra una, márcala como skipped. Las filas viejas quedan como skipped.

**Estructura de la fila (10 slides):**

1. Portada: "Propuesta Arctic Fever para → Cliente".
2. Carta "Hola <Nombre>!", firmada por Esteban. 3 párrafos: qué ya tiene resuelto el cliente, qué falta, qué cubre esta propuesta.
3. Clientes (no tocar).
4. Separador "01 Contexto & Necesidad" (no tocar).
5. Testimonio (no tocar salvo que Esteban pida otro).
6. Contexto y Objetivos: párrafo de contexto, cita del cliente con nombre y fecha, objetivo en una frase, tabla de 3 objetivos (número, título corto, descripción).
7. Propuesta con 2 tarjetas de etapa.
8. Propuesta con 1 tarjeta + bloque "Inversión" (Sub-total, Cliente Recurrente en naranja, Total + IVA) cuando aplica.
9. Cronograma: barras por etapa sobre grilla de semanas.
10. Desglose: tabla con partidas de Odoo, subtotal, descuento, IVA y total; a la derecha, condiciones.

**Tarjetas:** título "Etapa N · Nombre", precio "$ 25.9 K", Equipo (lista), Alcance (lista: nivel 1 = partida, nivel 2 = detalle), SLA, Entregables. Si el texto se sale de la tarjeta, recorta: máximo 4 o 5 líneas de nivel 2 por tarjeta.

**Propuestas grandes (dos proyectos o más de $400K), como Calimax:**

- Estructura v5 (Calimax, sep 2026), basada en el SOW de Brands&People pero con branding de Arctic: portada de alcance después de la portada; "Líneas de acción" con fotos antes de hablar de precio; separador con número y color por proyecto; una tabla por proyecto (columnas = fases; filas = inversión, incluye, tiempo, responsable, entregable con formato; total abajo); tabla de opcionales; "Resumen de propuesta" con una fila por proyecto; términos y condiciones en cuadrícula; cierre "Gracias" con aviso de confidencialidad, derechos y privacidad. El precio aparece una vez por fase y una vez en el resumen. El detalle por partida de Odoo va en la cotización formal, no en el deck.
- Un módulo regalado se muestra con precio tachado y "Incluido" en naranja (en Odoo, descuento de 100%). No usar "ajuste comercial".
- Empaques y piezas se entregan como diseño y visualización con editables en medidas estándar; planos mecánicos, salidas a imprenta y preprensa son opcionales.
- Opcionales en su propia slide, titulada "Opcionales" y marcada "Fuera del alcance", para que no se confundan con el proyecto.
- Una slide de "zoom" (detalle de una etapa) nunca lleva precios; dice "Incluido en la Etapa N".
- Equipo por fase con Strategy Lead y Project Manager; Jr. Designer en fases de diseño. Project Management va como partida en cada fase.
- Entregables concretos y contables ("12 piezas", "9 empaques", "2 guiones de 20 segundos"). Nada de "plataforma", "presentados en persona" o "calendario anual" sin decir qué incluye.
- Editables y plantillas en Illustrator e InDesign (CMYK). Nunca ofrecer Figma como formato de entrega de impresos.
- "Desglose" y "Link al desglose" solo en slides con precios.

**Detalles técnicos que ya costaron tiempo:**

- `get_metadata` no funciona en Slides. Inspecciona con scripts de `use_figma` y lee IDs de texto antes de editar.
- Fuente principal: Instrument Sans (Regular, Medium, Bold). Carga la fuente antes de editar.
- La fuente **Supply** (etiquetas W1, W2… y E1, E2… del cronograma) no se puede cargar. No cambies su texto; solo mueve u oculta esos nodos.
- El pie de página es un componente. El texto "Title of the presentation" se cambia con override por fila, nunca en el componente principal, porque cambia todas las filas. Cleber = "CLEBER", Click&Ship = "C&S", Calimax = "CALIMAX". Al terminar, revisa que los pies de la fila sigan con el nombre correcto: el 24 sep 2026 todas las filas amanecieron con "Salvaje".
- Naranja de marca: `{r:1, g:0.3725, b:0.0039}`.
- Listas con viñetas: después de cambiar `characters`, aplica `setRangeListOptions(start,end,{type:'UNORDERED'})` y `setRangeIndentation(start,end,nivel)` línea por línea.
- Cronograma: la grilla va de x=162 a x=1880 en 12 columnas. Para proyectos cortos, usa 2 columnas por semana y oculta las etiquetas sobrantes.
- Toma screenshot de cada slide editada y revisa que nada se desborde.

## 4. Cotización en Odoo (formato "Orange")

Esteban captura a mano. Entrégale, por cotización:

- Cliente con razón social exacta (ej. "Grupo Cleber, S.A. de C.V.").
- Por etapa: **Agregar una sección** con el nombre de la etapa.
- Por partida: producto (nombre exacto, con referencia si tiene, ej. "[DES-02] Campaign Rollout Toolkit"), cantidad, precio y descripción en bloque de código para copiar. La descripción va en líneas cortas, una idea por línea, y termina con "ETD X semanas" o "2 Rondas de revisión".
- **Agregar una nota** al final con tiempos totales y lo que no incluye.
- Subtotal, IVA y total esperados para que los verifique.

Avisos recurrentes:

- La iguala va en otra cotización con Plan recurrente Mensual; los productos deben tener "Recurrente" activado.
- Si el cliente tiene RFC, desmarca "CFDI para público en general".
- Al buscar "Post" aparecen también "Post Producción"; el correcto es el de $1,169.11.

## 5. Correo de envío

Correo (no WhatsApp), firmado por Esteban, con CC a quien corresponda (Paola, Frida). Estructura:

1. Saludo y referencia a la conversación previa.
2. Qué entendimos que necesitan, con sus palabras.
3. Etapas en lista numerada, una línea cada una, con tiempo total.
4. Inversión total (con descuento si aplica) y dónde está el desglose.
5. Siguiente paso concreto (junta de 20 minutos, presentar a quién).

## 6. Cierre de sesión

Actualiza `clientes/<cliente>.md` (qué se propuso, montos, supuestos pendientes, estado) y agrega la propuesta a `referencias/precios.md`. Commit y push.
