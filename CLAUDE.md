# Contexto del proyecto: plataforma intermediaria de vuelos espaciales comerciales

> Documento para darle contexto a Claude Code (con el MCP de Figma). Resume todo lo trabajado hasta ahora en el chat. Cuando algo es hipótesis o suposición, está marcado.

## 1. Qué es el proyecto

Trabajo de diseño universitario (en equipo). La idea es una **página web que actúa de intermediaria entre las empresas de vuelos espaciales comerciales y las personas**, para que consigan fácilmente el camino hacia su vuelo.

- La plataforma **maneja todo el proceso**: ver qué vuelos hay, con qué empresas y a qué precio; y también entrenamiento, pago, trámites y seguimiento. La empresa aeroespacial solo **opera el vuelo**.
- Aspiración **global**, pero seguramente empiece en un mercado específico (no definido).
- Pensada para lo **actual** (suborbital/orbital hoy) y para el **futuro** (vuelos a Marte el día que existan). Por eso el modelo de "vuelo" debe ser genérico: destino, duración, vehículo, requisitos.
- Idioma de trabajo del equipo: **español**. La landing y la UI del producto están en **inglés** (marca **ORBIT**).

### Consigna de la cátedra
1. Flujo AS IS. 2. Marcar la sección a mejorar. 3. Ideación. 4. Flujo TO BE. 5. Wireframes en baja.

### Estado actual
- Research, perfiles, AS IS, TO BE y wireframes en baja: **hechos**.
- El TO BE se dejó como lo armó un compañero (ver §5); la cátedra dijo que no hay que rehacerlo.
- **Ahora**: diseñar las **vistas de experiencia en alta fidelidad en Figma**, siguiendo la línea visual de la landing que hizo otro compañero.

### Dirección que dio la profesora (importante, manda sobre lo anterior)
**Vender la experiencia primero y dejar todo lo "fiaca" para el final.** O sea: en la parte previa y en la de comparación hay que mostrar simulador del viaje, fotos del asiento, del cohete, fotos de personas que hicieron el viaje mientras lo hacen, etc.: llevar al usuario a ver de qué se trata lo que va a comprar. **Al final** se comparan precio y condiciones. Después van los trámites (anotarse, certificados, pago). La idea es armar un flujo de muestra de experiencia por cada viaje que proponemos. **La lista de viajes son a la orbita, orbitar la Luna, ir a la Estacion Espacial Internacional y, proximamente, a Marte"

## 2. Perfiles de usuario (proto-personas, **hipótesis sin validar**)

El research fue solo documental (no hay acceso directo a usuarios).

1. **Alto poder adquisitivo.** Busca exclusividad y experiencia memorable; quiere que le resuelvan todo. Prioriza: seguridad/confianza, flexibilidad de fechas, atención personalizada, privacidad. Puede comprar para otra persona (regalo).
2. **Científico (asociado a una institución).** El que usa no es el que decide ni el que paga: investigador, oficina de fondos, compras/legal, comité de ética. Ciclo lento (meses). Necesita datos técnicos, documentación exportable, cotizaciones, aprobaciones. Pregunta abierta: ¿vuela la persona o solo la carga? (rama no dibujada).
3. **Aficionado a la cohetería.** Sueña con volar; alto conocimiento, presupuesto limitado. Necesita precio claro, plan de pago, contenido educativo, comunidad, camino progresivo ("escalera de experiencias").

Tema transversal: **la confianza** (el usuario deja mucho dinero y una experiencia de riesgo en manos de la plataforma). Supuestos abiertos: implicancias legales, seguros, requisitos médicos y migratorios según país.

## 3. Flujo AS IS (hoy, sin la plataforma) — caso New Shepard (Blue Origin)

Se tomó la misión New Shepard como ejemplo. **Casi toda la info pública es de 2021** (primer vuelo con pasajeros); puede haber cambiado. Gran parte del proceso real **no es público**, lo cual ya es un hallazgo.

