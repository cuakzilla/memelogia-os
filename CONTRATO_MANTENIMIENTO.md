# CONTRATO DE SOPORTE Y MANTENIMIENTO MENSUAL
## Memelogía OS — Acuerdo de Servicio Continuo
### [VERSIÓN PLANTILLA — Adjuntar al SOW o firmar independientemente]

---

**N° de Contrato:** MANT-[YYYY]-[NNN]
**Fecha de inicio:** [DD/MM/YYYY]
**Duración mínima:** [X] meses
**Renovación:** Automática mes a mes después del período mínimo
**Aviso de cancelación:** [30] días antes del fin de cada período

---

## PARTES

**Proveedor:** A51 · cuakzilla
RFC: [RFC] · Email: soporte@cuakzilla.com

**Cliente:** [NOMBRE_EMPRESA]
RFC: [RFC] · Contacto técnico: [NOMBRE] · [EMAIL]

---

## 1. SERVICIOS INCLUIDOS POR NIVEL

### NIVEL BÁSICO — $[____] USD/mes

| Servicio | Detalle |
|---|---|
| Horas de soporte técnico | [1] hora/mes |
| Canal de soporte | Email únicamente |
| Tiempo de respuesta | 2 días hábiles (P3-P4) |
| Actualizaciones de seguridad | ✓ Incluidas |
| Actualizaciones de versión minor | ✓ Incluidas |
| Monitoreo de disponibilidad | Básico (alertas manuales) |
| Reporte mensual | No incluido |

### NIVEL PROFESIONAL — $[____] USD/mes ⭐ Recomendado

| Servicio | Detalle |
|---|---|
| Horas de soporte técnico | [3] horas/mes |
| Canal de soporte | Email + WhatsApp Business |
| Tiempo de respuesta | 4h (P2) · 8h hábiles (P3-P4) |
| Actualizaciones de seguridad | ✓ Incluidas, prioritarias |
| Actualizaciones de versión minor | ✓ Incluidas |
| Actualizaciones de versión major | Con descuento del [30]% |
| Monitoreo de disponibilidad | ✓ Automatizado + alertas |
| Reporte mensual | ✓ Resumen de uso e incidentes |
| Check-in mensual | ✓ Llamada de 30 min |

### NIVEL ENTERPRISE — $[____] USD/mes

| Servicio | Detalle |
|---|---|
| Horas de soporte técnico | [8] horas/mes |
| Canal de soporte | Email + WhatsApp + Slack dedicado + Tel |
| Tiempo de respuesta | 1h (P1) · 4h (P2) · 8h (P3) |
| Actualizaciones de seguridad | ✓ Proactivas y urgentes |
| Actualizaciones de versión minor | ✓ Incluidas |
| Actualizaciones de versión major | ✓ Incluidas |
| Monitoreo de disponibilidad | ✓ 24/7 con alertas automáticas |
| Reporte mensual | ✓ Dashboard + análisis de tendencias |
| QBR (revisión trimestral) | ✓ Reunión estratégica trimestral |
| Horas adicionales | Descuento del [20]% vs. tarifa normal |
| SLA garantizado | ✓ Ver documento SLA adjunto |

**Nivel contratado:** ☐ Básico ☐ Profesional ☐ Enterprise
**Fee mensual acordado:** $[____] [MONEDA]

---

## 2. ALCANCE DETALLADO DE LOS SERVICIOS

### 2.1 Soporte técnico — Qué cubre

**Incluido:**
- Diagnóstico y resolución de errores del sistema (bugs)
- Orientación sobre uso de funcionalidades existentes
- Revisión de problemas de configuración de API Keys
- Troubleshooting de integración con Cloudflare Pages
- Validación de actualizaciones antes de deploy
- Respuesta a preguntas técnicas del equipo del cliente

**No incluido (genera horas adicionales o nueva cotización):**
- Desarrollo de nuevas funcionalidades
- Personalización adicional de diseño
- Capacitación de nuevos usuarios (se cotiza por separado)
- Migración a nueva infraestructura
- Integración con sistemas del cliente no contemplados originalmente

### 2.2 Actualizaciones — Qué incluye

| Tipo | Descripción | Incluido en |
|---|---|---|
| Parche de seguridad | Correcciones de vulnerabilidades críticas | Todos los niveles |
| Bugfix (corrección de errores) | Errores identificados en el sistema base | Todos los niveles |
| Minor update (x.y → x.y+1) | Mejoras y nuevas funcionalidades menores | Todos los niveles |
| Major update (x.y → x+1.y) | Nuevas versiones con cambios significativos | Profesional (50% dto.) / Enterprise (incluido) |

