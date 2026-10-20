# Cruceros x el Mundo — sitio web

Sitio estático (un solo archivo: index.html). Opera World Class Cruises S.A.

## Antes de publicar
En index.html, buscar `const CFG=` y completar:
- whatsapp: número de WhatsApp Business solo con números y código de país (ej. 5491112345678)
- mail: casilla para consultas
- legajo: número de legajo del Ministerio de Turismo (obligatorio mostrarlo en agencias)

## Publicar en GitHub Pages
1. Crear el repositorio (ej. christianmahia/cruceros-x-el-mundo) y subir index.html y CNAME.
2. Settings > Pages > Source: rama main, carpeta raíz.
3. Marcar "Enforce HTTPS" cuando aparezca.

## Apuntar el dominio en GoDaddy (crucerosxelmundo.com > DNS)
- Registros A para "@": 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
- Registro CNAME "www" -> christianmahia.github.io
- Quitar el "Parked"/sitio del creador de GoDaddy que hoy ocupa el dominio.
- cruceroxelmundo.com (sin s): reenvío (forwarding) 301 a https://crucerosxelmundo.com

## Medición (Google Analytics y píxel de Meta)
La página ya tiene la medición preparada. Se activa sola cuando se cargan los IDs en la línea `const CFG=` de index.html:
- `ga:'G-XXXXXXXXXX'` → crear una propiedad en analytics.google.com (Administrar → Crear propiedad → Flujo de datos web con crucerosxelmundo.com) y copiar el "ID de medición".
- `pixel:'123456789012345'` → en business.facebook.com → Administrador de eventos → Conectar orígenes de datos → Web → Píxel, y copiar el ID.

Eventos que se registran:
- `consulta_whatsapp` (Meta: Contact): cada clic en un botón de WhatsApp, con la sección desde donde se hizo.
- `formulario_enviado` (Meta: Lead): cada consulta por formulario, con destino y pasajeros.
- `ver_crucero` (Meta: ViewContent): cada vez que alguien abre un crucero.
- `page_view`: cada sección que se visita.

En Google Analytics conviene marcar `consulta_whatsapp` y `formulario_enviado` como "eventos clave" para ver cuántas consultas trae cada campaña.

## Videos
Los videos van como archivos aparte (promo.*, historia-relax.*, historia-vida-a-bordo.*). Subirlos junto con index.html.
