# Registro de Cambios - Versión Biblia Libre (Edición Johan Gutierrez)

Este archivo registra todas las modificaciones realizadas a la versión adaptada de la Versión Biblia Libre (VBL), cumpliendo con los requisitos de la licencia Creative Commons Attribution-Share Alike (BY-SA) 4.0 International.

## [1.0.0-alpha.2] - 2026-01-20

### Cambiado
- Refactorización de la estructura del código para mejorar la legibilidad y el mantenimiento.

### Corregido
- Actualización del nombre del archivo JSON en el README de `bible_optimized` a `spavbl-jg`.

## [1.0.0-alpha.1] - 2026-01-19

### Proceso de Transformación Detallado
Esta versión ha sido creada siguiendo este flujo de trabajo para garantizar la integridad y legalidad:
1. **Fuente**: Se obtuvo la versión 5.2 (Octubre 2025) de la VBL desde `ebible.org` en formato `spavbl_html.zip`.
2. **Conversión**: Los archivos HTML fueron parseados para extraer el texto y convertirlo a formato JSON.
3. **Enriquecimiento**: Se procesaron 3,823 notas al pie de página originales, vinculándolas mediante un mapeo de referencias HTML directamente a cada versículo.
4. **Optimización**: Se reestructuró el JSON para ser eficiente en bases de datos NoSQL (Firebase), eliminando la necesidad de consultas pesadas para obtener notas.
5. **Canonización**: Se aplicó el orden bíblico clásico a los libros.

### Añadido
- Nueva estructura de datos optimizada para bases de datos NoSQL (Firebase).
- Vinculación directa de las 3,823 notas al pie de página originales con sus respectivos versículos.
- Metadatos detallados que incluyen colaboradores originales (Gustavo Sanabria, Rebekah Põldaas) y fuentes.
- Información legal clara sobre la naturaleza de la obra derivada bajo la licencia CC BY-SA 4.0.
- Nuevo `README.md` profesional con sistema de versionado sugerido para crecimiento de la edición.

### Modificado
- Transformación del formato de datos original hacia una estructura única optimizada para alto rendimiento en bases de datos NoSQL.
- Estandarización de los metadatos globales (`info`) incluyendo atribución completa y detalles de licencia.

---
*Nota: Esta es una obra derivada basada en la Free Bible Version (VBL) de Jonathan Gallagher y Shelly Barrios de Avila, con la colaboración de Gustavo Sanabria y Rebekah Põldaas.*