**Proceso de actualización:**
1. Proveedor notifica al cliente con [X] días de antelación
2. El cliente aprueba la ventana de mantenimiento
3. El Proveedor realiza el deploy y valida con `node --check`
4. El cliente confirma el correcto funcionamiento
5. El Proveedor documenta el cambio en el CHANGELOG

### 2.3 Monitoreo — Qué cubre

El monitoreo verifica que:
- La URL del sistema esté accesible y respondiendo (uptime)
- La página cargue correctamente sin errores de JS
- Cloudflare Pages esté operativo

**No cubre:**
- La disponibilidad de los proveedores de IA (Anthropic, Google, etc.)
- Velocidad de red del lado del cliente
- Problemas del navegador del usuario final

---

## 3. HORAS ADICIONALES Y TRABAJO FUERA DE ALCANCE

Las horas de soporte no utilizadas en un mes **no se acumulan** para el
mes siguiente. Las horas adicionales por encima del paquete se facturan a:

**Tarifa hora adicional:** $[____] USD/hora
**Estimación previa:** Requerida para trabajos de más de [2] horas
**Autorización:** El cliente debe aprobar por escrito antes de ejecutar

---

## 4. RESPONSABILIDADES DEL CLIENTE

Para que el servicio de mantenimiento funcione correctamente, el cliente se
compromete a:

- Designar **un contacto técnico principal** con acceso al sistema
- Notificar al Proveedor de **cualquier cambio** que realice en el sistema
- No modificar el `index.html` sin informar al Proveedor
- Mantener actualizadas las claves de API de los proveedores de IA
- Responder a solicitudes de información del Proveedor en [5] días hábiles
- Participar en los check-ins mensuales programados

---

## 5. ESTRUCTURA DE FACTURACIÓN

**Fecha de cobro:** Del [1] al [5] de cada mes
**Método de pago:** [Transferencia bancaria / PayPal / Stripe]
**Referencia de pago:** MANT-[YYYY]-[NNN]-[MES]

**Pago anticipado:** Descuento del [10]% por pago de 6 meses adelantado
**Pago anticipado:** Descuento del [15]% por pago de 12 meses adelantado

**Ajuste de precios:** Los precios pueden ajustarse anualmente con [60] días
de aviso previo. Durante el período mínimo contratado, el precio está fijo.

---

## 6. TERMINACIÓN Y SUSPENSIÓN

### 6.1 Terminación por el cliente
El cliente puede cancelar este contrato con [30] días de aviso por escrito
**después** del período mínimo. Durante el período mínimo, la cancelación
anticipada implica el pago de los meses restantes.

### 6.2 Terminación por el proveedor
El Proveedor puede terminar el contrato con [30] días de aviso o de forma
inmediata en caso de:
- Falta de pago de más de [30] días
- Incumplimiento grave de los términos de licencia
- Uso del sistema para actividades ilegales o contrarias a los ToS de los
  proveedores de IA

### 6.3 Suspensión por falta de pago
Si el pago se retrasa más de [15] días, el Proveedor puede suspender
las actualizaciones y el soporte proactivo hasta regularizar el pago,
sin que ello constituya terminación del contrato.

### 6.4 Al terminar
- El cliente retiene el acceso al `index.html` en la versión que tenía
- El Proveedor no tiene obligación de continuar aplicando actualizaciones
- Las credenciales de acceso al soporte se desactivan

---

## 7. ESCALACIÓN DE DISPUTAS

Las disputas relacionadas con este contrato se resolverán:

1. **Paso 1:** Comunicación directa entre los contactos designados (hasta 10 días)
2. **Paso 2:** Mediación con un tercero neutral acordado por ambas partes
3. **Paso 3:** Arbitraje o vía judicial según la ley aplicable

---

## FIRMAS

---

**PROVEEDOR — A51 · cuakzilla:**

Nombre: ___________________________________
Cargo: ___________________________________
Fecha de inicio del servicio: _______________
Fecha de firma: ___________________________
Firma: ____________________________________

---

**CLIENTE — [NOMBRE_EMPRESA]:**

Nombre: ___________________________________
Cargo: ___________________________________
Contacto técnico designado: ________________
Fecha de firma: ___________________________
Firma: ____________________________________

---

*MANT-[YYYY]-[NNN] · Memelogía OS · A51 / cuakzilla · 2026*
