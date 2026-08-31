# Thays — App del Jardín Botánico de Buenos Aires
## Documentación de producto

**Versión** 2.0 · **Estado** prototipo probado en Chrome, escritorio y móvil · **Alcance** app web, mobile first · **Fecha** agosto 2026
**Contexto** Caso de cátedra, Diseño Gráfico 3, FADU

> Este documento es la referencia larga. La versión de presentación —22 slides con la investigación de UX: usuarios → insights → hipótesis → decisiones— está en `dossier.html`.

---

## 01 · Contexto y problema

### El sitio

El Jardín Botánico Carlos Thays abrió el 7 de septiembre de 1898 sobre un proyecto que Carlos Thays presentó en 1892. Ocupa cerca de **7,7 hectáreas** en Palermo, entre la avenida Santa Fe, la avenida Las Heras y la calle República Árabe de Siria, con Plaza Italia como acceso principal. Fue declarado Monumento Histórico Nacional en 1996 y, en marzo de 2023, primer refugio climático de la Ciudad: bajo su dosel se registran temperaturas hasta 4,8 °C menores que en las calles que lo rodean.

Reúne unas **5.500 especies** arbustivas, arbóreas y herbáceas organizadas por origen geográfico, familia y utilización, más de treinta obras de arte, cinco invernáculos —uno art nouveau, premiado en la Exposición Universal de París de 1889—, la casona de 1881 donde vivió Thays, un jardín de mariposas a cielo abierto, una biblioteca infantil y la Escuela Técnica de Jardinería «Cristóbal María Hicken».

### El problema del visitante

| Fricción | Qué pasa hoy | Consecuencia |
|---|---|---|
| **Orientación** | La cartelería de sectores es escasa y el trazado no es una grilla. | Sectores enteros —Oceanía, África, el yerbal histórico— quedan sin visitar. |
| **Interpretación** | Los carteles dan nombre científico, familia y origen. Nada explica por qué esa planta importa. | La visita es paisajística, no educativa. No hay aprendizaje ni recuerdo. |
| **Narrativa** | No hay recorrido sugerido para quien viene por primera vez ni para quien viene con chicos. | La visita se agota en veinte minutos y no se repite. |
| **Estacionalidad** | Lo mejor del Jardín cambia mes a mes y el visitante no tiene cómo saber qué está en flor hoy. | Se pierde el principal motivo para volver. |

> **Hipótesis de producto.** Si el visitante puede ubicarse, entender lo que ve y seguir un relato, la visita pasa de veinte minutos de paseo a una hora de experiencia — y genera una segunda visita. El Jardín ya tiene el contenido; lo que falta es el canal.

---

## 02 · Objetivos y métricas

| Objetivo | Métrica principal | Meta a 6 meses |
|---|---|---|
| **O1. Que el visitante se oriente** | Sectores visitados por sesión | De 4 a 8 de 14 |
| **O2. Que entienda lo que ve** | Fichas abiertas por sesión | ≥ 5 |
| **O3. Que vuelva** | Usuarios con dos o más visitas en 6 meses | 25 % |

**Métricas secundarias**

- Duración media de la visita: de 22 a 45 minutos.
- Tasa de finalización de recorridos: 40 % de los iniciados llegan a la última parada.
- Escaneos de QR por cartel: identifica qué especies generan curiosidad y dónde invertir en cartelería física.
- Postulaciones a voluntariado llegadas por este canal.

> **Métrica que no usamos: descargas.** Una app de sitio se mide por lo que pasa adentro del predio. Por eso el producto es una app web: no hay fricción de descarga y la métrica de entrada es la visita, no la instalación.

---

## 03 · Usuarios y personas

### Sofía · 28 · primera visita
- **Contexto:** pasa por Plaza Italia, tiene una hora libre y entra sin plan.
- **Necesita:** que alguien le diga por dónde empezar y qué vale la pena mirar.
- **Fricción:** no va a leer un mapa impreso ni a bajar una app de 80 MB en la puerta.
- *«Entré, caminé, era lindo, pero no entendí nada de lo que vi.»*

### Marcelo · 61 · visitante frecuente
- **Contexto:** viene dos veces por mes. Conoce el predio mejor que la cartelería.
- **Necesita:** saber qué está en flor esta semana y datos que todavía no sepa.
- **Fricción:** el contenido genérico lo aburre; quiere profundidad, no bienvenidas.
- *«Yo ya sé dónde está todo. Lo que quiero es que me cuenten algo nuevo.»*

