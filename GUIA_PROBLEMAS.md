# GUÍA DE PROBLEMAS COMUNES — MEMELOGÍA OS v9.0
### 15 problemas sistémicos con 2 soluciones alternativas cada uno

Categorías: 👤 Usuario · 🏢 Cliente · 🤝 Agencia/Aliados · ⚙️ Técnico · 📋 Legal/Documental

---

## PROBLEMA 1 — La app no carga o se queda en blanco
**Tipo:** 👤 Usuario · ⚙️ Técnico

**Causa más probable:** error de JavaScript que impide que la app arranque. Puede ocurrir por cache corrupta, versión antigua del browser, o un bug en el código.

**Solución A — Hard refresh**
Presiona `Ctrl+Shift+R` (Windows/Linux) o `Cmd+Shift+R` (Mac) para forzar recarga completa sin caché. En móvil: cierra completamente el browser y vuelve a abrirlo.

**Solución B — Revisar consola y limpiar storage**
Abre las herramientas de desarrollo (F12), ve a la pestaña "Console" y busca el error específico. Luego ve a "Application" → "Local Storage" → borra las entradas `ml_hist_v2`, `ml_api_keys`, `ml_lang`, `ml_theme`, `ml_library` y recarga. Esto resetea el estado sin perder el archivo.

---

## PROBLEMA 2 — "STRINGS is not defined" / App crashea con error de JS
**Tipo:** ⚙️ Técnico · 🤝 Agencia

**Causa más probable:** el objeto de internacionalización se perdió en una actualización del archivo. Es el bug más crítico documentado en el historial del proyecto.

**Solución A — Restaurar desde versión anterior**
Descarga la última versión estable del repo (`git log` para ver commits, `git checkout HASH -- index.html` para restaurar). El objeto `const STRINGS = {` debe existir en el JS.

**Solución B — Validar antes de deploy**
Antes de cualquier actualización de `index.html`, ejecutar: `node --check index.html` extrayendo el bloque JS entre `<script>` y `</script>`. Si falla, no hacer deploy. Guardar siempre una copia de respaldo fechada antes de modificar.

---

## PROBLEMA 3 — El Analyzer no responde / "Sin API Key configurada"
**Tipo:** 👤 Usuario

**Causa más probable:** la API key no está ingresada, está mal escrita, o no fue guardada correctamente.

**Solución A — Reconfigurar la key**
En móvil: toca el botón "APIs" en el topbar. En desktop: campo en el sidebar izquierdo. Asegúrate de pegar la key completa sin espacios al inicio o final. Verifica que el indicador de estado cambie a verde ("CONECTADO" o "Gemini active").

**Solución B — Verificar formato de la key**
Anthropic debe empezar con `sk-ant-`. Gemini con `AIza`. Grok con `xai-`. OpenAI con `sk-` (pero NO `sk-ant-`). Si tienes la key correcta pero el proveedor sigue sin detectarse, revisa que no haya caracteres adicionales o saltos de línea en el copiado.

---

## PROBLEMA 4 — Gemini da error de quota / El análisis de audio o video falla
**Tipo:** 👤 Usuario · 🏢 Cliente

**Causa más probable:** el tier gratuito de Gemini tiene límites de requests por minuto (RPM) y tokens por día. Es común en uso intensivo o en cuentas nuevas.

**Solución A — Esperar y reintentar**
El error incluye un tiempo de espera (`Please retry in X.Xs`). Espera ese tiempo y vuelve a intentar. Para uso continuo, espacia los análisis al menos 30 segundos.

**Solución B — Activar billing en Gemini / Agregar otra key**
Activa el billing en Google AI Studio para eliminar los límites del tier gratuito (los costos son mínimos). O agrega una segunda key de otro proveedor — el sistema hará fallback automático, aunque Anthropic/Grok/OpenAI no procesarán audio/video.

---

## PROBLEMA 5 — El switch de idioma no cambia todo el texto
**Tipo:** 👤 Usuario · 🤝 Agencia

**Causa más probable:** hay texto hardcodeado en algún módulo que no pasa por la función `t()`. Ocurre cuando se agrega código nuevo sin seguir el protocolo de internacionalización.

