# Bono Pro Amor · Antares CCT-89

Tablillas del Bono de Enrolamiento Pro Amor para los 10 Super Seniors. Cada uno entra desde el celular con el mismo enlace, toca su nombre y marca sus casillas. Los datos se guardan en Firebase (Firestore) y todos los ven al instante.

Archivos:

- `index.html`: la aplicación completa.
- `firebase-config.js`: aquí se pega la configuración de Firebase.
- `firestore.rules`: reglas de seguridad de la base de datos.

## 1. Crear el proyecto en Firebase

1. Entra a https://console.firebase.google.com y toca **Agregar proyecto**. Nombre sugerido: `bono-pro-amor-antares`. Puedes desactivar Google Analytics.
2. En el menú **Compilación > Firestore Database**, toca **Crear base de datos**. Elige una ubicación cercana (por ejemplo `nam5` o `southamerica-east1`) y el modo **producción**.
3. En la pestaña **Reglas** de Firestore, borra lo que haya, pega todo el contenido de `firestore.rules` y toca **Publicar**.
4. En **Configuración del proyecto** (engranaje) > **Tus apps**, toca el ícono web `</>`, ponle un nombre y registra la app. Copia el bloque `firebaseConfig` que te muestra.
5. Pega esos valores en `firebase-config.js`, reemplazando los `PEGA_AQUI`.

## 2. Subir al repositorio y publicar

1. Sube estos archivos a la raíz de un repositorio de GitHub (incluido el archivo oculto `.nojekyll`).
2. En el repositorio, ve a **Settings > Pages**. En **Source** elige **Deploy from a branch**, la rama `main` y la carpeta `/ (root)`. Guarda.
3. Después de uno o dos minutos GitHub muestra el enlace, con la forma `https://TU-USUARIO.github.io/NOMBRE-DEL-REPOSITORIO/`.
4. Comparte ese enlace con los 9 Super Seniors.

GitHub Pages gratis requiere que el repositorio sea público. Eso deja visible el código (incluida la llave Bre-B y la configuración de Firebase, que no es secreta), pero no los datos de las tablillas, que viven en Firebase.

## Cómo se usa

- Del listado se toca el nombre del Super Senior para abrir su tablilla.
- Se toca una casilla libre, se escribe el nombre de quien aporta y se elige **Ya aportó** o **Se comprometió**.
- Para quitar a alguien, se abre la casilla y se toca **Liberar casilla**.

## Seguridad

Cualquier persona con el enlace puede marcar casillas. Las reglas solo aceptan nombres de hasta 40 caracteres, estados válidos y casillas que existen, y no permiten borrar los nombres. Por eso conviene compartir el enlace solo con los 10 Super Seniors.
