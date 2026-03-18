# CLOUD RENDER DEPLOY MANUAL

1. Crear un proyecto en Github (puede ser privado o público).

2. Conectar el repo local con el repo remoto en Github.

3. En Render seleccionar "New Web Service" y conectar con el repo de Github.

4. Configurar el servicio en Render:
   - **Name**: Nombre del servicio.
   - **Languaje**: Node.
   - **Branch**: Seleccionar la rama que se desea desplegar (por ejemplo, `main`).
   - **Root Directory**: Dejar en blanco si el proyecto está en la raíz del repo, o especificar la carpeta si el proyecto está dentro de una subcarpeta.
   - **Build Command**: `npm install && npm run build`.
   - **Start Command**: `npm start`.
   - **Enviroment Variables**: Si existen variables de entorno se añaden aquí (por ejemplo, `PORT`, `DATABASE_URL`, etc.).

5. Hacer clic en "Deploy Web Service" y esperar a que Render construya y despliegue la aplicación.

6. Una vez desplegado, Render hará un deploy cada vez que se haga un push a la rama seleccionada en Github.
