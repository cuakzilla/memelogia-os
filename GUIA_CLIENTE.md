# GUÍA DE CLIENTE — MEMELOGÍA OS v9.0
### Onboarding · Costos · Embudo Comercial · Requisitos

---

## PARTE 1 — EMBUDO COMERCIAL COMPLETO

### Etapa 0 — Prospección y Calificación

**¿Para quién es Memelogía OS?**

| Perfil | Fit | Señal de compra |
|---|---|---|
| Agencia de comunicación / PR | ✅ Alto | "Nuestros clientes nos preguntan por el impacto de memes en su marca" |
| Medio de comunicación digital | ✅ Alto | "Necesitamos detectar tendencias antes que la competencia" |
| Departamento de marketing enterprise | ✅ Alto | "Tenemos una crisis de reputación online cada 3 meses" |
| Think tank / centro de investigación | ✅ Alto | "Analizamos cultura digital para reportes de política" |
| Gobierno / sector público | ✅ Medio | "Necesitamos monitorear narrativas sobre nuestras políticas" |
| Startup de contenido | ✅ Medio | "Queremos anticipar qué va a viralizarse" |
| Freelancer de social media | 🟡 Bajo | "Quiero entender mejor los memes para mis clientes" |
| Empresa sin presencia digital | ❌ No aplica | — |

**Preguntas de calificación:**
1. ¿Tienen equipo de comunicación, marketing o social media?
2. ¿Han tenido alguna vez un issue de reputación relacionado con contenido viral?
3. ¿Cuántas personas analizan tendencias digitales actualmente?
4. ¿Tienen presupuesto para herramientas de inteligencia digital?

---

### Etapa 1 — Demo (30-45 minutos)

**Estructura recomendada de la demo:**

```
00:00-05:00  Contexto — el problema que nadie está resolviendo bien
05:00-15:00  Demo en vivo — analizar UN meme relevante para el cliente
15:00-25:00  Mostrar módulos clave según perfil del cliente
25:00-35:00  Signal Card — mostrar la capa narrativa accesible
35:00-45:00  Preguntas + siguiente paso
```

**Memes recomendados para la demo según industria:**

| Industria del cliente | Meme recomendado para demo |
|---|---|
| Banca / Finanzas | "Doom spending" / "Broke but make it aesthetic" |
| Gobierno / Política | "Instituciones = incompetencia" / narrativas anti-institución |
| Retail / Consumer | "Quiet quitting" / memes de consumo culpable |
| Tech | "Anti-IA como identidad" / "Brain rot" gen Z |
| Salud | "Self-diagnosis TikTok" / "WebMD anxiety" |
| Educación | "Hell Joseon" / agotamiento de la meritocracia |

**Mensaje clave de la demo:**
> *"Lo que ves aquí no es una descripción del meme. Es inteligencia accionable: saber qué riesgo representa, por qué está pasando, y qué hacer al respecto — antes de que se convierta en un problema."*

---

### Etapa 2 — Propuesta Comercial

**Modelo de propuesta en 3 niveles:**

#### NIVEL 1 — Demo Personal / Piloto Individual
**Ideal para:** freelancers, analistas individuales, primeras pruebas

| Concepto | Detalle |
|---|---|
| Sistema | `index.html` + documentación completa |
| Deploy | Cloudflare Pages (el cliente gestiona) |
| APIs | El cliente obtiene y paga sus propias keys |
| Soporte | Sin soporte incluido |
| Personalización | Sin personalización |
| **Precio sugerido** | **$500-1,500 USD** (pago único) |

---

#### NIVEL 2 — Implementación Profesional
**Ideal para:** agencias, departamentos de marketing, medios digitales

| Concepto | Detalle |
|---|---|
| Sistema | `index.html` personalizado con marca del cliente |
| Deploy | Cloudflare Pages en dominio del cliente |
| APIs | Agencia configura keys con límites supervisados |
| Soporte | 3 horas/mes de soporte técnico incluidas |
| Personalización | Colores, logos, nombre del sistema |
| Capacitación | 2 sesiones de 1h para el equipo |
| Documentación | Manual + Guía de inicio personalizados |
| **Precio sugerido** | **$3,000-8,000 USD** (pago único) + **$300-500 USD/mes** soporte |

