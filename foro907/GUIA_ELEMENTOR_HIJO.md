# 📘 Guía paso a paso — Subir el Aviso de Privacidad del Foro 907 a oceantech.com.mx

> Para: el hijo de Felipe
> Dificultad: fácil (no requiere programar)
> Tiempo estimado: 20-30 minutos

## Qué vas a hacer

Copiar el texto de un Aviso de Privacidad que ya está publicado en esta URL temporal:

👉 **https://pipsgdl.github.io/oceantech-legal/foro907/privacidad.html**

Y crearlo como página oficial en **oceantech.com.mx/privacidad/foro907**

---

## 🔑 Paso 0 — Lo que necesitas antes de empezar

- [ ] Credenciales de admin de WordPress de `oceantech.com.mx` (pídeselas a tu papá)
- [ ] Chrome o Safari abierto
- [ ] Esta guía (compártela contigo en WhatsApp)

---

## 🚪 Paso 1 — Entrar a WordPress

1. Abre el navegador y ve a: **`https://oceantech.com.mx/wp-admin`**
2. Inicia sesión con las credenciales que te pasó tu papá
3. Vas a ver el **Dashboard** (panel negro a la izquierda)

---

## 📄 Paso 2 — Crear la página nueva

1. En el menú izquierdo, pasa el mouse sobre **"Páginas"** (icono de documento)
2. Click en **"Añadir nueva"** (o "Add New")
3. Si aparece un popup de Gutenberg o Elementor, escoge **"Editar con Elementor"** (botón azul)

Vas a ver el editor en blanco con widgets a la izquierda y canvas a la derecha.

---

## ✍️ Paso 3 — Configurar el título y la URL

En la parte de arriba del editor de Elementor:

1. En el campo grande donde dice "Añadir título" escribe:
   ```
   Aviso de Privacidad — App Foro 907
   ```

2. Debajo del título, verás `Permalink:` con la URL que WordPress generó. Click en **"Editar"** y cámbialo a:
   ```
   privacidad/foro907
   ```
   Debe quedar: `oceantech.com.mx/privacidad/foro907/`

---

## 🎨 Paso 4 — Opción rápida: pegar el HTML completo

La forma **más fácil** es usar un widget HTML y pegar el código ya armado.

1. En el buscador de widgets (izquierda), escribe **"HTML"**
2. Arrastra el widget **"HTML"** al canvas (zona blanca grande)
3. Te aparece un cuadro de código vacío

### Obtener el código HTML

1. Abre una pestaña nueva y ve a:
   **https://raw.githubusercontent.com/pipsgdl/oceantech-legal/main/foro907/privacidad.html**

2. Selecciona **todo** el código (Cmd+A o Ctrl+A)
3. Copia (Cmd+C o Ctrl+C)
4. Regresa a WordPress → pégalo en el widget HTML de Elementor (Cmd+V)

> [!warning] Solo pega el contenido DENTRO de `<body>...</body>`, no toda la página
> Si pegas todo con `<html>` y `<head>` puede romperse. Ve al paso 4.1 abajo.

### 4.1 Versión limpia (recomendado)

1. Del código que copiaste, **solo quédate con el contenido entre `<header>...` y `</footer>`** — NO los `<!DOCTYPE>`, `<html>`, `<head>`, `<style>` ni `<body>` tags.
2. Los estilos (el bloque `<style>...</style>` que está en `<head>`) pégalos aparte. Te explico cómo en el Paso 5.

### ALTERNATIVA MÁS FÁCIL: Iframe (si HTML te da problemas)

En lugar de pegar HTML, arrastra un widget **"iFrame"** y pega esta URL:

```
https://pipsgdl.github.io/oceantech-legal/foro907/privacidad.html
```

Ancho: 100%, Alto: 2500px. Queda la página embebida. No es lo ideal para SEO pero funciona.

---

## 🎨 Paso 5 — Agregar los estilos (CSS)

Los estilos hacen que se vea bonita la página. Hay 2 formas:

### Opción A — Custom CSS de la página (fácil)

1. En Elementor, click en el ícono de engranaje abajo a la izquierda (Settings)
2. Busca la pestaña **"Custom CSS"** (requiere Elementor Pro)
3. Pega el contenido del `<style>...</style>` que viste en el HTML (sin los tags `<style>`)

### Opción B — Usar los widgets nativos de Elementor (más bonito)

En vez de pegar HTML crudo, crea la estructura con widgets de Elementor. Tarda más pero queda mejor y se ve profesional. Sigue este template:

#### 📐 Estructura sugerida

**Sección 1 — Hero (arriba, fondo oscuro)**
- Widget **"Sección"** con color de fondo `#0B0F14` y borde inferior 3px `#00D4FF`
- Dentro:
  - Widget **"Título"** H6 → "OCEAN · TECHNOLOGY · SOLUTIONS" (color `#00D4FF`, uppercase, letter-spacing 2px)
  - Widget **"Título"** H1 → "Aviso de Privacidad — App Foro 907" (color blanco)
  - Widget **"Texto Editor"** → "Versión integral conforme a LFPDPPP México."
  - Widget **"Info Box"** o **"Icon List"** con: Versión 1.0, Última actualización 23 abr 2026

**Sección 2 — Contenido legal (fondo blanco)**
- Widget **"Sección"** con color de fondo `#F8FAFC`, max-width 860px centrado
- Para cada uno de los 10 puntos legales:
  - Widget **"Título"** H2 → Nombre del punto (ej: "1. Identidad del responsable")
  - Widget **"Texto Editor"** → Pega el texto del párrafo correspondiente
  - Si hay tablas: Widget **"Tabla"** (Elementor Pro) o **"Icon List"**

