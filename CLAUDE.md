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

### Design System (fuente de verdad)

El design system vive en el archivo de Figma **Grupo-4** (`bsXTSPXGMNIIPPeEE1m8Or`), página **Design System**, y sale de la landing (página Wireframes Alta → `ORBIT · Landing / Home`). **Los valores de Figma mandan sobre los del SVG original.** Las pantallas en alta que ya existen son solo una idea y se van a revisar.

Variables (colección `ORBIT / Foundations`, CSS `var(--orbit-<nombre con guiones>)`):

| Variable | Valor | Uso |
|---|---|---|
| `color/bg` | `#090909` | Fondo principal |
| `color/bg-alt` | `#101010` | Fondo alterno de secciones |
| `color/ink` | `#050505` | Texto sobre accent, superficie de tarjetas |
| `color/text-primary` | `#FFF7ED` | Texto principal (blanco cálido) |
| `color/text-secondary` | `#ABABAB` | Copy secundario, footer |
| `color/accent` | `#F5983B` | Botones/CTA, acentos |
| `color/accent-soft` | `#FFB56E` | Eyebrows, links de acento |
| `color/line` | `#414141` | Líneas finas |
| `space/4…80` | 4, 8, 12, 16, 24, 32, 40, 48, 64, 80 | Espaciado |
| `layout/*` | página 1440, margen 80, contenido 1280, nav 92 | Grilla |
| `radius/2` | 2 | Único radio |
| `stroke/hairline` | 1 | Línea fina |

Overlays de la landing (no son variables): hero 66 % de `color/bg`, banda del nav 58 % de `color/bg`, línea del hero 35 % de `color/text-primary`.

- **Tipografía:** Inter, 20 estilos de texto en Figma (usarlos, no crear tamaños sueltos). Los principales: `Display/Hero` 66 ExtraBold −2.4; `Heading/Section` 48 Bold −1.2; `Heading/Feature` 42 Bold −1; `Title/Large` 22 Bold −0.3 (título de parada y valores de métricas); `Body/Large` 17; `Body/Medium` 16; `Body/Small` 14 (color secundario); `Eyebrow` 11 SemiBold +1.1 en MAYÚSCULAS (color `accent-soft`); `Button/Label` 12 Bold +0.5; `Nav/Link` 11 Medium +0.2. Diferencia conocida: el título final de la landing mide 50, el estilo `Heading/Section` mide 48.
- **Grilla:** 1440 px de ancho, márgenes de 80, contenido de 1280. Nav de 92 px de alto.
- **Formas:** radio **2 px** (`radius/2`) en botones y tarjetas; el resto de los bloques e imágenes va con esquinas rectas. Botón primario: relleno `color/accent`, texto `color/ink`, alto 48 (nav), 50 (hero) o 54 (CTA final).
- **Componentes** (página Design System): `Button / Primary` (Size: Small, Medium, Large), `Button / Link` (Tone: Default, Accent), `Navigation / Desktop`, `Divider` (Orientation), `Section Header`, `Footer / Desktop` y `Card / Destination`. Las vistas de experiencia (Órbita, Luna) usaron `Image Placeholder`, `Media Tile`, `Fact Item`, `Step Item`, `Button / Outline` y `Metric Row`, pero al 2026-11-01 esos componentes ya no están en la página Design System (alguien del equipo los sacó) y esas páginas los tienen como marcos sueltos. No volver a agregarlos sin confirmar con el usuario. Reutilizar los componentes que sí están antes de dibujar algo nuevo.
- **Limitación de instancias:** en una instancia no se puede cambiar el tamaño ni la posición de nodos internos (se ignora en silencio). Para variar una barra de progreso o un marcador, usar relleno degradado en la barra y `paddingLeft` en un contenedor con auto-layout.
- **Tono:** fotografía cinematográfica (nave sobre la Tierra al amanecer, astronauta frente a la ventana), mucho aire, copy corto y confiado.

## 7. Simulador del equipo

URL desplegada por un compañero: https://melodic-praline-0ae0ea.netlify.app/ (HTML + JS). Lo que se pudo leer (solo texto, no se vio el aspecto visual): **"Viaje Interplanetario"** con "días de viaje", "Llegada", "Distancia al partir", "Δv necesario", "Fecha de partida" (con botón "↺ Hoy") y "costo del viaje" en escala barato → caro. Es decir: **la fecha de salida cambia duración, Δv y costo**. No se detectó animación.