---

#### NIVEL 3 — Enterprise / Institucional
**Ideal para:** empresas medianas-grandes, instituciones públicas, medios nacionales

| Concepto | Detalle |
|---|---|
| Sistema | Versión enterprise con backend + multi-usuario |
| Deploy | Infraestructura dedicada del cliente |
| APIs | Proxy de agencia o integración con proveedor enterprise |
| Soporte | SLA con tiempo de respuesta garantizado |
| Personalización | Completa, incluyendo módulos adicionales a medida |
| Capacitación | Programa completo para equipo |
| Compliance | Documentación legal, DPA, acuerdo de confidencialidad |
| **Precio sugerido** | **$15,000-50,000 USD** (proyecto) + **$1,500-3,000 USD/mes** |

---

### Etapa 3 — Onboarding del Cliente

**Proceso de onboarding estándar (Nivel 2):**

```
DÍA 1 — Firma de contrato y NDA
   ↓
DÍA 2-3 — Setup técnico
   · Deploy del sistema en URL del cliente
   · Configuración de API Keys (sesión 30 min con cliente)
   · Prueba de análisis en vivo
   ↓
DÍA 4-5 — Capacitación
   · Sesión 1 (1h): Meme Analyzer + Signal Cards
   · Sesión 2 (1h): Command Center + Módulos de inteligencia
   ↓
DÍA 6-7 — Primeros análisis supervisados
   · Cliente hace sus primeros 5 análisis con apoyo
   · Revisión de resultados y ajuste de expectativas
   ↓
DÍA 8-10 — Entrega completa
   · Manual personalizado entregado
   · Acceso al canal de soporte configurado
   · Facturación activada
```

---

### Etapa 4 — Seguimiento y Retención

**Indicadores de éxito a medir con el cliente (30-60-90 días):**

| Indicador | Cómo medirlo |
|---|---|
| Adopción | Número de análisis realizados por semana |
| Valor generado | ¿Han evitado algún issue gracias al sistema? |
| Satisfacción | NPS mensual de 1 pregunta |
| Expansión | ¿Hay otros equipos que podrían usar el sistema? |

**Palancas de expansión:**
- "¿Quieren agregar análisis de audio y video?" (feature activa en v9)
- "¿Les interesa la versión multi-usuario para todo el departamento?"
- "¿Quieren integrar los análisis con su herramienta de reportes?"

---

## PARTE 2 — ESTRUCTURA DE COSTOS COMPLETA

### Costos del cliente para operar el sistema

#### Costos de infraestructura (mínimos)

| Concepto | Proveedor | Costo mensual |
|---|---|---|
| Hosting del sistema | Cloudflare Pages | **$0** (gratuito hasta 500 builds/mes) |
| Dominio personalizado | Cualquier registrador | **$1-2 USD/mes** |
| Cloudflare (plan Pro, opcional) | Cloudflare | **$20 USD/mes** (no necesario para empezar) |
| **Total infraestructura** | | **$0-22 USD/mes** |

#### Costos de APIs de IA (variable por uso)

**Anthropic Claude (análisis imagen/texto):**

| Uso estimado | Análisis/día | Costo mensual est. |
|---|---|---|
| Uso personal/ocasional | 1-5 | $1-10 USD |
| Uso profesional | 10-30 | $10-50 USD |
| Uso intensivo | 50-100 | $50-200 USD |
| Enterprise | 200+ | $200-800 USD |

*Claude Sonnet: ~$3 por millón tokens input · ~$15 por millón tokens output*

**Google Gemini (audio/video/fallback):**

| Tier | Límite | Costo |
|---|---|---|
| Gratuito | 1,500 req/día · 1M tokens/min | **$0** |
| Pay-as-you-go | Sin límite | ~$0.075 por 1M tokens |

> Para la mayoría de clientes, Gemini gratuito + Anthropic pay-as-you-go cubre el 95% de los casos de uso.

**Estimación realista por tipo de cliente:**

| Perfil | APIs/mes | Costo total estimado |
|---|---|---|
| Freelancer / uso ligero | 50-100 análisis | $5-20 USD |
| Agencia pequeña | 200-500 análisis | $20-80 USD |
| Empresa mediana | 500-2,000 análisis | $80-300 USD |
| Enterprise | 2,000+ análisis | $300-1,000 USD |