### Carla y Tomi · 37 y 7 · familia
- **Contexto:** sábado a la tarde, con un chico de siete años y dos horas por delante.
- **Necesita:** una excusa para que el chico camine y mire, no una enciclopedia.
- **Fricción:** si la app es texto, el chico se aburre en tres minutos.
- *«Necesito que se entretenga y de paso aprenda algo.»*

### Lucía · 24 · estudiante de Agronomía
- **Contexto:** viene a estudiar especies concretas para un trabajo práctico.
- **Necesita:** nombre científico, familia, origen, conservación y ubicación exacta.
- **Fricción:** buscar una especie caminando el predio entero le lleva media hora.
- *«Necesito llegar a un ejemplar puntual sin dar dos vueltas al Jardín.»*

### Reparto de funciones

| Función | Sofía | Marcelo | Carla y Tomi | Lucía |
|---|---|---|---|---|
| Mapa interactivo | Crítica | Baja | Media | Crítica |
| Fichas técnicas | Media | Alta | Baja | Crítica |
| Recorridos guiados | Crítica | Media | Alta | Baja |
| Qué está en flor | Media | Crítica | Media | Media |
| Armá tu planta | Baja | Baja | Crítica | Baja |
| Actividades y voluntariado | Baja | Alta | Media | Media |

---

## 04 · Alcance y priorización (MoSCoW)

### Must have
- **Mapa interactivo de navegación** — 14 sectores, senderos, accesos, capas conmutables, búsqueda, zoom y desplazamiento, punto «estás acá».
- **Fichas técnicas de plantas** — nombre común y científico, familia, origen, porte, calendario de floración, conservación, descripción, dato de interés, usos y enlace al mapa.
- **Recorridos prearmados** — cinco itinerarios con duración, distancia, paradas numeradas, traza sobre el mapa y modo de seguimiento paso a paso.

### Should have
- **Arranque de primera vez** — tres pantallas: selección de idioma, tres ítems de cómo funciona la app, y ajuste de tamaño de texto y contraste antes de entrar.
- **Selector de idioma** — español, inglés y portugués en la interfaz de arranque, la barra de secciones y la pantalla de inicio, accesible después desde el globo del encabezado.
- **Audioguía por número** — cada parada tiene un número de audio que se teclea con botones grandes, se reproduce con la voz del sistema y trae transcripción completa.
- **Navegación paso a paso** — distancia en metros y giro hacia la parada siguiente, calculados sobre la geometría del plano.
- **Accesibilidad** — tres tamaños de texto, alto contraste, transcripciones permanentes, capa de servicios accesibles en el mapa y ficha de accesibilidad por recorrido.
- **Puntos de interés turístico** — esculturas, invernáculos, casona, columna meteorológica, jardín de mariposas, refugio climático.
- **Actividades y voluntariado** — agenda de visitas guiadas y talleres, más los tres programas de voluntariado con formulario de postulación.
- **Qué está en flor** — filtro por mes en curso, alimentado por el calendario de floración de cada ficha.
- **Escaneo de QR** — cada cartel del Jardín abre su ficha directamente.

### Could have
- **Armá tu planta** — juego de identificación por rasgos con porcentaje de coincidencia.
- **Galería del feed** — fotos de la cuenta oficial y de la comunidad, con moderación previa.
- **Colección personal** — herbario de especies guardadas e insignias por recorrido completado.
- **Recorrido propio compartible** — el visitante elige sus paradas, las ordena y comparte el itinerario por link.

### Won't have
- **Venta de entradas** — el ingreso es gratuito.
- **App nativa en tiendas** — duplica el mantenimiento y agrega fricción de descarga en la puerta.
- **Red social propia** — la comunidad ya está en Instagram; integrarse cuesta menos que competir.
- **Realidad aumentada** — alto costo, batería y compatibilidad irregular. Se evalúa en fase 3.
- **Identificación por foto** — requiere un modelo entrenado y falla mucho. iNaturalist ya lo resuelve y el Jardín ya lo usa.

---

## 05 · Arquitectura de información

```
Thays
├── Inicio
│   ├── Estado: abierto/cerrado y horario
│   ├── Accesos rápidos: ¿dónde estoy? · escanear cartel · armá tu planta · primera vez acá
│   ├── Qué está en flor este mes
│   ├── Dato del día
│   └── Este fin de semana
├── Mapa
│   ├── Buscador (especies, patrimonio, sectores)
│   ├── Capas: especies · patrimonio · servicios · recorrido activo
│   ├── Ficha rápida al tocar un pin
│   └── Zoom, desplazamiento, centrar
├── Recorridos
│   ├── Listado de 5 recorridos
│   ├── Detalle: duración, distancia, dificultad, paradas
│   └── Modo seguimiento: progreso, parada actual, siguiente
├── Descubrí
│   ├── Fichas técnicas → buscador, filtros, ficha completa
│   ├── Puntos de interés
│   ├── Armá tu planta
│   ├── Galería
│   └── Tu colección
└── Agenda
    ├── Actividades por fecha
    └── Voluntariado → tres programas + formulario
```