**Documentado (2021):**
- Se podía registrar interés en la web; la empresa no informó el precio de futuros vuelos. El primer asiento se vendió por **subasta** (ofertas selladas, luego abiertas, subasta en vivo); el monto se donó a su fundación.
- Ofertas de más de USD 50.000 exigían **verificación de identidad y un depósito reembolsable de USD 10.000**.
- Requisitos publicados: altura 1,52–1,84 m; peso 50–101 kg; subir 7 pisos en 90 s; tolerar ~5,5 G en descenso; entender instrucciones en inglés, etc. La **evaluación médica es responsabilidad del pasajero**.
- Llegada al sitio de West Texas ~4 días antes; **3 días de entrenamiento** (maqueta de la cápsula, entrada/salida, emergencias); alojamiento en "Astronaut Village".
- Vuelo de ~10 minutos; cápsula para 6 pasajeros.

**Suposiciones (no confirmadas):** qué pasa tras registrar interés (mails automáticos vs. contacto de ventas), existencia de compra directa, cómo y cuándo se paga, contrato/exención, logística y visas, post-vuelo, vías alternativas (invitación/patrocinio, intermediario).

**Flujo AS IS (9 fases, 16 pasos):** Descubrir → Interés (registro, respuesta de ventas) → Elegibilidad (requisitos/T&C, verificación de identidad) → Obtener asiento (6A subasta / 6B compra directa / 6C invitación o patrocinio / 6D intermediario) → Contrato y pago → Preparación (evaluación médica, fecha, viaje y trámites) → Entrenamiento (llegada, 3 días) → Día de vuelo (chequeos, lanzamiento) → Después.

Candidatos a "sección a mejorar" identificados: **Interés** (caja negra tras anotarse) y **Obtener asiento** (4 vías, 3 sin confirmar).

## 4. Decisiones de diseño tomadas en el chat

- **Una tabla densa de comparación se descartó** (mucha data, demasiado "cuadrada"). Se priorizan ~5 datos clave y el resto va detrás de "Ver detalle".
  - Datos clave por empresa: precio total (y qué incluye), salida más cercana + disponibilidad, elegibilidad para el usuario, una señal de confianza (vuelos realizados), un diferencial de experiencia (duración/vehículo).
  - Detalle: depósito, cronograma de pago, cancelación, licencias, logística, requisitos físicos.
  - Etiquetas de contraste ("Más económica", "Salida más cercana", "Más vuelos realizados").
- Se exploraron tres wireframes en baja: tabla comparativa; página scrolleable con una sección por dato (las 3 empresas lado a lado + barra fija); **simulador central** (globo/trayectoria + play, empresas y precio a la izquierda, seguridad y elegibilidad a la derecha, datos del vuelo debajo, barra de días abajo).
- **Orden recomendado** (alineado con la profesora): Inicio → Exploración de misiones → Elección → **Experiencia** → **Comparación y precio** → trámites (elegibilidad, perfil/certificados, pago) → preparación/seguimiento/confirmación → misión.
- Riesgos a mitigar: (1) mostrar el precio recién al final puede parecer trampa → un "desde USD X" discreto; (2) requisitos físicos al final frustran → aviso breve o autochequeo en la experiencia; (3) en vuelos suborbitales el globo dice poco (sube y baja ~10 min); luce más en vuelos orbitales/Marte; (4) ofrecer una vista alternativa sin animación ("Ver como lista").
- Todo lo ilustrativo debe **decirlo** ("Illustrative animation · not to scale").

## 5. Flujo TO BE (oficial: el del compañero)

9 pasos, fases: **Inicio → Respaldo → Exploración → Elección → Perfil → Plan → Seguimiento → Confirmación → Misión**.
1. La persona ingresa (expresa interés). 2. Define respaldo (autofinanciación o sponsor). 3. Compara misiones (destino, empresa, costo, fechas, requisitos). 4. Elige misión (opción o inicia postulación). 5. Completa perfil (datos, documentación, salud, seguros). 6. Recibe preparación (base común + módulos según misión/destino/nave). 7. Sigue el proceso (turnos, tareas, avances, aprobaciones). 8. Valida el vuelo (checklist, condiciones, fecha confirmada). 9. Viaje espacial (opera la empresa).
Color: azul = gestiones y seguimiento que centraliza la plataforma; verde = instancia operada por la empresa aeroespacial.

