# LocalHub Landing — U.D. 2 (12 h) Estilos con Flexbox y Grid

**Objetivo**: landing one-page responsive y accesible. **Grid** para macro-layout (elige UNA técnica: áreas _o_ auto-fit/minmax). **Flexbox** para nav y tarjetas. **2 puntos de corte** (libres). Accesibilidad AA básica. _Opcional_: micro‑Sass.

## Estructura
```
/localhub-landing-12h/
├─ index.html
├─ css/main.css
├─ sass/  (opcional – micro‑Sass)
├─ img/
└─ styleguide.md
```

## Flujo de trabajo recomendado
- S1: Skeleton + Grid macro.
- S2: Flex micro (nav + cards) + 1er breakpoint.
- S3: Accesibilidad + validación + 2º breakpoint.
- S4: Afinado visual + documentación + demo (5').

## Requisitos mínimos
- Responsive con **2 breakpoints** (libres).
- Grid:  **auto-fit/minmax**
- Flex: nav + cards.
- Accesibilidad AA: contraste, `:focus-visible`, `alt`, labels y teclado.
- Validación HTML/CSS (adjunta evidencias en forma de pantallazo junto con la entrega).
- Documentación breve: `README.md`, `styleguide.md`, **2 capturas** (móvil y escritorio).

## Mejora 1 (opcional)
- Tema claro/oscuro con Custom Properties + tipografía fluida `clamp()`.

## Mejora 2 (opcional) — micro‑Sass
- Solo `sass/_variables.scss`, `sass/_mixins.scss` y `sass/main.scss` con 1 mixin de breakpoint. Compila a `css/main.css` con **VSCode Live Sass Compiler**.

## Checklist (resumen)
Consulta `CHECKLIST.md` y márcala en la entrega final.

## Uso de IA
 Uso de herramientas como ChatGPT para dos funcionalidades en específico:

 - Implementación de un color de gradiente al borde del input utilizando `border-image`.
 - Funcionamiento de `grid-template-areas` especificamente para centrar contenidos dejando las columnas vacías a los lados.
 - Funcionamiento de la propiedad `scroll-behavior:smooth` aplicada al elemento raíz, para controlar la animación del desplazamiento cuando se navega por los enlaces de 'Servicios' y 'Contacto'.

## Decisiones Tomadas
**Imágenes:** en este proyecto no hemos utilizado imágenes, por lo que no fue necesario declaralas en el html. 
Aún así, si en un futuro se incorporan, la forma correcta de incluirlas sería: 
- Cuando se aporta información de importancia: `<img src='imagenes/logotipo.png' alt='Logotipo de la empresa'>`.
-Cuando la imagen es únicamente decorativa :`<img src='imagenes/logotipo.png' alt='' aria-hidden='true'>`.

**Grid:** en nuestro caso no hemos utilizado únicamente un solo método de grid, si no, que hemos combinado dos métodos diferentes, según las necesidades del diseño:

- **áreas:** para la organización general del layout hemos optado por usar Grid con áreas, ya que nos permite definir de manera clara la estructura principal de la página, y centrar el contenido dejando columnas vacias a los costados, ofreciendo flexibilidad.

- **auto-fit/minmax:** en este caso hemos elegído utilizar estos métodos para la selección de tarjetas porque ofrece uun comportamiento completamente responsive sin necesidad de múltiples breakpoints, esta combinación permite que las tarjetas se ajusten automáticamente al ancho disponible de la página.

**breakpoint:** decidimos utilizar un breakpoint específico a 607px, porque a esa anchura observamos un cambio clave en el comportamiento del diseño, ya que el grid de las tarjetas ya fuerza naturalmente la disposición en una sola columna, pero elementos como los márgenes, botones y títulos necesitaban un ajuste adicional.

**sticky:** en la barra de navegación utilizamos `position:sticky` para mantenerla siempre visible mientras el usuario hace scroll. Mejorando la accesibilidad y experiencia de uso, ya que permite acceder rápidamente al menú sin necesidad de volver a la parte superior de la página. Además solo se fija cuando llega al borde superior, evitando ocupar espacio innecesario antes de tiempo.

**separator:** debido a que el header es sticky, al hacer scroll el título de "Servicios" quedaba oculto bajo la barra de navegación, para corregir este incovenietne, añadimos un separador con una etiqueta `<div id='separator'></div>`, introduciendo un pequeño margen visual que evita que el título quede cubierto, cabe destacar que dicho elemento es invisible. 

**hover:** uso de la pseudoclase `.btn:hover` para cambiar el color de los botones al situar el cursor encima de ellos.

## Evidencias
**assets/screenshots:** creación de las carpetas para guardar evidencias de la página web tanto para móvil como para escritorio con píxeles de 360px en caso de celular y 1024px para ordenador.