# CHANGELOG — MEMELOGÍA OS
## Historial Oficial de Versiones

Formato: `[VERSION] — YYYY-MM-DD — Descripción`
Tipos de cambio: `feat` (nueva funcionalidad) · `fix` (corrección) · `refactor` · `docs` · `security`

---

## [9.0] — 2026-07-XX — Audio · Video · Micrófono

### feat
- Nuevo tab **🎵 Audio · Video** en el Meme Analyzer (tercer tab junto a Quick Scan y Deep Analysis)
- Upload de audio: MP3, WAV, OGG, M4A, WebM — hasta 20MB
- Upload de video: MP4, WebM, MOV, AVI — hasta 20MB
- Grabación de micrófono en vivo con `MediaRecorder API` — auto-stop a los 2 minutos, contador en tiempo real
- Extracción automática de hasta 6 frames clave de videos en el browser (HTMLVideoElement + Canvas) sin necesidad de servidor
- Tira visual de frames con selección interactiva
- `callGeminiMedia()` — función dedicada que envía audio/video como base64 a Gemini 1.5 Flash con soporte nativo multimodal
- `buildMediaPrompt()` — prompt optimizado para análisis de contenido audiovisual incluyendo transcripción, tono, ritmo, y referencias culturales
- `extractVideoFrames()` — extracción de frames en cliente, sin dependencias
- `toggleMic()` — control completo de grabación/detención con gestión de permisos
- `resetMedia()` — limpieza completa del estado de media
- Campo de contexto adicional para especificar plataforma, idioma o comunidad
- Preview de audio y video con controles nativos del navegador
- Caja de transcripción detectada (campo `_transcript` en el JSON de respuesta)
- Badge de estado de Gemini (verde/ámbar según si la key está configurada)
- Zona de drag & drop para zonas de audio y video
- CSS completo: `.media-zone`, `.mic-btn`, `.frames-strip`, `.frame-thumb`, `.transcript-box`, `.media-preview`, `.media-provider-badge`
- i18n completo: 17 nuevas claves en ES y EN para todos los elementos del módulo
- El resultado de análisis de media se guarda automáticamente en el historial con thumbnail del primer frame (video) o sin imagen (audio)
- Validación de tamaño de archivo (límite 20MB) antes de procesar

### fix
- Corrección de inserción de HTML del panel media que no se inyectaba correctamente en el primer intento de patch

### security
- Validación de tipo MIME antes de procesar archivos de media

---

## [8.0] — 2026-06-XX — Mundo · Biblioteca · 17 Países

### feat
- Nuevo módulo **🌐 Mundo · Biblioteca** — página completa con meme del día global + por país + biblioteca curada
- `COUNTRIES` array con 17 países: México, EE.UU., Suiza, Suecia, Noruega, Finlandia, China, Singapur, Japón, Corea del Sur, Chile, Antártida, Australia, Alemania, España, Brasil, Canadá
- Para cada país: bandera emoji, nombre ES/EN, tendencia del día ES/EN, narrativa cultural curada ES/EN, indicador de calor (hot/warm/low)
- `CURATED_MEMES` — 12 memes seed precargados de diferentes culturas con análisis narrativo
- Meme Global del Día con tarjeta hero, reach, virality score, sentiment y Signal Card narrativa
- Grid de países con indicadores de actividad (punto rojo/ámbar/verde)
- Panel de detalle por país con contexto cultural curado + botón "⚡ Generar con IA"
- `generateCountryMeme()` — análisis IA en tiempo real de la cultura memética de un país específico usando el cascade actual
- `analyzeCountryMemeDeep()` — navega al Analyzer con contexto del país pre-cargado
- Biblioteca con 4 filtros: Todo / Curados / Mis Análisis / Por País
- Buscador en tiempo real por título, narrativa, tipo de humor o país
- `addToLibrary()` — guarda automáticamente los análisis de países generados con IA
- `renderLibrary()` — grid visual de tarjetas con thumbnail, flag, decision badge
- `openLibCard()` — abre carta de biblioteca, navega al historial o al analyzer según tipo
- `handleLibUpload()` — upload directo a biblioteca que navega al Analyzer
- Zona de upload en biblioteca con auto-análisis al seleccionar archivo
- `localStorage.ml_library` — persistencia de biblioteca (hasta 200 entradas)
- `updateWorldDate()` — badge de fecha actualizado al abrir la página
- `updateWorldStrings()` — actualización de todos los strings del módulo en cambio de idioma
- Bottom nav: reemplaza "Atlas" con "🌐 Mundo" (Atlas sigue accesible en sidebar desktop)
- CSS completo: `.world-hero`, `.world-map-grid`, `.world-country-card`, `.lib-grid`, `.lib-card`, `.lib-upload-zone`, `.world-country-detail`, `.country-chip`
- i18n: 12 nuevas claves ES/EN para todo el módulo
- `showPage('world')` integrado: llama a `loadLibrary()` e `initWorldPage()` en primera visita
- `renderStaticUI()` actualizado para llamar a `updateWorldStrings()`
- `DOMContentLoaded` actualizado para llamar a `loadLibrary()` en el arranque

