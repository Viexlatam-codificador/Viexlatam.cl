## Viexlatam.cl

Landing estática para Viex Salud — Asesoría en Isapres.

Archivos
- `index.html`: página principal lista para servir como sitio estático.

Vista local

1. Abrir `index.html` directamente en el navegador (doble clic).
2. O servir en un servidor local (recomendado):

```bash
cd /workspaces/Viexlatam.cl
python3 -m http.server 8000
# luego abrir http://localhost:8000
```

Despliegue rápido

- GitHub Pages (recomendado): se añadió un workflow de GitHub Actions que despliega automáticamente la rama `main` a GitHub Pages. Para activarlo:
  1. Empuja este repositorio a GitHub (si aún no lo está).
  2. En el repositorio en GitHub, ve a Settings → Pages y en "Build and deployment" asegúrate de que la fuente esté en "GitHub Actions" (la acción creada usará la rama `main`).
  3. Tras el primer push la acción generará el sitio y Pages publicará `index.html`.

- Netlify / Vercel: conectar el repositorio o arrastrar `index.html` al panel de "drag & drop" para sitio estático.

Integración de leads

- El sitio ya incluye un formulario de lead nativo con envío vía webhook y confirmación por WhatsApp. Si no configuras `LEAD_WEBHOOK`, el formulario seguirá funcionando y abrirá WhatsApp con el contenido del lead.
- Puedes conectar el formulario a:
  - `Formspree` (envío por POST a Formspree, requiere crear una cuenta y reemplazar el endpoint en `index.html`).
  - `Zapier → Google Sheets` (configuración en Zapier que escucha un webhook y lo guarda en Sheets).
  - `Webhook propio` (endpoint en Node/Express o serverless para recibir y almacenar leads).

Notas

- El workflow de despliegue fue añadido en `.github/workflows/pages.yml`.
- Si quieres que yo empuje los cambios a GitHub y active Pages, autoriza la acción o dime si hago el push desde aquí (necesito permiso para crear commits remotos).

Configuración rápida para guardar leads (recomendada: Zapier → Google Sheets)

1. Crear Zap en Zapier con el trigger "Catch Hook" (app: Webhooks by Zapier).
2. Zapier te dará una URL tipo `https://hooks.zapier.com/hooks/catch/xxxxxx/yyyyyy`.
3. Abre `index.html` y en la parte superior del script modifica `LEAD_WEBHOOK` con esa URL.
   - Busca la línea: `var LEAD_WEBHOOK = '';` y pega tu URL entre las comillas.
4. En Zapier, añade una acción que guarde la entrada en Google Sheets, envíe un email o notifique por Slack.

Alternativa: usar Formspree

- Regístrate en Formspree, crea un formulario y copia el endpoint que te entregan.
- Puedes usarlo en `LEAD_WEBHOOK` o cambiar el formulario para enviar por `POST` al endpoint de Formspree.

Notas de seguridad

- No guardes secretos en `index.html` público. Si quieres proteger el endpoint, usa un servidor o serverless con autenticación.
- Zapier y Formspree son soluciones rápidas sin backend propio.

Formulario nativo

- El repositorio ahora usa un formulario nativo dentro de `index.html` con soporte webhook y confirmación por WhatsApp.
- Si seleccionas "Yo + pareja" o "Familia con hijos", se muestran campos adicionales para ingresar la edad de la pareja o de cada integrante extra.
- Ya no se usa el Google Form embebido en la versión principal de la landing.
