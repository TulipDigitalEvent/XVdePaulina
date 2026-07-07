# 🌟 XV Años · Paulina Padilla García
### Invitación Digital Premium — Inspirada en Rapunzel / Tangled

---

## 📁 Estructura del proyecto

```
paulina-xv/
├── index.html
├── styles.css
├── script.js
├── README.md
└── images/
    ├── imagen-01-portada.jpg          ← Portada principal
    ├── imagen-02-calendario.jpg       ← Fondo sección Calendario
    ├── imagen-03-cuenta-regresiva.jpg ← Fondo cuenta regresiva
    ├── imagen-04-mi-historia.jpg      ← (referencia, galería usa imágenes propias)
    ├── imagen-05-familia.jpg          ← Sección Familia
    ├── imagen-06-padrinos.jpg         ← Sección Padrinos (fondo sutil)
    ├── imagen-07-ceremonia.jpg        ← Sección Ceremonia
    ├── imagen-08-recepcion.jpg        ← Sección Recepción
    ├── imagen-09-dress-code.jpg       ← Sección Dress Code (fondo sutil)
    ├── imagen-10-confirmacion.jpg     ← Sección Confirmación
    ├── imagen-11-recuerdos.jpg        ← Sección Recuerdos (fondo sutil)
    ├── imagen-12-mensajes.jpg         ← Sección Mensajes
    ├── imagen-13-despedida.jpg        ← Sección Despedida
    ├── imagen-portada-cancion.jpg     ← Portada de la canción (tarjeta música)
    ├── imagen-galeria-01.jpg          ← Galería foto 1
    ├── imagen-galeria-02.jpg          ← Galería foto 2
    ├── imagen-galeria-03.jpg          ← Galería foto 3
    ├── imagen-galeria-04.jpg          ← Galería foto 4
    ├── imagen-galeria-05.jpg          ← Galería foto 5
    ├── imagen-galeria-06.jpg          ← Galería foto 6
    ├── imagen-galeria-07.jpg          ← Galería foto 7
    ├── imagen-galeria-08.jpg          ← Galería foto 8
    ├── imagen-galeria-09.jpg          ← Galería foto 9
    └── imagen-galeria-10.jpg          ← Galería foto 10
```

---

## 🖼️ Cómo cambiar las fotografías

1. Crea la carpeta `images/` en la misma ubicación que `index.html`.
2. Nombra tus fotos **exactamente** como aparecen arriba (incluyendo la extensión `.jpg`).
3. Si tus fotos están en `.png` o `.webp`, cambia la extensión en el atributo correspondiente dentro de `index.html`.

