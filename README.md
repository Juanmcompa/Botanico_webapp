# Thays — App del Jardín Botánico de Buenos Aires

Prototipo navegable de alta fidelidad y documentación de producto completa para una app del **Jardín Botánico Carlos Thays** (Palermo, CABA).

Material de cátedra para **Diseño Gráfico 3**, FADU. Trabajo académico sin fines comerciales.

### ▶ [Ver el prototipo](https://juanmcompa.github.io/Botanico_webapp/) · 📗 [Ver la documentación](https://juanmcompa.github.io/Botanico_webapp/dossier.html)

<p>
  <img src="capturas/inicio.png" width="260" alt="Pantalla de inicio">
  <img src="capturas/mapa.png" width="260" alt="Mapa interactivo del predio">
</p>

---

## Qué es

Una app de sitio para el visitante del Jardín. El problema que ataca es concreto: el Jardín tiene 5.500 especies y más de treinta esculturas, y el visitante promedio se queda veinte minutos y se va sin entender nada de lo que vio. No es un problema de contenido —el contenido está— sino de canal.

| | |
|---|---|
| **Imprescindible** | Mapa interactivo · Fichas técnicas · Recorridos prearmados |
| **Deseable** | Armá tu planta · Galería del feed · Puntos de interés · Actividades y voluntariado |
| **Dirección visual** | Naturaleza inmersiva — tema oscuro, imagen a sangre, interfaz flotante |
| **Plataforma** | App web, mobile first. En escritorio se ve enmarcada como teléfono; en mobile ocupa toda la pantalla |

## Cómo verlo

Entrá al [link de arriba](https://juanmcompa.github.io/Botanico_webapp/), o descargá `index.html` y abrilo en Chrome.

**No necesita servidor ni instalación**: es un único archivo HTML autónomo, sin dependencias más allá de las tipografías de Google Fonts. En un teléfono se ve a pantalla completa, como una app nativa. En escritorio aparece dentro de un marco de teléfono, con las notas del proyecto a los costados.

<img src="capturas/escritorio.png" width="620" alt="Vista de escritorio con el marco de teléfono">

## Contenido del prototipo

- **Mapa interactivo** — 14 sectores reales del predio, senderos, tres accesos, capas conmutables (especies, patrimonio, servicios, recorrido activo), buscador unificado, zoom y desplazamiento.
- **19 fichas técnicas** — familia, origen, porte, calendario de floración mes a mes, estado de conservación, descripción, usos y un dato memorable por especie.
- **5 recorridos guiados** — con traza sobre el mapa, paradas numeradas y modo de seguimiento paso a paso.
- **15 puntos de interés** — invernáculo art nouveau, casona de Thays, columna meteorológica, esculturas, jardín de mariposas, refugio climático.
- **Armá tu planta** — juego de identificación por rasgos (hoja, flor, tronco, hábitat) con porcentaje de coincidencia contra el catálogo.
- **Galería** — grilla del feed con filtros temáticos y visor.
- **Agenda y voluntariado** — actividades reales del Jardín y los tres programas del Área Educativa con formulario de postulación.

## Estructura del repositorio

```
├── index.html                            El prototipo navegable
├── dossier.html                          La documentación de producto, en HTML
├── docs/
│   └── documentacion-de-producto.md      La misma documentación, en Markdown editable
├── capturas/                             Capturas de las pantallas principales
└── .nojekyll                             Para que GitHub Pages sirva el HTML tal cual
```

## La documentación

El dossier cubre el paquete completo: contexto y problema, objetivos con métricas, cuatro personas de usuario, alcance priorizado por MoSCoW (incluida la lista de *won't have*), arquitectura de información, cuatro flujos principales, especificación funcional por módulo, modelo de datos, sistema de diseño documentado, notas técnicas, riesgos y supuestos, roadmap en tres fases, un guion de demo cronometrado de ocho minutos y una sección final con cuatro ejercicios para dar el caso en clase.

## Sobre los datos y las imágenes

**Los datos son reales.** Historia, superficie, sectores fitogeográficos, especies con su nombre científico y su familia, esculturas con autor, horarios, programación y los tres programas de voluntariado provienen de fuentes públicas del Gobierno de la Ciudad de Buenos Aires y del Área Educativa del Jardín.

**Las imágenes no son fotografías.** Son composiciones atmosféricas generadas en `<canvas>` por una función determinista: cada elemento recibe siempre la misma imagen a partir de su identificador. Se resolvió así porque no hay derechos sobre el material fotográfico del archivo del Jardín. En producción se reemplazan por fotografía real.

## Fuentes

- [Agenda del Jardín Botánico](https://buenosaires.gob.ar/vicejefatura/ambiente/jardin-botanico/agenda-del-jardin-botanico) — GCBA
- [Sendero «Árboles de mi Ciudad»](https://www.buenosaires.gob.ar/jardinbotanico/recorre-el-jardin/sendero-arboles-de-mi-ciudad) — GCBA
- [Jardín Botánico Carlos Thays](https://buenosaires.gob.ar/areas/med_ambiente/espacios_verdes/botanico.php?menu_id=6449) — GCBA
- [Voluntariados en Educación](https://educacionjbct.wordpress.com/voluntariado/) — Área Educativa del Jardín Botánico Carlos Thays
- [Jardín botánico de Buenos Aires](https://es.wikipedia.org/wiki/Jard%C3%ADn_bot%C3%A1nico_de_Buenos_Aires) — Wikipedia
- [Una sinfonía viva de arte, ciencia y memoria](https://palermonline.com.ar/wordpress/el-jardin-botanico-de-buenos-aires-una-sinfonia-viva-de-arte-ciencia-y-memoria/) — Palermonline

## Licencia y aviso

Publicado bajo [CC0 1.0 Universal](LICENSE): dedicación al dominio público, uso libre sin necesidad de atribución.

Este es un **ejercicio académico**. No representa, ni fue encargado por, el Gobierno de la Ciudad de Buenos Aires ni el Jardín Botánico Carlos Thays. Los nombres y datos de la institución se usan con fines didácticos.
