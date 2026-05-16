# CGREN - Sitio Web Oficial

## Consejo de Generales de la Reserva del Ejército Nacional de Colombia

**"Honor, Compromiso y Dignidad"**

---

## 📁 Estructura del Sitio

```
CGREN_Website/
├── index.html          # Página principal
├── noticias.html       # Sección de noticias (repositorio actualizable)
├── cepoe.html          # CEPOE - Centro de Pensamiento y Observatorio Estratégico
├── styles.css          # Estilos compartidos
├── scripts.js          # JavaScript compartido
├── logo.png            # Logo/Escudo del CGREN (favicon)
├── hero-bg.png         # Imagen de fondo del hero
└── README.md           # Este archivo
```

---

## 🚀 Cómo Usar

1. **Abrir localmente**: Simplemente abre `index.html` en cualquier navegador web moderno.

2. **Publicar en web**: Sube todos los archivos a un servidor web o servicio de hosting.

---

## 📰 Actualización de Noticias

La sección `noticias.html` está diseñada como un **repositorio actualizable**. Para agregar nuevas noticias:

1. Abre `noticias.html`
2. Copia el bloque de una noticia existente dentro de `<div class="news-grid">`
3. Modifica el contenido:
   - `data-category`: Categoría (comunicados, prensa, eventos, cepoe)
   - `data-year`: Año de publicación
   - Título, fecha, resumen y enlace

```html
<article class="news-card" data-category="comunicados" data-year="2025">
    <!-- Contenido de la noticia -->
</article>
```

---

## 📚 Actualización del CEPOE

La sección `cepoe.html` es un **repositorio de documentos**. Para agregar nuevos documentos:

1. Abre `cepoe.html`
2. Copia el bloque de un documento existente dentro de `<div class="documents-grid">`
3. Modifica:
   - `data-type`: Tipo (DI, DAE, DO)
   - `data-line`: Línea de investigación (juridica, seguridad, historia)
   - Título, descripción y enlace al PDF

```html
<article class="document-card" data-type="DI" data-line="seguridad">
    <!-- Contenido del documento -->
</article>
```

### Tipos de Documentos:
- **DI** - Documentos de Investigación
- **DAE** - Documentos de Análisis Estratégico
- **DO** - Documentos de Opinión

---

## 🌐 Publicación con GitHub + Netlify (Recomendado)

Para un sistema de actualización fácil sin tocar código:

### Paso 1: Crear repositorio en GitHub
1. Crea una cuenta en [github.com](https://github.com)
2. Crea un nuevo repositorio llamado `cgren-website`
3. Sube todos los archivos del sitio

### Paso 2: Conectar con Netlify
1. Crea una cuenta en [netlify.com](https://netlify.com)
2. Click en "Add new site" → "Import an existing project"
3. Conecta tu repositorio de GitHub
4. Configura:
   - Build command: (dejar vacío)
   - Publish directory: `/`
5. Click en "Deploy site"

### Paso 3: Configurar dominio
- El sitio estará disponible en `tu-sitio.netlify.app`
- Puedes configurar un dominio personalizado en Site settings → Domain management

---

## 📝 Gestión de Contenido con Decap CMS (Opcional)

Para permitir que personas sin conocimientos técnicos actualicen el contenido:

### Instalación:
1. Crea una carpeta `admin` en el sitio
2. Agrega `index.html` y `config.yml` según la documentación de [Decap CMS](https://decapcms.org/)
3. Configura los colecciones para noticias y documentos

### Archivo `admin/config.yml` ejemplo:
```yaml
backend:
  name: git-gateway
  branch: main

collections:
  - name: "noticias"
    label: "Noticias"
    folder: "content/noticias"
    create: true
    fields:
      - {label: "Título", name: "title", widget: "string"}
      - {label: "Fecha", name: "date", widget: "datetime"}
      - {label: "Categoría", name: "category", widget: "select", options: ["comunicados", "prensa", "eventos", "cepoe"]}
      - {label: "Resumen", name: "excerpt", widget: "text"}
      - {label: "Contenido", name: "body", widget: "markdown"}
```

---

## 📱 Características del Sitio

- ✅ **Diseño Responsive**: Se adapta a móviles, tablets y desktop
- ✅ **Navegación Suave**: Scroll animado entre secciones
- ✅ **Favicon**: Logo como icono del sitio
- ✅ **SEO Optimizado**: Meta tags y descripciones
- ✅ **Formulario de Contacto**: Con validación
- ✅ **Filtros**: En noticias y documentos
- ✅ **Animaciones**: Efectos sutiles al hacer scroll

---

## 🎨 Colores del Sitio

| Color | Hex | Uso |
|-------|-----|-----|
| Azul Primario | `#0A2342` | Headers, títulos |
| Burgundy | `#6B1C2A` | Acentos, footer |
| Dorado | `#D4AF37` | Botones, destacados |
| Blanco | `#FFFFFF` | Fondos |

---

## 📞 Contacto

- **Email**: cgrenejc@gmail.com
- **Teléfono**: 301 829 9297

### Redes Sociales:
- [Instagram](https://www.instagram.com/cgren_)
- [X (Twitter)](https://x.com/CgrenEjc)
- [Facebook](https://www.facebook.com/profile.php?id=61583975720467)
- [YouTube](https://youtube.com/@cgrenejc)

---

## 👨‍💻 Desarrollo

Diseño y desarrollo por **Seed EM**

---

© 2025 CGREN - Consejo de Generales en Retiro del Ejército Nacional de Colombia. Todos los derechos reservados.
