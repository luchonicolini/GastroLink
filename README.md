# GastroLink — Digital Menu & Link-in-Bio for Restaurants

<div align="center">

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![CSS3](https://img.shields.io/badge/Glassmorphism-2962FF?style=for-the-badge&logo=css3&logoColor=white)
![Responsive](https://img.shields.io/badge/Design-Mobile--First-success?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)

<p align="center">
  <b>Solución web ligera y personalizable de enlace en biografía (Link-in-Bio) y carta gastronómica interactiva para restaurantes y locales culinarios.</b>
</p>

[Visión General](#visión-general) • [Características](#características) • [Estructura del Proyecto](#estructura-del-proyecto) • [Personalización](#guía-de-personalización) • [Despliegue](#despliegue)

</div>

---

## Visión General

GastroLink es una solución web orientada al sector gastronómico diseñada para sustituir los árboles de enlaces genéricos (como Linktree o Beacons) por una experiencia visual alineada a la identidad de un restaurante.

El proyecto combina un portal de accesos directos (redes, reservas por WhatsApp, ubicación y delivery) con una carta digital interactiva estructurada por secciones. Está construido bajo una arquitectura de marca blanca (white-label), lo que permite reutilizar el código base y adaptarlo a distintos establecimientos culinarios modificando variables de diseño, recursos gráficos y contenidos.

---

## Características

### 1. Portal de Enlaces (index.html)
* **Interfaz con Glassmorphism**: Botones con efecto de desenfoque (`backdrop-filter`), bordes con contraste sutil y textura de ruido para evitar gradientes planos.
* **Cabecera con Máscara Radial**: Integración fluida del logotipo con el fondo mediante gradientes y máscaras CSS.
* **Micro-interacciones**: Transiciones con físicas elásticas en estados de hover y active optimizadas para pantallas táctiles.
* **Acceso Directo a WhatsApp y Redes**: Botón destacado con miniatura gráfica para reservas directas y enlaces a perfiles sociales.
* **Web Share API**: Botón superior que invoca el diálogo nativo de compartir del sistema operativo móvil, con fallback automático de copiado al portapapeles.

### 2. Carta Gastronómica Digital (menu.html)
* **Navegación Sticky por Categorías**: Barra superior con anclaje fijo y scroll suave hacia cada sección del menú (Entradas, Pastas, Ensaladas, Postres, Vinos).
* **Tipografía Editorial**: Combinación de fuentes display serif (*Bodoni Moda*) para encabezados y sans-serif (*Montserrat*) para ingredientes y descripciones de platos.
* **Detalle de Ítems**: Estructura modular para nombres de platos, precios, especificaciones de ingredientes y notas de maridaje.
* **Ilustraciones Integradas**: Acentos visuales vectoriales pensados para la lectura del comensal desde códigos QR en mesa.

### 3. Rendimiento y Accesibilidad
* **Sin Dependencias de Runtime**: Construido exclusivamente con HTML5 semántico, Tailwind CSS y JavaScript vanilla.
* **Enfoque Mobile-First**: Diseñado priorizando la experiencia en smartphones, fuente principal de tráfico en gastronomía.
* **Compatibilidad con Áreas Seguras**: Configuración de `viewport-fit=cover` para pantallas con notch e isla dinámica.

---

## Estructura del Proyecto

```plaintext
GastroLink/
├── index.html              # Portal principal Link-in-Bio
├── menu.html               # Carta gastronómica interactiva
├── assets/
│   ├── hero.png            # Logotipo / imagen principal
│   ├── hero-blur.png       # Resplandor ambiental de cabecera
│   ├── whatsapp-thumb.png  # Miniatura gráfica para botón de WhatsApp
│   └── menu/               # Ilustraciones de secciones y platos
│       ├── spaghetti.png
│       ├── lasagna.png
│       ├── wine-glass.png
│       └── ...
├── .gitignore              # Archivos excluidos del control de versiones
└── README.md               # Documentación técnica del repositorio
```

---

## Guía de Personalización

Para adaptar GastroLink a otro restaurante:

### 1. Colores e Identidad Visual
En `index.html`, modificar los valores de las variables en la sección de estilos:
```html
<style>
  :root {
    --profile-bg: #10215c; /* Fondo general del perfil */
    --button-bg: rgba(255, 255, 255, 0.12); /* Fondo de los botones */
  }
</style>
```

### 2. Recursos Gráficos
Reemplazar los archivos dentro de la carpeta `assets/`:
* `assets/hero.png`: Logotipo o isotipo del restaurante.
* `assets/hero-blur.png`: Imagen difuminada para el resplandor superior.
* `assets/whatsapp-thumb.png`: Icono o distintivo del canal de reservas.

### 3. Enlaces y Canales de Contacto
Actualizar las rutas y números telefónicos en `index.html`:
```html
<a href="https://wa.me/54911XXXXXXXX?text=Hola,%20quisiera%20reservar%20una%20mesa" target="_blank">
  Reservar por WhatsApp
</a>
```

### 4. Platos y Categorías de la Carta
En `menu.html`, editar los bloques de artículos según la oferta gastronómica:
```html
<article class="menu-item">
  <div class="menu-item__head">
    <h3>Nombre del Plato</h3>
    <span class="price">$12.500</span>
  </div>
  <p class="description">Ingredientes, preparación y detalles del plato.</p>
</article>
```

---

## Despliegue

Al tratarse de una aplicación web estática sin backend, puede desplegarse de forma directa en servicios de hosting estático:

* **GitHub Pages**: En la configuración del repositorio (`Settings` > `Pages`), seleccionar la rama `main` y guardar.
* **Vercel**: Importar el repositorio `GastroLink` y ejecutar el despliegue automático.
* **Netlify**: Conectar el repositorio o arrastrar el directorio del proyecto para publicación inmediata.

---

## Tecnologías Utilizadas

* **HTML5**: Marcado semántico y accesibilidad.
* **Tailwind CSS**: Utilidades para diagramación, espaciado y tipografía.
* **CSS3**: Variables CSS, soporte de `backdrop-filter` para glassmorphism y animaciones.
* **JavaScript (ES6+)**: Implementación de Web Share API y manejo del portapapeles.
* **Google Fonts**: Familias tipográficas *Sora*, *Manrope*, *Bodoni Moda* y *Montserrat*.

---

## Autor

Desarrollado por **Luciano Nicolini**

* GitHub: [@luchonicolini](https://github.com/luchonicolini)
* Correo: [nicolini.luciano@hotmail.com](mailto:nicolini.luciano@hotmail.com)

---

## Licencia

Este proyecto se distribuye bajo la licencia **MIT**. Su uso es libre tanto para fines personales como comerciales.