Idea del equipo: mostrar el recorrido del cohete hasta el planeta con play. Para Figma se acordó usar una **animación fija** (no depende de la fecha) con el mismo trayecto.

### Animación fija (generada)
- Tierra → Marte con **órbita de transferencia de Hohmann** calculada: **259 días**; fase de Marte ~44° por delante; posiciones coherentes (el cohete llega donde está Marte). Tamaños y distancias **no a escala** y rotulado como ilustrativo.
- Versión reteñida con la paleta de ORBIT: fondo `#090909`, trayectoria `#F5983B`, textos en mayúsculas; contador "TRAVEL TIME 000 / 259 DAYS", barra de progreso, marcadores DEPARTURE / ARRIVAL. 1280×720, ~11,5 s.

### Prototipo interactivo del vuelo a la Órbita
`prototypes/orbit-flight/index.html` (un solo archivo, se abre con doble clic; ver su README). Es la versión viva de la sección "The flight" de la página de Órbita en Figma: se arrastra la línea del vuelo y cambian en vivo lo que se siente, la fuerza G, la altitud, la velocidad, el peso del usuario y la vista por la ventana; en la banda de ingravidez los objetos flotan y se pueden agarrar y tirar; sonido opcional. Los datos son ilustrativos.
- **Cómo se muestra en la demo:** en Figma queda la versión estática (misma maqueta, congelada en T+4:00, imagen de la escena exportada del prototipo en `assets/orbit-flight/`). Para la demo se cambia al HTML, que abre en el mismo momento. El Figma no puede correr código ni incrustar el HTML.
- La idea escala a los otros viajes (ya hecho para la Luna, abajo): un mismo componente configurable con los datos de cada uno (Luna, EEI, y para Marte la transferencia de 259 días).
- `#t=<minutos>` abre en un momento; `#t=4&shot` renderiza solo la escena (para exportar el still).

### Prototipo interactivo del vuelo a la Luna
`prototypes/moon-flight/index.html` (ver su README). Vuelta a la Luna sin alunizar, 6 días de ejemplo. Bloque propio de este viaje: la **Tierra del tamaño del pulgar** (se achica según la distancia y aparece un marco de 2° que representa el pulgar con el brazo estirado), el **silencio de radio** detrás de la Luna (pantalla oscura, "NO SIGNAL", Earthrise) y el **mensaje con retraso** (pulso en tiempo real, ~1,3 s por sentido a la distancia de la Luna). La página de Figma es `ORBIT · Experience / Moon Flyby · High` (clon de la de Órbita, sin la sección "The view": el bloque del vuelo ya es la vista) y su still está en `assets/moon-flight/`. Sin sonido ni peso del usuario, a propósito, para no sobrecargar. Un compañero la editó (2026-11-01): texturas reales de Tierra y Luna, marco de ventana de cabina con HUD, datos plegados bajo "Flight data", nombres de las paradas bajo el gráfico; el still de Figma (`assets/moon-flight/scene-t320-v2.png`) y el panel están actualizados a esa versión. Para exportar el still con Chrome sin pantalla usar `--timeout=5000` (con `--virtual-time-budget` se cuelga). Las imágenes de "Your cabin": afuera, `assets/Gemini_Generated_Image_kw22kykw22kykw22.jpeg` (hecha por el usuario con Gemini; se parece mucho a una nave real, está marcada como ilustrativa) y adentro, `assets/moon/interior.png` (generada en `ORBIT · Generated images`). El hero usa una foto real de la Tierra saliendo sobre la Luna: `assets/nasa-w9sZL_hvNug-unsplash.jpg` (Unsplash, usuario NASA). Se acredita en pantalla ("IMAGE: NASA") y no debe sugerir respaldo ni auspicio de la NASA; no usar su logo.

