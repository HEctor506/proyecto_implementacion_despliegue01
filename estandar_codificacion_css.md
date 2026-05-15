# Estándar de Codificación CSS

## Propósito

Este documento establece un conjunto de buenas prácticas para la escritura de estilos en CSS, integrando tanto CSS tradicional como el uso de Tailwind CSS. Su objetivo es garantizar código legible, mantenible, consistente y escalable en proyectos web.

---

## 1. Organización y estructura

### 1.1 Criterio: Estructura del proyecto

Separar estilos en archivos `.css` cuando se use CSS tradicional, por ejemplo:

En la carpeta `stylesheets`, el archivo `style.css`, contiene las reglas CSS del sitio web.

### 1.2 Criterio: Orden del código

Definir primero estilos globales (`body`, `html`), luego componentes (`header`, `nav`, `cards`, `footer`), por ejemplo:

```css
/* 1. Importaciones */
@import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;700&display=swap');

/* 2. Estilos globales */
body {
    min-height: 100dvh;
}

/* 3. Componentes y utilidades */
.active-pill {
    background-color: #f97306;
    color: #ffffff;
}
```

### 1.3 Criterio: Comentarios

Usar comentarios para dividir secciones del archivo CSS, por ejemplo:

```css
/* Fuentes e Iconos Globales */

/* Componentes y Utilidades */

/* Animaciones Custom */

/* SPA Views */
```

## 2. Sintaxis y formato

### 2.1 Criterio: Sintaxis  

Usar correctamente `selector { propiedad: valor; }`, por ejemplo:

```css
.active-pill {
    background-color: #f97306;
    color: #ffffff;
}
```

### 2.2 Criterio: Indentación 

2 o 4 espacios consistentes, por ejemplo:

```css
.no-scrollbar {
    -ms-overflow-style: none;
    scrollbar-width: none;
}
```

### 2.3 Criterio: Cierre de reglas  

Siempre cerrar con `;` y `}`, por ejemplo:

```css
body {
    min-height: 100dvh;
}
```

### 2.4 Criterio: Legibilidad 

Una propiedad por línea, por ejemplo:

```css
.material-symbols-outlined {
    font-variation-settings: 'FILL' 0, 'wght' 400, 'GRAD' 0, 'opsz' 24;
}
```

## 3. Uso de selectores

### 3.1 Criterio: Prioridad 

Preferir clases (.clase) sobre etiquetas o IDs, por ejemplo:

```css
/* Preferir clases específicas en lugar de redefinir etiquetas globales */
.spa-view {
    display: none;
}

.spa-view.active {
    display: block;
}
```

### 3.2 Criterio: Nombres 

Descriptivos, en minúsculas y con guiones (`.menu-principal`), por ejemplo:

```css
.active-pill { ... }
.no-scrollbar { ... }
.step-active { ... }
.logo-twist { ... }
.hover-scale { ... }
```

### 3.3 Criterio: Complejidad 

Evitar selectores anidados innecesarios, por ejemplo:

```css
/* Correcto: Selector plano y directo */
.btn-add {
    position: relative;
}

/* Incorrecto: Demasiado anidado innecesariamente */
header div.flex button.btn-add {
    position: relative;
}
```

## 4. Uso de clases

### 4.1 Criterio: Claridad  

Usar clases que representen claramente la intención visual, por ejemplo:

```html
<button class="bg-primary text-white font-bold py-4 px-8 rounded-full shadow-lg">
    Order Now
</button>
```

### 4.2 Criterio: Orden 

Mantener un orden lógico: `layout → espaciado → color → tipografía`, por ejemplo:

```html
<!-- Layout → Espaciado → Color → Transiciones -->
<header class="fixed top-0 w-full h-16 px-6 bg-background border-b border-border transition-colors">
```
### 4.3 Criterio: Legibilidad 

Evitar listas desordenadas de clases, por ejemplo:

```html
<!-- Mantener un número razonable de clases ordenadas por su propósito -->
<div class="max-w-container-max mx-auto grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
```

## Referencias

* CSS | MDN. (n.d.). Retrieved May 14, 2026 from https://developer.mozilla.org/es/docs/Web/CSS
* All CSS specifications. (n.d.). Retrieved May 14, 2026 from https://www.w3.org/Style/CSS/specs.en.html
* Tailwind CSS - Rapidly build modern websites without ever leaving your HTML. (n.d.). Retrieved May 14, 2026 from https://tailwindcss.com/