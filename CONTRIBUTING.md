# CONTRIBUTING — MEMELOGÍA OS
## Guía de Contribución para el Equipo Interno
### Solo para colaboradores de A51 · cuakzilla

---

> Este documento es para el equipo interno que trabaja en el código de
> Memelogía OS. No es una invitación a contribución pública — el proyecto
> es propietario y privado.

---

## Reglas de Oro (Leer antes de tocar el código)

```
1. NUNCA edites index.html sin hacer primero `node --check`
   antes Y después del cambio.

2. NUNCA hardcodees texto visible al usuario.
   Todo pasa por t('clave') y ambos bloques de STRINGS.

3. NUNCA instales dependencias npm sin aprobación del lead técnico.
   El proyecto es intencionalmente dependency-free.

4. NUNCA rompas el cascade de APIs.
   Siempre es waterfall: Anthropic → Gemini → Grok → OpenAI.

5. SIEMPRE crea una copia de respaldo antes de un patch grande.
   cp index.html index.html.bak.$(date +%Y%m%d%H%M)
```

---

## Setup del Entorno

```bash
# Verificar Node.js (solo para validación, no para build)
node --version  # Requiere v16+

# Clonar el repo
git clone https://github.com/A51/cuakzilla.git
cd cuakzilla

# Arrancar servidor local de pruebas
python -m http.server 8080
# Abrir: http://localhost:8080

# No hay npm install, no hay build step.
# index.html es la app completa.
```

---

## Flujo de Trabajo

### Para cambios menores (fix, copy, CSS)

```bash
# 1. Crear rama desde main
git checkout main && git pull
git checkout -b fix/descripcion-breve

# 2. Hacer el cambio en index.html

# 3. Validar JS SIEMPRE
python3 -c "
with open('index.html') as f:
    html = f.read()
js = html[html.find('<script>')+8:html.rfind('</script>')]
with open('/tmp/check.js','w') as f:
    f.write(js)
" && node --check /tmp/check.js

# 4. Probar en navegador
# - Chrome (principal)
# - Firefox
# - Safari si posible
# - Chrome móvil (DevTools → emulación)

# 5. Commit con formato convencional
git add index.html
git commit -m "fix: descripción del cambio en español"

# 6. Push y PR
git push origin fix/descripcion-breve
```

### Para features nuevas

```bash
# 1. Rama desde main
git checkout -b feat/nombre-del-modulo

# 2. Diseñar ANTES de codificar:
#    - Dónde vive el HTML (qué página, qué div)
#    - Qué CSS necesita (variables existentes primero)
#    - Qué funciones JS (nombres claros, sin colisiones)
#    - Qué claves de STRINGS (ES + EN desde el inicio)
#    - Qué localStorage keys nuevas (si aplica)

# 3. Orden de implementación recomendado:
#    CSS → HTML → STRINGS → JS → validar → probar

# 4. Checklist de feature completa:
# ☐ CSS añadido ANTES de </style>
# ☐ HTML añadido en el lugar correcto de la página
# ☐ Claves de i18n añadidas en AMBOS bloques (es y en)
# ☐ setTextById() llamadas añadidas en renderStaticUI() si hay elementos estáticos
# ☐ showPage() actualizado si es una página nueva
# ☐ DOMContentLoaded actualizado si hay init necesario
# ☐ node --check pasa ✓
# ☐ Console del navegador: 0 errores
# ☐ Funciona en dark Y light mode
# ☐ Funciona en móvil (320px) Y desktop (1280px)
# ☐ Switch de idioma actualiza correctamente los textos nuevos
# ☐ CHANGELOG.md actualizado
```

---

## Convenciones de Código

### Nombres de funciones
```javascript
// Módulos: camelCase con prefijo del módulo
renderWorldGlobal()     // módulo world
generateCountryMeme()   // módulo world
renderSignalCard()      // signal layer
callGeminiMedia()       // cascade

// Handlers: handle + Qué
handleAudio(e)
handleVideo(e)
handleFile(e)

// Toggles: toggle + Qué
toggleMic()
toggleSignalDetail()
toggleTechTable()

// Renders: render + Qué
renderResult()
renderLibrary()
renderHistory()
renderRisk()
```

### Claves de STRINGS
```javascript
// Formato: modulo_elemento_tipo
nav_world_key       // navegación
az_mode_media       // analyzer, modo
world_gen_btn_key   // world, botón
media_audio_title   // media, título
err_title           // error
```

### CSS — BEM simplificado
```css
/* Componentes: nombre-componente */
.signal-card { }
.world-country-card { }
.lib-card { }
.media-zone { }

/* Elementos: nombre-componente-elemento */
.signal-eyebrow { }
.world-detail-flag { }
.lib-card-title { }

/* Modificadores: nombre-componente.modificador */
.world-country-card.active { }
.mic-btn.recording { }
.nfeed-item.sev-high { }
```

