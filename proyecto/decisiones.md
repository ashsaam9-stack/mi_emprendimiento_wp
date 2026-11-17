# Registro de Decisiones - STUDIO ASH

## 1. Selección y Comprobación de Plugins (10 pts)
A continuación se detallan los 5 plugins seleccionados para el sitio, verificados según su compatibilidad, gratuidad y función específica para el proyecto:

| Nombre del Plugin | Función Principal | ¿Es Gratis? | Versión de WP Compatible | ¿Funciona con Tema Custom? | Enlace Oficial |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Contact Form 7** | Gestión de formularios de contacto y reservas para clientas (reemplazó a WPForms según Plan B). | Sí | 5.5 o superior (Probado hasta 7.1) | Sí | [Contact Form 7 en WordPress.org](https://wordpress.org/plugins/contact-form-7/) |
| **Rank Math SEO** | Optimización del posicionamiento en buscadores (SEO) local. | Sí | 5.6 o superior (Probado hasta 7.1) | Sí | [Rank Math SEO en WordPress.org](https://wordpress.org/plugins/seo-by-rank-math/) |
| **W3 Total Cache** | Optimización de velocidad y rendimiento de carga del sitio web. | Sí | 4.0 o superior (Probado hasta 7.1) | Sí | [W3 Total Cache en WordPress.org](https://wordpress.org/plugins/w3-total-cache/) |
| **Loginizer** | Protección contra ataques de fuerza bruta y seguridad de acceso al panel. | Sí | 5.0 o superior (Probado hasta 7.1) | Sí | [Loginizer en WordPress.org](https://wordpress.org/plugins/loginizer/) |
| **UpdraftPlus** | Creación de copias de seguridad (backups) automáticas y restauración. | Sí | 4.7 o superior (Probado hasta 7.1) | Sí | [UpdraftPlus en WordPress.org](https://wordpress.org/plugins/updraftplus/) |

---

## 2. Páginas Seleccionadas para la Fase 1 (5 pts)
Para esta primera etapa de construcción (excluyendo pagos y carrito por ahora), se configuraron las siguientes 5 páginas:

1. **Inicio:** Es la carta de presentación principal del estudio para captar la atención de las clientas.
2. **Contacto:** Permite que se comuniquen de forma directa a través de un formulario integrado con Contact Form 7.
3. **Servicios:** Detalla los diferentes tipos de extensiones de pestañas, lifting y diseño de cejas disponibles.
4. **Sobre mí:** Muestra la historia, experiencia y profesionalismo detrás de STUDIO ASH.
5. **Blog:** Espacio destinado a compartir consejos de cuidado posterior y tendencias.

* **Páginas para una fase posterior:** Zona de Preguntas Frecuentes (FAQ), Carrito de compras/Tienda, Términos y Condiciones, y Políticas de Privacidad.

---

## 3. Plan del Tema (5 pts)
* **Nombre del tema implementado:** `Twenty Twenty-Five` (adaptación personalizada de la identidad visual de Studio Ash mediante Editor del Sitio / Full Site Editing, aplicando el Plan B frente al tema inicial `studio-ash-theme`).
* **Tipo:** Tema de bloques estructurado adaptado a la identidad visual de la marca (paleta pastel/rosada, tipografía elegante y encabezados/pies de página globales personalizados).
* **Justificación:** Inicialmente se proyectó un tema codificado desde cero (`studio-ash-theme`), pero en aplicación del **Plan B** de la Sección 4 se optó por adaptar el tema oficial de bloques **Twenty Twenty-Five**. Esto permitió garantizar la correcta integración de las 5 páginas, el responsive móvil y los plugins activos sin comprometer la fecha de entrega del Checkpoint, manteniendo fielmente la estética definida para Studio Ash.
* **Carta Gantt simplificada:**
  * *5 al 10 de Noviembre:* Investigación y elección de plugins / Creación de estructura base.
  * *11 al 17 de Noviembre:* Activación de Plan B en tema estructurado, personalización visual e integración de las 5 páginas y entradas de blog.
  * *18 de Noviembre:* **Checkpoint (Entrega intermedia).**
  * *19 al 24 de Noviembre:* Pruebas finales, optimización de caché/SEO y ajustes estéticos.
  * *25 de Noviembre:* **Entrega final y publicación del sitio.**

---

## 4. Plan B / Gestión de Riesgos (5 pts)
* **Incompatibilidad o mal funcionamiento de un plugin:** Desactivar el plugin afectado y reemplazarlo por una alternativa ligera y compatible (aplicado con *Contact Form 7* en reemplazo de *WPForms* y *W3 Total Cache*).
* **Demora en la codificación desde cero del tema:** Utilizar un tema base estructurado (`Twenty Twenty-Five`) y adaptarlo mediante Full Site Editing para asegurar la entrega a tiempo manteniendo la identidad visual (aplicado para el Checkpoint).
* **Caída del servidor gratuito o pérdida de cambios:** Mantener copias de seguridad periódicas mediante *UpdraftPlus* y respaldar el código y documentación en este repositorio de GitHub.
