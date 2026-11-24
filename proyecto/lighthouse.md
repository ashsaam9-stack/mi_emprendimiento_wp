# Auditoría de Rendimiento y Calidad — Lighthouse

Evaluación técnica realizada sobre el sitio en producción (`https://studioash.infinityfree.me`) utilizando **Google PageSpeed Insights / Lighthouse** (versión 13.0.0) el 24 de noviembre de 2026. https://pagespeed.web.dev/analysis/https-studioash-infinityfree-me/hbgg9sodcpsxu62vpqboq7?form_factor=desktop

---

## 1. Resultados Obtenidos

La rúbrica solicita el análisis principal en **dispositivo móvil**, y adicionalmente se adjuntan los resultados obtenidos en **ordenador** como respaldo:

| Categoría | Puntaje Móvil | Puntaje Ordenador | Estado |
| :--- | :---: | :---: | :--- |
| **Rendimiento (Performance)** | **84 / 100** | **97 / 100** | Bueno / Óptimo |
| **Accesibilidad (Accessibility)** | **100 / 100** | **100 / 100** | Óptimo |
| **Buenas Prácticas (Best Practices)** | **100 / 100** | **100 / 100** | Óptimo |
| **SEO** | **100 / 100** | **100 / 100** | Óptimo |

### Métricas Clave de Rendimiento (Móvil vs. Ordenador)
* **First Contentful Paint (FCP):** `1,6 s` en móvil / `0,7 s` en ordenador.
* **Largest Contentful Paint (LCP):** `4,3 s` en móvil / `1,1 s` en ordenador.
* **Total Blocking Time (TBT):** `0 ms` en ambos dispositivos (cero bloqueo de interactividad).
* **Cumulative Layout Shift (CLS):** `0.01` en móvil / `0` en ordenador (estabilidad visual sobresaliente).
* **Speed Index:** `3,3 s` en móvil / `1,2 s` en ordenador.

### Enlace y Capturas del Informe
* **URL analizada:** https://studioash.infinityfree.me
* *(Sube tus capturas de pantalla de PageSpeed Insights a la carpeta `proyecto/` y enlázalas aquí)*:
  ![Reporte Lighthouse Móvil](lighthouse-movil.png)
  ![Reporte Lighthouse Ordenador](lighthouse-ordenador.png)

---

## 2. Análisis de Resultados

* **Rendimiento (84 en Móvil / 97 en Ordenador):** El sitio presenta una velocidad muy alta en escritorio y un buen desempeño en dispositivos móviles considerando que está alojado en un servidor gratuito (InfinityFree) con limitación de red 4G simulada. El único indicador en alerta moderada en móvil es el **Largest Contentful Paint (4,3 s)**, influenciado por el peso de las imágenes principales (`1.545 KiB` de ahorro estimado) y el bloqueo inicial de renderizado por hojas de estilo y fuentes (`450 ms` y `1.010 ms` estimados). Por otro lado, el **Total Blocking Time de 0 ms** demuestra que el sitio no tiene scripts pesados que congelen la pantalla.
* **Accesibilidad (100 / 100):** El tema *Twenty Twenty-Five* cumple con todos los estándares automáticos de jerarquía de encabezados, etiquetas ARIA, contraste de colores y navegación legibles. (Como recomendación manual, el informe sugiere revisar que los enlaces con textos idénticos tengan la misma finalidad).
* **Buenas Prácticas (100 / 100):** El sitio carga íntegramente bajo protocolo seguro HTTPS sin errores de consola ni dependencias obsoletas.
* **SEO (100 / 100):** La estructura de metadatos gestionada junto a **Rank Math SEO**, la configuración móvil (*viewport*) y los datos estructurados son totalmente válidos para su indexación en buscadores.

---

## 3. Mejoras Aplicadas y Propuestas

1. **Optimización de caché y entrega estática con W3 Total Cache (Aplicada):**
   * **Problema detectado:** Latencia en la respuesta inicial del servidor gratuito y recarga repetitiva de recursos del tema y plugins.
   * **Solución:** Se instaló y configuró el plugin **W3 Total Cache**, logrando mantener un *Total Blocking Time* de `0 ms` y alcanzando un puntaje de **84/100 en móvil** y **97/100 en escritorio**.

2. **Optimización y compresión de imágenes a formato WebP (Propuesta):**
   * **Problema detectado:** El diagnóstico de Lighthouse indica en la sección *"Mejorar la entrega de imágenes"* un ahorro estimado de **1.545 KiB**, lo que retrasa el *Largest Contentful Paint (4,3 s)* en redes móviles.
   * **Solución:** Convertir las fotografías del estudio y galería de trabajos a formato **WebP**, redimensionarlas al tamaño máximo de visualización en pantalla y asegurar la carga diferida (*Lazy Loading*) en imágenes fuera del primer pantallazo.

3. **Optimización de carga de fuentes y CSS que bloquean el renderizado (Propuesta):**
   * **Problema detectado:** El reporte señala *"Solicitudes que bloquean el renderizado"* (ahorro estimado de `450 ms`) y *"Visualización de fuentes"* (ahorro estimado de `1.010 ms`).
   * **Solución:** Configurar la minificación y carga diferida de archivos CSS no críticos mediante *W3 Total Cache* y aplicar la propiedad `font-display: swap` en las tipografías del tema para que el texto sea visible de inmediato mientras cargan las fuentes personalizadas.
