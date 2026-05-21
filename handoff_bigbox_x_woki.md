# Handoff — Pieza Bigbox × Woki

**Para:** Claude Code (implementación)
**De:** Woki Marketing
**Versión:** 1.0
**Deliverables:** (1) un email · (2) una landing page

---

## 0. Contexto y objetivo

Bigbox y Woki van a hacer una **comunicación cruzada**: Bigbox manda este email + landing a su base de restaurantes prestadores. La pieza vive del lado de Woki (Bigbox la distribuye). En paralelo, Woki hace lo simétrico hacia su base con una pieza de Bigbox (no es objeto de este handoff).

**Audiencia:** restaurantes del catálogo Bigbox en LatAm (Argentina, Chile, Uruguay, Perú, México). Mezcla heterogénea: desde cafeterías de barrio hasta fine dining con estrella Michelin. Algunos ya son clientes de Woki, la mayoría no.

**Objetivo de negocio:** que los restaurantes Bigbox que todavía no usan Woki se interesen lo suficiente para iniciar una conversación por WhatsApp.

---

## 1. Concepto rector

### Frase ancla (no negociable)

> **Bigbox te trae al cliente. Woki te ayuda a que vuelva.**

Esta frase es la columna vertebral de las dos piezas. Debe aparecer literal en al menos un lugar visible de cada una (mail y landing).

### Insight

El restaurante Bigbox ya resolvió **cómo llegar a un cliente nuevo**. Lo que no tiene resuelto — y Bigbox no resuelve por diseño — es **qué pasa después** del canje. Cada Bigbox canjeada es un cliente nuevo que, sin estrategia de retención, no vuelve. Y los números de industria muestran que ahí está el grueso de la rentabilidad.

### Los dos ejes (orden y peso)

| # | Eje | Peso | Mensaje |
|---|---|---|---|
| 1 | **Retención** | Principal | Los clientes Bigbox dejan de ser anónimos y entran a una máquina de recurrencia (perfiles, segmentación, briefs, comunicación) |
| 2 | **Operación** | Soporte | La integración nativa hace que las reservas Bigbox entren directo al panel de Woki, sin coordinación manual por WhatsApp |

**Regla:** retención siempre antes que operación. Operación es el "y además" que cierra y baja a tierra.

### Tono y posicionamiento

- **No competimos con Bigbox.** Lo complementamos. Bigbox es el partner que nos prestó la audiencia; el mensaje los respeta y los valora.
- **No descalificamos otros sistemas de reservas.** No mencionamos a Meitre, CoverManager, etc.
- **No prometemos llenar mesas.** Prometemos mejorar la hospitalidad — mesas llenas son la consecuencia, no la promesa.

---

## 2. Disciplinas comerciales (no negociables)

### 2.1 Números permitidos (los únicos)

Solo se pueden citar estos 7 datos como evidencia:

| Dato | Qué dice | Fuente a citar |
|---|---|---|
| **5% → 25–95%** | Aumento del 5% en retención puede traducirse en 25–95% más de ganancias | Bain & Company / HBR |
| **51%** | De la facturación en fine dining viene de clientes recurrentes | NRA |
| **67%** | Más gasta en promedio un cliente recurrente vs. uno nuevo | NRA |
| **+95%** | Cobrabilidad de la pasarela de pagos (la más alta de LatAm) | Dato propio Woki |
| **+700** | Restaurantes operando con Woki en Argentina, Chile y la región | Dato propio Woki |
| **72hs** | De implementación end-to-end (migración + configuración + capacitación) | Dato propio Woki |
| **Único** | Sistema integrado con la Guía Michelin en LatAm | Dato propio Woki |

### 2.2 Números prohibidos

**No usar bajo ninguna circunstancia:**
- +38% de conversión del perfil
- ROI específico de email marketing
- Mejoras de recurrencia por porcentaje
- +12% de ticket promedio
- Cualquier otro número no listado en 2.1

Si hace falta un número y no está en la tabla, **no se usa**. Se reformula la frase.

