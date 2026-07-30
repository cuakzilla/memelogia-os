# ONBOARDING CHECKLIST — MEMELOGÍA OS v9.0
## Checklist Operativo de Implementación
### Para uso interno de la agencia — Un documento por cliente

---

**Cliente:** _______________________________________________
**N° de proyecto:** _______________________________________________
**Nivel:** ☐ Básico ☐ Profesional ☐ Enterprise
**Fecha de inicio:** _______________________________________________
**PM asignado:** _______________________________________________
**Técnico asignado:** _______________________________________________
**Fecha objetivo de Go Live:** _______________________________________________

---

## FASE 0 — PRE-PROYECTO (Antes de firmar)

### Calificación y Discovery
```
☐ Formulario de descubrimiento completado por el cliente
☐ Lead calificado (A / B / C) con razón documentada
☐ Nivel de implementación identificado y acordado
☐ Presupuesto del cliente confirmado (rango)
☐ Decisor identificado (quien firma)
☐ Contacto técnico designado por el cliente
☐ Fecha de inicio tentativa acordada
```

### Documentación pre-firma
```
☐ Propuesta comercial enviada y aprobada
☐ NDA firmado por ambas partes (si aplica)
☐ Cotización formal enviada (COT-YYYY-NNN)
☐ SOW / Contrato de licencia enviado para revisión
☐ Contrato de mantenimiento mensual enviado (si aplica)
☐ DPA enviado (si el cliente opera en UE/Brasil o tiene reqs. legales)
☐ SLA enviado y nivel acordado (si Profesional o Enterprise)
```

### Cierre comercial
```
☐ SOW firmado por ambas partes
☐ Anticipo recibido (50% del total)
☐ Factura del anticipo emitida
☐ Carpeta del proyecto creada internamente
☐ Acceso al canal de comunicación configurado (email / WhatsApp / Slack)
☐ Kickoff call agendado
```

---

## FASE 1 — KICKOFF Y BRIEFING (Día 1-2)

### Kickoff call (30-45 min con el cliente)
```
☐ Presentación del equipo de la agencia
☐ Presentación del contacto técnico del cliente
☐ Revisión del alcance y cronograma
☐ Aclaración de dudas del cliente sobre el SOW
☐ Proceso de aprobación definido (¿quién aprueba cada hito?)
☐ Canal de comunicación preferido confirmado
☐ Frecuencia de updates acordada
☐ Kickoff call documentado (resumen enviado en 24h)
```

### Recopilación de assets del cliente
```
☐ Logo del cliente (SVG o PNG fondo transparente, alta resolución)
☐ Colores de marca (códigos HEX primario y secundario)
☐ Tipografías de marca (si aplica y son web-safe)
☐ Nombre personalizado para el sistema (si quieren cambiar "Memelogía OS")
☐ Tagline personalizado (si quieren cambiar el subtítulo)
☐ URL final donde vivirá el sistema (subdominio o .pages.dev)
☐ Dominio del cliente (si van a usar dominio propio)
☐ Cuenta de Cloudflare del cliente (usuario/acceso compartido o la agencia crea)
☐ Información de contacto de soporte para incluir en documentación
```

---

## FASE 2 — IMPLEMENTACIÓN TÉCNICA (Día 2-5)

### Setup base
```
☐ Verificar que index.html base (v9.0) pasa node --check
☐ Copia de trabajo renombrada: memelogia-[cliente]-v9.html
☐ Validación JS del archivo base: ✓ / ✗ (si ✗, resolver antes de continuar)
```

### Personalización visual
```
☐ Variable --accent actualizada con color primario del cliente
☐ Variable --accent2 actualizada con color secundario
☐ Logo del cliente integrado en el sidebar y onboarding
☐ Nombre del sistema actualizado en HTML (título, onboarding, footer)
☐ Tagline/subtítulo actualizado
☐ Favicon personalizado (si aplica)
☐ Revisión visual en dark mode: ✓
☐ Revisión visual en light mode: ✓
☐ Revisión visual en móvil (320px): ✓
☐ Revisión visual en tablet (768px): ✓
☐ Revisión visual en desktop (1280px+): ✓
☐ Validación JS post-personalización: node --check ✓
```