Huecos detectados al revisarlo (se pueden resolver dentro de los pasos existentes): pago/contrato poco visibles, logística y trámites migratorios, confianza (seguridad, cancelación), post-vuelo, camino para quien "todavía no puede".

Versión alternativa que se discutió (11 pasos, solo referencia): Inicio, Exploración, Elección (preselección), Comparación, Elegibilidad, Respaldo y pago, Perfil, Plan, Seguimiento, Confirmación, Misión.

## 6. Landing existente (referencia visual obligatoria)

Hecha por un compañero. SVG de Figma de 1440×2560, texto en inglés, marca **ORBIT**.
Secciones: nav → hero ("Beyond the horizon.", "PRIVATE SPACEFLIGHT · FUTURE-READY", botones EXPLORE MISSIONS / HOW ORBIT WORKS) → "The mission begins before launch." (DISCOVER / PREPARE) → imagen de astronauta con "A clearer way to prepare." → "Your path to orbit starts here." + START PLANNING → footer.

### Tokens (extraídos del SVG)
| Token | Valor |
|---|---|
| Fondo | `#090909` |
| Fondo alterno | `#101010` |
| Texto principal (blanco cálido) | `#FFF7ED` |
| Texto secundario | `#ABABAB` |
| Naranja etiquetas/acentos | `#FFB56E` |
| Naranja botones/CTA | `#F5983B` |
| Líneas finas (hairlines) | `#414141` |

- **Tipografía:** Inter. Títulos 700–800, muy apretados (letter-spacing ≈ −1.5 a −1.6 en 56 px; 40 px para títulos de sección). Etiquetas en **MAYÚSCULAS**, 11–12 px, peso 600, tracking 2.2–2.4, color `#FFB56E`. Nav 12 px, peso 500, tracking 1.2.
- **Grilla:** 1440 px de ancho, márgenes de 80, contenido de 1280. Nav de 92 px de alto.
- **Formas:** esquinas **rectas** (sin radio) en botones, imágenes y paneles. Botón primario: relleno `#F5983B`, texto `#090909` 12 px peso 700 tracking 1.2–1.4, alto 48–56.
- **Tono:** fotografía cinematográfica (nave sobre la Tierra al amanecer, astronauta frente a la ventana), mucho aire, copy corto y confiado.

## 7. Simulador del equipo

URL desplegada por un compañero: https://melodic-praline-0ae0ea.netlify.app/ (HTML + JS). Lo que se pudo leer (solo texto, no se vio el aspecto visual): **"Viaje Interplanetario"** con "días de viaje", "Llegada", "Distancia al partir", "Δv necesario", "Fecha de partida" (con botón "↺ Hoy") y "costo del viaje" en escala barato → caro. Es decir: **la fecha de salida cambia duración, Δv y costo**. No se detectó animación.

Idea del equipo: mostrar el recorrido del cohete hasta el planeta con play. Para Figma se acordó usar una **animación fija** (no depende de la fecha) con el mismo trayecto.

### Animación fija (generada)
- Tierra → Marte con **órbita de transferencia de Hohmann** calculada: **259 días**; fase de Marte ~44° por delante; posiciones coherentes (el cohete llega donde está Marte). Tamaños y distancias **no a escala** y rotulado como ilustrativo.
- Versión reteñida con la paleta de ORBIT: fondo `#090909`, trayectoria `#F5983B`, textos en mayúsculas; contador "TRAVEL TIME 000 / 259 DAYS", barra de progreso, marcadores DEPARTURE / ARRIVAL. 1280×720, ~11,5 s.

## 8. Pantalla de experiencia (ya armada, SVG importable a Figma)

`pantalla_experiencia_orbit.svg` (1440×2360), estilo ORBIT:
nav → "‹ BACK TO MISSIONS" → label "MISSION 01 · EARTH TO MARS" → título "See the journey before you commit." → subtítulo → **escenario 1280×720 con la animación** → fila de 4 datos (DESTINATION Mars / TRAVEL TIME 259 days / DEPARTURE 15 Nov 2026 + "CHANGE DATE ›" / ARRIVAL 01 Aug 2027; fechas de ejemplo coherentes con 259 días) → "INSIDE THE EXPERIENCE: Where you'll sit. What you'll see." con 4 tiles (YOUR SPACECRAFT y THE VIEW con imágenes de la landing; YOUR SEAT y PEOPLE WHO FLEW son placeholders "PHOTO") → "NEXT STEP: Ready to compare?" + botón **COMPARE OPERATORS & PRICES** → footer.

