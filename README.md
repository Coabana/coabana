# 🌴 Coabana — GitHub Page

Sitio web de **Coabana**, estudio de ingeniería de datos especializado en **Google Cloud**: qué es la marca, qué servicios ofrece y cómo contactar.

Construido con HTML, CSS y JavaScript puros — sin frameworks ni paso de build. GitHub Pages lo sirve tal cual.

## Estructura

```
├── index.html          # Toda la página (una sola página con secciones)
├── 404.html            # Página de error
├── css/style.css       # Estilos (tema caribeño-tech oscuro)
├── js/i18n.js          # ✏️ TEXTOS del sitio en español e inglés
├── js/main.js          # Idioma, menú, animaciones y formulario
└── assets/             # Logo y favicon (SVG)
```

## Cómo editar los textos

Todos los textos viven en **`js/i18n.js`**, en dos diccionarios (`es` y `en`) con las mismas claves. Edita el valor de la clave en ambos idiomas y listo. El HTML tiene el texto en español como contenido por defecto (por si JavaScript no carga); si cambias algo grande, actualízalo también en `index.html` para mantenerlos alineados.

El idioma se detecta automáticamente (navegador → `es`/`en`), se puede forzar con `?lang=en` o `?lang=es` en la URL, y el visitante puede cambiarlo con el botón **EN/ES** del menú.

## ⚠️ Pendientes de configurar

1. **LinkedIn** — En `index.html` hay dos enlaces marcados con `<!-- TODO -->` que apuntan a `https://www.linkedin.com/`. Reemplázalos con la URL exacta de tu perfil.
2. **Formulario de contacto** — Crea una cuenta gratuita en [Formspree](https://formspree.io), crea un formulario y copia el endpoint en la constante `FORM_ENDPOINT` de `js/main.js`. Mientras esté vacío, el formulario abre la app de correo del visitante con el mensaje ya redactado (funciona, pero es menos cómodo).
3. **GitHub personal** — El enlace del fundador apunta a `https://github.com/roanny`; verifica que sea tu usuario.

## Publicar en GitHub Pages

1. Haz merge de este contenido a la rama `main`.
2. En GitHub: **Settings → Pages → Build and deployment**.
3. En *Source* elige **Deploy from a branch**, rama `main`, carpeta `/ (root)` y guarda.
4. En unos minutos el sitio estará en **`https://coabana.github.io/coabana/`**.

> 💡 **URL más corta**: si renombras este repositorio a `Coabana.github.io`, el sitio se publica en la raíz: `https://coabana.github.io/`. Todos los enlaces internos son relativos, así que funciona sin cambios (solo actualiza las URLs de `og:url` y el JSON-LD en `index.html`).

## Probar en local

```bash
python3 -m http.server 8000
# abre http://localhost:8000
```