### Configuración de APIs
```
☐ Sesión de 30 min con contacto técnico del cliente para configurar APIs
☐ Anthropic key configurada y probada: ✓ / ✗ / No aplica
☐ Gemini key configurada y probada: ✓ / ✗ / No aplica
☐ Grok key configurada y probada: ✓ / ✗ / No aplica
☐ OpenAI key configurada y probada: ✓ / ✗ / No aplica
☐ Cascade de fallback probado (desactivar proveedor 1, verificar que usa proveedor 2)
☐ Audio/video probado (requiere Gemini key): ✓ / No aplica
☐ Análisis de prueba completo realizado: ✓
☐ Signal Card generada correctamente: ✓
```

### Deploy
```
☐ Repo GitHub configurado (nuevo o existente del cliente)
☐ Archivos de deploy incluidos: _headers ✓ · _redirects ✓ · .gitignore ✓
☐ Primer commit y push realizados
☐ Cloudflare Pages conectado al repo
☐ Framework preset: None ✓
☐ Build command: vacío ✓
☐ Deploy inicial completado
☐ URL de deploy accesible y funcional: [URL] ✓
☐ Dominio personalizado configurado (si aplica): [DOMINIO] ✓
☐ HTTPS activo: ✓
☐ Headers de seguridad activos (_headers): ✓
```

### QA técnico completo
```
☐ Command Center carga sin errores: ✓
☐ Meme Analyzer — imagen funciona: ✓
☐ Meme Analyzer — texto funciona: ✓
☐ Meme Analyzer — audio funciona: ✓ / No aplica
☐ Meme Analyzer — video funciona: ✓ / No aplica
☐ Meme Analyzer — micrófono funciona: ✓ / No aplica
☐ Switch de idioma ES↔EN funciona en todos los módulos: ✓
☐ Switch de tema Dark↔Light funciona: ✓
☐ Historial guarda y recupera análisis: ✓
☐ Export JSON funciona: ✓
☐ Export Markdown funciona: ✓
☐ Módulo Mundo — 17 países cargan: ✓
☐ Módulo Mundo — Generar con IA funciona: ✓
☐ Biblioteca — filtros funcionan: ✓
☐ Atlas carga: ✓
☐ Causality Engine carga: ✓
☐ Scenario Lab — sliders funcionan: ✓
☐ Risk Engine carga: ✓
☐ Kill banner localizado correctamente (ES/EN): ✓
☐ Console del navegador: 0 errores ✓
☐ Prueba en Chrome: ✓
☐ Prueba en Safari: ✓ / No aplica
☐ Prueba en Firefox: ✓
☐ Prueba en móvil Android (Chrome): ✓
☐ Prueba en móvil iOS (Safari): ✓ / No aplica
```

---

## FASE 3 — REVISIÓN CON EL CLIENTE (Día 5-7)

### Sesión de revisión (30-45 min)
```
☐ Demo del sistema personalizado al cliente
☐ Revisión de personalización visual: ✓ aprobada
☐ Prueba en vivo de un análisis con el cliente
☐ Feedback del cliente recibido y documentado
☐ Cambios solicitados: [listar]
☐ Cambios implementados y re-validados
☐ Aprobación formal del cliente: ✓
☐ Segundo pago solicitado (30% del total)
☐ Factura del segundo pago emitida
```

---

## FASE 4 — CAPACITACIÓN (Día 7-10)

