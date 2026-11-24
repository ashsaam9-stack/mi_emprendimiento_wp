# Plan de Continuidad — Etapa 2 (Studio Ash)

Este documento define las funcionalidades pendientes para la segunda etapa de evolución del sitio web de **Studio Ash**, los recursos necesarios para implementarlas, su cronograma estimado y la gestión de riesgos asociados.

---

## 1. Funcionalidades para la Etapa 2

Durante la primera etapa se priorizó la presencia digital, el catálogo informativo de servicios y el contacto directo. Para la Etapa 2 se proyectan las siguientes mejoras que quedaron fuera del alcance inicial por restricciones de tiempo, presupuesto de hosting gratuito y curva de aprendizaje técnico:

1. **Sistema de reservas automatizado con calendario en tiempo real:** Reemplazar el formulario de solicitud manual por una agenda sincronizada con disponibilidad horaria, bloqueo automático de cupos y recordatorios por correo/WhatsApp.
2. **Sección de Preguntas Frecuentes (FAQ) interactiva:** Acordeón desplegable con dudas habituales sobre contraindicaciones, duración de cada técnica, preparación previa y cuidados posteriores.
3. **Páginas legales (Términos y Condiciones y Política de Privacidad):** Documentación formal sobre tratamiento de datos personales capturados en formularios y políticas de cancelación/reagendamiento de citas.
4. **Tienda online / Venta de productos de cuidado (E-commerce):** Catálogo con carrito de compras para vender kits de limpieza de pestañas, cepillos y sérums fortalecedores.

---

## 2. Recursos Necesarios

| Recurso | Detalle | Tipo / Costo estimado |
| :--- | :--- | :--- |
| **Hosting y Dominio** | Migración de hosting gratuito (InfinityFree) a un plan de hosting compartido con SSL dedicado y dominio `.cl` o `.com` propio para mayor estabilidad y entregabilidad de correos. | Pago (~$35.000 - $50.000 CLP anuales) |
| **Plugin de Reservas** | *Amelia Lite*, *Simply Schedule Appointments* o *Bookly* para gestión de citas por servicio y bloque horario. | Freemium / Licencia opcional (~$49 - $89 USD) |
| **Plugin E-commerce** | *WooCommerce* + pasarela de pago local (Webpay Plus / Mercado Pago) para venta de productos de cuidado posterior. | Gratuito (comisión por transacción en pasarela) |
| **Configuración SMTP** | Plugin *WP Mail SMTP* conectado a una cuenta de correo corporativa (`contacto@studioash.cl`) para garantizar la llegada de notificaciones sin caer en spam. | Gratuito |
| **Conocimientos técnicos** | Configuración de registros DNS (SPF/DKIM para correo), gestión de pasarelas de pago y configuración de flujos de reserva. | Autoaprendizaje / Documentación oficial |

---

## 3. Priorización y Cronograma Estimado

La implementación de la Etapa 2 se planifica en un horizonte de **4 semanas**:

* **Semana 1 (Prioridad Alta — Estabilidad y Legalidad):**
  * Contratación de dominio propio y migración a hosting de pago.
  * Configuración de correo corporativo y *WP Mail SMTP*.
  * Redacción y publicación de *Política de Privacidad* y *Términos de Cancelación*.
* **Semana 2 (Prioridad Alta — Experiencia de Usuario):**
  * Creación e integración de la sección de *Preguntas Frecuentes (FAQ)* en la página de Servicios y Contacto.
  * Optimización de imágenes y revisión de velocidad móvil.
* **Semana 3 (Prioridad Media — Automatización):**
  * Instalación y configuración del plugin de agendamiento con bloques horarios por servicio (*Pestañas, Cejas, Lash Lifting*).
  * Pruebas de flujo completo de reserva y notificaciones.
* **Semana 4 (Prioridad Baja — Monetización):**
  * Instalación de *WooCommerce*, carga de productos de cuidado posterior e integración de pasarela de pago en modo prueba y producción.

---

## 4. Riesgos y Mitigación

| Riesgo identificado | Impacto | Estrategia de mitigación |
| :--- | :--- | :--- |
| **Fallas en el envío de correos de confirmación** (bloqueos del servidor gratuito o caída en carpeta de spam). | Alto | Implementar *WP Mail SMTP* autenticado con registros SPF y DKIM bajo dominio propio. |
| **Pérdida de datos o desconfiguración durante la migración** desde InfinityFree al nuevo hosting. | Alto | Generar respaldos completos con *All-in-One WP Migration* antes de cada cambio y mantener una copia local verificada. |
| **Sobrecarga de plugins y caída en rendimiento móvil** al incorporar agenda y tienda online. | Medio | Mantener configurado *W3 Total Cache*, comprimir imágenes a formato WebP y desactivar scripts innecesarios en páginas donde no se usen. |
| **Doble reserva o desfase de horarios** entre citas tomadas por Instagram y citas tomadas por la web. | Medio | Centralizar toda la disponibilidad en el calendario del sitio web y redirigir el enlace de la biografía de Instagram directamente a la agenda online. |
