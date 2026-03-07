# 🍽️ Restaurante PWA

Menú digital con panel de administración. Estilo luxury rojo vino y dorado.

## 📂 Archivos

```
├── index.html        ← Vista del CLIENTE (carta del menú)
├── admin.html        ← Vista del ADMIN (solo tú)
├── productos.json    ← Base de datos del menú
├── manifest.json     ← Configuración PWA
├── service-worker.js ← Cache offline
├── icon-192.png
└── icon-512.png
```

## 🚀 Configuración inicial (una sola vez)

### 1. Sube todos los archivos a GitHub Pages
- Repositorio → Settings → Pages → Source: `main / root`

### 2. Crea un Personal Access Token en GitHub
- GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic)
- Permisos necesarios: `repo` (completo)
- Cópialo, solo lo verás una vez

### 3. Configura el Admin
- Abre `https://tu-usuario.github.io/tu-repo/admin.html`
- Contraseña por defecto: **admin123** (cámbiala en la pestaña Configuración)
- Ve a la pestaña **⚙️ Configuración** e ingresa:
  - Tu usuario de GitHub
  - Nombre del repositorio
  - El token que creaste
  - Tu número de WhatsApp (con código de país, sin +)
  - Nombre del restaurante y slogan
- Guarda la configuración

### 4. Agrega tu primer platillo
- Ve a **➕ Agregar platillo**
- Completa nombre, precio, categoría, descripción y foto
- Haz clic en **Agregar al menú**
- Ve a **📋 Mis platillos** y haz clic en **🚀 Publicar cambios en GitHub**

### 5. Comparte el link con tus clientes
```
https://tu-usuario.github.io/tu-repo/
```

## 📱 Para instalar como app
- **Android**: Chrome → menú ⋮ → Agregar a pantalla de inicio
- **iPhone**: Safari → compartir → Agregar a pantalla de inicio

## 🔄 Actualizar versión (service worker)
Cada vez que hagas cambios importantes, en `service-worker.js` cambia:
```js
const CACHE_NAME = 'restaurante-v1';  →  'restaurante-v2'
```