**Reglas de navegación**

1. Las cinco secciones raíz son hermanas: siempre accesibles, sin jerarquía entre ellas.
2. Fichas y puntos de interés se abren como **panel inferior**, no como pantalla nueva: el usuario nunca pierde el contexto del mapa o de la lista.
2 bis. Ningún modo captura la navegación. La barra de recorrido se superpone a la de secciones y se pliega a una tira mínima, pero las cinco secciones siguen a un toque.
3. Las pantallas hijas llevan botón de retroceso rotulado con el nombre de su sección padre.
4. El panel de recorrido activo flota sobre el mapa y sobrevive a la navegación entre secciones.

---

## 06 · Flujos principales

**F1 · Primera visita, sin plan (Sofía)**
Entra por Plaza Italia → ve el estado y qué está en flor → toca «Primera vez acá» → inicia el recorrido → avanza parada por parada → termina con insignia y sugerencia del próximo.

**F2 · Buscar una especie concreta (Lucía)**
Abre el mapa → escribe el nombre (común, científico o familia) → elige el resultado y el mapa se centra → lee la ficha rápida → abre la ficha completa.
*Alternativa:* escanea el QR del cartel y llega directo a la ficha.

**F3 · Visita con chicos (Carla y Tomi)**
Abre Recorridos → elige «Expedición botánica en familia» → cumple las seis misiones → juega «Armá tu planta» → abre la ficha de la especie más parecida.

**F4 · Volver (Marcelo)**
Abre la app en casa → ve qué está en flor este mes → consulta la agenda → va al Jardín con un objetivo → guarda especies en su herbario → se postula como voluntario.

---

## 07 · Especificación funcional

### M1 · Mapa interactivo
Mapa vectorial trazado sobre **el plano oficial del Jardín**, no sobre un mapa de calles. Un mapa comercial muestra el predio como un polígono verde vacío: los catorce sectores fitogeográficos, los senderos, los invernáculos y el yerbal histórico son invisibles en él.

- **Perímetro real:** Av. Las Heras, Rep. de la India, Rep. Árabe Siria con sus cruces (Juncal, Beruti, Arenales), Av. Santa Fe, y la Plaza Intendente Casares recortada al este. La Escuela Técnica de Jardinería «Cristóbal M. Hicken» aparece como predio propio dentro del Jardín.
- **Catorce sectores de la leyenda oficial:** Colección Sistemática, Plantas Medicinales, Jardín Romano, Jardín Francés, Argentina, Oceanía, América, Asia, África, Europa, Palmeral, Cicadal, Yerba Mate y Jardín de Mariposas. Se conserva el matiz de cada color institucional y se ajusta la luminosidad para leerse sobre fondo oscuro.
- **Capas conmutables:** especies, patrimonio (invernáculos A–J, esculturas, edificio central), servicios, sectores, accesibilidad y recorrido activo.
- **Dos plantas:** el predio y el interior del Invernáculo N.º 1, como los pisos de un museo.
- **Buscador unificado:** especies, patrimonio, servicios y sectores en el mismo campo.
- **Ubicación:** punto pulsante «estás acá», simulado en el prototipo. En producción, GPS con corrección de encuadre y recalibrado por número de cartel.

**Criterio de aceptación:** desde cualquier punto del mapa, llegar a la ficha de una especie en menos de tres toques.

**Nota de precisión:** el plano oficial no señala la posición de las esculturas. Esas fichas declaran su ubicación como indicativa dentro de la propia app.

### M2 · Fichas técnicas

| Bloque | Contenido | Fuente |
|---|---|---|
| Encabezado | Imagen, sector, nombre común, nombre científico en cursiva | Archivo del Jardín |
| Datos duros | Familia, altura, origen, tipo de hoja, conservación | Herbario y bibliografía |
| Calendario | Doce meses, resaltados los de floración, marcado el mes en curso | Registro fenológico |
| Descripción | Dos o tres frases sobre qué mirar y por qué esa planta es como es | Redacción propia |
| Sabías que | Un dato memorable por especie | Redacción propia |
| Usos | Ornamental, medicinal, maderable, alimentario, urbano | Bibliografía |
| Acciones | Ver en el mapa · Escuchar · Guardar | — |