### fix
- Strings ES del módulo Mundo no se insertaban en el primer patch — corregido con match del bloque correcto

---

## [7.0] — 2026-06-XX — Signal Layer · Narrativa Humana

### feat
- Nueva **Signal Card** — tarjeta de narrativa humana que aparece al tope de cada resultado del Analyzer
- Campo `signal` en el JSON de respuesta del sistema: `headline`, `body`, `invisible_forces`, `so_what_journalist`, `so_what_analyst`, `so_what_public`, `deeper_context`
- Sistema prompt actualizado para generar simultáneamente el análisis técnico y la narrativa accesible
- `renderSignalCard()` — renderiza la Signal Card completa con todos sus componentes
- `renderSignalFromSummary()` — fallback cuando el modelo no devuelve el campo `signal`
- `detectForceType()` — clasifica automáticamente las fuerzas invisibles por tipo (económica/social/emocional/política/cultural) para asignar el color del chip
- `formatSignalBody()` — convierte marcado `**texto**` en negritas HTML
- `toggleSignalDetail()` — expand/collapse del contexto histórico profundo
- `toggleImpl()` — expand/collapse de la sección "¿Qué significa esto?"
- Force chips con 5 colores: económico (ámbar), social (morado), emocional (cyan), político (rojo), cultural (verde)
- 3 perspectivas en "¿Qué significa esto?": periodista/creador 📰, analista 🔬, persona curiosa 👁
- **Narrative Feed** en el Command Center — reemplaza la tabla técnica como vista por defecto
- `renderNarrativeFeed()` — muestra los últimos 4 análisis en lenguaje humano con Force chips
- `toggleNfeed()` — expand/collapse de contexto profundo en cada card del feed
- La tabla técnica ahora está oculta por defecto detrás del botón "▾ VER DATOS TÉCNICOS"
- `toggleTechTable()` — muestra/oculta la tabla con etiqueta dinámica
- i18n: ~20 nuevas claves ES/EN para todo el Signal Layer
- CSS completo: `.signal-card`, `.signal-eyebrow`, `.signal-pulse`, `.signal-headline`, `.signal-body`, `.signal-expand-btn`, `.signal-detail`, `.invisible-forces`, `.force-chip`, `.signal-implications`, `.impl-header`, `.impl-body`, `.impl-persona`, `.nfeed-item`, `.nfeed-headline`, `.nfeed-body`, `.nfeed-meta`, `.nfeed-expand`
- `updateCommandFromHistory()` actualizado para llamar a `renderNarrativeFeed()`

