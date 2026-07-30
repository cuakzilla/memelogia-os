# MANUAL DE USUARIO — MEMELOGÍA OS v9.0
### Guía completa para sacarle el máximo provecho al sistema

---

## ÍNDICE

1. [Qué es Memelogía OS](#qué-es)
2. [Primeros pasos — Configuración de APIs](#primeros-pasos)
3. [Módulo: Command Center](#command-center)
4. [Módulo: Meme Analyzer (Imagen + Texto)](#meme-analyzer)
5. [Módulo: Audio y Video](#audio-y-video)
6. [Módulo: Analysis History](#historial)
7. [Módulo: Mundo · Biblioteca](#mundo-y-biblioteca)
8. [Módulo: Meme Atlas](#meme-atlas)
9. [Módulo: Causality Engine](#causality-engine)
10. [Módulo: Scenario Lab](#scenario-lab)
11. [Módulo: Risk Engine](#risk-engine)
12. [Cómo leer una Signal Card](#signal-card)
13. [Switches de Tema e Idioma](#tema-e-idioma)
14. [Exportar tus análisis](#exportar)
15. [Preguntas frecuentes](#faq)

---

## 1. Qué es Memelogía OS {#qué-es}

Memelogía OS es un **sistema de inteligencia cultural** que convierte memes, audios virales y videos de TikTok/Reels en inteligencia real — explicada en lenguaje que cualquier persona entiende.

**No es** una app para "explicar memes" de forma superficial.

**Sí es** un sistema que te dice:
- Qué significa un meme en 4 capas simultáneas de lectura
- Qué fuerza invisible (económica, social, emocional, política) lo está empujando
- Qué riesgo representa en 6 dimensiones
- Cómo va a evolucionar en 4 escenarios posibles
- Qué está haciendo el mismo meme en 17 países del mundo

---

## 2. Primeros Pasos — Configuración de APIs {#primeros-pasos}

Al abrir la app por primera vez verás el **onboarding**. Tienes dos opciones:

### Opción A: Con API Key (recomendada)
Ingresa tu clave en el campo del onboarding. El sistema detecta automáticamente qué tipo de clave es.

### Opción B: Modo Demo
Sin API key, puedes explorar todos los módulos con datos demo. El Analyzer no funcionará, pero puedes ver cómo luce la interfaz completa.

### Configurar múltiples APIs (cascada)
En cualquier momento, toca el botón **"APIs"** (móvil) o busca el campo en el sidebar (desktop) para configurar hasta 4 proveedores:

| Proveedor | Clave empieza con | Capacidades |
|---|---|---|
| 🥇 Anthropic Claude | `sk-ant-` | Análisis texto+imagen + Web Search en tiempo real |
| 🥈 Google Gemini | `AIza` | Audio y Video nativo |
| 🥉 xAI Grok | `xai-` | Análisis texto+imagen |
| 4️⃣ OpenAI GPT-4o | `sk-` | Análisis texto+imagen |

El sistema usa el **primer proveedor disponible en orden**. Si uno falla por límite de uso, salta automáticamente al siguiente sin que tengas que hacer nada.

> **Importante:** Para analizar audio y video necesitas la clave de Google Gemini (`AIza...`). Es la única que soporta estos formatos nativamente.

---

## 3. Command Center {#command-center}

El dashboard principal. Lo primero que ves al abrir la app.

### Lo que verás en tiempo real:
- **Narrativas Activas:** cuántas narrativas culturales están siendo rastreadas
- **Volatilidad Memética:** qué tan agitado está el ecosistema cultural (0-100)
- **Análisis Realizados:** cuántos análisis has hecho en total (dato real tuyo)
- **Risk Score Medio:** promedio de riesgo de todos tus análisis

### "Lo que está pasando realmente"
Esta sección muestra tus últimos análisis en lenguaje humano, con sus fuerzas invisibles y opción de expandir para ver el contexto completo. Toca cualquier tarjeta para profundizar.

### Ver Datos Técnicos
El botón "▾ VER DATOS TÉCNICOS" muestra la tabla detallada con momentum, tipo y estado de cada narrativa. Por defecto está oculta para priorizar la narrativa accesible.

### Gráficas
- **Volatilidad 24h:** tendencia de actividad del día
- **Tipos de Humor:** distribución de los tipos de humor que has analizado
- **Risk por Plataforma:** qué plataformas concentran más riesgo

---

## 4. Meme Analyzer — Imagen y Texto {#meme-analyzer}

El corazón del sistema.

### Cómo analizar una imagen

1. Toca el tab **◎ Meme Analyzer** en la navegación
2. Elige el modo:
   - **⚡ Quick Scan** — resultado en ~5 segundos. Análisis esencial
   - **◈ Deep Analysis** — ~15-30 segundos. Usa web search para contexto real actual
3. Arrastra tu imagen a la zona de upload, o toca para seleccionarla
4. El análisis comienza automáticamente

### Cómo analizar con texto

Si no tienes la imagen pero conoces el meme, descríbelo en el campo de texto:
> *"Hombre arrodillado frente a dos botones, uno dice 'pagar el alquiler' y el otro 'comprarse algo que no necesita'. El hombre suda nerviosamente."*

Toca **Analizar →** y el sistema lo procesa como si tuvieras la imagen.

> **Tip:** Cuantos más detalles des (plataforma, comunidad, contexto), mejor el análisis.

### Entendiendo el resultado

**Signal Card (arriba del todo):**
El resumen en lenguaje humano. Es lo primero que debes leer. Tiene:
- Titular periodístico — la esencia en ≤12 palabras
- Cuerpo narrativo — qué está pasando y por qué importa
- Fuerzas Invisibles — los chips de colores que nombran las fuerzas detrás del meme
- "Ver Más" — contexto histórico y cultural profundo
- "Qué significa esto" — una oración para cada perfil: periodista, analista, persona curiosa

**Datos técnicos (debajo):**
- Tags de clasificación: tipo de humor, narrativa, vector emocional
- Confidence Scores: qué tan seguro está el sistema de cada parte del análisis
- Risk Dimensions: 6 dimensiones de riesgo del 0 al 100
- Interpretaciones múltiples: literal, irónica, meta-irónica, community-specific
- Cadena causal: el paso a paso de por qué este meme existe
- Decision Recommendation: SAFE / MONITOR / INVESTIGATE / ESCALATE / CRITICAL
- Self-Audit: el sistema critica sus propias conclusiones

### Chat de seguimiento

Después de cada análisis aparece un chat. Puedes preguntar:
- "¿Qué comunidades comparten este meme?"
- "¿Es contenido coordinado o espontáneo?"
- "¿Cómo evolucionará en los próximos días?"
- "¿Qué pasaría si una marca lo usa?"

---

## 5. Audio y Video {#audio-y-video}

El tab **🎵 Audio · Video** en el Analyzer amplía el análisis a contenido audiovisual.

> **Requisito:** necesitas la clave de **Google Gemini** (`AIza...`) configurada. Es el único proveedor que procesa audio y video nativamente.

### Analizar audio

1. Selecciona el tab 🎵 Audio · Video
2. Arrastra o sube tu archivo en la zona de audio
3. Formatos: MP3, WAV, OGG, M4A, WebM — máximo 20MB
4. El sistema detecta letra/diálogos, tono, ritmo, referencias culturales, contexto memético del sonido

### Analizar video

1. Sube tu video (MP4, WebM, MOV, AVI — máximo 20MB)
2. El sistema extrae automáticamente 6 frames clave del video
3. Verás la tira de frames — puedes seleccionar los más relevantes
4. Gemini analiza el video completo: contenido visual + audio + texto en pantalla + música + efectos

### Grabar audio en vivo

Perfecto para analizar audio de TikToks, Reels o videos que estás viendo:
1. Toca **🎤 Grabar audio en vivo**
2. Acepta el permiso de micrófono
3. Reproduce el audio/video que quieres analizar cerca del micrófono
4. Toca **⏹ Detener grabación** cuando termines (máximo 2 minutos)
5. El audio grabado se envía a Gemini para análisis

### Campo de contexto adicional

En cualquier análisis de media, el campo de texto debajo te permite dar información adicional: plataforma de origen, idioma si no es obvio, comunidad específica. Esto mejora significativamente la calidad del análisis.

---

## 6. Analysis History {#historial}

Todos tus análisis guardados automáticamente.

### Acceso
Tab **◷** en la navegación → "Analysis History" / "Historial de Análisis"

### Lo que guarda
- Imagen/descripción del meme analizado
- Resultado completo del análisis
- Fecha y hora
- Modo usado (Quick/Deep/Media)
- Decision final (SAFE/MONITOR/etc.)

### Cómo usar
- **Tap en una entrada:** carga ese análisis en el Analyzer para revisarlo
- **⬇ Export JSON:** descarga todo el historial como archivo JSON (para uso programático o respaldo)
- **✕ Clear:** borra todo el historial (confirmación requerida)

> El historial guarda hasta **50 análisis**. Los más antiguos se eliminan automáticamente cuando superas ese límite.

---

## 7. Mundo · Biblioteca {#mundo-y-biblioteca}

### Meme Global del Día
Arriba de la página, la tarjeta del meme dominante a nivel mundial con su Signal Card narrativa y los países donde más está trending.

### Meme del Día por País
Grid de 17 países con sus tendencias curadas:
- **Punto verde** = actividad normal
- **Punto ámbar** = tendencia activa
- **Punto rojo** = alta volatilidad

**Para ver el detalle de un país:**
1. Toca la tarjeta del país
2. Se abre el panel de detalle con contexto cultural curado
3. Toca **⚡ Generar con IA** para análisis profundo en tiempo real
4. El resultado se guarda automáticamente en tu Biblioteca

**Para ir directo al Analyzer:** toca "◎ Análisis Profundo" en el panel de detalle.

### Biblioteca Memética

Colección de memes con 4 filtros:
- **Todo:** todos los memes disponibles
- **Curados:** 12 memes seed seleccionados de diferentes culturas (siempre disponibles, no requieren IA)
- **Mis Análisis:** tu historial real del Analyzer
- **Por País:** memes generados con IA del módulo de países

**Búsqueda:** el campo de búsqueda filtra en tiempo real por título, narrativa, tipo de humor o país.

**Upload directo:** la zona de upload en la parte baja te lleva al Analyzer con auto-análisis.

---

## 8. Meme Atlas {#meme-atlas}

Mapa visual del ecosistema cultural activo.

### Los 6 clusters
Cada bola representa un cluster temático. El número es su nivel de "energía" actual (0-100):
- 🔴 **POLÍTICO** — narrativas sobre poder e instituciones
- 🟡 **ECONÓMICO** — ansiedad financiera, trabajo, consumo
- 🟣 **IDENTIDAD** — pertenencia tribal, generaciones, culturas
- 🔵 **TECH/IA** — tecnofobia, hype, backlash digital
- 🟢 **NOSTALGIA** — idealización del pasado, escapismo
- 🟣 **CRINGE** — vergüenza social como arma, exclusión

**Toca un cluster** para ver más detalles sobre su nivel de actividad.

### Templates más Mutados
Los memes base que están generando más variaciones activas — indicador de qué plantillas están siendo apropiadas y resignificadas.

### Flujos de Migración
De qué plataformas a cuáles está migrando el contenido. Indica hacia dónde se moverán las narrativas próximamente.

---

## 9. Causality Engine {#causality-engine}

Responde la pregunta más importante: **¿por qué está pasando esto?**

### La cadena causal principal
Visualización horizontal del recorrido de una narrativa:
```
Trigger → Emoción → Mecanismo de Humor → Tipo de Meme → Narrativa → Riesgo
```

### Cadenas causales activas
Las 4 narrativas más activas con su nivel de confianza y clasificación de riesgo.

### Mapa de relaciones
Diagrama SVG que muestra cómo se conectan los nodos causales.

### Base de evidencia
Las fuentes que respaldan cada análisis causal, con su nivel de confianza (HIGH / MODERATE / LOW).

---

## 10. Scenario Lab {#scenario-lab}

Simulador de futuros posibles.

### Los 4 parámetros (ajusta con sliders)

| Parámetro | Qué controla |
|---|---|
| Virality Multiplier | Factor de amplificación orgánica del contenido |
| Coordinated Amplification | Probabilidad de que haya coordinación artificial detrás |
| Sentiment Negativity | Qué tan negativa es la carga emocional del contenido |
| Cross-Platform Spread | Con qué velocidad migra entre plataformas |

### Los 4 escenarios

- **CASO BASE (45%):** el estado actual se mantiene
- **OPTIMISTA (20%):** dilución natural — el meme pierde fuerza sin consecuencias
- **CASO ESTRÉS (25%):** escalada hacia narrativa tóxica o desinformación activa
- **ADVERSARIAL (10%):** manipulación coordinada activa — flood sintético

### Decision Output
Calcula automáticamente la recomendación de acción basada en los parámetros:
- **SAFE** (0-35 puntos): monitoreo básico
- **MONITOR** (35-55): seguimiento activo
- **ESCALATE** (55-75): acción recomendada
- **CRITICAL** (75+): intervención urgente

---

## 11. Risk Engine {#risk-engine}

Sistema de scoring de riesgo multidimensional.

### Las 6 dimensiones

| Dimensión | Qué mide |
|---|---|
| Reputacional | Riesgo para la imagen pública de una persona u organización |
| Político | Carga política o potencial de polarización |
| Extremismo | Señales de radicalización o contenido extremo |
| Desinformación | Potencial de difundir información falsa |
| Acoso | Riesgo de uso para targeting o acoso de personas |
| Manipulación | Señales de coordinación artificial o bot activity |

**Escala:** 0-100 donde 0-45 = LOW, 46-70 = MEDIUM, 71-100 = HIGH

### Kill Switches
6 interruptores de seguridad que se activan automáticamente ante señales críticas. Cuando alguno está en ACTIVE, se muestra la alerta roja en la parte superior.

### Supply Chain Security Score
Indicador de la salud del sistema: dependencias actualizadas, artefactos firmados, sin vulnerabilidades críticas.

---

## 12. Cómo Leer una Signal Card {#signal-card}

La Signal Card es la capa de traducción del análisis técnico al lenguaje humano. Aparece en cada análisis del Analyzer.

```
┌────────────────────────────────────────────┐
│ ◉ SEÑAL DETECTADA                          │  ← Eyebrow: tipo de señal
│                                            │
│ TITULAR PERIODÍSTICO EN ≤12 PALABRAS       │  ← Headline: la esencia
│                                            │
│ Cuerpo narrativo: 2-3 oraciones que        │  ← Body: qué pasa y por qué
│ explican qué está pasando en lenguaje      │
│ cotidiano que cualquier persona entiende.  │
│                                            │
│ FUERZAS INVISIBLES                         │
│ [ansiedad laboral] [desconfianza inst.]    │  ← Force chips por color
│ [nihilismo generacional]                   │
│                                            │
│ ▾ VER MÁS                                  │  ← Expande contexto histórico
│                                            │
│ QUÉ SIGNIFICA ESTO ▾                       │
│  📰 PERIODISTA: historia aquí para cubrir  │  ← 3 perspectivas según perfil
│  🔬 ANALISTA: patrón a investigar          │
│  👁 PERSONA CURIOSA: por qué te importa   │
└────────────────────────────────────────────┘
```

**Colores de los Force Chips:**
- 🔵 Azul = fuerza económica
- 🟣 Morado = fuerza social
- 🔵 Cyan = fuerza emocional
- 🔴 Rojo = fuerza política
- 🟢 Verde = fuerza cultural

---

## 13. Switches de Tema e Idioma {#tema-e-idioma}

**En desktop:** en la parte inferior del sidebar izquierdo encontrarás dos toggles.

**En móvil:** en la barra compacta debajo del topbar (arriba de la pantalla).

### Tema Dark / Light
- **Dark (predeterminado):** fondo negro, acentos cyan — estética terminal/intelligence
- **Light:** fondo gris azulado claro, mismos acentos en tonos más oscuros

### Idioma ES / EN
Cambia **absolutamente todo** el texto de la interfaz en tiempo real: navegación, módulos dinámicos, mensajes de error, Signal Cards generadas, loader steps, chat, botones. El cambio es instantáneo sin recargar.

Ambas preferencias se guardan y persisten entre sesiones.

---

## 14. Exportar tus Análisis {#exportar}

### Exportar un análisis individual
Después de cualquier análisis, toca **⬇ Exportar ▾** para elegir:
- **JSON completo:** todos los datos estructurados, ideal para procesamiento posterior o bases de datos
- **Reporte Markdown:** documento legible formateado con título, clasificación, risk scoring, interpretaciones, cadena causal y notas de audit

### Exportar todo el historial
En la pestaña de Historial → botón **⬇ Export JSON** descarga todos tus análisis en un único archivo JSON.

---

## 15. Preguntas Frecuentes {#faq}

**¿Mis datos están seguros?**
Sí. Todo se guarda exclusivamente en tu navegador (localStorage). Nada se envía a ningún servidor nuestro. La única información que sale de tu dispositivo son las llamadas a las APIs de IA para procesar cada análisis.

**¿Qué pasa si cambio de dispositivo?**
El historial, la biblioteca y las API keys se guardan en el navegador de tu dispositivo actual. Si cambias de dispositivo, puedes exportar tu historial como JSON y guardarlo para referencia, pero no se sincroniza automáticamente.

**¿Cuánto me cuesta usar el sistema?**
El sistema en sí es gratuito. Pagas directamente a los proveedores de IA (Anthropic, Google, xAI u OpenAI) por el uso de sus APIs. Los costos típicos por análisis son de $0.001 a $0.01 USD dependiendo del proveedor y el modo.

**¿Funciona sin internet?**
Los módulos de navegación, historia, atlas, causality, scenario y risk funcionan sin internet (usan datos locales/demo). El Analyzer, el módulo de Mundo con generación IA, y el chat de seguimiento requieren conexión para llamar a las APIs.

**¿Puedo analizar contenido en cualquier idioma?**
Sí. El sistema analiza memes en cualquier idioma — el análisis se genera en el idioma de la interfaz que tengas configurado (ES o EN). Puedes especificar el idioma del contenido en el campo de contexto adicional para mejor precisión.

**¿Hay límite de análisis?**
No hay límite de análisis — solo el límite de tu API key de cada proveedor. El historial local guarda los últimos 50 análisis; los más antiguos se eliminan automáticamente.

---

*Manual de Usuario · Memelogía OS v9.0 · 2026*