> **Decisión editorial.** El bloque «Sabías que» no es decorativo: convierte una placa de museo en una historia. Que el ombú no sea un árbol sino una hierba gigante, o que seis ginkgos hayan sobrevivido a Hiroshima, es lo que el visitante le cuenta a otro. Cada ficha necesita exactamente uno.

### M3 · Recorridos guiados

| Recorrido | Duración | Distancia | Paradas | Para quién |
|---|---|---|---|---|
| Primera vez en el Jardín | 45 min | 1,2 km | 9 | Visitante nuevo |
| Árboles de mi Ciudad | 40 min | 1,0 km | 10 | Interés urbano |
| Thays y el jardín que soñó | 50 min | 1,1 km | 7 | Interés histórico |
| Mármoles bajo los árboles | 35 min | 0,8 km | 6 | Interés artístico |
| Expedición botánica en familia | 30 min | 0,7 km | 6 | Chicos desde 5 años |

El **modo seguimiento** adopta el patrón de las audioguías de museo. Con un recorrido activo:

- Las paradas se dibujan sobre el mapa como **círculos grandes numerados con ícono de auricular**; la parada actual se invierte en claro.
- Aparece la **barra de recorrido** —Anterior · Listado · Teclado · Mapa · Siguiente— flotando *sobre* la de secciones, con su propia cabecera para plegarla o terminar el recorrido. La navegación general nunca se bloquea: se puede volver al inicio sin perder el paso.
- Sobre ella, la **ficha activa**: miniatura, nombre, número de audio, parada X de N y botón de reproducción con barra de progreso.
- Encima, la **instrucción de navegación**: «Girá a la derecha · 25 m hasta la parada 3». Distancia y giro se derivan de la geometría del plano, no están escritos a mano.
- El botón **Simular** mueve el punto «estás acá» por la traza para demostrar el patrón sin salir a caminar.

La traza del recorrido se genera desde sus paradas con interpolación suave: no puede desincronizarse del contenido.

El recorrido sobrevive a la navegación: se puede abrir una ficha, ir a la agenda y volver sin perder el paso.

### M3 bis · Recorrido propio
El visitante elige paradas del catálogo completo, las ordena y las guarda. El itinerario se comparte por link (`#r=id,id,id`): quien lo abre ve las paradas y puede empezarlo. Está pensado para que un docente arme una consigna de visita.

### M4 · Puntos de interés
Quince hitos en cuatro tipos —patrimonio, escultura, naturaleza y servicio— con la misma estructura de ficha. Es la capa que explica por qué hay una loba romana en bronce en medio de un jardín botánico.

### M5 · Armá tu planta
Juego en cuatro pasos: hoja, flor, tronco y hábitat. Cada elección redibuja una planta imaginaria. Al terminar, compara los cuatro rasgos contra el catálogo y devuelve las tres especies más parecidas con su porcentaje.

**Ponderación:** hoja 30, flor 26, tronco 24, hábitat 20. Los pesos son distintos a propósito: evitan empates triples y reflejan que el follaje es el rasgo más discriminante en identificación botánica de campo.

**Por qué existe:** es el único módulo que enseña *a mirar* —el tipo de hoja, la corteza, la forma de la copa— en lugar de enseñar nombres.

### M5 bis · Audioguía
Cada especie y cada punto de interés tiene un **número de audio**: 1 a 22 las especies, 101 en adelante los puntos de interés.

- **Reproducción:** síntesis de voz del navegador en español rioplatense, con selección automática de la mejor voz disponible. No requiere descargar archivos ni tener señal.
- **Controles:** reproducir, pausar y cuatro velocidades (0,75× a 1,5×).
- **Transcripción:** el texto completo acompaña siempre al audio y puede fijarse como permanente desde los ajustes de accesibilidad.
- **Teclado numérico:** pantalla de marcado con botones grandes para escribir el número del cartel. Es la puerta de entrada principal, no un accesorio.

### M5 ter · Accesibilidad
La accesibilidad entró en la definición del producto, no en la revisión final.

| Ajuste | Qué hace |
|---|---|
| Tamaño de texto | Tres escalas: normal, grande y muy grande |
| Alto contraste | Negro y blanco puros con bordes marcados |
| Transcripción permanente | Muestra el texto completo de cada audio sin recortar |
| Capa de accesibilidad | Sanitarios accesibles, rampas, bebederos a altura y bancos a la sombra sobre el mapa |