---

### Costos de la agencia para entregar el proyecto

#### Nivel 2 — Implementación Profesional

| Actividad | Horas est. | Tarifa | Subtotal |
|---|---|---|---|
| Personalización visual (colores/logo) | 3h | $80/h | $240 |
| Deploy y configuración Cloudflare | 2h | $80/h | $160 |
| Configuración API Keys del cliente | 1h | $80/h | $80 |
| Sesión capacitación × 2 | 2h | $100/h | $200 |
| Personalización manual y guía | 3h | $80/h | $240 |
| Soporte primer mes | 3h | $80/h | $240 |
| **Total costo de entrega** | **14h** | | **$1,160** |
| **Margen sugerido (60-70%)** | | | **$1,740-2,700** |
| **Precio al cliente** | | | **$3,000-4,000** |

#### Nivel 3 — Enterprise

| Actividad | Horas est. | Tarifa | Subtotal |
|---|---|---|---|
| Análisis de requerimientos | 8h | $120/h | $960 |
| Personalización completa | 20h | $100/h | $2,000 |
| Backend multi-usuario | 40h | $120/h | $4,800 |
| Integración con sistemas del cliente | 16h | $120/h | $1,920 |
| QA y testing | 12h | $100/h | $1,200 |
| Deploy y configuración | 8h | $100/h | $800 |
| Documentación legal (con abogado) | 4h | $150/h | $600 |
| Capacitación equipo | 8h | $100/h | $800 |
| **Total costo de entrega** | **116h** | | **$13,080** |
| **Margen sugerido (40-50%)** | | | **$8,720-13,080** |
| **Precio al cliente** | | | **$20,000-26,000** |

---

## PARTE 3 — REQUISITOS PREVIOS POR NIVEL

### Checklist Nivel 1 — Piloto Personal

**Del cliente:**
```
□ Dispositivo con navegador moderno (Chrome, Safari, Firefox)
□ Acceso a internet
□ Tarjeta de crédito para crear cuenta en al menos 1 proveedor de IA
□ 30 minutos para el onboarding inicial
```

**De la agencia:**
```
□ Archivo index.html v9+ validado
□ Documentación completa (manual + guía de inicio)
□ Instrucciones de configuración de API Keys
```

---

### Checklist Nivel 2 — Implementación Profesional

**Del cliente:**
```
□ Dominio propio (o disposición a usar .pages.dev)
□ Cuenta de Cloudflare (gratuita)
□ Presupuesto de APIs: mínimo $30/mes para empezar
□ 1 persona técnica de contacto para coordinación
□ 2-3 horas disponibles para capacitación del equipo
□ Firma de contrato de licencia y NDA
```

**De la agencia:**
```
□ Especificaciones de marca del cliente (colores hex, logos, tipografía)
□ Nombre personalizado para el sistema
□ Contrato de licencia de uso preparado
□ NDA firmado antes de compartir código
□ Estructura de soporte definida (canal, horarios, SLA)
□ Facturación configurada (inicial + mensual)
```

---

### Checklist Nivel 3 — Enterprise / Institucional

**Del cliente:**
```
□ Requerimientos documentados de seguridad y compliance
□ Contacto de IT / DevOps para coordinación técnica
□ Infraestructura propia o acuerdo de cloud (AWS/GCP/Azure)
□ DPO designado si aplica (GDPR/LGPD/regulación local)
□ Proceso interno de aprobación de herramientas de IA
□ Número de usuarios y casos de uso definidos
□ Presupuesto aprobado con firma de autorización
□ Firma de contrato enterprise + NDA + DPA
```

**De la agencia:**
```
□ Propuesta técnica detallada con arquitectura
□ Plan de proyecto con hitos y entregables
□ Equipo asignado (lead técnico + PM)
□ Asesoría legal para contrato enterprise
□ Plan de contingencia y rollback
□ Acuerdo de SLA definido (uptime, tiempo respuesta)
□ Plan de capacitación personalizado
□ Documentación de transferencia de conocimiento
```

---

## PARTE 4 — DOCUMENTACIÓN LEGAL MÍNIMA

### Documentos necesarios por nivel

