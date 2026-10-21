# Guía de instalación del perfil — Mirep68

## 0. Lo más importante
Tu README actual está en el repositorio **Mirep68s** (con "s"), y GitHub **solo** muestra en tu perfil el README del repositorio que se llama **exactamente igual a tu usuario: `Mirep68`**. Por eso tu perfil hoy solo dice "Hi there 👋".
Todo lo de esta carpeta va en **`Mirep68/Mirep68`**.

## 1. Subir los archivos
Entra a https://github.com/Mirep68/Mirep68 y sube esta estructura tal cual:

```
README.md
assets/banner.svg
.github/workflows/snake.yml
.github/workflows/profile-cards.yml
```

> La carpeta `.github` empieza con punto y a veces el arrastrar-y-soltar la ignora. Si pasa, usa
> **Add file → Create new file**, escribe el nombre `.github/workflows/snake.yml` (las barras crean las carpetas) y pega el contenido. Repite con `profile-cards.yml`.

## 2. Darle permiso de escritura a las Actions
En el repo `Mirep68`: **Settings → Actions → General → Workflow permissions → "Read and write permissions" → Save**.

## 3. Crear el token para las tarjetas de estadísticas
1. Ve a https://github.com/settings/personal-access-tokens/new
2. Nombre: `profile-cards` · Expiración: 90 días (o más).
3. Repository access: **Public repositories (read-only)**. No marques nada más.
4. Genera y **copia** el token (solo se muestra una vez).
5. En el repo `Mirep68`: **Settings → Secrets and variables → Actions → New repository secret**
   - Name: `SUMMARY_GITHUB_TOKEN`
   - Secret: pega el token.

## 4. Ejecutar los workflows por primera vez
Pestaña **Actions** del repo `Mirep68`:
- "Generar snake de contribuciones" → **Run workflow**
- "Generar tarjetas de estadísticas" → **Run workflow**

Tardan 1–2 minutos. Después se actualizan solos (snake a diario, tarjetas cada 12 h).
Hasta que corran, esas dos secciones aparecerán como imagen rota: es normal.

## 5. Limpieza y mejoras recomendadas
- **Borra o archiva `Mirep68s`** cuando el nuevo perfil esté listo (Settings → Danger Zone). Hoy aparece como tu repo "popular" #1 y no aporta.
- **Fija (Pin) tus 4 proyectos**: en tu perfil → "Customize your pins" → ReWeather, NightGuard, Vitalis IA, Video Game Sales.
- **Agrega descripción y topics** a `Nightguard-Driver-Drowsiness-Detection` y `Vitalis-IA-Dashboard` (botón ⚙️ junto a "About"). Ej. topics: `esp32`, `tinyml`, `edge-impulse`, `iot`, `pytorch`, `flask`, `machine-learning`.
- **Sube el código del firmware** (C++/Arduino) de ReWeather y NightGuard. Ahora GitHub no detecta C++ en tus repos, así que las tarjetas de lenguajes solo mostrarán Jupyter y HTML. Con el código subido se verá tu lado embebido.
- Cuando tengas LinkedIn o un correo público, descomenta las líneas marcadas en el README (sección de badges del encabezado).

## Personalizar
- **Colores del banner**: en `assets/banner.svg`, cambia `#00e5ff` (cian) y `#39ff9c` (verde neón).
- **Frases que se escriben solas**: en el README, parámetro `lines=` de la imagen *Typing SVG* (los espacios van como `+` y cada frase se separa con `;`).
- **Tema de las tarjetas**: cambia `THEME` en `profile-cards.yml` (opciones: `github_dark`, `2077`, `dracula`, `radical`, `nord_dark`…) y la carpeta `tokyonight` en el README por el mismo nombre.
