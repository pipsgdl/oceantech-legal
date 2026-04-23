# Migración a WordPress Elementor (oceantech.com.mx)

Cuando esté lista la versión definitiva en WordPress, seguir estos pasos:

## 1. Crear página en WordPress

- URL: `oceantech.com.mx/privacidad/foro907/`
- Título: "Aviso de Privacidad — App Foro 907"
- Plantilla: Elementor Full Width (sin sidebar)

## 2. Estructura Elementor sugerida

### Sección 1: Hero (fondo gradiente Ocean Tech)

- Fondo: Linear gradient `#0B0F14` → `#0B2040`, con borde inferior de 3px `#00D4FF`
- Padding: 60px 24px
- Contenido:
  - **Heading Pequeño**: `OCEAN · TECHNOLOGY · SOLUTIONS` (estilo uppercase, letter-spacing 2px, color `#00D4FF`)
  - **Heading H1**: `Aviso de Privacidad — App Foro 907`
  - **Text**: "Versión integral conforme a LFPDPPP México"
  - **Info Box** con versión, última actualización, vigencia

### Sección 2: Contenido legal

- Contenedor blanco centrado, max-width 860px, padding 40px, sombra suave
- Usar widget **Table of Contents** de Elementor Pro (o manual con anchor links)
- 10 secciones (widget Heading H2 + Text Editor):
  1. Identidad del responsable
  2. Datos personales que recabamos
  3. Finalidades del tratamiento
  4. Transferencias de datos
  5. Medidas de seguridad
  6. Derechos ARCO
  7. Retención y eliminación
  8. Menores de edad
  9. Cambios al aviso
  10. Contacto y autoridad

- Usar **Widget Tabla** (Elementor Pro) para las transferencias y datos

### Sección 3: Footer

- Texto centrado con copyright y links a hub legal + email contacto

## 3. Importar contenido rápido

Pega el HTML de `privacidad.html` directamente en un widget **HTML Code** de Elementor — los estilos inline funcionan igual. Luego lo rehaces bonito con widgets nativos cuando tengas tiempo.

## 4. SEO (Yoast o RankMath)

- Meta title: "Aviso de Privacidad — App Foro 907 | Ocean Tech"
- Meta description: "Aviso de Privacidad integral de la app Foro 907, conforme LFPDPPP de México. Ocean Technology Solutions."
- Canonical: `https://oceantech.com.mx/privacidad/foro907/`
- Noindex: FALSE (queremos que Google la encuentre)

## 5. Redirect de GitHub Pages

Una vez publicada la página en oceantech.com.mx:

### En WordPress
- Plugin Redirection → Source: `https://pipsgdl.github.io/oceantech-legal/foro907/privacidad.html` → Target: `https://oceantech.com.mx/privacidad/foro907/` (301)

### En GitHub Pages
Agregar meta refresh en `foro907/privacidad.html`:

```html
<meta http-equiv="refresh" content="0; url=https://oceantech.com.mx/privacidad/foro907/">
```

### En App Store Connect vía API

```python
# Actualizar privacyPolicyUrl a la URL definitiva
NEW_URL = "https://oceantech.com.mx/privacidad/foro907/"
# PATCH /v1/appInfoLocalizations/{id} con body:
# {"data":{"type":"appInfoLocalizations","id":"34acd370-7167-4564-87c3-85e29d0134d4",
#   "attributes":{"privacyPolicyUrl":NEW_URL}}}
```

## 6. Diseño visual sugerido

Si quieres que matchee al estilo Ocean Tech actual de oceantech.com.mx:

| Elemento | Color | Uso |
|----------|-------|-----|
| Fondo dark | `#0B0F14` | Header |
| Azul naval | `#0B2040` | Secundario |
| Acento cian | `#00D4FF` | Badges, links, acentos |
| Texto oscuro | `#1A1A1A` | Cuerpo |
| Texto muted | `#5A6472` | Footer, labels |
| Fondo suave | `#F8FAFC` | Body |
| Card blanco | `#FFFFFF` | Contenedor contenido |
| Bordes | `#E5E9F0` | Tablas, separadores |

## 7. Checklist de migración

- [ ] Subir imágenes Ocean Tech (favicon, logo) al Media Library
- [ ] Crear página `/privacidad/foro907/` con Elementor
- [ ] Pegar contenido desde `privacidad.html`
- [ ] Configurar SEO con Yoast/RankMath
- [ ] Agregar redirect 301 desde GitHub Pages
- [ ] Probar la página en mobile + desktop
- [ ] Actualizar `privacyPolicyUrl` en App Store Connect vía API
- [ ] Actualizar URL también en Google Play Console (cuando subas la app Android)
- [ ] Commit del archivo `privacidad.html` en este repo con comentario apuntando a la URL nueva