Cada recorrido declara además: aptitud para silla de ruedas, superficie, pendiente, dónde sentarse, sombra, duración a paso lento y una advertencia concreta (por ejemplo, que el acceso al Invernáculo N.º 1 tiene un escalón de 12 cm sin rampa).

**La decisión estructural:** el número del cartel, y no el código QR, es la puerta principal a la audioguía. Funciona sin cámara, sin GPS, sin señal, con visión reducida y con un teléfono viejo. El QR queda como atajo.

### M5 quater · Arranque e idioma
La primera vez que se abre la app, antes de cualquier contenido:

1. **Idioma** — español, inglés o portugués, en botones grandes con el nombre en su propia lengua.
2. **Cómo funciona** — tres ítems con ícono: la rueda del año, el número del cartel y los recorridos con paradas.
3. **¿Lo ves cómodo?** — tamaño de texto y alto contraste, ofrecidos en la puerta y no escondidos en ajustes.

Queda guardado en el dispositivo: en la segunda visita no vuelve a aparecer. El idioma se cambia después desde el globo del encabezado de inicio.

**Alcance del multiidioma en el prototipo:** la interfaz de arranque, la barra de secciones y la pantalla de inicio. El contenido botánico permanece en español y la app lo declara en pantalla con un aviso, en lugar de fingir una traducción que no existe. Traducir las 36 fichas es trabajo de contenido de fase 2, no de interfaz.

### M6 · Galería
Grilla del feed oficial más fotos de la comunidad con hashtag. Sincronización cada seis horas por la API de Instagram, con moderación previa. Visor con autor, epígrafe y etiqueta temática.

### M7 · Agenda y voluntariado
Actividades por fecha con horario, tipo y cupo. Los tres programas del Área Educativa —Divulgadores Botánicos, Coordinación de Expediciones Botánicas y Lazos Huerteros— con requisitos y formulario de postulación de seis campos con consentimiento explícito de datos.

---

## 08 · Modelo de datos

| Entidad | Campos | Relaciones |
|---|---|---|
| **Especie** | id, nombre común, nombre científico, familia, origen, altura, floración [meses], color de flor, tipo de hoja, tipo de tronco, hábitat, descripción, dato, usos, conservación, coordenadas | pertenece a un Sector; aparece en N Paradas |
| **Sector** | id, nombre, geometría, color | contiene N Especies y N Puntos |
| **Punto de interés** | id, nombre, tipo, descripción, dato, coordenadas | pertenece a un Sector; aparece en N Paradas |
| **Recorrido** | id, nombre, resumen, duración, distancia, dificultad, traza | tiene N Paradas ordenadas |
| **Parada** | orden, referencia polimórfica (Especie o Punto), indicación | pertenece a un Recorrido |
| **Actividad** | id, nombre, fecha, horario, tipo, cupo, descripción | — |

> **La decisión que sostiene todo.** Los rasgos morfológicos —hoja, flor, tronco, hábitat— son campos estructurados, no texto libre. Esa sola decisión permite que funcionen el juego, el filtro «en flor ahora» y los recorridos temáticos sin duplicar contenido.

---

## 09 · Sistema de diseño

**Dirección: naturaleza inmersiva.** Tema oscuro único y deliberado, fotografía a sangre, interfaz flotante y translúcida.

### Por qué oscuro
Tres razones, ninguna estética. La app se usa a la intemperie bajo un dosel arbóreo, donde el contraste alto cansa menos que un fondo blanco reflejando el cielo. La fotografía botánica se lee mejor sobre negro. Y el consumo de batería importa en una visita de una hora sin enchufes.

### Las tres escalas

El sistema descansa en tres escalas y no admite valores intermedios elegidos a ojo:

| Escala | Valores | Para qué |
|---|---|---|
| **Elevación** | `--e0` fondo · `--e1` superficie · `--e2` elevada · `--e3` interactiva | Que no todo pese igual: listas en un plano, tarjetas en otro, campos y teclas en un tercero |
| **Espaciado** | 4 · 8 · 12 · 20 · 32 · 48 | Un ritmo vertical único en toda la app |
| **Tipografía** | 30 · 22 · 16 · 14 · 12 · 10 | Seis pasos: display, título, bajada, cuerpo, metadato, rótulo |

A eso se suman **tres radios** —14 para controles, 22 para tarjetas, 30 para paneles— y **una sola cabecera de pantalla**, con o sin retroceso, en lugar de que cada sección resolviera el suyo.