### 2.3 Lenguaje

- **Español rioplatense con voseo** (CTAs en imperativo: "Hablá con nosotros", "Conocé", "Activá").
- **Sentence case** en titulares y UI ("Cómo funciona", no "Cómo Funciona").
- **Brand terms con mayúscula:** Woki, Bigbox, Hospitality Manager, Guest Center, Guía Michelin.
- **Sin emojis** en headlines ni copy de producto. Sin emojis en el mail.
- **Sin tecnicismos:** "los clientes que vuelven" mejor que "tasa de recurrencia". Si se usa "recurrencia", explicarla.

---

## 3. Sistema de diseño (Woki B2B)

Track **B2B (azul)** — esto va a restaurantes.

### 3.1 Tokens base

Todos los tokens están en `assets/colors_and_type.css` (que se entrega junto con este handoff). Variables clave:

```css
--brand: #0066CC;          /* azul Woki celeste, accent */
--brand-dark: #132F60;     /* azul Woki primario, CTAs */
--b2b-gradient: linear-gradient(60deg, #202B3F 0%, #0066CC 100%);
--bg: #FFFFFF;             /* fondo principal */
--bg-soft: #FAF7F4;        /* off-white cálido */
--bg-muted: #F3EFEA;       /* neutro cálido más fuerte */
--fg: #212227;             /* tinta principal, casi negro */
--fg-3: #6B6C72;           /* tinta secundaria */
--border: #E8E3DD;         /* borde cálido sutil */
```

### 3.2 Tipografía

- **Mona Sans** (display) — titulares, nombres de marca, etiquetas de CTA. **Nunca para números.**
- **Figtree** (body) — todo el resto, incluidos **todos los números** (porcentajes, datos, precios, KPIs).
- Tracking: `-0.02em` para 40px+, `-0.01em` para 24–32px, normal para body.
- Line-height: display ≤1.08, body 1.5.

### 3.3 Logos disponibles

En `assets/logos/`:
- `woki-b2b-solid.svg` — uso general en fondo claro
- `woki-b2b-gradient.svg` — versiones destacadas (open graph, hero)
- `woki-b2b-white.svg` — sobre fondo oscuro o gradiente

**Logo de Bigbox:** no lo tengo en mano. Decisión pendiente (ver §7). Si se incluye, usar el oficial enviado por Bigbox, nunca uno reconstruido.

### 3.4 Botones

