# DarkGrid Operations — Landing Page

Landing page institucional para **DarkGrid Operations** (*Specialized Data Center Cleaning & Mission-Critical Facility Services*), desarrollada con **Astro 5**, **Tailwind CSS 4** y **Lucide Icons**, siguiendo estrictamente la guía y tokens de diseño documentados en `desing.md`.

---

## 🚀 Tecnologías Utilizadas

- **Framework:** [Astro 5](https://astro.build/)
- **Estilos:** [Tailwind CSS v4](https://tailwindcss.com/) vía `@tailwindcss/vite`
- **Iconografía:** [Lucide Icons](https://lucide.dev/) (sin emojis, 100% SVG vectorial corporativo)
- **Tipografía:** [Inter](https://fonts.google.com/specimen/Inter) con jerarquía y pesos según `desing.md` (weight 500 en display headlines, tight line-height, uppercase tracking en botones).

---

## 🎨 Sistema de Diseño (`desing.md`)

- **Canvas Principal:** `#ffffff` (Pure White)
- **Bandas Alternadas:** `#f7f7f7` (Cloud) y `#e8e8e8` (Fog / Hairline)
- **Color de Acción / Acento:** `#024ad8` (Electric Blue), `#296ef9` (Bright Blue para slabs oscuros), `#0e3191` (Deep Navy)
- **Contraste & Texto:** `#1a1a1a` (Ink), `#3d3d3d` (Charcoal), `#636363` (Graphite)
- **Slabs Oscuros:** `#1a1a1a` para la sección de Seguridad & Calidad y el Footer
- **Formas:** 
  - Botones y campos de entrada: Radio de curvatura nítido de `4px` (`rounded.md`), botones en mayúsculas con tracking de `0.7px`.
  - Tarjetas y contenedores de fotos: `16px` (`rounded.xl`) con sombra suave `Soft Lift` (`0 2px 8px rgba(26,26,26,0.08)`).
  - Chevrons geométricos arquitectónicos en color azul eléctrico en el Hero.

---

## 📂 Estructura del Proyecto

```text
├── assets/                  # Imágenes y logos originales
├── public/
│   └── assets/              # Assets estáticos servidos por Astro
│       ├── Emblema.png
│       ├── darkgrid-logo.png
│       ├── gente-limpiando.jpg
│       ├── personal-limpiando.png
│       └── personal-working.png
├── src/
│   ├── components/
│   │   ├── UtilityStrip.astro       # Barra superior con teléfono, email y lema
│   │   ├── Navbar.astro             # Cabecera sticky con menú responsive
│   │   ├── Hero.astro               # Sección principal con chevrons y propuesta de valor
│   │   ├── AboutSection.astro       # Quiénes somos, Misión y Visión
│   │   ├── ServicesSection.astro    # Los 7 servicios especializados con cards técnicas
│   │   ├── ApproachSection.astro    # "Safety First. Quality Always" (4 pilares)
│   │   ├── IndustriesSection.astro  # Entornos y centros de datos soportados
│   │   ├── WhyChooseUs.astro        # 5 razones para elegir DarkGrid
│   │   ├── SafetyCommitment.astro   # Slab oscuro con compromisos de seguridad
│   │   ├── CareersSection.astro     # Oportunidades laborales y envío de CV
│   │   ├── ContactSection.astro     # Formulario de cotización e información directa
│   │   └── Footer.astro             # Footer corporativo completo
│   ├── layouts/
│   │   └── Layout.astro             # Layout HTML con metadatos y fuentes
│   ├── pages/
│   │   └── index.astro              # Ensamblado de la landing page
│   └── styles/
│       └── global.css               # Import de Tailwind v4 y tokens de diseño
├── astro.config.mjs
├── package.json
└── desing.md
```

---

## 🛠️ Comandos Disponibles

En la raíz del proyecto:

```bash
# Iniciar servidor de desarrollo
npm run dev

# Compilar para producción
npm run build

# Previsualizar el build de producción
npm run preview
```

---

## 📬 Configuración del Formulario ("Request a Quote") con Web3Forms

El formulario ya está 100% conectado mediante AJAX con **Web3Forms** (incluye protección Honeypot anti-spam y estados de carga y confirmación sin recargar la página).

### Pasos para recibir los correos (Tarda 1 minuto):
1. Entra a [https://web3forms.com/](https://web3forms.com/).
2. Ingresa el correo donde deseas recibir los mensajes (ej: `info@darkgridoperations.com` o tu correo personal).
3. Haz clic en **"Create your Access Key"** y recibirás una clave gratuita en tu correo (es una cadena tipo `a1b2c3d4-e5f6-...`).
4. Pega tu clave en el archivo `.env`:
   ```bash
   PUBLIC_WEB3FORMS_KEY=tu_clave_aqui
   ```
5. **Al desplegar en Vercel:**
   - Ve a tu proyecto en Vercel > **Settings** > **Environment Variables**.
   - Añade el nombre `PUBLIC_WEB3FORMS_KEY` con el valor de tu clave. ¡Y listo! Cada cotización llegará al instante a tu correo.