### fix
- `killBannerText`: se añadió `<span id="killBannerText">` dentro del banner de kill switch (antes era texto hardcodeado, no se actualizaba con cambio de idioma)
- 21 IDs faltantes en HTML añadidos: `alertCoordTitle`, `alertSentTitle`, `azTitle`, `cnode_trigger_type`, `cnode_trigger_val` y sus pares, `riskScoringTitle`, `riskSupplyTitle`
- Llamadas `setTextById()` a elementos dinámicos removidas (`causTitle`, `scenTitle`, etc. — ya son renderizados por sus funciones respectivas que usan `t()`)
- Acceso `lastChild.textContent` en labels de proveedores refactorizado a búsqueda de nodos de texto segura

---

## [6.0] — 2026-06-XX — Fix Crítico: STRINGS Reconstruido

### fix ⚠️ CRÍTICO
- **`ReferenceError: STRINGS is not defined`** — el objeto completo `const STRINGS = {}` fue eliminado silenciosamente durante patches encadenados con `str.replace()` en sesiones anteriores. La app crasheaba completamente al cargar.
- Objeto STRINGS reconstruido desde cero con ~260 claves en ES y EN, incluyendo todas las claves dinámicas de los módulos v4-v5 que no estaban en el bloque original de v5
- Validación con `node --check` aplicada después de cada operación de patch para detectar errores tempranamente
- Error de sintaxis en línea 569: fragmento sobrante de función antigua removido

### docs
- Protocolo establecido: siempre validar JS con `node --check` antes de entregar cualquier versión

---

## [5.0] — 2026-05-XX — Cascade Waterfall Real

### feat
- **Cascade de 4 proveedores completamente reescrito** como waterfall real: antes solo intentaba el primer proveedor disponible. Ahora itera en orden (Anthropic → Gemini → Grok → OpenAI), captura silenciosamente errores de quota/rate-limit, y prueba el siguiente automáticamente
- `cascadeApiCall()` refactorizado con array de proveedores y lógica de filtrado + iteración secuencial
- El loader muestra el proveedor actual ("Conectando con Gemini...")  y mensajes de fallback ("Anthropic no disponible — intentando siguiente...")
- Distinción entre errores de auth (detienen el cascade) y errores de quota/rate-limit (activan el fallback)
- Modelos actualizados: `grok-beta` (xAI), `gemini-1.5-flash` (Google), `gpt-4o` (OpenAI)
- Errores inline — eliminados todos los `alert()` del navegador, reemplazados por `showInlineError()`
- `showInlineError()` — muestra errores dentro de la UI con botón de cerrar
- Anti-prompt injection: función `sanitize()` aplicada a todos los inputs de texto antes de enviar al modelo

### fix
- Provider labels en el drawer de APIs ahora muestran el nombre correcto del proveedor activo
- Keys de tipo incorrecto rechazadas antes de llamar a la API

---

## [4.0] — 2026-05-XX — i18n Completo + Dark/Light Theme

### feat
- **i18n ES/EN al 100%**: objeto `const STRINGS = { es:{}, en:{} }` con ~180 claves
- Función `t(key)` con fallback: `STRINGS[currentLang]?.[key] || STRINGS['es'][key] || key`
- `applyLang(lang)` — actualiza todos los textos visibles de la interfaz en caliente sin recargar
- `renderStaticUI()` — función centralizada que llama a `setTextById()` para todos los elementos estáticos
- `setTextById(id, key)` — wrapper null-safe para `el.textContent = t(key)`
- Switch de idioma en sidebar (desktop) y barra superior (móvil) sin recargar la página
- **Dark/Light Theme completo**: variables CSS en `:root` (dark por defecto) y `:root[data-theme="light"]`
- `applyTheme(theme)` — aplica el tema vía `data-theme` en `:root`
- Preferencias de idioma y tema persistidas en `localStorage`
- Todos los módulos dinámicos (renderAtlas, renderCausality, renderScenParams, renderRisk) usan `t()` internamente

### fix
- Textos hardcodeados en módulos dinámicos reemplazados por llamadas a `t()`

---

## [3.0] — 2026-05-XX — Mobile First + Cascade de 4 APIs