### Variables CSS (siempre usar las existentes)
```css
/* Colores principales — NO hardcodear hex directamente */
var(--accent)     /* cyan #00e5ff */
var(--accent2)    /* purple #7c3aed */
var(--accent3)    /* amber #f59e0b */
var(--danger)     /* red #ef4444 */
var(--warn)       /* orange #f97316 */
var(--safe)       /* green #22c55e */
var(--text)       /* texto principal */
var(--text2)      /* texto secundario */
var(--muted)      /* texto muted */
var(--bg)         /* fondo principal */
var(--bg2)        /* fondo secundario */
var(--bg3)        /* fondo terciario */
var(--border)     /* bordes */

/* Tipografías */
var(--sans)       /* Inter / system-ui */
var(--mono)       /* Space Mono */
```

---

## Arquitectura del Archivo (Mapa de navegación)

```
index.html
│
├── <style>
│   ├── Variables CSS (:root dark + :root[data-theme="light"])
│   ├── Reset y base
│   ├── Layout (sidebar, main, pages)
│   ├── Componentes (card, badge, tag, btn, etc.)
│   ├── Páginas específicas (command, analyzer, history, world, atlas...)
│   ├── Signal Layer CSS
│   ├── Media Analyzer CSS
│   └── World + Library CSS
│
├── <body>
│   ├── #onboarding (overlay de bienvenida)
│   ├── .sidebar (desktop nav)
│   ├── .mob-topbar (móvil topbar)
│   ├── .key-drawer (panel de APIs móvil)
│   ├── .main-content
│   │   ├── #page-command
│   │   ├── #page-analyzer (incluye #mediaInputPanel)
│   │   ├── #page-history
│   │   ├── #page-world
│   │   ├── #page-atlas
│   │   ├── #page-causality
│   │   ├── #page-scenario
│   │   └── #page-risk
│   └── .bottom-nav (móvil)
│
└── <script>
    ├── STATE (variables globales)
    ├── ONBOARDING (startSystem, setApiKey)
    ├── NAVIGATION (showPage, setBottomActive)
    ├── MODE/UPLOAD (setMode, handleFile, handleAudio, handleVideo)
    ├── ANALYSIS (runAnalysis, buildPrompt, buildContent)
    ├── RENDER RESULT (renderResult, renderSignalCard)
    ├── CHAT (sendChat)
    ├── HISTORY (renderHistory, loadEntry, clearHistory)
    ├── EXPORT (doExportJSON, doExportMD)
    ├── COMMAND CENTER (updateCommandFromHistory, addLiveAlert, initCommandCharts)
    ├── MODULES (renderAtlas, renderCausality, renderScenParams, runScenario, renderRisk)
    ├── SIGNAL LAYER (renderSignalCard, detectForceType, toggleSignalDetail, toggleImpl)
    ├── MEDIA ANALYZER (handleAudio, handleVideo, toggleMic, extractVideoFrames, analyzeMedia, callGeminiMedia)
    ├── WORLD MODULE (COUNTRIES, CURATED_MEMES, initWorldPage, selectCountry, generateCountryMeme, renderLibrary)
    ├── STRINGS + t() (const STRINGS, function t)
    ├── CASCADE API (cascadeApiCall, callAnthropic, callGemini, callGrok, callOpenAI)
    └── INIT (DOMContentLoaded)
```

---

## Commits — Formato Convencional

```bash
feat: nueva funcionalidad
fix: corrección de bug
refactor: refactorización sin cambio de comportamiento
docs: solo documentación
style: cambios de CSS sin cambio de lógica
security: corrección de seguridad
chore: cambios de configuración, CI, etc.

# Ejemplos reales:
feat: agregar análisis de audio y video con Gemini
fix: killBannerText sin span wrapper causaba crash en renderRisk
refactor: cascade API reescrito como waterfall real
security: validación de tipo MIME en upload de media
docs: CHANGELOG actualizado con v9.0
```

---

## Antes de Hacer PR / Merge a Main

```bash
# Checklist obligatorio:
☐ node --check pasa sin errores
☐ 0 errores en console del navegador (Chrome, en cold start)
☐ Switch idioma ES↔EN funciona para todos los textos nuevos
☐ Dark y Light mode correctos
☐ Móvil 320px sin overflow horizontal
☐ Historial guarda y carga correctamente
☐ Export JSON funciona
☐ CHANGELOG.md actualizado
☐ Si es feature: documentación de usuario actualizada (MANUAL_USUARIO.md)
```

---

## Contacto del Equipo

**Lead técnico:** [NOMBRE] · [EMAIL]
**Canal de equipo:** [SLACK/DISCORD/WHATSAPP CHANNEL]
**Repo:** github.com/A51/cuakzilla (privado)

---

*CONTRIBUTING.md · Memelogía OS · A51 / cuakzilla · 2026*
*Solo para uso interno del equipo*