## 9. Archivos generados en el chat

- AS IS: `flujo_as_is_new_shepard.svg/.png`
- TO BE alternativo (11 pasos): `flujo_to_be_nuevo.svg/.png`
- Wireframes en baja: `wireframe_comparacion.svg`, `wireframe_comparacion_scroll.svg`, `wireframe_simulador.svg` (+ PNG)
- Animación: `viaje_a_marte.gif/.mp4` (azul, versión inicial) y `viaje_a_marte_orbit.gif/.mp4` (paleta ORBIT)
- Pantalla: `pantalla_experiencia_orbit.svg/.png`
- Del equipo: SVG del flujo TO BE de un compañero; SVG de la landing ORBIT.

## 10. Restricciones técnicas de Figma (verificadas)

- El HTML/JS **no corre dentro de Figma** y no se puede incrustar un iframe en un archivo de diseño. Opciones: importar HTML como capas estáticas (html.to.design), Figma Make, Smart Animate con varios frames, o mostrar el simulador publicado aparte.
- **Video** (MP4, MOV, WebM) soportado en archivos y prototipos, pero **requiere plan pago**. Los **GIF** se pueden usar, pero solo se mueven en **modo presentación**.
- Los SVG se importan como capas vectoriales editables; los textos usan Inter (debe estar disponible).
- El equipo trabaja en **otra cuenta de Figma**: pedir la URL del archivo destino antes de escribir.

## 11. Pendiente / próximos pasos sugeridos

1. Pasar la pantalla de experiencia a Figma (alta fidelidad) y refinar: variante con selector de empresa, estados del play, versión mobile.
2. Pantalla de **comparación y precio** (al final de la experiencia): 5 datos clave por empresa, etiquetas de contraste, "Ver detalle", confianza/seguridad, elegibilidad personalizada, botón Elegir.
3. Pantallas de lo "fiaca": anotarse, certificados/perfil, pago (con depósito reembolsable), seguimiento.
4. Definir cómo se integra el selector de **fecha de salida** (qué cambia en la experiencia/precio/disponibilidad) y qué ve el usuario si una empresa no tiene salida en esos días.
5. Pantalla de exploración de misiones (entrada al flujo) y "Ver como lista" sin animación.
6. Material real (con permiso) para fotos de asiento y de pasajeros; **nunca presentar como reales testimonios o reseñas inventados**: marcar como ejemplo.

## 12. Cómo trabajar con este contexto

- Hablarle al usuario en **español**; el copy de la UI va en **inglés**, siguiendo la landing.
- Respetar los tokens de §6; no inventar otra paleta ni redondear esquinas.
- Marcar siempre lo hipotético: datos de empresas, precios, fechas y estadísticas son **de ejemplo** salvo que se verifiquen con fuente.
- No usar nombres, logos ni marcas reales de operadores en piezas que parezcan oficiales; usar "Empresa A/B/C" o marcarlo como ejemplo.
- Priorizar pocos datos visibles y el resto en capas ("Ver detalle"); la narrativa es experiencia primero, precio al final.

## Fuentes de la investigación AS IS

- SpacePolicyOnline, "Bidding Is Open to Make the First Flight On New Shepard": https://spacepolicyonline.com/news/bidding-is-open-to-make-the-first-flight-on-new-shepard-if-youre-physically-fit/
- SpaceNews, Blue Origin anuncia el primer vuelo tripulado: https://spacenews.com/?p=114150
- Benzinga, "Bid On A Flight With Blue Origin": https://www.benzinga.com/news/21/05/20972975/bid-on-a-flight-with-blue-origin-how-you-can-go-to-space-on-july-20
- Requisitos del pasajero: https://hard-sf.com/?p=3205
- Figma Help, imágenes y videos: https://figma-signup.helpjuice.com/color-gradients-and-images/add-images-and-videos-to-design-files
- Figma Help, embeds: https://help.figma.com/hc/en-us/articles/360039827134