### Prototipo interactivo de la Estación Espacial
`prototypes/iss-flight/index.html` (ver su README). La página de la ISS la armó un compañero clonando la de la Luna: mismo esqueleto (hero, "On board", cabina, camino, personas, CTA); el simulador era una copia con otras etiquetas (curva de "altitud" subiendo en 14 días, que no dice nada de una estadía en órbita). Se rehízo con bloque propio: **un día a bordo con 16 amaneceres** (la vista de la Cúpula pasa de amanecer a día, atardecer y noche con luces de ciudades cada ~93 min; el gráfico es la onda de luz del día) y **dónde estás** (mapa con la traza de la órbita y "OVER · región"), más "Take a photo". Usa como base la foto de la Cúpula del equipo (`assets/iss/cupola-view.png`). Mismo modo `#t=<minutos>&shot` para el still (`assets/iss-flight/scene-1440.png`).
- Idea para una segunda fase (no hecha): modo "Arrival" con la aproximación y el acople (distancia y velocidad relativa decreciendo).
- Los tres simuladores comparten el esqueleto (escena + panel + línea que se arrastra) y cambian el momento propio: Órbita = peso (G, ingravidez, objetos flotando); Luna = distancia (Tierra del tamaño del pulgar, silencio de radio, mensaje con retraso); ISS = ciclo de luz (16 amaneceres, dónde estás).

### Prototipo de Marte
`prototypes/mars-flight/index.html` (lo hizo un compañero; HTML + canvas, en español, con su propio look: Space Grotesk y colores propios). Calcula la ruta Tierra → Marte con la posición real de los planetas (Lambert) y deja elegir la fecha de partida con una tira de costo. Se modificó (2026-11-02) para que el destino sea **solo Marte**: se sacaron los chips de destinos (ISS, Mercurio, Venus, Júpiter...). Todavía queda el código del modo ISS sin usar. Su still (`assets/mars-flight/prototype.png`, 1280×720 a 2x, con la fecha de "hoy") es lo único que muestra la sección "The flight" de la página de Marte en Figma: se sacaron el panel de datos de la derecha y el gráfico de abajo. Para exportar el still: `--timeout=7000` con Chrome sin pantalla.

### Páginas de elección (después de explorar el viaje)
Entre la página de experiencia del viaje y "Profile" (paso 1 de 3 del onboarding existente). Pensadas como "Comparación y precio" (§4, §11): experiencia primero, elecciones administrativas después.
- `ORBITA · Choose your flight · High`: 1) elegir operador (3 tarjetas con 5 datos: precio total y qué incluye, próxima salida, asientos, vuelos hechos, elegibilidad; etiquetas de contraste "Lowest price / Earliest departure / Most flights"), 2) elegir salida (4 fechas con disponibilidad), 3) quién vuela (yo / regalo); panel "Your flight" con operador, fecha, pasajero, total estimado, depósito reembolsable de ejemplo y "Compare all details". "No es una reserva: no se cobra nada" (igual que Funding).
- `ORBITA · Operator details · High`: la capa "Ver detalle": depósito, cronograma de pago, cancelación, licencias y seguridad, logística y requisitos, por operador, con la columna elegida resaltada.
- Al pie de las páginas de experiencia (Órbita, Luna, ISS) el bloque "Next step" ofrece dos caminos (decisión del usuario, 2026-11-02): título "Compare operators, or choose your flight.", enlace "Compare operators →" (va a Operator details) y botón principal "Choose your flight" (va a Choose your flight). Todavía no están enlazados como prototipo en Figma.
- Armadas para Earth Orbit 01 (coincide con Funding y Roadmap); sirven de plantilla para los otros viajes cambiando el viaje y los datos. Operadores: por decisión del usuario (2026-11-02) usan nombres reales en esas páginas y en el resumen de Profile (SpaceX, Blue Origin, Rocket Lab). Precios, fechas, vuelos hechos, depósito y condiciones son inventados y se rotulan como ejemplo; no son ofertas reales. Radio 2 y estilos de texto del DS; el estilo de las tarjetas de selección sigue el de la página Funding.
- Decisiones del usuario (2026-11-02): Funding lo está cambiando otra persona y alcanza con que muestre solo Earth Orbit; los pasos "1/2/3 de 3" se quedan así (es "entrar en la etapa oficial del viaje"); los nombres de pantallas y la marca (ORBITA/ORBIT) se pulen al final; el TO BE quedó atrasado y no se arregla. **Profile** ya no pregunta el interés: muestra una tarjeta "Saved to your profile" con el viaje elegido (Earth Orbit 01, operador, fecha, pasajero), "Change flight" y "We remember what you chose", para que el usuario sepa que la plataforma se acuerda de lo que estaba haciendo.
- Nota de marca: las páginas de proceso, Destinations e ISS ya dicen **ORBITA**; las páginas de Órbita y Luna y los prototipos todavía dicen ORBIT. Pendiente unificar (preguntar al usuario).

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
- Archivo de trabajo: https://www.figma.com/design/bsXTSPXGMNIIPPeEE1m8Or/Grupo-4 (equipo/plan dueño **sin verificar**; la cuenta tiene los planes `tbregoli's team` como admin y `@guadislab` como guest). La generación de imágenes con IA gasta créditos del plan del archivo donde se genera: no generar en este archivo hasta confirmar de quién es. El MCP está autenticado como `tomibregoli`, así que todo lo que se escriba aparece a su nombre. Si hay que escribir en otro archivo, pedir la URL antes.
- **Imágenes generadas con IA:** se generan en el archivo propio `ORBIT · Generated images` (`Ylh9uZtwjEMR4oxQ42iBa2`, equipo `tbregoli's team`, así los créditos salen del plan del usuario), se bajan a `assets/<viaje>/` (para Órbita: `assets/orbit/`) y se suben a `Grupo-4` con `upload_assets` + `imageHash` aplicado al `Image Placeholder`. La herramienta solo genera desde texto (no edita fotos) y entrega hasta ~1536 px de lado. Estilo común de los prompts: fotografía cinematográfica, realista, oscura, luz cálida ámbar, grano sutil, mucho espacio negativo, sin texto/logos/marcas de agua; sin caras visibles. Todo marcado `ILLUSTRATIVE` o `EXAMPLE`.

