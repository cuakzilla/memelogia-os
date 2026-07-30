# SECURITY POLICY — MEMELOGÍA OS
## Política de Seguridad y Reporte de Vulnerabilidades

---

## Versiones Soportadas

| Versión | Soporte de seguridad |
|---|---|
| 9.x (actual) | ✅ Soporte completo |
| 8.x | ⚠️ Solo parches críticos |
| 7.x y anteriores | ❌ Sin soporte |

Recomendamos siempre usar la versión más reciente.

---

## Reportar una Vulnerabilidad

**NO reportes vulnerabilidades de seguridad en Issues públicos de GitHub.**

Para reportar una vulnerabilidad:

**Email:** seguridad@cuakzilla.com
**Asunto:** `[SECURITY] Descripción breve`
**Cifrado PGP:** [FINGERPRINT si aplica]

### Qué incluir en el reporte

```
1. Descripción de la vulnerabilidad
2. Pasos para reproducirla
3. Impacto potencial estimado
4. Versión afectada
5. Prueba de concepto (si tienes)
6. Tu nombre/alias para el crédito (opcional)
```

### Proceso de respuesta

| Paso | Plazo |
|---|---|
| Confirmación de recepción | 48 horas |
| Evaluación de severidad | 5 días hábiles |
| Parche para vulnerabilidades críticas | 7 días |
| Parche para vulnerabilidades altas | 15 días |
| Parche para vulnerabilidades medias/bajas | 30 días |
| Divulgación pública coordinada | Al publicar el parche |

---

## Arquitectura de Seguridad

### Modelo de amenazas

Memelogía OS es una aplicación single-file HTML sin backend propio.
El modelo de seguridad es deliberadamente minimalista:

```
SUPERFICIE DE ATAQUE:
┌──────────────────────────────────────────────────────┐
│  Browser del usuario (localStorage)                  │
│  ↕ HTTPS                                             │
│  Cloudflare Pages (hosting estático)                 │
│  ↕ HTTPS                                             │
│  APIs de IA (Anthropic / Google / xAI / OpenAI)      │
└──────────────────────────────────────────────────────┘

FUERA DEL MODELO:
- No hay servidor de aplicaciones
- No hay base de datos
- No hay autenticación de usuarios
- No hay sesiones server-side
```

### Controles de seguridad implementados

**Anti-prompt injection**
La función `sanitize()` filtra el input del usuario antes de enviarlo
al modelo de IA. Elimina patrones comunes de jailbreak y limita la longitud
máxima del input a [5000] caracteres.

**HTTPS forzado**
Cloudflare Pages sirve el contenido exclusivamente por HTTPS.
El archivo `_headers` incluye headers de seguridad:
```
X-Frame-Options: SAMEORIGIN
X-Content-Type-Options: nosniff
Referrer-Policy: strict-origin-when-cross-origin
```

**Almacenamiento de API Keys**
Las claves de API se almacenan en `localStorage` del navegador del usuario.
Nunca se transmiten a servidores de la agencia. Solo salen del dispositivo
en llamadas directas a las APIs de los proveedores correspondientes.

**Sin eval() ni innerHTML no sanitizado**
El código no usa `eval()`. Los únicos bloques de `innerHTML` son
para renderizar resultados ya procesados del modelo de IA, no inputs
directos del usuario.

**Validación de tipos MIME**
Los archivos de media (audio/video) son validados por tipo MIME y
tamaño (máximo 20MB) antes de ser procesados.

---

## Vulnerabilidades Conocidas y Aceptadas

### localStorage — Acceso desde herramientas de desarrollo
**Descripción:** Las API keys almacenadas en localStorage son accesibles
desde las herramientas de desarrollo del navegador.
**Impacto:** Un usuario con acceso físico al dispositivo o mediante
malware puede extraer las API keys.
**Mitigación:** Usar keys con límites de gasto configurados en el panel
de cada proveedor. Rotar las keys periódicamente.
**Estado:** Aceptado — inherente al diseño single-file sin backend.

### Dependencia de CDN (Chart.js)
**Descripción:** Chart.js se carga desde `cdn.jsdelivr.net`.
**Impacto:** Si el CDN fuera comprometido, podría inyectarse código
malicioso en la aplicación.
**Mitigación:** La versión está fijada (`chart.js@4.4.1`). Monitorear
alertas de seguridad de Chart.js.
**Estado:** Aceptado — riesgo bajo, beneficio alto (zero-build).

---

## Políticas de Divulgación

Seguimos **Responsible Disclosure coordinada**:

1. El reportador notifica privadamente
2. La agencia confirma, evalúa y desarrolla el parche
3. Se acuerda una fecha de divulgación pública
4. La agencia publica el parche y el advisory simultáneamente
5. El reportador recibe crédito si lo desea

---

## Hall of Fame

Agradecemos a quienes han contribuido a la seguridad del proyecto:

*[Sin reportes hasta la fecha]*

---

*SECURITY.md · Memelogía OS · A51 / cuakzilla · 2026*