**Consejo:** Para mejor rendimiento, usa imágenes en formato `.jpg` con un ancho máximo de **1920px** y calidad entre 75–85%. Herramientas gratuitas: [Squoosh.app](https://squoosh.app) o [TinyJPG](https://tinyjpg.com).

---

## 🎵 Cómo cambiar la canción

El video se reproduce **embebido directamente en la página** (no abre YouTube en otra pestaña). Abre `script.js` y localiza el objeto `CONFIG` al inicio del archivo:

```javascript
const CONFIG = {
  YOUTUBE_VIDEO_ID: 'h9SAUq5-V7o',
  ...
};
```

Para cambiar la canción:
1. Busca el video en YouTube y copia su ID — es la parte después de `v=` en la URL.
   Ejemplo: en `https://www.youtube.com/watch?v=h9SAUq5-V7o` el ID es `h9SAUq5-V7o`.
2. Reemplaza el valor de `YOUTUBE_VIDEO_ID` con ese ID.
3. La miniatura del video se obtiene automáticamente de YouTube, no necesitas subir una imagen de portada.

> **Nota:** algunos videos tienen la reproducción embebida deshabilitada por su dueño. Si al tocar play no carga, prueba con otro video de la misma canción (busca "lyric video" o "audio oficial", que normalmente sí permiten embeberse).

Para cambiar el nombre de la canción y el artista en la tarjeta, edita en `index.html`:

```html
<p class="music-track">I See The Light</p>
<p class="music-artist">Mandy Moore &amp; Zachary Levi</p>
```

---

## 📱 Cómo cambiar el número de WhatsApp

En `script.js`, dentro del objeto `CONFIG`:

```javascript
WHATSAPP_URL: 'https://wa.me/526648053160?text=Hola...',
```

Reemplaza `526648053160` con el número en formato internacional:
- **México:** `52` + número sin el cero inicial (10 dígitos)
- Ejemplo: número `664 123 4567` → `526641234567`

El texto del mensaje también puede personalizarse (la parte después de `?text=`).

---

## 📍 Cómo cambiar los enlaces de Google Maps

### Ceremonia
En `script.js`, dentro de `CONFIG`:
```javascript
CEREMONIA_MAPS_URL: 'https://maps.google.com/?q=Parroquia...',
```
Ve a [Google Maps](https://maps.google.com), busca el lugar, haz clic en "Compartir" y copia el enlace corto.

### Recepción — Jardín Secreto
La URL de recepción está configurada directamente en `index.html` (sección `#recepcion`) ya que fue proporcionada como URL fija:
```html
href="https://maps.app.goo.gl/3YdFWLRQhAQmbXDv8?g_st=ic"
```
Cámbiala si la dirección del lugar varía.

---

## 📋 Cómo cambiar los formularios de Google

1. Crea tus formularios en [Google Forms](https://forms.google.com)
2. Publica cada formulario y copia el enlace de respuesta
3. En `script.js`, dentro de `CONFIG`:

```javascript
GOOGLE_FORM_RECUERDOS_URL: 'https://forms.gle/TU_ENLACE_FOTOS',
GOOGLE_FORM_MENSAJES_URL:  'https://forms.gle/TU_ENLACE_MENSAJES',
```

---

## 🚀 Cómo publicar en GitHub Pages

### Paso 1: Crear repositorio
1. Ve a [github.com](https://github.com) y crea una cuenta o inicia sesión.
2. Crea un nuevo repositorio (puede ser privado, pero Pages necesita uno público en el plan gratuito).
3. Nómbralo, por ejemplo: `paulina-xv-anos`

### Paso 2: Subir los archivos
Puedes hacerlo de dos formas:

**Opción A — Arrastrando archivos (más fácil):**
1. Entra a tu repositorio en GitHub.
2. Haz clic en "Add file" → "Upload files".
3. Arrastra **todos** los archivos (`index.html`, `styles.css`, `script.js`, `README.md`) y la carpeta `images/`.
4. Haz clic en "Commit changes".

**Opción B — Con Git (si ya lo tienes instalado):**
```bash
git init
git add .
git commit -m "XV Años Paulina - Invitación Digital"
git remote add origin https://github.com/TU_USUARIO/paulina-xv-anos.git
git push -u origin main
```

### Paso 3: Activar GitHub Pages
1. En tu repositorio, ve a **Settings** → **Pages** (en el menú lateral izquierdo).
2. En "Source", selecciona **"Deploy from a branch"**.
3. En "Branch", selecciona **`main`** y la carpeta **`/ (root)`**.
4. Haz clic en **Save**.
5. Espera 1–2 minutos y tu sitio estará disponible en:
   ```
   https://TU_USUARIO.github.io/paulina-xv-anos/
   ```

### Paso 4: Compartir el enlace 🎉
¡Listo! Copia ese enlace y compártelo por WhatsApp, Instagram o cualquier red social.

---

## 🎨 Personalización adicional

### Cambiar colores
En `styles.css`, busca la sección `/* ─── TOKENS ───*/` al inicio del archivo:
```css
:root {
  --lavanda:  #C8A2D8;  /* Color principal */
  --gold:     #D4AF37;  /* Dorado */
  --ivory:    #FAF7F2;  /* Marfil */
  ...
}
```

### Cambiar tipografía
Los fonts están importados desde Google Fonts al inicio de `index.html`. Para cambiar la fuente script (firma), busca `Great Vibes` en el link de Google Fonts.

### Cambiar datos del evento
Busca y reemplaza en `index.html` las fechas, horas y nombres directamente en el HTML.
Para la fecha del countdown, edita en `script.js`:
```javascript
EVENT_DATE: new Date('2026-08-07T16:00:00'),
```

---

## ✅ Checklist antes de publicar

- [ ] Todas las fotos están en la carpeta `images/` con los nombres correctos
- [ ] `YOUTUBE_VIDEO_ID` apunta al video correcto y permite reproducción embebida
- [ ] `WHATSAPP_URL` tiene el número correcto
- [ ] `CEREMONIA_MAPS_URL` tiene el enlace correcto de Google Maps
- [ ] `GOOGLE_FORM_RECUERDOS_URL` y `GOOGLE_FORM_MENSAJES_URL` están actualizados
- [ ] La fecha en `EVENT_DATE` es correcta
- [ ] El sitio se ve bien en móvil (prueba en Chrome DevTools → modo responsive)

---

## 💜 Notas técnicas

- **Compatible con:** Chrome, Safari, Firefox, Edge (versiones modernas)
- **Mobile First:** Optimizado para iPhone y Android
- **Sin dependencias:** Solo HTML5, CSS3 y JavaScript Vanilla
- **GitHub Pages:** Funciona sin configuración adicional de servidor
- **Accesibilidad:** Roles ARIA, navegación por teclado, reduced-motion

---

*Diseñado con amor para los XV Años de Paulina Padilla García · 07 de Agosto de 2026*
