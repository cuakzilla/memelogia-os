# SERVICE LEVEL AGREEMENT (SLA)
## Acuerdo de Nivel de Servicio — Memelogía OS
### [VERSIÓN PLANTILLA — Ajustar métricas según nivel de cliente]

---

**N° de SLA:** SLA-[YYYY]-[NNN]
**Fecha de inicio:** [DD/MM/YYYY]
**Vigencia:** [X] meses / hasta [DD/MM/YYYY]
**Revisión:** Anual o a solicitud de cualquiera de las Partes

---

## PARTES

**Proveedor del Servicio:** A51 · cuakzilla
**Cliente:** [NOMBRE_EMPRESA_CLIENTE]
**Nivel de servicio contratado:** ☐ Básico ☐ Profesional ☐ Enterprise

---

## 1. DESCRIPCIÓN DEL SERVICIO

Memelogía OS v9.0 como sistema alojado en:
**URL del cliente:** [URL_SISTEMA_CLIENTE]
**Plataforma de hosting:** Cloudflare Pages
**Proveedor(es) de IA activos:** [Anthropic / Gemini / Grok / OpenAI]

---

## 2. MÉTRICAS DE NIVEL DE SERVICIO

### 2.1 Disponibilidad del sistema

| Nivel | Disponibilidad objetivo | Tiempo máx. de inactividad/mes |
|---|---|---|
| Básico | 99.0% | ~7.3 horas |
| Profesional | 99.5% | ~3.6 horas |
| Enterprise | 99.9% | ~43 minutos |

**Nivel contratado:** [____]% — máximo [____] horas de inactividad/mes

> **Nota:** La disponibilidad del sistema depende de:
> 1. Cloudflare Pages (SLA propio: 100% en su contrato Enterprise)
> 2. Proveedores de IA (Anthropic/Google/xAI/OpenAI — fuera del control del Proveedor)
> Los incidentes causados por los proveedores de IA de terceros no cuentan
> contra el SLA del Proveedor, siempre que el sistema en sí esté accesible.

### 2.2 Tiempos de respuesta a incidentes

| Prioridad | Definición | Respuesta inicial | Resolución objetivo |
|---|---|---|---|
| P1 — Crítico | Sistema inaccesible / datos comprometidos | [1] hora | [4] horas |
| P2 — Alto | Funcionalidad principal degradada | [4] horas | [24] horas |
| P3 — Medio | Funcionalidad secundaria afectada | [8] horas hábiles | [72] horas hábiles |
| P4 — Bajo | Consultas, mejoras, cambios menores | [2] días hábiles | [10] días hábiles |

**Horario de soporte:**
- **Básico:** Lunes a Viernes 9:00-18:00 (hora de México)
- **Profesional:** Lunes a Viernes 8:00-20:00 + Sábados 9:00-14:00
- **Enterprise:** 24/7 para P1 · Horas hábiles extendidas para P2-P4

### 2.3 Tiempos de actualización

| Tipo de actualización | Plazo máximo | Notificación previa |
|---|---|---|
| Parche de seguridad crítico | 24 horas | Notificación simultánea |
| Actualización de seguridad menor | 7 días | 2 días |
| Actualización de versión (minor) | 15 días | 5 días |
| Nueva versión (major) | A convenir | 15 días |

---

## 3. CANALES Y PROCEDIMIENTOS DE SOPORTE

### 3.1 Canales disponibles según nivel

| Canal | Básico | Profesional | Enterprise |
|---|---|---|---|
| Email: soporte@cuakzilla.com | ✓ | ✓ | ✓ |
| WhatsApp Business: [NÚMERO] | — | ✓ | ✓ |
| Slack (canal dedicado) | — | — | ✓ |
| Teléfono directo: [NÚMERO] | — | — | ✓ P1/P2 |
| Videollamada programada | — | ✓ | ✓ |

### 3.2 Cómo reportar un incidente

1. **Identificar la prioridad** usando la tabla de la sección 2.2
2. **Reportar por el canal correspondiente** incluyendo:
   - Descripción del problema
   - Prioridad estimada (P1-P4)
   - Pasos para reproducirlo
   - Capturas de pantalla o evidencia
   - Impacto en el negocio