### feat
- **Diseño mobile-first completo**: bottom navigation de 5 módulos para móvil
- `.bottom-nav` con 5 ítems: Centro / Analyzer / Historial / Atlas / Risk
- `.mob-topbar` — barra compacta con logo, toggles de tema/idioma y botón de APIs
- `.key-drawer` — panel deslizante desde la derecha para configurar las 4 API keys en móvil
- `setBottomActive()` — sincroniza el estado activo del bottom nav con la página visible
- Responsive desde 320px con grid colapsable y tipografía adaptada
- Cascade inicial de 4 proveedores (versión básica, perfeccionada en v5)
- Onboarding screen con inputs de API key y opción de modo demo
- `startSystem()` — oculta onboarding y muestra la app
- `loadKeys()` / `saveKeys()` — persistencia de API keys en localStorage

### fix
- Layout del sidebar desktop no colapsaba correctamente en pantallas intermedias (641-900px)

---

## [2.0] — 2026-04-XX — IA Real + Historial + Chat

### feat
- **Analyzer con IA real**: primera integración con Anthropic Claude Sonnet
- `runAnalysis()` — orquesta el análisis completo (imagen o texto)
- `buildPrompt(mode)` — prompt institucional con 10 capas de análisis y schema JSON
- `buildContent(imageB64)` — construye el mensaje multipart para imágenes
- `renderResult()` — renderiza el resultado completo del análisis en la UI
- Modos Quick Scan (~5s) y Deep Analysis (con web search via Anthropic)
- Historial persistente: `localStorage.ml_hist_v2` (50 entradas máximo)
- `renderHistory()` — lista de análisis con miniaturas y metadata
- `loadEntry(id)` — recarga un análisis del historial en el Analyzer
- `clearHistory()` — borra el historial con confirmación
- Chat de seguimiento post-análisis: `sendChat()` con historial conversacional completo
- Export JSON: `doExportJSON()` — descarga el análisis como archivo `.json`
- Export Markdown: `doExportMD()` — descarga el análisis como reporte `.md`
- `addLiveAlert()` — añade alerta al feed del Command Center tras cada análisis
- `updateCommandFromHistory()` — actualiza métricas del dashboard con datos reales
- `updateHistoryBadge()` — contador de análisis en el nav item del historial
- Anti-regresión: función `handleFile()` con soporte drag & drop + file input

---

## [1.0] — 2026-04-XX — Prototipo Base

### feat
- Single-file HTML+CSS+JS inicial (~80KB)
- 6 módulos con datos demo estáticos: Command Center, Meme Analyzer, Analysis History, Meme Atlas, Causality Engine, Scenario Lab + Risk Engine
- Arquitectura CSS con variables `:root` para theming futuro
- Navegación por sidebar (desktop) funcional
- Chart.js 4.4.1 vía CDN para las gráficas del Command Center
- Layout responsive base (sin mobile-first completo)
- Placeholder de upload de imagen sin funcionalidad IA
- Schema JSON del análisis definido (10 capas)
- Framework epistémico de 7 principios implementado en el prompt base

---

## VERSIONES PENDIENTES / ROADMAP

### [10.0] — Planeado
- [ ] Modo batch: analizar múltiples memes en paralelo
- [ ] Comparación side-by-side de dos memes
- [ ] Soporte de URLs de TikTok/YouTube vía Cloudflare Worker proxy
- [ ] Backend mínimo para sincronización multi-dispositivo (Cloudflare D1)
- [ ] Multi-usuario con historial compartido

### [11.0] — Considerado
- [ ] Detección de audio coordinado (mismo audio en múltiples videos)
- [ ] Timeline de evolución de un meme (serie temporal de análisis)
- [ ] Integración con APIs de social listening
- [ ] Export a PDF (reporte institucional)
- [ ] Modo offline completo con service worker

---

*CHANGELOG · Memelogía OS · A51 / cuakzilla · 2026*