**Un destacado por pantalla.** Existe un tratamiento `.destacado` con degradado y borde de acento, reservado a un único elemento por vista. Si todo está destacado, nada lo está.

### Color

| Token | Hex | Rol |
|---|---|---|
| Noche | `#070C09` | Fondo base (negro con sesgo verde) |
| Corteza | `#0F1913` | Superficie de tarjeta |
| Musgo | `#17251C` | Superficie elevada |
| Tinta | `#ECF3ED` | Texto principal |
| Atenuado | `#8FA396` | Texto secundario |
| Palo borracho | `#F0709B` | Acento primario — especies vivas, traza del recorrido |
| Tipa | `#E8B24C` | Acento secundario — datos de interés, contexto histórico |
| Invernáculo | `#7ED8C3` | Interacción y estado del sistema |
| Mármol | `#DED6C6` | Patrimonio y esculturas |

**Regla:** un elemento nunca toma dos acentos a la vez.

### Tipografía

| Rol | Fuente | Especificación |
|---|---|---|
| Títulos de pantalla | Fraunces Light 300 | 30–38 px, −3 % de tracking |
| Nombres científicos | Fraunces Italic 400 | 15–19 px, sin excepción |
| Texto de interfaz | Instrument Sans Regular 400 | 14 px / 1,6 |
| Rótulos y datos | Monoespaciada de sistema | 10–11 px, +15 % de tracking, versalitas |

La serif *Fraunces* aporta la referencia a la lámina botánica antigua sin caer en la nostalgia; su eje óptico variable permite usarla fina en tamaños grandes. La sans *Instrument Sans* sostiene la interfaz sin competir. La monoespaciada solo aparece en rótulos y datos.

### Componentes

| Componente | Uso | Especificación |
|---|---|---|
| Panel inferior | Todo detalle que no cambia de sección | Radio 32 px superior, máx. 88 % de alto, cortina con desenfoque, cierre por toque fuera / Esc / navegación |
| Píldora o chip | Filtros y capas | Radio total, 12 px, activo en inverso |
| Ítem de lista | Catálogos | Miniatura 56 px, tres líneas, cheurón a la derecha |
| Etiqueta | Sector, tipo, estado | Fondo del acento al 15 %, texto del acento pleno |
| Panel flotante | Recorrido en curso | Sobre el mapa, encima de la barra de pestañas, con desenfoque |
| Aviso | Confirmaciones | Vidrio sobre tinta oscura, 2,6 s, no bloqueante |

### Accesibilidad
- **Contraste:** texto principal sobre fondo base supera 15:1. El texto atenuado nunca baja de 4,5:1.
- **Áreas táctiles:** mínimo 44 × 44 px. Los pines tienen círculo de impacto invisible mayor que el visible.
- **Teclado:** interfaz recorrible con tabulación, foco visible en verde vidrio, Esc cierra el panel abierto.
- **Movimiento:** se respeta `prefers-reduced-motion`.
- **Semántica:** pines como botones con rótulo accesible; paneles con `role="dialog"`.
- **Pendiente (fase 2):** audioguía por parada.

---

## 10 · Notas técnicas

| Aspecto | En el prototipo | En producción |
|---|---|---|
| Plataforma | Un archivo HTML autónomo, sin dependencias | Aplicación web progresiva instalable, con caché sin conexión |
| Presentación | Marco de teléfono en escritorio; pantalla completa bajo 900 px | Igual: mobile first, escritorio como vista de consulta |
| Mapa | SVG propio con desplazamiento y zoom sobre el `viewBox` | Igual, más capa de georreferenciación |
| Ubicación | Punto fijo simulado en Plaza Italia | API de geolocalización con corrección y respaldo por QR |
| Imágenes | Composiciones generadas en canvas, deterministas por semilla, con sistema de reemplazo por foto real ya montado | Fotografía del archivo del Jardín, AVIF con variantes por densidad |
| Audioguía | Síntesis de voz del navegador | Locución grabada, con la síntesis como respaldo |
| Contenido | Estructuras de datos en el propio archivo | Gestor de contenidos sin cabeza |
| Galería | Feed simulado con moderación descripta | API de Instagram, sincronización cada 6 h, moderación previa |
| Formularios | Validación en el navegador, sin envío | Integración con el Área Educativa y consentimiento registrado |

> **Por qué las imágenes se generan.** El prototipo no usa fotos de archivo porque no tenemos derechos sobre ellas. En vez de dejar rectángulos grises, se dibujan composiciones atmosféricas en canvas: una función determinista por semilla que apila capas de follaje con desenfoque, claros de luz, pétalos y grano. Cada elemento recibe siempre la misma imagen. Es una decisión de producción, no un efecto.