### Sesión 1 — Meme Analyzer + Signal Cards (1 hora)
```
☐ Agenda enviada al cliente 48h antes
☐ Asistentes confirmados: [nombres]
☐ Sesión grabada (con permiso del cliente): ✓ / No aplica
☐ Temas cubiertos:
   ☐ Configuración de API Keys
   ☐ Modos Quick Scan vs Deep Analysis
   ☐ Upload de imagen y análisis de texto
   ☐ Cómo leer una Signal Card
   ☐ Fuerzas Invisibles — qué significan
   ☐ Decision recommendations — cómo actuar
   ☐ Export de resultados
   ☐ Historial y recuperación de análisis
☐ Preguntas del cliente respondidas y documentadas
☐ Grabación enviada al cliente (si aplica)
```

### Sesión 2 — Módulos de Inteligencia (1 hora) — Si Nivel 2+
```
☐ Agenda enviada 48h antes
☐ Temas cubiertos:
   ☐ Command Center — lectura del dashboard
   ☐ Módulo Mundo — meme del día y países
   ☐ Biblioteca — filtros y búsqueda
   ☐ Audio y Video — uso del tab 🎵
   ☐ Causality Engine — cómo interpretar cadenas causales
   ☐ Scenario Lab — simulación de escenarios
   ☐ Risk Engine — kill switches y scoring
   ☐ Switch de idioma y tema
☐ Preguntas respondidas
☐ Casos de uso específicos del cliente demostrados
```

---

## FASE 5 — ENTREGA DE DOCUMENTACIÓN (Día 10-12)

```
☐ Manual de usuario personalizado (nombre/logo del cliente)
☐ Guía de inicio rápido personalizada
☐ Guía de problemas comunes (versión genérica o personalizada)
☐ Acceso al repositorio GitHub del cliente (si aplica)
☐ Credenciales de Cloudflare documentadas de forma segura
☐ Contacto de soporte de la agencia comunicado claramente
☐ Canal de soporte configurado y probado
☐ Documentación entregada vía [email / Drive / Notion / otro]
☐ Cliente confirmó recepción
```

---

## FASE 6 — GO LIVE Y CIERRE (Día 12-14)

```
☐ Go Live oficial confirmado con el cliente
☐ Pago final solicitado (20% del total)
☐ Factura final emitida
☐ Pago final recibido
☐ Carta de cierre / acta de entrega enviada
☐ Encuesta de satisfacción enviada (NPS)
☐ Foto/testimonial del cliente solicitado (si aplica)
☐ Caso de éxito documentado internamente
☐ Carpeta del proyecto archivada
☐ Inicio del soporte mensual confirmado (fecha de primer cobro)
☐ Primera fecha de check-in mensual agendada
```

---

## FASE 7 — SEGUIMIENTO POST-ENTREGA

### Check-in a los 7 días
```
☐ Llamada de 20 min realizada
☐ Preguntas del primer uso real respondidas
☐ Problemas detectados: [listar]
☐ Problemas resueltos: ✓
☐ Satisfacción del cliente evaluada (1-10): ___
```

### Check-in a los 30 días
```
☐ Número de análisis realizados por el cliente: ___
☐ Módulos más usados: _______________
☐ Módulos menos usados: _______________
☐ Problemas reportados: _______________
☐ Oportunidad de upsell identificada: ☐ Sí (cuál: ___) ☐ No
☐ Renovación de soporte confirmada: ☐ Sí ☐ Pendiente
```

### Check-in a los 90 días (Nivel Profesional / Enterprise)
```
☐ QBR realizado (si Enterprise)
☐ ROI del cliente evaluado
☐ Expansión a otros equipos/áreas discutida
☐ Actualización de versión presentada (si aplica)
☐ Contrato de soporte renovado/ampliado: ☐ Sí ☐ No
```

---

## NOTAS DEL PROYECTO

**Incidencias durante implementación:**
_______________________________________________
_______________________________________________

**Cambios fuera de alcance ejecutados (con autorización):**
_______________________________________________
_______________________________________________

**Lecciones aprendidas para próximos proyectos:**
_______________________________________________
_______________________________________________

**Referidos o leads generados por este cliente:**
_______________________________________________

---

*ONBOARDING CHECKLIST · Memelogía OS v9.0 · A51 / cuakzilla · 2026*
*Uso interno — No compartir con el cliente*
