# Documentación de Propiedades CSS y Análisis del Estándar de Codificación

Este documento tiene como propósito explicar a detalle cada una de las propiedades CSS nativas implementadas en la hoja de estilos del proyecto (**`stylesheets/style.css`**), así como desglosar y explicar a fondo el archivo de lineamientos **`estandar_codificacion_css.md`**.

---

## 1. Explicación de las Propiedades CSS del Proyecto

A continuación se detallan las propiedades nativas de CSS utilizadas en el archivo unificado `stylesheets/style.css` y su propósito específico en la interfaz:

### 🎨 Tipografía e Iconos
* **`font-variation-settings`**: Permite ajustar los ejes personalizados de fuentes variables. En nuestro proyecto se usa para la clase `.material-symbols-outlined` para definir el relleno (`FILL`), peso (`wght`), grado (`GRAD`) y tamaño óptico (`opsz`) de los iconos de Google.

### 📐 Modelo de Caja y Dimensiones
* **`width` / `height`**: Establecen la anchura y altura explícita de un elemento (ej. `4px` para los puntos indicadores del stepper).
* **`min-height`**: Define la altura mínima que debe tener un elemento. `min-height: 100dvh` asegura que el `body` ocupe al menos el 100% de la altura de la ventana gráfica dinámica (*dynamic viewport height*), adaptándose perfectamente a las barras de navegación móviles.

### 👁️ Visibilidad y Desplazamiento (*Scroll*)
* **`display: none` / `display: block`**: Controla el comportamiento de renderizado del elemento. Se usa para alternar las vistas SPA (`.spa-view`), ocultando las inactivas y mostrando la activa.
* **`::-webkit-scrollbar` (con `display: none`)**: Oculta visualmente la barra de desplazamiento en navegadores basados en WebKit (Chrome, Safari, Edge) manteniendo la capacidad de hacer scroll horizontal en las categorías.
* **`-ms-overflow-style: none`**: Oculta la barra de desplazamiento en navegadores Internet Explorer y versiones antiguas de Edge.
* **`scrollbar-width: none`**: Oculta la barra de desplazamiento estándar en el navegador Firefox.

### 📌 Posicionamiento
* **`position: absolute`**: Posiciona un elemento de forma libre respecto a su ancestro posicionado más cercano. Se utiliza para colocar el punto naranja debajo del paso activo en el stepper (`.step-active::after`).
* **`bottom` / `left`**: Coordenadas de anclaje para elementos con posicionamiento absoluto o fijo.
* **`transform`**: Modifica el espacio de coordenadas del elemento.
  * `translateX(-50%)`: Desplaza el elemento hacia la izquierda exactamente la mitad de su propio ancho, logrando un centrado horizontal perfecto.
  * `translate(-50%, 100px)`: Combina el centrado horizontal con un desplazamiento vertical, usado para ocultar el *Toast* hacia abajo antes de animarlo.

### 🌸 Decoración y Contenido
* **`background-color` / `color`**: Definen el color de fondo y el color del texto respectivamente (utilizados en las píldoras activas `.active-pill`).
* **`border-radius`**: Redondea las esquinas del borde de un elemento. Un valor de `50%` convierte un cuadrado en un círculo perfecto.
* **`content: ''`**: Propiedad obligatoria al usar pseudoelementos como `::after`. Genera un elemento en el DOM sin contenido textual para poder darle estilos visuales (como el indicador del stepper).
* **`opacity`**: Controla el nivel de transparencia de un elemento (`0` completamente invisible, `1` totalmente visible).
* **`pointer-events: none`**: Desactiva la capacidad del elemento para capturar eventos del ratón o toques. Es crucial en el *Toast* oculto para evitar que bloquee clics accidentales en la pantalla.

### 🎬 Transiciones y Animaciones
* **`transition`**: Permite que los cambios de valores de las propiedades ocurran de forma suave durante un tiempo determinado. Se configuran curvas de aceleración avanzadas como `cubic-bezier(0.25, 0.8, 0.25, 1)` para lograr animaciones muy fluidas y naturales al hacer scroll o pasar el cursor.
* **`animation`**: Aplica una secuencia de animación definida mediante fotogramas clave.
* **`@keyframes`**: Define los estados intermedios de una animación. En el proyecto tenemos:
  * `twist`: Rota el logotipo de un pretzel desde `-180deg` y una escala pequeña hasta su tamaño y ángulo original.
  * `fadeIn`: Anima suavemente la opacidad de `0` a `1` al cambiar de vista en la SPA.

