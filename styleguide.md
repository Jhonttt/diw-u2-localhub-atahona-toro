# Guía de estilos — LocalHub (12 h)

## Paleta
- Brand: `#1e293b`  •  Acento: `#0ea5e9`  •  Texto: claro `#111111` / oscuro `#e6edf3` • Color 1:` #ddd` • Gradiente 1: `#fafafa` • Gradiente 2: `#ffffff` • Gradiente 3: `#111111`

## Tipografía
- Base: system-ui; Tallas: `--step-0`, `--step-1`, `--step-2` (ver `css/main.css`).

## Espaciado
- Escala: `--space-1`, `--space-2`, `--space-3`.

## Componentes mínimos
- Botón `.btn` — estados `:hover`/`:focus-visible`.
- Tarjeta `.card` — dentro de `.grid-auto`.
- Navegación `.site-nav` — distribución con Flex.

## Layout / Grid
- Layout principal: `.layout` — grid con 3 columnas, header/main/footer  
- Grid automático: `.grid-auto` — tarjetas responsive con `minmax(18rem, 1fr)`  
- Pie de página `.site-footer` — grid centrado, separado del contenido principal

## Responsive
- Móvil: `max-width: 639px`  
- Ajustes de márgenes, tamaños de título y botones  
- Grid y layout adaptables al ancho de pantalla

## Accesibilidad
- Foco visible, contraste AA, navegación por teclado, `alt`/labels.
