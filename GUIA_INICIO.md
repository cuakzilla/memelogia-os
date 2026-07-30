# GUÍA DE INICIO RÁPIDO — MEMELOGÍA OS v9.0
### De cero a tu primer análisis en menos de 10 minutos

---

## ANTES DE EMPEZAR — Checklist de 2 minutos

```
□ Tienes acceso a internet
□ Tienes al menos UNA de estas API Keys:
    □ Anthropic Claude  →  console.anthropic.com
    □ Google Gemini     →  aistudio.google.com
    □ xAI Grok          →  console.x.ai
    □ OpenAI GPT-4o     →  platform.openai.com
□ Tienes la URL del sistema (o el archivo index.html)
□ Opcional: tienes un meme listo para analizar
```

> Si no tienes ninguna API Key todavía, ve primero a la sección "Cómo obtener tu primera API Key" al final de esta guía.

---

## PASO 1 — Abrir el sistema (30 segundos)

**Opción A — URL en línea (recomendada)**
Abre en tu navegador: `https://cuakzilla.pages.dev` (o la URL que te compartieron)

**Opción B — Archivo local**
Descarga el archivo `index.html` y ábrelo directamente en Chrome, Safari o Firefox.
No necesitas instalar nada. No necesitas un servidor.

**Opción C — Desde el celular**
Comparte el archivo `index.html` a tu celular vía WhatsApp/AirDrop/Drive y ábrelo con Chrome.

---

## PASO 2 — Configurar tu API Key (1 minuto)

Al abrir el sistema por primera vez verás la pantalla de bienvenida:

```
┌─────────────────────────────────┐
│  Memelogía OS                   │
│  v3.0 — SISTEMA DE INTELIGENCIA │
│                                 │
│  1. API Key de Anthropic,       │
│     Gemini, Grok u OpenAI       │
│                                 │
│  2. Sube un meme o descríbelo   │
│                                 │
│  3. Historial persistente       │
│                                 │
│  [ sk-ant-...              ]    │
│                                 │
│  [ Iniciar Sistema →       ]    │
│                                 │
│  Continuar sin API Key (demo)   │
└─────────────────────────────────┘
```

1. Pega tu API Key en el campo (acepta cualquiera de los 4 proveedores)
2. Toca **Iniciar Sistema →**

Si no tienes API Key todavía, toca "Continuar sin API Key (modo demo)" — podrás explorar todos los módulos con datos de ejemplo.

---

## PASO 3 — Tu primer análisis (3 minutos)

### Ruta A — Analizar una imagen

1. Toca **◎ Analyzer** en la navegación (o el ícono ◎ en el bottom nav del celular)
2. Selecciona el modo **⚡ Quick Scan** (el más rápido para empezar)
3. Arrastra una imagen a la zona de upload, o toca para seleccionarla desde tu galería
4. Espera ~5 segundos
5. **¡Listo!** Verás el análisis completo

### Ruta B — Analizar con texto

1. Ve al **◎ Analyzer**
2. En el campo de texto escribe:
   > *"Persona viendo memes en el teléfono en vez de trabajar. La jefa llega. Cara de pánico."*
3. Toca **Analizar →**

### Ruta C — Analizar un audio o video

1. Ve al **◎ Analyzer**
2. Selecciona el tab **🎵 Audio · Video**
3. Sube tu archivo MP3/MP4 o graba con el micrófono
4. (Requiere clave de Google Gemini)

---

## PASO 4 — Entender tu primer resultado (2 minutos)

Después del análisis verás esto:

```
┌──────────────────────────────────────────┐
│ [tag humor] [tag narrativa] [DECISION]   │
├──────────────────────────────────────────┤
│ ◉ SEÑAL DETECTADA                        │
│                                          │
│ "TITULAR EN LENGUAJE COTIDIANO"          │
│                                          │
│ Narrativa accesible que explica qué      │
│ está pasando sin jerga técnica...        │
│                                          │
│ FUERZAS INVISIBLES                       │
│ [fuerza 1] [fuerza 2] [fuerza 3]        │
├──────────────────────────────────────────┤
│ Confidence Scores    │ Risk Dimensions   │
│ overall: 84%         │ reputacional: 45  │
│ template_id: 72%     │ político: 22      │
│ context: 91%         │ manipulación: 18  │
├──────────────────────────────────────────┤
│ INTERPRETACIONES MÚLTIPLES               │
│ Literal: ...                             │
│ Irónica: ...                             │
│ Meta-irónica: ...                        │
│ Community-specific: ...                  │
├──────────────────────────────────────────┤
│ CADENA CAUSAL                            │
│ Crisis → Emoción → Meme → Narrativa      │
├──────────────────────────────────────────┤
│ DECISION: MONITOR                        │
├──────────────────────────────────────────┤
│ SELF-AUDIT                               │
│ ⚠ Punto ciego 1...                      │
│ ⚠ Punto ciego 2...                      │
└──────────────────────────────────────────┘
```