| Documento | Nivel 1 | Nivel 2 | Nivel 3 |
|---|---|---|---|
| Contrato de licencia de software | Recomendado | ✅ Obligatorio | ✅ Obligatorio |
| NDA / Acuerdo de confidencialidad | Opcional | ✅ Obligatorio | ✅ Obligatorio |
| Términos de servicio | Recomendado | ✅ Obligatorio | ✅ Obligatorio |
| Data Processing Agreement (DPA) | No aplica | Recomendado | ✅ Obligatorio |
| Acuerdo de nivel de servicio (SLA) | No aplica | Recomendado | ✅ Obligatorio |
| Propuesta comercial firmada | Recomendado | ✅ Obligatorio | ✅ Obligatorio |
| Factura / Recibo | ✅ Siempre | ✅ Siempre | ✅ Siempre |

### Cláusulas mínimas para el contrato de licencia

1. **Alcance de uso:** número de usuarios, proyectos y tiempo de la licencia
2. **Restricciones:** prohibición de redistribución, sublicencia o ingeniería inversa
3. **Propiedad intelectual:** el código y la arquitectura permanecen propiedad de la agencia
4. **Responsabilidad limitada:** el sistema es herramienta de apoyo, no decisor final
5. **Uso de IA:** el cliente acepta los términos de uso de los proveedores de IA (Anthropic, Google, etc.)
6. **Datos y privacidad:** el sistema no almacena datos del cliente en servidores de la agencia
7. **Soporte:** alcance exacto del soporte incluido y costos de soporte adicional
8. **Rescisión:** condiciones para terminar el contrato
9. **Ley aplicable:** jurisdicción y legislación que rige el contrato

### Consideraciones de cumplimiento regulatorio

**México (LFPDPPP):**
- Los datos personales que aparezcan en imágenes/videos deben manejarse con consentimiento
- El cliente es responsable de obtener consentimientos para el contenido que analice
- La agencia debe tener aviso de privacidad propio

**Unión Europea (GDPR / EU AI Act):**
- EU AI Act clasifica sistemas de análisis cultural como "riesgo limitado" — requiere transparencia
- Si el contenido analizado incluye datos de personas identificables, aplica GDPR
- Recomendable nombrar un representante EU si la agencia no tiene presencia física

**Estados Unidos:**
- No hay regulación federal única — verificar regulaciones estatales aplicables
- Para sector financiero o salud: regulaciones sectoriales adicionales (SEC, HIPAA)

**Nota de la agencia:** *siempre consultar con un abogado local antes de firmar contratos en jurisdicciones desconocidas.*

---

## PARTE 5 — SISTEMA DE ONBOARDING PERSONALIZABLE

### Template de email de bienvenida al cliente

```
Asunto: [NOMBRE_CLIENTE] — Tu acceso a Memelogía OS está listo

Hola [NOMBRE],

Tu sistema de inteligencia memética ya está configurado y listo.

🔗 URL del sistema: [URL_CLIENTE]

📋 Para empezar en los próximos 10 minutos:
1. Abre [URL_CLIENTE] en tu navegador
2. La API Key ya está configurada — solo toca "Iniciar Sistema →"
3. Ve al tab "◎ Meme Analyzer" y sube tu primer meme
4. Lee la GUÍA DE INICIO adjunta para una orientación completa

📞 Tu sesión de capacitación:
[FECHA Y HORA DE CAPACITACIÓN]
[LINK DE VIDEOLLAMADA]

📁 Documentos adjuntos:
· Guía de Inicio Rápido
· Manual de Usuario Completo
· Guía de Problemas Comunes

Cualquier pregunta antes de la sesión: [CANAL_SOPORTE]

[FIRMA_AGENCIA]
```

### Checklist de entrega al cliente

```
□ URL del sistema funcionando correctamente
□ API Key configurada y probada con un análisis de prueba
□ Todos los módulos accesibles
□ Manual personalizado con nombre del cliente
□ Sesión de capacitación agendada
□ Canal de soporte comunicado (WhatsApp/Slack/Email)
□ Factura enviada
□ Contratos firmados archivados
□ Contacto técnico de emergencia compartido
□ Fecha de primer check-in (15 días) agendada
```

---

*Guía de Cliente · Memelogía OS v9.0 · 2026*
*Uso interno de agencia — documento confidencial*