- **Primario:** fondo `--brand-dark` (#132F60), texto blanco, radio 12px, hover oscurece 8%.
- **Secundario:** fondo blanco, borde 1px `--brand-dark`, texto `--brand-dark`.
- **Ghost (link estilo):** texto `--brand-dark`, sin fondo, underline en hover.

### 3.5 Iconografía

**Lucide** vía CDN (`https://unpkg.com/lucide@latest`). Stroke 1.5px, line caps redondeados, color hereda `currentColor`. Nada de emojis ni unicode (✓✗★→) como íconos.

### 3.6 Sombras y radios

- Cards: `1px solid var(--border)`, radio 12px (`--r-md`), sombra `--shadow-sm` en reposo, `--shadow-md` en hover.
- Sin bordes coloreados a la izquierda en cards (anti-patrón).
- Sin texturas, sin patrones repetidos, sin ilustraciones dibujadas a mano.

### 3.7 Referencia visual

La landing actual de Woki B2B (`restaurantes.wokiapp.com`) está incluida como `index.html` en los assets. **Es la referencia principal de calidad y aire visual** para esta landing nueva. La densidad, el ritmo de secciones, las animaciones y la jerarquía deben sentirse de la misma familia.

---

## 4. EL MAIL

### 4.1 Metadata

| Campo | Valor |
|---|---|
| **De** | Bigbox (mail enviado desde su dominio habitual, sin remitente personal) |
| **Para** | Base de restaurantes prestadores de Bigbox en Argentina |
| **Asunto (principal)** | Los clientes que canjean tu Bigbox: ¿vuelven? |
| **Asunto (alternativa A)** | Bigbox te trae al cliente. ¿Qué pasa después? |
| **Asunto (alternativa B)** | El 51% que tu restaurante está dejando pasar |
| **Preheader** | En fine dining, el 51% de la facturación viene de clientes que vuelven. Te contamos cómo no perderlos. |
| **Co-branding** | Header con co-branding "Bigbox × Woki" (logos lado a lado, separador sutil) |

### 4.2 Estructura (orden y bloques)

1. Header co-branding (Bigbox × Woki)
2. Saludo + apertura (por qué Bigbox escribe sobre Woki)
3. Hook: el problema del canje sin vuelta
4. Banda de datos (2 números, no más)
5. Frase ancla
6. Tres bullets de valor (1 operación + 2 retención, en orden: integración → perfil → activación)
7. Bloque de oferta exclusiva (30 días gratis + 2 meses al 50%)
8. Reaseguro de implementación (72hs)
9. CTA único: hablar por WhatsApp
10. PD con prueba social (+700 restaurantes)

### 4.3 Copy completo (versión recomendada)

```
[Header — barra superior con co-branding]
[logo Bigbox]   ×   [logo Woki B2B]

[H1 — Mona Sans, 28–32px, --brand-dark]
Bigbox te trae al cliente.
Woki te ayuda a que vuelva.

[Párrafo 1 — Figtree 16px]
Hola,

Te escribimos desde Bigbox para contarte de Woki, una plataforma con
la que estamos integrados y que muchos de los restaurantes de nuestro
catálogo ya están usando.

[Párrafo 2 — Figtree 16px]
La razón es simple: cada vez que un cliente canjea una Bigbox en tu
restaurante, vivís una versión condensada del problema que más golpea
la rentabilidad de la gastronomía. Alguien nuevo entra, se va contento,
y muchas veces no vuelve.

[Banda de datos — 2 números, layout en dos columnas]
51%                                       5% → 25–95%
de la facturación en fine dining          de aumento en la tasa de
viene de clientes recurrentes¹            retención puede traducirse en
                                          25 a 95% más de ganancias²

[Párrafo 3 — destacado, --brand-dark, Mona Sans semibold]
Bigbox es muy bueno trayéndote ese cliente nuevo.
Woki es muy bueno ayudándote a que vuelva.

[Subtítulo]
Lo que cambia con Woki

[Bullet 1 — icono Lucide: zap o link]
La reserva Bigbox entra sola a tu panel de Woki.
Cuando alguien compra una experiencia o giftcard en Bigbox, reserva
desde ahí mismo y la reserva aparece en tu panel de Woki con el
detalle de qué compró. Sin coordinación por WhatsApp ni hilos
sueltos.

[Bullet 2 — icono Lucide: user-circle o sparkles]
El cliente Bigbox deja de ser anónimo.
Queda cargado en tu base con un perfil que se enriquece visita a
visita: preferencias, alergias, celebraciones, recurrencia.

[Bullet 3 — icono Lucide: send o mail]
Y entra a tu máquina de recurrencia.
Email y WhatsApp segmentados, briefs pre-servicio para el equipo de
sala, y alertas para que la próxima vez que aparezcan los reconozcas.

[Bloque oferta exclusiva — fondo --brand-dark, texto blanco,
 padding generoso, esquinas 12px]
[Eyebrow — uppercase blanco con opacidad 70%]
EXCLUSIVO PARA RESTAURANTES BIGBOX

[H3 — Mona Sans 24–28px, blanco]
Empezá Woki con 30 días gratis,
y 2 meses al 50% off después.

[Texto auxiliar — Figtree 14px, blanco opacidad 80%]
Una propuesta exclusiva para los restaurantes que vienen del
catálogo de Bigbox. Sin compromiso, sin contratos.

[Reaseguro — fondo --bg-soft, padding generoso]
Migrar lleva 72 horas y lo hace el equipo de Woki. Vos seguís
ocupándote del restaurante. Hoy ya hay más de 700 restaurantes
operando con Woki en la región, desde cafeterías de barrio hasta
restaurantes con estrellas Michelin.

[CTA — botón primario centrado, --brand-dark]
Hablar con el equipo por WhatsApp →

[Link real del CTA]
https://wa.me/5491176520777?text=Hola%2C%20vengo%20del%20cat%C3%A1logo%20de%20Bigbox%20y%20quiero%20saber%20m%C3%A1s%20sobre%20Woki.

[Subtexto del CTA — --fg-3, 14px, centrado]
Te contamos cómo funciona en 10 minutos.

[PD — separado, --fg-3, 14px]
PD: Woki es la plataforma de hospitalidad para los mejores
restaurantes de LatAm. La integración con Bigbox es solo uno
de los muchos canales que la nutren — el resto (perfiles
enriquecidos, comunicación segmentada, métricas, pagos) se
activa solo cuando vos decidís.

[Footnotes — --fg-3, 12px]
¹ National Restaurant Association (NRA).
² Bain & Company / Harvard Business Review.
```

### 4.4 Notas de implementación del mail

- **HTML email-friendly:** tablas para layout, estilos inline donde haga falta, fonts websafe como fallback (Arial/Helvetica) por si no cargan Mona Sans/Figtree en el cliente de mail.
- **Ancho:** 600px máximo del contenedor principal.
- **Dark mode:** que sobreviva en Gmail dark / Outlook dark. Evitar texto en `--brand-dark` sobre fondos potencialmente oscuros sin fallback.
- **Imágenes:** mínimas. El mail debe leer 100% sin imágenes (mucho usuario las bloquea). Si se usa una imagen hero, debe ser decorativa y tener alt text claro.
- **CTA:** botón táctico (no link), mínimo 44×44px de área tocable, fondo `--brand-dark`, texto blanco, padding 14px 28px, radio 12px.
- **Versión texto plano:** incluir como fallback. Mismo copy, sin maquetación.

---

## 5. LA LANDING

### 5.1 Metadata

| Campo | Valor |
|---|---|
| **URL sugerida** | `wokiapp.com/bigbox` o `restaurantes.wokiapp.com/bigbox` |
| **Title** | Woki para restaurantes Bigbox — Hacé que tus clientes vuelvan |
| **Meta description** | Bigbox te trae al cliente. Woki te ayuda a que vuelva. Integración nativa, perfiles enriquecidos, comunicación segmentada. Alta en 72hs. |
| **OG image** | Usar `assets/logos/woki-b2b-gradient.svg` o componer hero del propio sitio |
| **Favicon** | `assets/logos/woki-b2b-solid.svg` |

### 5.2 Estructura general

Diez secciones, en este orden:

1. Top nav minimal
2. Hero
3. Contexto / problema
4. Banda de datos (3 números)
5. **Eje 1 — Retención** (sección principal)
6. **Eje 2 — Operación** (sección de soporte)
7. "Y mucho más" — Woki en una vista
8. Implementación en 72hs
9. CTA final
10. Footer minimal

**Densidad:** marketing, ~96px de padding vertical entre secciones (cumplir con la base 8pt). Contenedor máximo 1200px.

---

### 5.3 Sección por sección

#### Sección 1 — Top nav

**Layout:** sticky top, fondo blanco con backdrop-blur, altura 60px, padding lateral 32px.

**Contenido:**
- Izquierda: co-branding "Logo Woki × Logo Bigbox", separados por un "×" sutil en `--fg-4` (16px alto cada logo)
- Derecha: botón CTA secundario "Escribinos" (variante ghost, link a WhatsApp `https://wa.me/5491176520777?text=...`)

**Comportamiento:** se mantiene visible al hacer scroll. El borde inferior se vuelve más visible cuando hay scroll > 10px.

---

#### Sección 2 — Hero

**Layout:** dos columnas en desktop (texto izquierda 60%, visual derecha 40%), una columna en mobile. Padding superior 96px, fondo `--bg-soft`.

**Copy:**

```
[Eyebrow — uppercase, Mona Sans 12px, letter-spacing 0.08em, --brand]
PARA RESTAURANTES DEL CATÁLOGO BIGBOX

[H1 — Mona Sans, 56–72px desktop / 32–40px mobile, --brand-dark, line-height 1.05]
Bigbox te trae al cliente.
Woki te ayuda a que vuelva.

[Subtítulo — Figtree 20px, --fg-3]
La plataforma de hospitalidad que convierte cada cliente Bigbox en
un cliente que vuelve. Integración nativa, perfiles enriquecidos
y comunicación segmentada.

[CTA principal — botón --brand-dark, 16px font, padding 16px 32px]
Hablar con el equipo por WhatsApp

[Link real]
https://wa.me/5491176520777?text=Hola%2C%20vengo%20del%20cat%C3%A1logo%20de%20Bigbox%20y%20quiero%20saber%20m%C3%A1s%20sobre%20Woki.

[CTA texto auxiliar — --fg-3, 14px]
Te contamos cómo funciona en 10 minutos.
```

**Visual derecha:** una composición simple que muestre conceptualmente la conexión Bigbox → Woki. Sugerencia: una tarjeta estilizada de reserva con badge "Bigbox" y debajo de eso un perfil de cliente enriquecido con datos (visitas, preferencias, alertas). Estilo Apple-minimalist, fondo blanco, sombra suave.

**Alternativa simple:** si la composición visual es compleja de armar, dejar solo el bloque de texto centrado horizontalmente, con más aire. Es preferible un hero limpio sin visual a un visual mediocre.

---

#### Sección 3 — Contexto / problema

**Layout:** una columna centrada, max-width 720px, padding vertical 96px, fondo blanco.

**Copy:**

```
[H2 — Mona Sans 32–40px, --brand-dark, centrado]
Cada canje es un cliente nuevo.
La pregunta es qué pasa después.

[Párrafo — Figtree 18px, --fg, centrado, line-height 1.6]
El cliente que canjea una Bigbox en tu restaurante vive una experiencia
puntual: viene una vez, se va contento, y casi siempre no vuelve.
Bigbox cumplió su parte trayéndolo. Sin una estrategia de retención
del lado del restaurante, todo ese tráfico se evapora.
```

---

#### Sección 4 — Banda de datos

**Layout:** tres columnas en desktop, una en mobile. Padding vertical 96px, fondo `--bg-soft`. Cada dato en su propia card, sin bordes, separadas por un divisor sutil vertical en desktop.

**Contenido (en este orden):**

```
[Columna 1]
51%
de la facturación en fine dining
viene de clientes recurrentes.¹

[Columna 2]
67%
más gasta un cliente recurrente
por visita que uno nuevo.¹

[Columna 3]
25–95%
más de ganancias por aumentar
la retención solo un 5%.²
```

**Tipografía de los números:** Figtree (no Mona Sans), 64–80px, `--brand-dark`, line-height 1.

**Tipografía del texto debajo:** Figtree 16px, `--fg-3`, line-height 1.5, max 3 líneas.

**Footnotes al pie de la sección (12px, `--fg-3`):**
```
¹ National Restaurant Association (NRA).
² Bain & Company / Harvard Business Review.
```

---

#### Sección 5 — Eje 1: Retención (sección principal)

**Layout:** título centrado, debajo grid de 3 cards en desktop, stack vertical en mobile. Padding vertical 96px, fondo blanco.

**Copy del header:**

```
[Eyebrow — uppercase, --brand]
RETENCIÓN

[H2 — Mona Sans 32–40px, --brand-dark]
El cliente Bigbox deja de ser anónimo.

[Subtítulo — Figtree 18px, --fg-3, max-width 640px, centrado]
Cada canje entra a Woki como un perfil que se enriquece visita a
visita. Y entra a una máquina de recurrencia que ya conocen +700
restaurantes de la región.
```

**Tres cards (en grid):**

```
[Card 1 — Lucide icon: user-circle]
Perfiles enriquecidos
Cada cliente Bigbox queda cargado en tu base con preferencias,
alergias, celebraciones e historial de visitas. La próxima vez que
vuelva, lo reconocés.

[Card 2 — Lucide icon: send]
Comunicación segmentada
Email y WhatsApp dirigidos por comportamiento real, no por listas
masivas. Recuperá a los que canjearon y no volvieron en 3 meses.

[Card 3 — Lucide icon: bell]
Briefs pre-servicio
Tu equipo de sala arranca cada turno sabiendo qué clientes Bigbox
están viniendo, qué prefieren y cuál es la oportunidad de fidelizar.
```

**Card style:** fondo blanco, 1px borde `--border`, radio 12px, padding 32px, sombra `--shadow-sm`. Icono arriba (40×40px, color `--brand`), título Mona Sans 20px `--brand-dark`, body Figtree 15px `--fg-3`.

---

#### Sección 6 — Eje 2: Operación (sección de soporte)

**Layout:** dos columnas en desktop (texto izquierda 50%, mockup derecha 50%), una columna en mobile. Padding vertical 96px, fondo `--bg-soft`.

**Copy izquierda:**

```
[Eyebrow — uppercase, --brand]
OPERACIÓN

[H2 — Mona Sans 32–40px, --brand-dark]
La reserva Bigbox entra sola
a tu panel de Woki.

[Párrafo — Figtree 18px, --fg-3]
Cuando alguien compra una experiencia o giftcard en Bigbox, reserva
desde ahí mismo. La reserva aparece en tu panel de Woki con un
indicador de que viene de Bigbox y el detalle exacto de qué compró.
Sin WhatsApp, sin coordinación manual, sin hilos sueltos.

[Lista — bullets con icono Lucide check, Figtree 16px, --fg]
✓ Reserva creada desde Bigbox aparece directo en tu panel
✓ Indicador visual y detalle de qué experiencia compró
✓ Asignación automática de mesa según disponibilidad real
✓ Garantías y cobro de no-shows configurables
✓ Listas de espera, walkins y reservas regulares en el mismo lugar
```

(Reemplazar las marcas ✓ por íconos Lucide `check`, no por el carácter unicode.)

**Mockup derecha:** una representación estilizada de un panel de reservas Woki, mostrando una lista de reservas entrantes con una de ellas claramente etiquetada como "Bigbox" (con un badge sutil en `--brand`) y un expandible debajo que muestra el detalle de la experiencia comprada ("Cena maridaje · 2 personas · incluye 5 tiempos + maridaje de vinos"). Mismo estilo que los mockups que ya tiene la landing actual de Woki (`restaurantes.wokiapp.com`). Si es complejo de armar de cero, copiar uno de los mockups existentes del index.html actual y modificarlo agregando el badge "Bigbox" + el detalle.

---

#### Sección 7 — "Y mucho más"

**Propósito:** los que llegaron hasta acá ya pican. Mostrarles que Woki no es solo "operación + retención de Bigbox", es un ecosistema. Pero sin saturar.

**Layout:** título centrado, grid de 6 ítems compactos (2 filas × 3 columnas en desktop, 1 columna en mobile). Padding vertical 96px, fondo blanco.

**Copy:**

```
[H2 — Mona Sans 32–40px, --brand-dark, centrado]
Y mucho más.

[Subtítulo — Figtree 18px, --fg-3, centrado]
Woki es la plataforma de hospitalidad que usan los mejores
restaurantes de la región para conocer a sus clientes, activar
su base y operar sin fricciones.

[Grid — 6 ítems, cada uno con ícono Lucide pequeño + título + 1 frase]

1. [icon: layout-dashboard]
   Perfil del restaurante en wokiapp.com
   Tu marca, tu galería, tus promos. Con reserva en un click.

2. [icon: bar-chart-3]
   Métricas y reseñas con IA
   Panel unificado Woki + Google. Reporte mensual al mail.

3. [icon: credit-card]
   Pasarela de pagos
   +95% de cobrabilidad. Anticipos, garantías, tarjetas internacionales.

4. [icon: megaphone]
   Campañas con atribución
   Integraciones nativas con Meta, Google y TikTok Ads.

5. [icon: calendar-clock]
   Experiencias y eventos
   Cobro como entrada, métricas por evento, base que se enriquece.

6. [icon: award]
   Reservas desde la Guía Michelin
   Único sistema integrado en LatAm.
```

**Item style:** sin card, sin borde. Icono 24px `--brand`, título Mona Sans 18px `--brand-dark`, body Figtree 14px `--fg-3`. Espaciado generoso entre ítems.

---

#### Sección 8 — Oferta exclusiva + Implementación

**Layout:** una columna centrada, fondo `--brand-dark` con texto blanco. Padding vertical 96px. Visualmente quiebra la página, es el "cierre" antes del CTA. Dos sub-bloques claramente separados verticalmente.

**Sub-bloque A — Oferta exclusiva** (arriba)

```
[Eyebrow — uppercase blanco con opacidad 70%]
EXCLUSIVO PARA RESTAURANTES BIGBOX

[H2 — Mona Sans 40–56px, blanco]
30 días gratis,
y 2 meses al 50% off.

[Párrafo — Figtree 18px, blanco opacidad 80%, max-width 600px, centrado]
Una propuesta exclusiva para los restaurantes que vienen del
catálogo de Bigbox. Sin compromiso, sin contratos.
```

**Divisor visual:** línea horizontal sutil (1px, blanco opacidad 15%), max-width 480px, centrada, con padding vertical 64px arriba y abajo.

**Sub-bloque B — Implementación 72hs** (abajo)

```
[Eyebrow — uppercase, blanco opacidad 70%]
ALTA EN 72 HORAS

[H3 — Mona Sans 24–28px, blanco]
La migración la hace nuestro equipo.
Vos seguís ocupándote del restaurante.

[Tres columnas con números — Figtree 56px blanco, opacidad 40% para los números]

01                  02                  03
Migración           Configuración       Capacitación

Bases de clientes   La hace el equipo   Al equipo del
y reservas, en      de Woki, adaptada   restaurante, para
minutos.            a tu operación.     que rinda desde
                                        el día uno.
```

**Estilo de los sub-bloques:** los números "01 / 02 / 03" en Figtree grande, blanco con opacidad 40%, como decoración. Los títulos en Mona Sans 18px blanco. Body Figtree 15px blanco con opacidad 80%.

---

#### Sección 9 — CTA final

**Layout:** una columna centrada, max-width 720px, padding vertical 120px, fondo blanco.

**Copy:**

```
[H2 — Mona Sans 40–56px, --brand-dark, centrado]
Que tus clientes Bigbox vuelvan.

[Párrafo — Figtree 18px, --fg-3, centrado]
Escribinos por WhatsApp y te contamos cómo funciona Woki en tu caso
en 10 minutos. Sin compromiso, sin contratos, sin demos eternas.

[CTA primario — botón --brand-dark grande, 18px font, padding 18px 36px]
Hablar con el equipo por WhatsApp

[Link real]
https://wa.me/5491176520777?text=Hola%2C%20vengo%20del%20cat%C3%A1logo%20de%20Bigbox%20y%20quiero%20saber%20m%C3%A1s%20sobre%20Woki.

[Texto auxiliar — Figtree 14px, --fg-3]
+700 restaurantes ya operan con Woki.
Desde cafeterías de barrio hasta restaurantes Michelin.
```

---

#### Sección 10 — Footer minimal

**Layout:** una fila, padding vertical 48px, fondo blanco, borde superior 1px `--border`.

**Contenido:**

- Izquierda: logo Woki B2B (20px alto) + texto pequeño "© 2026 Woki. La plataforma de hospitalidad para los mejores restaurantes."
- Derecha: links pequeños: "wokiapp.com" · "restaurantes.wokiapp.com" · "Hablanos"

---

## 6. Assets entregados con este handoff

| Archivo | Uso |
|---|---|
| `assets/logos/woki-b2b-solid.svg` | Logo principal sobre fondo claro |
| `assets/logos/woki-b2b-gradient.svg` | OG image, hero, destacados |
| `assets/logos/woki-b2b-white.svg` | Sobre sección 8 (fondo oscuro) |
| `assets/logos/bigbox-logo.svg` | **Pendiente — pedirlo al equipo de Bigbox.** Versión oficial en SVG, sobre fondo claro y fondo oscuro |
| `assets/colors_and_type.css` | Todos los tokens (colores, tipografía, spacing, sombras) |
| `index.html` (landing actual de Woki B2B) | Referencia visual de calidad y componentes |
| `biblia_comercial_woki.docx` + `.pptx` | Fuente de verdad sobre tono, datos y propuesta de valor |

---

## 7. Inputs cerrados (decisiones tomadas)

| # | Decisión | Valor definitivo |
|---|---|---|
| 1 | **Co-branding visual** | Sí. Logos Woki + Bigbox lado a lado, separados por "×" sutil, en el header del mail y en el top nav de la landing. Logo Bigbox a recibir de su equipo (ver §6). |
| 2 | **Beneficio comercial exclusivo** | **30 días gratis + 2 meses al 50% off** para los restaurantes que vienen del catálogo Bigbox. Se comunica en bloque destacado en el mail (antes del CTA) y en sección dedicada en la landing (§8 sub-bloque A). |
| 3 | **Número WhatsApp del CTA** | `+54 9 11 7652 0777`. Link: `https://wa.me/5491176520777?text=Hola%2C%20vengo%20del%20cat%C3%A1logo%20de%20Bigbox%20y%20quiero%20saber%20m%C3%A1s%20sobre%20Woki.` Hardcodeado en todos los CTAs (mail + landing). |
| 4 | **Firma del mail** | Sin firma personal. El mail se envía desde el dominio habitual de Bigbox y cierra directo con el PD de social proof. El co-branding del header ya identifica al remitente. |
| 5 | **Alcance de la integración Woki ↔ Bigbox** | El cliente compra una experiencia o giftcard en Bigbox, reserva desde ahí mismo a través de Woki, y la reserva aparece en el panel del restaurante con un indicador de que viene de Bigbox y el detalle de qué incluye la experiencia comprada. **El copy de §4.3 (bullet 1) y §5.3 sección 6 ya refleja esto con precisión.** |
| 6 | **Mercado y lenguaje** | **Solo Argentina.** Voseo en todas las piezas. No se hace versión multi-país en esta tanda. |

---

## 8. Resumen ejecutivo (para reuniones)

- **Pieza:** mail + landing que Bigbox manda a sus restaurantes prestadores en Argentina, contándoles de Woki.
- **Insight:** Bigbox trae al cliente. Woki resuelve qué pasa después.
- **Dos ejes:** retención (principal) y operación (soporte).
- **Oferta exclusiva:** 30 días gratis + 2 meses al 50% off para restaurantes que vienen de Bigbox.
- **CTA único:** WhatsApp `+54 9 11 7652 0777`, con texto pre-cargado.
- **Tono:** complementario a Bigbox, no competitivo. Cercano + profesional, voseo (solo Argentina).
- **Co-branding:** logos Woki × Bigbox en header del mail y top nav de la landing.
- **Disciplinas:** sin mesas llenas como promesa, solo 7 números defendibles, sin logos de restaurantes específicos.
- **Diseño:** track B2B (azul Woki #132F60), Mona Sans + Figtree, Lucide icons, estética Apple-minimalist con calidez.
- **Implementación:** Claude Code lo arma con base en este documento + los assets adjuntos + la landing actual de Woki como referencia visual. Logo de Bigbox: a recibir de su equipo antes de empezar.

---

*Fin del handoff. Cualquier ambigüedad: defaultear al tono y disciplinas del documento maestro de Woki (`biblia_comercial_woki.docx`).*
