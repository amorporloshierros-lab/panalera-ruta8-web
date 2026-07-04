# 🚀 Cómo publicar la web (Vercel + GitHub) y editar textos

La web es **un solo archivo** (`index.html`). No necesita build ni nada especial.

---

## ✅ OPCIÓN A — La más rápida (Vercel, SIN GitHub) — 2 minutos

Ideal para verla online ya.

1. Entrá a **https://vercel.com** e iniciá sesión (con tu cuenta, la misma de `lca-automatic`).
2. Botón **"Add New…" → "Project"**.
3. Buscá abajo la opción de **importar/deploy sin git** o simplemente **arrastrá la carpeta `07-tienda-web`** a la ventana (Vercel acepta drag & drop de una carpeta).
4. En el nombre poné **panaleraruta8**. Deploy.
5. En segundos te da una URL tipo **`panaleraruta8.vercel.app`**. ¡Listo, está online!

> Para editar un texto con este método: cambiás el `index.html` en tu PC y volvés a arrastrar la carpeta (re-deploy). Simple pero manual.

---

## ⭐ OPCIÓN B — Con GitHub (recomendada: editás online y se actualiza sola)

Así podés cambiar textos desde la web de GitHub y Vercel republica solo.

### 1) Crear el repositorio en GitHub
1. Entrá a **https://github.com** → botón **"+"** (arriba a la derecha) → **"New repository"**.
2. Nombre: **panalera-ruta8-web**. Dejalo **Public** (o Private). NO tildes "Add README".
3. **Create repository**.

### 2) Subir la web
La forma más fácil, sin comandos:
1. En el repo recién creado, tocá **"uploading an existing file"** (link azul en el medio).
2. Arrastrá el archivo **`index.html`** (y si querés, `BRIEF-WEB.md`) desde la carpeta `07-tienda-web`.
3. Abajo, **"Commit changes"**.

### 3) Conectar Vercel al repo
1. En **https://vercel.com** → **"Add New… → Project"**.
2. **Import** el repositorio `panalera-ruta8-web` (autorizá GitHub si te lo pide).
3. Framework: **Other** (es estático). Deploy.
4. Te da la URL `panalera-ruta8-web.vercel.app`.

### 4) Editar textos online (lo que pediste)
1. En GitHub, abrí **`index.html`** → tocá el **lápiz ✏️** (editar).
2. Buscá el texto que querés cambiar (Ctrl+F), editalo, y **"Commit changes"**.
3. **Vercel republica solo en ~30 seg.** No tocás nada más.

---

## 🌐 Dominio propio (panaleraruta8.com.ar)
Cuando tengas el dominio comprado: en Vercel → tu proyecto → **Settings → Domains → Add** → escribís `panaleraruta8.com.ar` y seguís las instrucciones de DNS. Queda con tu dominio real.

---

## ✍️ Qué textos vas a querer editar (dónde están en index.html)
- **Título grande (hero):** buscá `Pañales al precio de fábrica`
- **Envío gratis desde $:** buscá `desde $30.000`
- **WhatsApp / redes:** buscá `aria-label="Instagram"` / `"Facebook"` (poné tus links)
- **Productos y precios (demo):** buscá `const PRODUCTOS`
- **Textos de Rita:** buscá `function ritaReply`

> Nota: si querés que estos textos y el prompt de Rita se editen desde el **dashboard** (sin tocar código), esa es la etapa de **backend** (tabla `web_config` + Edge Function) que quedó como próximo paso.