3. **Recibir número de ticket** de confirmación
4. **Seguimiento** hasta resolución

### 3.3 Contactos de escalación

| Nivel | Contacto | Canal | Disponibilidad |
|---|---|---|---|
| Soporte técnico (1er nivel) | [NOMBRE] | Email / WhatsApp | Horas hábiles |
| Líder técnico (2do nivel) | [NOMBRE] | WhatsApp / Tel | P1-P2 urgentes |
| Responsable de cuenta (3er nivel) | [NOMBRE] | Tel directo | P1 críticos |

---

## 4. EXCLUSIONES DEL SLA

Los compromisos de este SLA **no aplican** en los siguientes casos:

a) Interrupciones causadas por los proveedores de IA (Anthropic, Google, xAI, OpenAI)
b) Interrupciones de Cloudflare (proveedor de hosting) fuera del control del Proveedor
c) Interrupciones de internet del lado del Cliente
d) Incidentes causados por cambios realizados por el Cliente sin autorización
e) Mantenimiento programado (notificado con anticipación)
f) Casos de fuerza mayor (desastres naturales, pandemias, guerras, etc.)
g) Ataques DDoS u otros ataques externos de terceros
h) Uso del sistema fuera de las condiciones especificadas en el manual de usuario

---

## 5. MANTENIMIENTO PROGRAMADO

El Proveedor notificará con **[48] horas** de anticipación cualquier
mantenimiento que requiera inactividad del sistema.

El mantenimiento se realizará preferentemente en:
**[Domingo 22:00 - 02:00 hora de México]** (ventana de mínimo impacto)

El tiempo de mantenimiento programado **no cuenta** contra los objetivos
de disponibilidad del SLA.

---

## 6. MEDICIÓN Y REPORTES

### 6.1 Medición de disponibilidad
La disponibilidad se calcula mensualmente:
```
Disponibilidad = (Minutos totales - Minutos de inactividad no programada)
                 ─────────────────────────────────────────────────────────
                              Minutos totales del mes
```

### 6.2 Reportes de servicio

| Nivel | Frecuencia | Contenido |
|---|---|---|
| Básico | Trimestral | Disponibilidad, incidentes resueltos |
| Profesional | Mensual | + Tiempos de respuesta, actualizaciones |
| Enterprise | Mensual + QBR | + Análisis de tendencias, roadmap |

---

## 7. COMPENSACIONES POR INCUMPLIMIENTO

Si el Proveedor no alcanza los objetivos de disponibilidad comprometidos:

| Disponibilidad real | Crédito de servicio |
|---|---|
| 98.0% - 99.0% (Básico) | 10% del fee mensual |
| 95.0% - 98.0% | 25% del fee mensual |
| 90.0% - 95.0% | 50% del fee mensual |
| < 90.0% | 100% del fee mensual |

**Proceso de reclamación:** El Cliente debe solicitar el crédito dentro de
los [30] días siguientes al incidente. Los créditos se aplican en la
siguiente factura y no son reembolsables en efectivo.

**Límite máximo de créditos:** El total de créditos en un mes no puede
exceder el 100% del fee mensual correspondiente.

---

## 8. REVISIÓN Y MODIFICACIÓN

Este SLA puede ser revisado:
- Anualmente (revisión programada)
- Cuando cambie significativamente el alcance del servicio
- A solicitud de cualquiera de las Partes con [30] días de aviso

---

## FIRMAS

---

**PROVEEDOR DEL SERVICIO — A51 · cuakzilla:**

Nombre: ___________________________________
Cargo: ___________________________________
Fecha: ___________________________________
Firma: ___________________________________

---

**CLIENTE — [NOMBRE_EMPRESA]:**

Nombre: ___________________________________
Cargo: ___________________________________
Fecha: ___________________________________
Firma: ___________________________________

---

*SLA-[YYYY]-[NNN] · Memelogía OS · A51 / cuakzilla · 2026*
