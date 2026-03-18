# CLOUD RENDER DEPLOY MANUAL

1. Crear un proyecto en Github (puede ser privado o público).

2. Conectar el repo local con el repo remoto en Github.

3. En Render `https://render.com/` ingresar a tu cuenta y en el Dashboard seleccionar "New" -> "Static Site" y conectar con el repo de Github. (En este caso se selecciona Static site porque el proyecto se va a construir en Render, no se va a subir la carpeta `dist` al repo y porque no hay un servidor propio en el proyecto, sino que se va a servir el contenido estático generado por Vite).

4. Configurar el sitio en Render:
   - **Name**: Nombre del sitio.
   - **Branch**: Seleccionar la rama que se desea desplegar (por ejemplo, `main`).
   - **Root Directory**: Dejar en blanco si el proyecto está en la raíz del repo, o especificar la carpeta si el proyecto está dentro de una subcarpeta.
   - **Build Command**: `npm install && npm run build`.
   - **Publish Directory**: `dist`.

5. Hacer clic en "Deploy Static Site" y esperar a que Render construya y despliegue la aplicación.

6. Una vez desplegado, Render hará un deploy cada vez que se haga un push a la rama seleccionada en Github.

## Notas

- No necesitas crear una rama separada para `dist`.
- No subas la carpeta `dist` al repositorio.
- Para Static Site, no se usa el comando `npm start`.
- Aunque sea Static Site, `fetch` sigue funcionando porque el navegador ejecuta el JavaScript del frontend y realiza las llamadas HTTP directamente a la API externa.
