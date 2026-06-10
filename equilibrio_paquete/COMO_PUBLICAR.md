# Equilibrio — Publicar la app y usarla en tu iPhone

## Qué hay en este paquete
| Archivo | Para qué sirve |
|---|---|
| `index.html` | La app completa (todo vive aquí) |
| `manifest.json` | Hace que se instale como app (PWA) |
| `sw.js` | Permite que funcione sin internet |
| `icon-192.png`, `icon-512.png`, `apple-touch-icon.png` | Íconos de la app |
| `firebase.json` | Solo si algún día usas Firebase Hosting |

**Importante:** sube los archivos sueltos, tal cual, todos en la raíz (no dentro de una subcarpeta).

---

## OPCIÓN A — GitHub Pages (recomendada, gratis, 5 min)

### 1. Crear la cuenta y el repositorio
1. Entra a **github.com** e inicia sesión (o crea cuenta gratis).
2. Clic en **+** (arriba a la derecha) → **New repository**.
3. Repository name: `equilibrio` (o el que quieras).
4. Déjalo **Public** (tranquilo: solo se publica el código del programa; tus datos personales NUNCA salen de tu teléfono).
5. Clic **Create repository**.

### 2. Subir los archivos
1. En la página del repo nuevo, clic en **uploading an existing file** (o `Add file → Upload files`).
2. Arrastra los 7 archivos de este paquete (¡descomprime el ZIP primero!).
3. Abajo clic **Commit changes** y espera a que termine.

### 3. Activar GitHub Pages
1. En el repo: **Settings** (pestaña de arriba) → **Pages** (menú izquierdo).
2. En *Build and deployment* → Source: **Deploy from a branch**.
3. Branch: **main** y carpeta **/ (root)** → **Save**.
4. Espera 1–2 minutos y recarga: arriba aparece tu dirección:
   `https://TUUSUARIO.github.io/equilibrio/`
5. Ábrela en el computador para comprobar que carga.

### 4. Instalarla en el iPhone
1. Abre esa dirección en **Safari** del iPhone.
2. Botón **Compartir** (cuadrado con flecha) → **Añadir a pantalla de inicio** → **Añadir**.
3. Ya tienes Equilibrio como app, con su ícono, a pantalla completa y funciona sin internet.

### 5. Actualizar la app más adelante
1. En el repo: entra a `index.html` → ícono del lápiz (o sube el archivo nuevo encima con Upload files).
2. Commit changes. En 1–2 min se actualiza.
3. En el iPhone: cierra y abre la app un par de veces para que tome la versión nueva.

---

## OPCIÓN B — Firebase Hosting (si la prefieres)
Usa un proyecto **personal nuevo** (no mezclar con proyectos de trabajo).
1. `console.firebase.google.com` → Add project → nombre: `equilibrio-fm` (sin Analytics).
2. En tu PC instala Node.js y luego en una terminal:
   ```
   npm install -g firebase-tools
   firebase login
   cd carpeta-del-paquete
   firebase init hosting   (elige el proyecto, public: . , single-page: No)
   firebase deploy
   ```
3. Te da una URL `https://equilibrio-fm.web.app` → instálala en el iPhone igual que arriba (paso 4).

---

## Notas
- **Privacidad:** tus registros (hábitos, notas, peso, etc.) se guardan SOLO en el dispositivo donde usas la app. El repo público no los contiene ni los puede ver nadie.
- **Compartir:** puedes pasar el mismo link a tu esposa o a quien quieras; cada teléfono tiene sus propios datos, independientes.
- **Respaldo:** en la app → ⚙️ Más → Respaldo: descarga el JSON de vez en cuando.
- **Koa en Rive (futuro):** cuando exportes tu `koa.riv` desde rive.app, súbelo al repo junto a `index.html`. La app lo detecta sola y lo usa.
- **Espejo (IA):** en la versión publicada requiere un proxy con tu API key; eso lo configuramos juntos cuando quieras.