## 11. Pendiente / próximos pasos sugeridos

1. Pasar la pantalla de experiencia a Figma (alta fidelidad) y refinar: variante con selector de empresa, estados del play, versión mobile.
2. Pantalla de **comparación y precio** (al final de la experiencia): 5 datos clave por empresa, etiquetas de contraste, "Ver detalle", confianza/seguridad, elegibilidad personalizada, botón Elegir.
3. Pantallas de lo "fiaca": anotarse, certificados/perfil, pago (con depósito reembolsable), seguimiento.
4. Definir cómo se integra el selector de **fecha de salida** (qué cambia en la experiencia/precio/disponibilidad) y qué ve el usuario si una empresa no tiene salida en esos días.
5. Pantalla de exploración de misiones (entrada al flujo) y "Ver como lista" sin animación.
6. Material real (con permiso) para fotos de asiento y de pasajeros; **nunca presentar como reales testimonios o reseñas inventados**: marcar como ejemplo.

## 12. Cómo trabajar con este contexto

- Hablarle al usuario en **español**; el copy de la UI va en **inglés**, siguiendo la landing.
- Respetar el design system de §6 (variables, estilos de texto y componentes); no inventar otra paleta ni usar más radio que `radius/2`.
- Marcar siempre lo hipotético: datos de empresas, precios, fechas y estadísticas son **de ejemplo** salvo que se verifiquen con fuente.
- Operadores: el usuario decidió usar nombres reales (SpaceX, Blue Origin, Rocket Lab) en las páginas de elección y detalle. Aun así, no usar sus logos y mantener rotulados como ejemplo los precios, fechas y condiciones.
- "People who flew": solo imágenes de personas (sin caras, marcadas EXAMPLE) con un título sobre cómo el espacio cambia a las personas; sin testimonios ni nombres uno a uno (decisión del usuario, 2026-11-01).
- Priorizar pocos datos visibles y el resto en capas ("Ver detalle"); la narrativa es experiencia primero, precio al final.

## Fuentes de la investigación AS IS

- SpacePolicyOnline, "Bidding Is Open to Make the First Flight On New Shepard": https://spacepolicyonline.com/news/bidding-is-open-to-make-the-first-flight-on-new-shepard-if-youre-physically-fit/
- SpaceNews, Blue Origin anuncia el primer vuelo tripulado: https://spacenews.com/?p=114150
- Benzinga, "Bid On A Flight With Blue Origin": https://www.benzinga.com/news/21/05/20972975/bid-on-a-flight-with-blue-origin-how-you-can-go-to-space-on-july-20
- Requisitos del pasajero: https://hard-sf.com/?p=3205
- Figma Help, imágenes y videos: https://figma-signup.helpjuice.com/color-gradients-and-images/add-images-and-videos-to-design-files
- Figma Help, embeds: https://help.figma.com/hc/en-us/articles/360039827134