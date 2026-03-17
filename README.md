# FacuApp 📚

PWA de gestión académica personal — Mobile First, Dark Mode, Offline Ready.

## Estructura de archivos

```
facuapp/
├── index.html          ← App principal (React + Tailwind inline)
├── manifest.json       ← Configuración PWA
├── sw.js               ← Service Worker (offline)
├── icons/
│   ├── icon-192.png    ← Ícono PWA
│   └── icon-512.png    ← Ícono PWA grande
└── README.md
```

## Deploy en GitHub Pages (paso a paso)

### 1. Crear el repositorio
1. Entrá a [github.com](https://github.com) → **New repository**
2. Nombre: `facuapp` (o el que quieras)
3. Visibility: **Public** ✓ (necesario para GitHub Pages gratis)
4. Clic en **Create repository**

### 2. Subir los archivos
**Opción A — Desde el navegador (más fácil):**
1. En tu repo recién creado, clic en **"uploading an existing file"**
2. Arrastrá todos los archivos: `index.html`, `manifest.json`, `sw.js`
3. Creá la carpeta `icons/` y subí `icon-192.png` y `icon-512.png`
4. Clic en **Commit changes**

**Opción B — Con Git:**
```bash
git init
git add .
git commit -m "Initial commit — FacuApp PWA"
git branch -M main
git remote add origin https://github.com/TU_USUARIO/facuapp.git
git push -u origin main
```

### 3. Activar GitHub Pages
1. En tu repo → **Settings** → **Pages** (menú lateral izquierdo)
2. Source: **Deploy from a branch**
3. Branch: `main` / `/ (root)`
4. Clic en **Save**
5. En 1-2 minutos tu app estará en:
   `https://TU_USUARIO.github.io/facuapp/`

### 4. Instalar en iPhone
1. Abrí la URL en **Safari** (no Chrome)
2. Tocá el botón **Compartir** ⬆
3. Seleccioná **"Añadir a pantalla de inicio"**
4. Poné el nombre que quieras → **Agregar**
5. ¡Listo! Se abre como app nativa sin barras de navegador

---

## Funcionalidades

| Sección | Descripción |
|---------|-------------|
| 📋 Tareas | Lista con prioridades, fechas límite y filtros inteligentes |
| 📅 Clases | Calendario semanal con bitácora por clase |
| 📚 Materias | Gestión con colores y barra de progreso |
| 🏆 Progreso | Sistema de niveles y medallas gamificadas |
| ⚙️ Config | Exportar/Importar JSON para backup y sincronización |

## Backup entre dispositivos

1. **Exportar**: Config → "Exportar → backup_facu.json"
2. Mandarte el archivo por WhatsApp / Mail / Drive
3. **Importar** en el otro dispositivo: Config → "Importar desde JSON"

## Stack técnico

- **React 18** (CDN, sin bundler — funciona directo en GitHub Pages)
- **Babel Standalone** para JSX en el browser
- **LocalStorage** para persistencia offline
- **Service Worker** para caché offline
- **PWA Manifest** para instalación nativa en iOS/Android
- **CSS Variables** — Dark Mode por defecto
- **Safe Areas** (`env(safe-area-inset-*)`) para iPhones con notch