**Solución A — Reportar el texto específico**
Identificar exactamente qué texto no cambia y en qué módulo aparece. Compartir con el equipo técnico para agregar la clave faltante al objeto `STRINGS` y hacer que pase por `t()`.

**Solución B — Forzar re-render del módulo**
Navegar a otra página y volver. Algunos módulos solo actualizan su texto cuando se renderizan de nuevo. Si el texto cambia al volver a la página, es un problema de orden de ejecución corregible con un `updateWorldStrings()` o equivalente en el `renderStaticUI()`.

---

## PROBLEMA 6 — El video no se analiza correctamente / Los frames no se extraen
**Tipo:** 👤 Usuario · ⚙️ Técnico

**Causa más probable:** el video es demasiado corto (menos de 2 segundos), tiene un codec no soportado, o excede los 20MB de límite.

**Solución A — Comprimir el video antes de subir**
Usa [handbrake.fr](https://handbrake.fr) (gratuito) o comprime online en [cloudconvert.com](https://cloudconvert.com). Target: MP4 H.264, menos de 20MB, resolución máxima 1080p. Videos de TikTok/Reels ya suelen ser MP4 compatibles.

**Solución B — Usar grabación de micrófono como alternativa**
Si el video tiene componente de audio importante, reproduce el video cerca del micrófono del dispositivo y usa la función de grabación en vivo. Perderás el análisis visual pero obtendrás el análisis del audio con transcripción.

---

## PROBLEMA 7 — El historial se perdió / Los análisis no se guardan
**Tipo:** 👤 Usuario

**Causa más probable:** el browser limpió el localStorage (por modo incógnito, limpieza automática de datos, o cambio de dispositivo).

**Solución A — Activar preservación de datos en el browser**
En Chrome: Configuración → Privacidad → Cookies → asegúrate de que el sitio no está bloqueado para guardar datos. No usar modo incógnito para sesiones donde quieres guardar historial.

**Solución B — Exportar periódicamente**
Después de cada sesión importante, ve a History → "⬇ Export JSON" y guarda el archivo. Este JSON puede ser conservado indefinidamente y es la única forma de persistencia cross-dispositivo actual.

---

## PROBLEMA 8 — El cliente quiere que el sistema tenga sus propios colores/logo
**Tipo:** 🏢 Cliente · 🤝 Agencia

**Causa más probable:** necesidad de white-label o personalización de marca para presentaciones o uso interno del cliente.

**Solución A — Personalización básica (1-2 horas)**
Modificar las variables CSS en `:root`: `--accent`, `--accent2`, `--accent3` cambian los colores primarios. Cambiar el texto "Memelogía" en el HTML del sidebar y el logo en el onboarding. Cambiar "v3.0 — SISTEMA DE INTELIGENCIA MEMÉTICA" por el tagline del cliente. Costo de agencia: 1-2 horas de desarrollo.

**Solución B — Personalización completa + subdominio (4-8 horas)**
Personalización visual completa, logos, colores, tipografías del cliente. Deploy en subdominio propio del cliente (`inteligencia.empresa.com`). Requiere que el cliente tenga dominio propio y acceso a Cloudflare o similar. Incluir en el alcance del proyecto y cotizar por separado.

---

## PROBLEMA 9 — La API Key del cliente queda expuesta en el browser
**Tipo:** 🏢 Cliente · 📋 Legal · 🤝 Agencia

**Causa más probable:** las keys se guardan en localStorage y son visibles en las herramientas de desarrollo del navegador. Para uso personal es aceptable; para uso empresarial puede ser una preocupación de seguridad.

**Solución A — Rotación periódica de keys y scoping**
En Anthropic y OpenAI es posible crear keys con límites de gasto y scopes restringidos. Crear una key dedicada para Memelogía OS con un presupuesto máximo mensual. Si la key se compromete, el daño está acotado. Rotar mensualmente.

**Solución B — Backend proxy (proyecto fase 2)**
Implementar un Cloudflare Worker que actúe como proxy: el frontend llama al worker, el worker llama a la API con la key guardada como variable de entorno del worker (nunca expuesta al cliente). Costo adicional de implementación: 8-16 horas. Agregar al scope de la propuesta si el cliente tiene requerimientos de seguridad enterprise.

---

## PROBLEMA 10 — El cliente quiere análisis de más de 50 memes al día sistemáticamente
**Tipo:** 🏢 Cliente · 🤝 Agencia · ⚙️ Técnico

**Causa más probable:** el sistema actual está diseñado para uso personal/demo. Uso intensivo choca con: límite de 50 entradas en historial, sin modo batch, sin cola de procesamiento.

**Solución A — Modo batch manual + export frecuente**
Establecer un workflow donde el usuario analiza en sesiones de máximo 50 memes, exporta el JSON, y reinicia. Crear una plantilla de hoja de cálculo para consolida los JSONs exportados. Es manual pero funciona sin cambios técnicos.

**Solución B — Cotizar versión enterprise con backend**
Escalar el localStorage a IndexedDB (sin límite de tamaño), agregar modo batch (analizar lista de URLs o archivos simultáneamente), y backend de persistencia. Esto es un proyecto separado de 3-6 semanas. Incluir en propuesta con precio diferenciado de la demo personal.

---

## PROBLEMA 11 — Proceso de regularización y compliance para uso institucional
**Tipo:** 📋 Legal · 🏢 Cliente · 🤝 Agencia

**Causa más probable:** una institución (gobierno, empresa pública, universidad) necesita cumplir requisitos legales antes de usar herramientas de IA para análisis de contenido.

**Solución A — Documentar el flujo de datos y presentar DPA**
Preparar un documento de flujo de datos (Data Processing Agreement / DPA) que especifique: qué datos entran (imágenes/texto/audio), adónde van (API del proveedor elegido), qué retiene el sistema (localStorage del dispositivo, cero server-side). Adjuntar los términos de uso de Anthropic/Google/OpenAI relevantes. En la UE esto puede necesitar validación de un DPO.

**Solución B — Modo air-gapped con modelos locales**
Para instituciones con requerimientos de datos en territorio nacional o sin salida a internet: implementar la capa de IA con modelos locales (Ollama + Llama 3, Mistral o similar). El análisis será de menor calidad pero cumplirá con requerimientos de soberanía de datos. Requiere hardware adecuado del cliente. Cotizar como variante del proyecto.

---

## PROBLEMA 12 — Documentación legal para contrato agencia-cliente
**Tipo:** 📋 Legal · 🤝 Agencia

**Causa más probable:** el cliente quiere protección contractual sobre el código, los análisis generados, y la propiedad intelectual del sistema.

**Solución A — Contrato de licencia de software personalizado**
El cliente licencia el uso del sistema (no adquiere la propiedad). Incluir: alcance de uso (número de usuarios, proyectos, tiempo), restricciones (no redistribuir, no hacer ingeniería inversa), soporte incluido (horas de soporte/mes), y condiciones de renovación. No transferir el código fuente — entregar solo el `index.html` compilado.

**Solución B — Contrato de desarrollo a medida (obra por encargo)**
Si el cliente requiere propiedad del código y modificaciones: cotizar como desarrollo a medida con cesión de derechos patrimoniales. Precio significativamente mayor. Mantener la licencia de la arquitectura base y solo ceder las personalizaciones. Usar acuerdo de confidencialidad (NDA) antes de compartir código fuente.

---

## PROBLEMA 13 — El análisis produce resultados incorrectos o inconsistentes
**Tipo:** 👤 Usuario · 🏢 Cliente · 🤝 Agencia

**Causa más probable:** los LLMs tienen variabilidad inherente. Un mismo meme puede producir análisis ligeramente diferentes en ejecuciones distintas. Para contenido muy nuevo o muy de nicho, el modelo puede no tener contexto suficiente.

**Solución A — Usar modo Deep con web search**
El modo Deep activa búsqueda web en tiempo real (solo con Anthropic). Esto da al modelo contexto actualizado sobre el meme específico, reduciendo errores para contenido reciente. Para análisis institucionales importantes, siempre usar Deep.

**Solución B — Campo de contexto adicional + revisión humana**
Agregar contexto en el campo de texto: plataforma de origen, fecha aproximada de creación, comunidad específica, idioma. Esto reduce la variabilidad. Establecer como proceso que los análisis de riesgo ESCALATE o CRITICAL sean revisados por un humano antes de actuar sobre ellos — el sistema es herramienta de apoyo, no decisor final.

---

## PROBLEMA 14 — El cliente necesita que múltiples usuarios accedan al mismo sistema simultáneamente
**Tipo:** 🏢 Cliente · 🤝 Agencia · ⚙️ Técnico

**Causa más probable:** el sistema v9 es single-user por diseño (localStorage es por navegador). Un equipo de 5 personas no puede compartir historial, biblioteca o análisis.

**Solución A — Workflow de archivo compartido**
Cada usuario trabaja en su instancia local. Al final de cada jornada, exporta su historial como JSON y lo sube a una carpeta compartida (Google Drive, SharePoint). Un agregador designado consolida manualmente los JSONs. Sin cambios técnicos, funciona para equipos pequeños.

**Solución B — Versión multi-usuario (propuesta de fase 2)**
Agregar backend mínimo: Cloudflare Workers + D1 (base de datos SQLite en Cloudflare, gratuita hasta ciertos límites) para sincronización de historial y biblioteca entre usuarios. El frontend hace fetch al worker en vez de localStorage. Estimación: 2-4 semanas de desarrollo adicional. Cotizar como upgrade del proyecto.

---

## PROBLEMA 15 — Cuello de botella en onboarding del cliente: no sabe qué API key obtener
**Tipo:** 🏢 Cliente · 🤝 Agencia

**Causa más probable:** para clientes no técnicos, el proceso de crear una cuenta en un portal de desarrolladores, obtener una API key, entender el billing, y configurarla en la app es una barrera de entrada significativa que puede detener el proceso de venta o adopción.

**Solución A — Sesión de onboarding incluida en el proyecto**
Incluir una sesión de 30 minutos (videollamada o presencial) de "setup inicial" en la propuesta. En esa sesión: crear la cuenta del proveedor elegido, configurar el método de pago, obtener la key, y configurarla en el sistema junto con el cliente. Documentar el proceso con capturas de pantalla para que el cliente pueda repetirlo.

**Solución B — API Key de agencia con límite dedicado**
La agencia crea y paga la API Key, y la configura en el sistema del cliente bajo un límite de gasto mensual acordado (ej. $20/mes de Anthropic). El costo de las APIs se incluye en el fee mensual de soporte. Esto elimina completamente la fricción técnica del cliente. Requiere acuerdo de billing claro y monitoreo activo del consumo para no tener sorpresas.

---

## TABLA DE REFERENCIA RÁPIDA

| # | Problema | Urgencia | Quién lo resuelve |
|---|---|---|---|
| 1 | App no carga | 🔴 Alta | Usuario / Agencia |
| 2 | STRINGS crash | 🔴 Alta | Agencia (técnico) |
| 3 | Sin API Key | 🟡 Media | Usuario / Agencia |
| 4 | Quota Gemini | 🟡 Media | Usuario / Cliente |
| 5 | i18n incompleto | 🟢 Baja | Agencia (técnico) |
| 6 | Video no analiza | 🟡 Media | Usuario |
| 7 | Historial perdido | 🟡 Media | Usuario |
| 8 | White-label | 🟢 Baja | Agencia (dev) |
| 9 | Key expuesta | 🟡 Media | Agencia / Cliente |
| 10 | Uso masivo | 🟡 Media | Agencia (propuesta) |
| 11 | Compliance legal | 🔴 Alta | Agencia / Legal |
| 12 | Contrato | 🟡 Media | Agencia / Legal |
| 13 | Análisis incorrecto | 🟡 Media | Usuario / Agencia |
| 14 | Multi-usuario | 🟢 Baja | Agencia (fase 2) |
| 15 | Onboarding API | 🔴 Alta | Agencia |

---

*Guía de Problemas Comunes · Memelogía OS v9.0 · 2026*
