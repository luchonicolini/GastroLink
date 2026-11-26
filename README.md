# 🍽️ GastroLink — Digital Menu & Link-in-Bio for Restaurants

<div align="center">

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![CSS3](https://img.shields.io/badge/Glassmorphism-2962FF?style=for-the-badge&logo=css3&logoColor=white)
![Responsive](https://img.shields.io/badge/Design-Mobile--First-success?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)

<p align="center">
  <b>Una solución web premium, ligera y 100% personalizable de enlace en biografía (Link-in-Bio) y carta digital interactiva para el sector gastronómico.</b>
</p>

[Ver Demo](#-demostración-en-vivo) • [Características](#-características-principales) • [Estructura](#-estructura-del-proyecto) • [Personalización](#-cómo-adaptarlo-a-cualquier-restaurante) • [Deploy](#-despliegue-rápido)

</div>

---

## 📌 ¿Qué es GastroLink?

**GastroLink** nace como una alternativa de alto impacto visual frente a los árboles de enlaces convencionales (como Linktree o Beacons). Diseñado específicamente para **restaurantes, bistrós, cafeterías, bares y locales gastronómicos**, combina la simplicidad de un portal de accesos directos con la elegancia de una **carta gastronómica digital navegable**.

El proyecto está concebido bajo una arquitectura **White-Label (marca blanca)**: con cambios mínimos en variables de estilo, imágenes y textos, puede adaptarse a la identidad corporativa de cualquier establecimiento culinario.

---

## ✨ Características Principales

### 📱 1. Portal de Enlaces (`index.html`)
* **Diseño Glassmorphism Premium**: Botones con efecto de vidrio esmerilado (`backdrop-filter: blur`), bordes con brillo sutil y textura de ruido SVG para evitar gradientes planos.
* **Hero con Máscara Radial**: El logotipo y la cabecera se funden suavemente con el fondo del perfil mediante gradientes y máscaras CSS.
* **Micro-interacciones Táctiles**: Físicas elásticas (spring physics) al interactuar con los enlaces en dispositivos móviles y de escritorio.
* **Integración con Redes y WhatsApp**: Enlaces directos a perfiles sociales (Instagram, TikTok, Spotify) y botón prioritario para reservas o pedidos vía WhatsApp con insignia gráfica.
* **Compartir Nativo (Web Share API)**: Barra superior con botón flotante que activa el menú nativo de compartir del smartphone (WhatsApp, Instagram Stories, AirDrop) o copia el enlace con toast interactivo de confirmación.

### 📖 2. Carta Gastronómica Digital (`menu.html`)
* **Navegación Sticky por Categorías**: Barra superior pegajosa con scroll automático suave hacia cada sección (Antipasti, Pastas, Ensaladas, Postres, Vinos).
* **Tipografía Editorial**: Combinación cuidada de tipografía display serif (*Bodoni Moda*) para títulos elegantes y sans-serif legible (*Montserrat*) para descripciones de platos e ingredientes.
* **Detalle de Platos y Precios**: Estructura clara para descripción de ingredientes, opciones para celíacos o vegetarianos, y maridaje de bebidas.
* **Ilustraciones Integradas**: Acentos visuales que enriquecen la experiencia del comensal en mesa (escaneo de código QR).

### ⚡ 3. Rendimiento y Accesibilidad
* **Cero Dependencias Pesadas**: Construido con HTML5 semántico, Tailwind CSS y Vanilla JS. Carga ultra rápida sin latencia de frameworks.
* **100% Mobile-First**: Optimizado para pantallas táctiles de smartphones, la principal fuente de visitas desde códigos QR y perfiles de Instagram.
* **Soporte PWA / Safe Areas**: Respeta los márgenes seguros (`viewport-fit=cover`) de iPhones con notch e islas dinámicas.

---

## 📂 Estructura del Proyecto

```plaintext
GastroLink/
├── index.html              # Portal principal Link-in-Bio (Landing)
├── menu.html               # Carta gastronómica interactiva y categorizada
├── assets/
│   ├── hero.png            # Logotipo / imagen destacada del restaurante
│   ├── hero-blur.png       # Resplandor ambiental para el fondo hero
│   ├── whatsapp-thumb.png  # Miniatura gráfica para el botón de WhatsApp
│   └── menu/               # Ilustraciones y recursos visuales de la carta
│       ├── spaghetti.png
│       ├── lasagna.png
│       ├── wine-glass.png
│       └── ...
├── .gitignore              # Archivos y carpetas excluidas de Git
└── README.md               # Documentación del proyecto
```

---

## 🎨 Cómo adaptarlo a cualquier restaurante

GastroLink está pensado para que cualquier desarrollador o dueño de restaurante pueda personalizarlo en pocos minutos:

### 1. Cambiar los colores de marca
En `index.html`, ajusta las variables CSS o clases de Tailwind en la cabecera:
```html
<style>
  :root {
    --profile-bg: #10215c; /* Color de fondo corporativo */
    --button-bg: rgba(255, 255, 255, 0.12); /* Fondo de los botones */
  }
</style>
```

### 2. Sustituir los recursos gráficos
Reemplaza los archivos en `assets/`:
* `assets/hero.png`: El logo o isotipo del nuevo local.
* `assets/hero-blur.png`: Versión difuminada para el resplandor ambiental superior.
* `assets/whatsapp-thumb.png`: Icono o logo para pedidos y reservas.

### 3. Configurar enlaces y WhatsApp
Modifica los atributos `href` en `index.html` con las URLs del restaurante:
```html
<a href="https://wa.me/54911XXXXXXXX?text=Hola,%20quiero%20hacer%20una%20reserva" target="_blank">
  Reservar por WhatsApp
</a>
```

### 4. Actualizar la carta de platos
En `menu.html`, añade, edita o elimina platos fácilmente cambiando los bloques de categoría:
```html
<article class="menu-item">
  <div class="menu-item__head">
    <h3>Nombre del Plato</h3>
    <span class="price">$12.500</span>
  </div>
  <p class="description">Descripción de los ingredientes y detalles del plato.</p>
</article>
```

---

## 🚀 Despliegue Rápido

Al ser un proyecto estático (Vanilla HTML/CSS/JS), puedes publicarlo gratis en segundos en cualquier plataforma:

* **GitHub Pages**: Ve a `Settings` > `Pages` > Selecciona la rama `main` y guarda.
* **Vercel**: Importa el repositorio `GastroLink` y haz click en **Deploy**.
* **Netlify**: Arrastra la carpeta o conecta el repositorio de GitHub.

---

## 🛠️ Tecnologías Utilizadas

* **HTML5 Semántico**: Para estructura, accesibilidad y soporte SEO.
* **Tailwind CSS**: Estilos utilitarios rápidos y consistentes.
* **CSS3 Custom Properties & Backdrop Filter**: Glassmorphism avanzado, gradientes radiales y animaciones fluidas.
* **Vanilla JavaScript (ES6+)**: Manejo de Web Share API, clipboard fallback y navegación por anclas.
* **Google Fonts**: *Sora*, *Manrope*, *Bodoni Moda* y *Montserrat*.

---

## 👤 Autor

Desarrollado por **Luciano Nicolini**

* 🐙 **GitHub**: [@luchonicolini](https://github.com/luchonicolini)
* 💼 **Email**: [nicolini.luciano@hotmail.com](mailto:nicolini.luciano@hotmail.com)

---

## 📄 Licencia

Este proyecto se distribuye bajo la licencia **MIT**. Puedes usarlo libremente para proyectos personales o comerciales.
