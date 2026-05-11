# RetroVault

Página de aterrizaje de alta fidelidad para **RetroVault**, una tienda exclusiva de consolas retro restauradas y teclados mecánicos a medida. Construida como un único archivo HTML autocontenido, sin dependencias externas más allá de Google Fonts.

---

## Características principales

### Diseño y estética
- Paleta oscura industrial: carbón profundo `#0c0b10`, blanco roto `#e8e3d5` y acento neón púrpura `#b07cff`
- Tipografía en tres capas: `Press Start 2P` para títulos (estilo pixel-art), `Space Grotesk` para cuerpo y `JetBrains Mono` para metadata y etiquetas
- Efectos CRT con líneas de escaneo, radial glows y grid de puntos — todo en CSS puro, sin imágenes externas

### Secciones de la página

| # | Sección | Descripción |
|---|---------|-------------|
| — | **Header sticky** | Logo, navegación centrada, selector de idioma y carrito con contador |
| — | **Marquee** | Banda animada con info de edición, envíos y garantía |
| 01 | **Hero** | Titular en pixel-art, deck descriptivo, CTAs y ilustración SVG del GameBoy Color translúcido + teclado RV-65 |
| 02 | **Beneficios** | Grid de 3 columnas: Restauración Experta · Mejoras Modernas · Estética Única, cada uno con micro-checklist de specs |
| 03 | **Catálogo** | Rail horizontal con 8 tarjetas de producto (consolas + teclados) con navegación por botones |
| 04 | **Proceso** | Strip de 4 pasos del taller: Diagnóstico → Recap → Mejoras → Firma |
| 05 | **Testimonios** | Rail horizontal con 5 reseñas verificadas de coleccionistas y profesionales |
| — | **Footer** | Newsletter, formulario de contacto, links de tienda/taller, redes sociales y aviso legal |

### Ilustración SVG del Hero
La pieza central del hero es una ilustración vectorial compuesta enteramente en SVG inline:
- **GameBoy Color translúcido** con carcasa semitransparente púrpura, pantalla IPS animada (píxeles parpadeantes), D-pad, botones A/B, altavoz y puerto USB-C
- **Teclado mecánico RV-65** con dos filas de teclas visibles, keycaps en off-white y acento púrpura, placa base oscura
- Filtros de sombra, glow radial y rejilla de fondo integrados con `<defs>` y gradientes

### Interactividad
- Animación de marquee infinita en CSS (`@keyframes scroll`)
- Cursor parpadeante en el titular del hero (`@keyframes blink`)
- Pulso en el indicador de estado (`@keyframes pulse`)
- Navegación del rail de catálogo con scroll suave via JavaScript (< 5 líneas)
- Formulario de newsletter con feedback visual al enviar
- Hover states en todos los elementos interactivos con transiciones CSS

### Responsivo
- Breakpoint en `980px`: hero en columna única, beneficios en una sola columna, proceso en 2 columnas, nav oculta en móvil
- Rails de scroll horizontal con `scroll-snap-type` y scrollbar oculta para experiencia táctil nativa

---

## Estructura del archivo

```
RetroVault/
└── RetroVault.html   # Página completa — HTML + CSS + SVG + JS en un solo archivo
```

---

## Cómo abrir

No requiere servidor ni proceso de build. Basta con abrir el archivo en cualquier navegador moderno:

```bash
open RetroVault.html
```

---

## Tecnologías

- HTML5 semántico
- CSS3 (custom properties, grid, flexbox, animaciones, backdrop-filter)
- SVG inline con gradientes y filtros
- JavaScript vanilla (< 10 líneas)
- Google Fonts: `Press Start 2P`, `VT323`, `Space Grotesk`, `JetBrains Mono`

---

*© 2026 RetroVault · GYE, Ecuador*
