================================================================================
GUÍA PARA GESTIONAR LA GALERÍA DE TRABAJOS (CARRUSEL)
Express Pressure Clean | Professional Cleaning
================================================================================

Este documento explica cómo funciona el carrusel de la sección "Nuestros Trabajos"
y cómo puedes agregar, quitar o editar imágenes fácilmente sin necesidad de tocar
el código HTML ni CSS de la página web.

--------------------------------------------------------------------------------
1. CÓMO FUNCIONA EL SISTEMA
--------------------------------------------------------------------------------
- El carrusel lee automáticamente la información desde el archivo:
  "trabajos.json" ubicado en la carpeta principal del proyecto.
- Todas las imágenes se muestran con un tamaño 100% UNIFORME (proporción 4:3)
  y ajuste automático inteligente ("object-fit: cover"), evitando que las fotos
  se deformen o tengan diferentes alturas.
- Los botones de navegación (< y >), los puntos inferiores (dots) y el avance
  automático (autoplay) se recalculan solos según la cantidad de imágenes que tengas.
- Soporta de forma nativa el cambio de idioma (Español / Inglés).

--------------------------------------------------------------------------------
2. PASOS PARA AGREGAR UN TRABAJO NUEVO
--------------------------------------------------------------------------------

PASO 1: GUARDA LA FOTO
Coloca tu imagen en la carpeta principal del sitio web (junto a index.html).
Ejemplo de nombre: "terraza-lavado.webp" (o .jpg / .png).

PASO 2: EDITA EL ARCHIVO "trabajos.json"
Abre el archivo "trabajos.json" con cualquier editor de texto (como Notepad o VS Code).
Agrega un nuevo bloque con los datos del trabajo antes del corchete final de cierre "]".

--------------------------------------------------------------------------------
3. EJEMPLO PRÁCTICO PARA COPIAR Y PEGAR EN "trabajos.json"
--------------------------------------------------------------------------------
Asegúrate de colocar una coma (,) al final del elemento anterior antes de pegar el nuevo:

  {
    "id": 5,
    "imagen": "terraza-lavado.webp",
    "alt": "Lavado de Terraza y Adoquines",
    "categoria": {
      "es": "Terrazas",
      "en": "Patios"
    },
    "titulo": {
      "es": "Limpieza Profunda de Terraza",
      "en": "Deep Patio Cleaning"
    },
    "subtitulo": {
      "es": "Eliminación de manchas y moho en adoquines",
      "en": "Stain and mold removal on pavers"
    }
  }

--------------------------------------------------------------------------------
4. SIGNIFICADO DE CADA CAMPO
--------------------------------------------------------------------------------
- "id": Número identificador (1, 2, 3, etc.).
- "imagen": Nombre exacto del archivo de la foto (ej: "mi-foto.webp").
- "alt": Descripción de accesibilidad para Google y personas con discapacidad visual.
- "categoria":
    - "es": Etiqueta superior en español (ej: "Fachadas", "Techos", "Concreto", etc.).
    - "en": Etiqueta superior en inglés (ej: "Facades", "Roofs", "Concrete", etc.).
- "titulo":
    - "es": Título principal del trabajo en español.
    - "en": Título principal del trabajo en inglés.
- "subtitulo":
    - "es": Breve descripción del acabado en español.
    - "en": Breve descripción del acabado en inglés.

--------------------------------------------------------------------------------
5. CÓMO ELIMINAR O REORDENAR FOTOS
--------------------------------------------------------------------------------
- Para ELIMINAR una foto: simplemente borra el bloque completo {...} de ese trabajo
  en "trabajos.json" (ten cuidado de mantener las comas bien puestas entre elementos).
- Para CAMBIAR EL ORDEN: corta y pega los bloques en el orden en que quieras que
  aparezcan en el carrusel (el primer bloque será la primera foto).

--------------------------------------------------------------------------------
6. CONSEJOS Y RECOMENDACIONES DE IMÁGENES
--------------------------------------------------------------------------------
- Formato recomendado: .webp (ofrece la mejor calidad con el menor peso de archivo).
  También puedes usar .jpg o .png.
- Orientación recomendada: Horizontal (apaisada). Al estar configurado en 4:3,
  las fotos horizontales lucen de manera impecable.
- Peso recomendado: Menos de 500 KB por foto para que la página cargue al instante.
- Respaldo de seguridad: Si en algún momento hubiera un problema de conexión con
  el archivo .json, la página web tiene un respaldo interno automático para que
  la galería nunca se muestre en blanco.
================================================================================