> **Cómo enchufar fotos reales.** La app busca `fotos/<id>.jpg` para cada especie y punto de interés y, si el archivo existe, lo superpone a la composición generada con un fundido. Sumar fotografía propia no requiere tocar una línea de código: alcanza con dejar los archivos en esa carpeta con el identificador como nombre (`palo-borracho.jpg`, `invernaculo1.jpg`, `ginkgo.jpg`). Los identificadores están listados en `fotos/LEEME.md`.

---

## 11 · Riesgos y supuestos

| Riesgo | Impacto | Mitigación |
|---|---|---|
| Señal irregular bajo el dosel | Alto | PWA con caché: mapa, fichas y recorridos disponibles sin conexión tras la primera carga |
| Precisión del GPS en 7,7 ha | Alto | El QR de cada cartel es el recalibrado real; el punto de ubicación se declara aproximado |
| El contenido envejece | Medio | Gestor de contenidos y responsable editorial designado |
| Nadie escanea los QR | Medio | Requiere cartelería nueva, legible y bien ubicada. La app no compensa un cartel malo |
| Moderación de la galería | Medio | Toda foto de comunidad pasa por revisión antes de publicarse |
| Obra en curso en el predio | Bajo | Sectores y recorridos deben poder marcarse como cerrados desde el gestor |

**Supuestos que habría que validar**

1. Que el visitante está dispuesto a usar el teléfono durante la visita, y no viene justamente a despegarse de él.
2. Que el Jardín puede sostener la carga editorial de mantener las fichas actualizadas.
3. Que la cartelería física puede modificarse para incorporar los QR.
4. Que 19 fichas alcanzan para la versión 1 y el catálogo puede crecer hasta 200 especies señalizadas.

---

## 12 · Roadmap

| Fase | Plazo | Entrega | Condición de salida |
|---|---|---|---|
| **1 · Fundación** | 0–3 meses | Mapa, 50 fichas, 5 recorridos, PWA, QR en los carteles del sendero «Árboles de mi Ciudad» | Un visitante nuevo completa un recorrido sin ayuda |
| **2 · Profundidad** | 3–6 meses | Puntos de interés, agenda y voluntariado en vivo, «qué está en flor», audioguía, gestor de contenidos | El Jardín publica contenido sin intervención de desarrollo |
| **3 · Comunidad** | 6–12 meses | Juego, galería, colección e insignias, integración con iNaturalist, catálogo a 200 especies | 25 % de usuarios recurrentes a seis meses |

---

## 13 · Guion de demo (8 minutos)

Abrí el prototipo en Chrome antes de empezar y dejalo en Inicio.

**0:00 — Abrir con el problema, no con la app.** Mostrá la pantalla de inicio en silencio dos segundos antes de hablar.
> «El Jardín Botánico tiene 5.500 especies y más de treinta esculturas. El visitante promedio se queda veinte minutos y se va sin entender nada de lo que vio. No es un problema de contenido: el contenido está. Es un problema de canal.»

**1:00 — Inicio: el estado del Jardín.** Señalá la píldora de horario y la fila «en flor».
> «Lo primero que ve no es un menú: es si el Jardín está abierto y qué está floreciendo hoy. Es el motivo por el que vuelve.»

**2:00 — Mapa: la orientación.** Apagá y encendé la capa de Patrimonio. Acercá con la rueda. Buscá «ombú» y tocá el resultado.
> «El mapa no es de calles: es el predio real, con sus catorce sectores. Las capas dejan al visitante elegir qué le interesa. Y el buscador lo lleva a un ejemplar puntual sin dar dos vueltas.»

**3:15 — Ficha: el corazón del producto.** Abrí la ficha completa del ombú. Bajá hasta el calendario y hasta «Sabías que».
> «Todas las fichas tienen la misma estructura, así son comparables. Y todas tienen un dato que el visitante se lleva puesto: el ombú no es un árbol, es una hierba gigante. Eso es lo que después le cuenta a alguien.»

**4:30 — Recorridos: el relato.** Abrí «Primera vez en el Jardín», tocá Iniciar y avanzá dos paradas.
> «Acá el producto deja de ser una base de datos y se vuelve una experiencia. La traza aparece sobre el mapa, el panel dice qué mirar en cada parada, y el recorrido sobrevive si el visitante se distrae con otra cosa.»