**Lee primero la Signal Card** (el bloque de arriba con el titular). Es el resumen en lenguaje humano. Los datos técnicos están debajo para quien quiera profundizar.

---

## PASO 5 — Explorar el resto del sistema (opcional, 5 minutos)

| Si quieres... | Ve a... |
|---|---|
| Ver qué está pasando culturalmente hoy | ⬡ Command Center |
| Ver memes por país | 🌐 Mundo · Biblioteca |
| Recuperar un análisis anterior | ◷ History |
| Simular cómo puede evolucionar un meme | ◧ Scenario Lab |
| Entender las fuerzas detrás de una narrativa | ⟁ Causality Engine |
| Ver el mapa del ecosistema cultural | ◈ Meme Atlas |
| Ver el riesgo sistémico actual | ◬ Risk Engine |

---

## CÓMO OBTENER TU PRIMERA API KEY

### Anthropic (recomendada para empezar)

1. Ve a [console.anthropic.com](https://console.anthropic.com)
2. Crea una cuenta gratuita
3. Ve a "API Keys" → "Create Key"
4. Copia la clave (empieza con `sk-ant-`)
5. Anthropic da crédito inicial gratuito para empezar

**Costo estimado:** $0.003 por análisis Quick Scan · $0.008 por Deep Analysis

### Google Gemini (necesario para audio/video)

1. Ve a [aistudio.google.com](https://aistudio.google.com)
2. Inicia sesión con tu cuenta de Google
3. "Get API Key" → "Create API Key"
4. Copia la clave (empieza con `AIza`)
5. **Gemini tiene tier gratuito** con límites generosos

**Costo estimado:** $0.00 en tier gratuito para uso personal

### xAI Grok

1. Ve a [console.x.ai](https://console.x.ai)
2. Crea una cuenta
3. "API Keys" → crear nueva clave (empieza con `xai-`)

### OpenAI GPT-4o

1. Ve a [platform.openai.com](https://platform.openai.com)
2. "API Keys" → "+ Create new secret key"
3. Copia la clave (empieza con `sk-` pero NO `sk-ant-`)

---

## CONFIGURAR MÚLTIPLES KEYS (para máxima disponibilidad)

Si configuras las 4 keys, el sistema funciona sin interrupciones incluso cuando un proveedor tiene problemas:

**En desktop:** sidebar izquierdo → campo "Anthropic API Key" → para las otras keys toca el botón de ajustes

**En móvil:** botón **⚡ APIs** en el topbar → se abre un drawer con los 4 campos

El sistema detecta automáticamente qué tipo de clave es cada una y las ordena en cascada.

---

## ATAJOS ÚTILES

| Acción | Desktop | Móvil |
|---|---|---|
| Nuevo análisis | Click en ◎ sidebar | Tap ◎ bottom nav |
| Cambiar idioma | Toggle "LANG" sidebar | Toggle "LANG" barra superior |
| Cambiar tema | Toggle "THEME" sidebar | Toggle "THEME" barra superior |
| Ver historial | Click ◷ sidebar | Tap ◷ bottom nav |
| Configurar APIs | Campo sidebar | Botón "APIs" topbar |
| Exportar análisis | Botón "⬇ Exportar" en resultado | Mismo |

---

## CONSEJOS PARA MEJORES ANÁLISIS

**Para imágenes:**
- Usa imágenes con texto visible cuando sea relevante — el sistema hace OCR
- No necesitan ser de alta resolución — 800px es suficiente

**Para texto:**
- Describe el meme como si se lo contaras a alguien por teléfono
- Incluye el texto visible en la imagen entre comillas
- Menciona la plataforma si la sabes ("se comparte en TikTok de Colombia")

**Para audio:**
- Graba en un ambiente silencioso para mejor transcripción
- Si el audio es en otro idioma, menciónalo en el campo de contexto

**Para videos:**
- El sistema extrae 6 frames — funciona mejor con videos que tienen cambios visuales
- Para TikToks/Reels: graba la pantalla con el micrófono o descarga el archivo

**Modo Deep vs Quick:**
- Usa **Quick** para análisis rápidos cuando ya conoces el contexto del meme
- Usa **Deep** cuando el meme es nuevo, ambiguo, o quieres el contexto actual más reciente

---

## ¿ALGO NO FUNCIONA?

Consulta la **Guía de Problemas Comunes** (`GUIA_PROBLEMAS.md`) que acompaña este documento. Cubre los 15 problemas más frecuentes con 2 soluciones alternativas cada uno.

---

*Guía de Inicio Rápido · Memelogía OS v9.0 · 2026*
