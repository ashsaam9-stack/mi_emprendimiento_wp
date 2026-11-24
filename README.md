# Studio Ash — Sitio Web Corporativo y de Reservas

Sitio web oficial de **Studio Ash**, estudio especializado en belleza, diseño de cejas, extensiones de pestañas y lash lifting. El proyecto fue desarrollado sobre WordPress con un enfoque en identidad visual limpia, navegación intuitiva en dispositivos móviles y captación de clientes mediante formulario de contacto directo.

* **URL en producción:** https://studioash.infinityfree.me

---

## Requisitos Técnicos

* **CMS:** WordPress (versión 6.x)
* **Servidor / Hosting:** InfinityFree (PHP 8.x, MySQL / MariaDB)
* **Tema activo:** Twenty Twenty-Five (Editor de Bloques / Full Site Editing)
* **Plugins instalados y activos:**
  1. **WPForms Lite:** Gestión del formulario de contacto y agendamiento.
  2. **All-in-One WP Migration:** Generación de respaldos completos y migración del sitio.
  3. **W3 Total Cache:** Optimización de caché y velocidad de carga.
  4. **Really Simple SSL / Seguridad básica:** Gestión de certificado HTTPS y refuerzo de seguridad.
  5. **Yoast SEO (o plugin SEO activo):** Optimización de metadatos y estructura para buscadores.

---

## Estructura del Sitio

* **Páginas principales:** Inicio, Servicios, Sobre mí, Blog y Contacto.
* **Entradas de blog:** Artículos informativos sobre cuidados posteriores, comparativa *Lash Lifting vs. Extensiones*, tendencias y presentación del estudio.

---

## Guía de Respaldo y Reinstalación

### Cómo generar un respaldo (Backup)
1. Ingresar al panel de administración de WordPress (`/wp-admin`).
2. En el menú lateral izquierdo, ir a **All-in-One WP Migration > Exportar**.
3. Hacer clic en **Exportar a > Archivo**.
4. Esperar a que el sistema empaquete la base de datos, medios, temas y plugins.
5. Descargar el archivo generado con extensión `.wpress` y guardarlo en un almacenamiento seguro (local o en la nube).

### Cómo reinstalar el sitio en un nuevo servidor
1. Instalar una copia limpia de WordPress en el nuevo hosting o entorno local.
2. Acceder al nuevo panel `/wp-admin`, ir a **Plugins > Añadir nuevo**, buscar e instalar **All-in-One WP Migration** y activarlo.
3. Ir a **All-in-One WP Migration > Importar**.
4. Seleccionar **Importar desde > Archivo** y cargar el respaldo `.wpress` previamente descargado.
5. Confirmar la advertencia de sobrescritura de la base de datos y esperar a que finalice el proceso.
6. Una vez completado, ir a **Ajustes > Enlaces permanentes** y hacer clic en **Guardar cambios** (dos veces si es necesario) para regenerar el archivo `.htaccess` y evitar errores 404 en las páginas internas.