**6:00 — Armá tu planta: el módulo para chicos.** Jugá los cuatro pasos y abrí una de las coincidencias.
> «Este es el único módulo que enseña a mirar en vez de enseñar nombres. Elegís hoja, flor, tronco y hábitat, y el sistema te dice a qué especie del Jardín te acercaste. Termina siempre en una ficha real.»

**7:00 — Agenda y voluntariado: el cierre institucional.**
> «El Jardín ya tiene tres programas de voluntariado y convoca entre febrero y marzo. Hoy esa información vive en un blog. Acá está donde está el visitante que ya se enamoró del lugar.»

**7:40 — Cerrar con el alcance.** Volvé a Inicio. No prometas la fase 3.
> «Lo que vieron es la fase 1: mapa, fichas y recorridos. El juego y la galería son fase 3 y están acá para mostrar hacia dónde puede crecer, no para pedirlos ahora.»

**Dos cosas que conviene decir vos antes de que las pregunten:** que las imágenes están generadas por código porque no tenemos derechos sobre las fotos del archivo; y que el punto de ubicación es simulado, porque el GPS urbano tiene un margen de error mayor que la distancia entre dos sectores del Jardín.

---

## 14 · Uso en clase

### Qué muestra el caso
- **Que la documentación viene antes que la pantalla.** El orden de este dossier es el orden real del trabajo.
- **Que priorizar es decir que no.** La lista de *won't have* es tan importante como la de *must have*.
- **Que el contenido estructurado habilita funciones.** Los rasgos morfológicos como campos —y no como prosa— hacen posible el juego y el filtro de floración con una sola base.
- **Que la dirección visual se argumenta.** El tema oscuro no se eligió porque «queda bien».

### Cuatro ejercicios sobre este mismo caso
1. **Redacción de fichas.** Tres especies por estudiante, con la estructura de siete bloques. La consigna difícil es el «Sabías que»: exige investigación real.
2. **Rediseño de dirección visual.** Mismo alcance y misma arquitectura, otra dirección: botánico contemporáneo, ilustrado editorial o minimal moderno. Obliga a separar estructura de estilo.
3. **Sexto recorrido.** Diseñar un itinerario nuevo con su público, sus paradas y su justificación.
4. **Auditoría crítica.** Encontrar tres decisiones discutibles en este prototipo y argumentar la alternativa. Siempre hay más de tres.

> **Nota sobre el uso de IA.** Este caso se produjo con asistencia de IA en todas sus etapas: investigación de fuentes, redacción, escritura del código y prueba automatizada del prototipo en el navegador. Lo que no delegó la IA fue el criterio: qué problema resolver, a quién, con qué alcance y por qué esa dirección visual y no otra. Esa distinción —ejecución delegable, criterio no delegable— es discutible en clase y probablemente sea la conversación más útil que ofrece el caso.

---

## 15 · Fuentes

- [Agenda del Jardín Botánico](https://buenosaires.gob.ar/vicejefatura/ambiente/jardin-botanico/agenda-del-jardin-botanico) — GCBA. Visitas guiadas, expediciones en familia, biblioteca infantil, centro de interpretación.
- [Sendero «Árboles de mi Ciudad»](https://www.buenosaires.gob.ar/jardinbotanico/recorre-el-jardin/sendero-arboles-de-mi-ciudad) — GCBA. Fichas de especies del arbolado porteño.
- [Jardín Botánico Carlos Thays](https://buenosaires.gob.ar/areas/med_ambiente/espacios_verdes/botanico.php?menu_id=6449) — GCBA. Horarios, superficie, colecciones, invernáculo.
- [Voluntariados en Educación](https://educacionjbct.wordpress.com/voluntariado/) — Área Educativa del Jardín Botánico Carlos Thays.
- [Jardín botánico de Buenos Aires](https://es.wikipedia.org/wiki/Jard%C3%ADn_bot%C3%A1nico_de_Buenos_Aires) — Wikipedia. Historia, sectores fitogeográficos, esculturas, invernáculos, refugio climático.
- [El Jardín Botánico de Buenos Aires: una sinfonía viva de arte, ciencia y memoria](https://palermonline.com.ar/wordpress/el-jardin-botanico-de-buenos-aires-una-sinfonia-viva-de-arte-ciencia-y-memoria/) — Palermonline. Especies destacadas y patrimonio escultórico.

---

*Trabajo académico sin fines comerciales, realizado como material de cátedra para Diseño Gráfico 3. No representa al Gobierno de la Ciudad de Buenos Aires ni al Jardín Botánico Carlos Thays.*