**Sección 3 — Footer**
- Widget **"Texto Editor"** centrado con: "© 2026 Ocean Technology Solutions" + links a email y sitio

#### 📋 Los 10 puntos legales que necesitas copiar

Abre la URL de GitHub en otra pestaña y ve copiando texto por sección:
👉 https://pipsgdl.github.io/oceantech-legal/foro907/privacidad.html

1. **Identidad del responsable** — Ocean Tech, Foro 907 como venue partner
2. **Datos personales que recabamos** — Tabla de 5 categorías + lista de "NO recabamos"
3. **Finalidades del tratamiento** — Primarias (6 items) + Secundarias (3 items)
4. **Transferencias de datos** — Tabla con Stripe, Apple/Google, Foro 907
5. **Medidas de seguridad** — TLS 1.3, AES-256, bcrypt, RLS, respaldos, MFA
6. **Derechos ARCO** — Tabla (Acceso, Rectificación, Cancelación, Oposición) + procedimiento
7. **Retención y eliminación** — 4 puntos (cuenta activa, cancelación, fiscal, logs)
8. **Menores de edad** — 17+ por venta alcohol
9. **Cambios al aviso** — Se avisan por push
10. **Contacto y autoridad** — privacidad@oceantech.com.mx + INAI

---

## 🎨 Paso 6 — Paleta de colores (pégala en el Color Picker de Elementor)

| Dónde | Color HEX |
|-------|-----------|
| Fondo oscuro (Hero) | `#0B0F14` |
| Azul naval secundario | `#0B2040` |
| Acento cian (links, badges) | `#00D4FF` |
| Texto oscuro | `#1A1A1A` |
| Texto gris (muted) | `#5A6472` |
| Fondo suave | `#F8FAFC` |
| Blanco card | `#FFFFFF` |
| Bordes sutiles | `#E5E9F0` |

En Elementor:
- Site Settings → Global Colors → agrega estos 8 colores con nombre "OT + color"

---

## 🔍 Paso 7 — SEO (importante para que Google la encuentre)

Si tu papá tiene **Yoast SEO** o **RankMath** instalado:

1. Scroll abajo del editor Elementor → pestaña SEO
2. **Meta título**: `Aviso de Privacidad — App Foro 907 | Ocean Tech`
3. **Meta descripción**: `Aviso de Privacidad integral de la app Foro 907, conforme LFPDPPP de México. Ocean Technology Solutions.`
4. **URL canónica**: `https://oceantech.com.mx/privacidad/foro907/`
5. **Noindex**: **NO** (queremos que Google la indexe)

---

## 🚀 Paso 8 — Publicar la página

1. Arriba a la derecha en Elementor, click **"Publicar"** (botón verde)
2. Espera 2-3 segundos
3. Verás "Publicado" con un link para ver la página
4. Abre el link en otra pestaña y verifica que se ve bien

**La URL final debe ser:** `https://oceantech.com.mx/privacidad/foro907/`

---

## 📱 Paso 9 — Prueba en celular

1. Copia la URL
2. Mándatela a WhatsApp y ábrela en tu iPhone o Android
3. Verifica:
   - [ ] Los textos se leen bien
   - [ ] Las tablas no se salen de la pantalla
   - [ ] Los botones/links funcionan
   - [ ] Se carga rápido (menos de 3 segundos)

Si algo se ve raro en móvil, en Elementor hay un switch abajo izquierda para previsualizar en móvil/tablet y ajustar.

---

## ✅ Paso 10 — Avísale a papá cuando esté listo

Dile: **"Ya está en oceantech.com.mx/privacidad/foro907"**.

Él se encarga del último paso técnico: actualizar la URL en App Store Connect (le toma 10 segundos con un script).

---

## ❓ Si algo no funciona

1. **No sale Elementor al crear la página** → Busca arriba el botón "Editar con Elementor" (azul)
2. **El widget HTML no renderiza** → Revisa que no tenga tags `<html>` o `<body>` sobrantes
3. **Los colores no se ven** → Los estilos están en el `<style>` del HTML. Si usas widgets nativos, aplica los colores de la tabla del Paso 6
4. **Error 404 al entrar a la URL** → En WordPress, ve a Settings → Permalinks → click "Save" (sin cambiar nada, solo refresca el rewrite)
5. **El submenu /privacidad/ no existe** → Crea primero una página padre llamada "privacidad" (vacía), y luego haz esta página hija de ella

---

## 🎨 Bonus: qué agregar después (cuando tengas tiempo)

- **Breadcrumbs** (Inicio > Privacidad > App Foro 907)
- **Botón flotante** para bajar al contacto INAI
- **Versión en inglés** (duplicate la página, cambia URL a `/privacy/foro907` y traduce)
- **Tabla de contenidos flotante** lateral (widget "Table of Contents" de Elementor Pro)

---

## 🙌 Cheat sheet final

| Cosa | Valor |
|------|-------|
| Admin URL | `oceantech.com.mx/wp-admin` |
| URL final de la página | `oceantech.com.mx/privacidad/foro907` |
| HTML fuente a copiar | https://raw.githubusercontent.com/pipsgdl/oceantech-legal/main/foro907/privacidad.html |
| Vista previa de referencia | https://pipsgdl.github.io/oceantech-legal/foro907/privacidad.html |
| Color acento | `#00D4FF` |
| Email de contacto | privacidad@oceantech.com.mx |

¡Suerte! Cuando termines dile a tu papá 🚀
