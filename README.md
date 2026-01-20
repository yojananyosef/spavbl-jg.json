# Versión Biblia Libre (Edición Johan Gutierrez)

## Descripción

Este proyecto toma la **Versión Biblia Libre (VBL)** en su versión más reciente (5.2 - Octubre 2025) y la transforma en un formato JSON altamente optimizado para bases de datos NoSQL y aplicaciones modernas.

A diferencia de otras versiones, este proyecto enriquece el texto bíblico vinculando directamente **3,823+ notas explicativas** originales a sus respectivos versículos, permitiendo una experiencia de lectura profunda y técnicamente eficiente.

## Versión

**Versión actual: 1.0.0-rc.3** (Basada en VBL 5.2 de fecha 2025-12-22)

### Sistema de Versionado

Para que esta versión crezca de forma clara, he implementado una estructura basada en Semantic Versioning (SemVer):

- **X.X.X-rc.N**: Versiones candidatas para revisión de contenido (versículos y notas).
- **1.0.1, 1.0.2...**: Para correcciones de ortografía o puntuación.
- **1.1.0...**: Si se añaden nuevas funciones o cambios importantes en las notas.
- **2.0.0...**: Si en el futuro se decide cambiar palabras o el estilo del lenguaje de forma extensiva, alejándote mucho de la original.

## Fuente de Datos

Los datos originales provienen de **eBible.org** bajo el formato `spavbl_html.zip` (Zipped mobile HTML). El proceso de transformación realizado por **Johan Gutierrez** incluye:

1. Parsing de archivos HTML para extracción de texto y referencias.
2. Mapeo dinámico de notas al pie de página (`FN`) a cada versículo.
3. Reordenamiento de libros según el canon bíblico clásico.
4. Estandarización de metadatos de autoría y licencia.

## Estructura del JSON (spavbl-jg.json)

El archivo principal utiliza una estructura plana bajo la clave `libros`, optimizada para consultas directas por código de libro (ej. `GEN`, `EXO`):

```json
{
  "info": {
    "nombre": "Versión Biblia Libre (Edición Adaptada)",
    "editor_adaptacion": "Johan Gutierrez",
    "version_base": "Free Bible Version (VBL) 5.2",
    "licencia": "CC BY-SA 4.0"
  },
  "libros": {
    "GEN": {
      "nombre": "Génesis",
      "testamento": "at",
      "capitulos": {
        "1": {
          "1": {
            "texto": "En el principio, Dios creó los cielos y la tierra.",
            "notas": []
          },
          "5": {
            "texto": "Entonces Dios llamó a la luz “día”...",
            "notas": [
              "Es importante decir que el “día” se mide desde la oscuridad a la luz..."
            ]
          }
        }
      }
    }
  }
}
```

## Contribución

Si deseas contribuir a la optimización técnica o reportar errores en la vinculación de notas, por favor sigue las mejores prácticas para el manejo de textos sagrados y mantén la integridad del mensaje original.

## Licencia

El texto de la Biblia utilizado es la **Free Bible Version (VBL)**, copyright © 2018-2020 Jonathan Gallagher y Shelly Barrios de Avila.

Esta adaptación de formato y estructura realizada por **Johan Gutierrez** se distribuye bajo la misma licencia **Creative Commons Attribution-Share Alike 4.0 (CC BY-SA 4.0)**.

**Condiciones de la licencia:**

1. **Atribución**: Debes incluir la información de copyright original y citar a Johan Gutierrez como editor de esta versión optimizada.
2. **Indicar Cambios**: Debes indicar que esta es una obra derivada y que los cambios realizados (formateo JSON, vinculación de notas) no son necesariamente avalados por los autores originales.
3. **Compartir Igual**: Cualquier obra derivada de este JSON debe distribuirse bajo la misma licencia CC BY-SA 4.0.

Para más detalles, consulta [Creative Commons BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/legalcode).

---

**Nota espiritual**: Revisar y adaptar la Palabra de Dios implica una gran responsabilidad para ser fiel a ella (ver Apocalipsis 22:18-19).

_Proyecto actualizado el 20 de enero de 2026._