---

## 2. Análisis a Detalle de `estandar_codificacion_css.md`

El archivo **`estandar_codificacion_css.md`** actúa como el "contrato de calidad" y la guía oficial de estilo del equipo. Asegura que cualquier desarrollador que toque el proyecto escriba código limpio, predecible y fácil de mantener. 

A continuación se explica el porqué de cada una de sus 4 secciones principales:

### 📂 Sección 1: Organización y estructura
* **Propósito:** Evitar el caos de tener estilos regados por todas partes.
* **Detalle:** 
  * Dicta que todo el CSS tradicional debe vivir centralizado en un único archivo (`stylesheets/style.css`), prohibiendo el uso de bloques `<style>` incrustados en el HTML.
  * Establece una jerarquía estricta de lectura: primero se importan recursos externos (`@import`), luego se definen etiquetas globales (`body`), y por último las clases utilitarias y animaciones.
  * Exige el uso de comentarios estandarizados (`/* Título */`) para actuar como separadores visuales, permitiendo navegar por un archivo largo de forma rápida.

### ✍️ Sección 2: Sintaxis y formato
* **Propósito:** Garantizar la legibilidad y facilitar las revisiones de código (*Code Reviews*) en Git.
* **Detalle:**
  * Define el uso riguroso de **4 espacios para la indentación**, evitando mezclar tabuladores y espacios que se ven distintos según el editor de cada programador.
  * Impone la regla de **una propiedad por línea**. Esto es vital porque si ocurre un error o un cambio, herramientas como Git mostrarán exactamente qué línea específica se modificó, en lugar de marcar todo un bloque incomprensible de una sola línea.
  * Obliga a cerrar siempre con punto y coma `;`, previniendo errores de interpretación en el navegador.

### 🎯 Sección 3: Uso de selectores
* **Propósito:** Mantener un alto rendimiento de renderizado y evitar colisiones (que un estilo afecte accidentalmente a otro elemento).
* **Detalle:**
  * **Prioridad a las clases:** Se prohíbe usar selectores de ID (`#id`) para aplicar estilos, ya que tienen una especificidad demasiado alta y son difíciles de sobrescribir. También se evita estilizar etiquetas genéricas de forma directa si se puede usar una clase.
  * **Nomenclatura Kebab-Case:** Nombres descriptivos, en minúsculas y separados por guiones medios (ej. `.hover-scale`). Esto hace que el código sea autoexplicativo.
  * **Baja complejidad (Aplanamiento):** Evita selectores profundamente anidados. Un selector largo como `main section div div button.btn` obliga al navegador a evaluar el árbol DOM de derecha a izquierda, consumiendo más recursos. Usar directamente `.btn` es infinitamente más rápido y modular.

### ⚡ Sección 4: Uso de clases (Enfoque Tailwind CSS)
* **Propósito:** Mantener limpio el marcado HTML cuando se utilizan frameworks de clases utilitarias como Tailwind CSS.
* **Detalle:**
  * **Claridad:** Las clases aplicadas deben reflejar el resultado visual de forma inequívoca.
  * **Orden lógico estricto:** Para evitar que las listas de clases en una etiqueta HTML parezcan una sopa de letras desordenada, se establece un orden mental al escribirlas:
    1. **Layout y Posición:** (ej. `fixed`, `absolute`, `grid`, `flex`).
    2. **Espaciado:** Dimensiones y márgenes (ej. `w-full`, `h-16`, `px-6`, `gap-4`).
    3. **Color y Fondo:** (ej. `bg-background`, `border-b`, `text-primary`).
    4. **Tipografía y Efectos:** (ej. `font-bold`, `text-xl`, `shadow-lg`, `transition-all`).
  * **Legibilidad en el HTML:** Sugiere separar estructuras complejas o aprovechar el motor de Tailwind para no saturar una sola etiqueta con decenas de clases inmanejables.
