# DATA PROCESSING AGREEMENT (DPA)
## Acuerdo de Procesamiento de Datos — Memelogía OS
### [VERSIÓN PLANTILLA — Revisar con abogado antes de firmar]

---

**N° de Acuerdo:** DPA-[YYYY]-[NNN]
**Fecha:** [DD/MM/YYYY]
**Versión:** 1.0

---

## PARTES

**RESPONSABLE DEL TRATAMIENTO (Controller):**
[NOMBRE_EMPRESA_CLIENTE] — quien determina los fines y medios del tratamiento
RFC / ID Fiscal: [RFC]
Domicilio: [DOMICILIO]
DPO (si aplica): [NOMBRE_DPO] · [EMAIL_DPO]
Representante: [NOMBRE]

**ENCARGADO DEL TRATAMIENTO (Processor):**
A51 · cuakzilla — quien trata datos en nombre del Responsable
RFC: [RFC_AGENCIA]
Domicilio: [DOMICILIO_AGENCIA]
Email de privacidad: privacidad@cuakzilla.com
Representante: [NOMBRE]

---

## 1. OBJETO Y ALCANCE

Este DPA regula el tratamiento de datos personales que el Encargado
realiza en nombre del Responsable en el contexto del uso de
Memelogía OS v9.0.

**Naturaleza del tratamiento:** Análisis de contenido cultural (imágenes,
texto, audio, video) mediante APIs de inteligencia artificial para generar
reportes de inteligencia memética.

**Finalidad del tratamiento:** Proveer el servicio de análisis memético
contratado por el Responsable.

**Tipos de datos tratados:**
- Imágenes que puedan contener personas identificables
- Archivos de audio con voz humana identificable
- Archivos de video con imágenes y audio de personas
- Texto que pueda contener datos de personas

**Categorías de interesados:** Personas que aparecen en el contenido
analizado (público general, figuras públicas, empleados, clientes, etc.)

**Duración:** Mientras dure el contrato de servicios entre las Partes.

---

## 2. OBLIGACIONES DEL ENCARGADO

El Encargado se compromete a:

### 2.1 Instrucciones documentadas
Tratar los datos únicamente según las instrucciones documentadas del
Responsable y para las finalidades establecidas en el contrato de servicio.

### 2.2 Confidencialidad
Garantizar que las personas autorizadas para tratar datos estén sujetas
a obligaciones de confidencialidad.

### 2.3 Seguridad
Implementar medidas técnicas y organizativas apropiadas para garantizar
un nivel de seguridad adecuado al riesgo:

| Medida | Implementación en Memelogía OS |
|---|---|
| Cifrado en tránsito | HTTPS/TLS en todas las comunicaciones |
| Sin almacenamiento server-side | Los datos del usuario permanecen en localStorage del navegador |
| Claves de API | Almacenadas en el dispositivo del usuario, no en servidores del Encargado |
| Acceso mínimo | Solo el usuario final accede a sus propios análisis |

### 2.4 Sub-encargados (Sub-processors)
El Encargado utiliza los siguientes sub-encargados para prestar el servicio:

| Sub-encargado | Función | País | Garantías |
|---|---|---|---|
| Anthropic | Análisis IA de texto e imágenes | EE.UU. | anthropic.com/privacy |
| Google LLC | Análisis IA de texto, imagen, audio y video | EE.UU. | policies.google.com/privacy |
| xAI | Análisis IA de texto e imágenes | EE.UU. | x.ai/privacy |
| OpenAI | Análisis IA de texto e imágenes | EE.UU. | openai.com/policies/privacy-policy |
| Cloudflare | Hosting y CDN | EE.UU. / Global | cloudflare.com/privacypolicy |

El Encargado notificará al Responsable con [30] días de anticipación sobre
cualquier cambio en los sub-encargados, dando al Responsable la oportunidad
de objetar dichos cambios.

### 2.5 Asistencia al Responsable
Asistir al Responsable para cumplir con sus obligaciones relativas a:
- Solicitudes de ejercicio de derechos de los interesados
- Notificaciones de violaciones de seguridad
- Evaluaciones de impacto de privacidad (DPIA)

### 2.6 Eliminación o devolución
Al terminar el contrato, eliminar o devolver todos los datos personales
al Responsable según sus instrucciones, salvo que la ley exija conservarlos.

### 2.7 Auditorías
Poner a disposición del Responsable toda la información necesaria para
demostrar el cumplimiento de este DPA y permitir auditorías razonables.

---

## 3. OBLIGACIONES DEL RESPONSABLE

El Responsable se compromete a:

a) Proporcionar instrucciones claras y documentadas sobre el tratamiento.
b) Garantizar que cuenta con base legal para el tratamiento de los datos.
c) Obtener los consentimientos necesarios para analizar contenido que incluya
   datos de terceros identificables.
d) Informar al Encargado de cualquier requisito legal adicional aplicable.
e) No proporcionar al sistema datos de categorías especiales (salud, religión,
   orientación sexual, etc.) de personas identificadas sin medidas adicionales.

---

## 4. TRANSFERENCIAS INTERNACIONALES DE DATOS

El servicio implica transferencias a EE.UU. donde operan los proveedores
de IA. Estas transferencias se realizan bajo:

☐ Decisión de adecuación de la Comisión Europea
☐ Cláusulas Contractuales Tipo (SCCs)
☐ Binding Corporate Rules
☐ Exención por necesidad contractual (Art. 49 GDPR)
☐ [MECANISMO APLICABLE]

*[Completar según jurisdicción del cliente y tipo de datos]*

---

## 5. VIOLACIONES DE SEGURIDAD

En caso de violación de seguridad que afecte datos personales, el Encargado:

1. Notificará al Responsable **sin dilación indebida** y, a más tardar,
   en **[72] horas** desde que tenga conocimiento de la violación.
2. Proporcionará la siguiente información:
   - Naturaleza de la violación y categorías de datos afectados
   - Número aproximado de interesados afectados
   - Medidas adoptadas o propuestas para remediar la violación
   - Punto de contacto para información adicional

---

## 6. REGISTRO DE ACTIVIDADES DE TRATAMIENTO

El Encargado mantendrá un registro de las actividades de tratamiento
realizadas en nombre del Responsable, conforme al Art. 30(2) GDPR
o normativa equivalente aplicable.

---

## 7. EVALUACIÓN DE IMPACTO (DPIA)

Cuando el Responsable considere que un tipo de tratamiento puede suponer
un alto riesgo para los derechos de los interesados, el Encargado asistirá
en la elaboración de la DPIA correspondiente.

---

## 8. VIGENCIA Y TERMINACIÓN

Este DPA tendrá la misma vigencia que el contrato de servicios principal.
A su terminación, el Encargado eliminará o devolverá todos los datos
personales en un plazo de **[30] días**.

---

## 9. RESPONSABILIDAD

Cada parte será responsable de los daños causados por el tratamiento
de datos que viole la normativa aplicable en la medida en que sea
imputable a su acción u omisión.

---

## 10. LEY APLICABLE

Este DPA se rige por [las leyes de México (LFPDPPP) / el GDPR / LGPD /
la normativa acordada entre las Partes].

---

## FIRMAS

---

**RESPONSABLE DEL TRATAMIENTO — [NOMBRE_EMPRESA_CLIENTE]:**

Nombre: ___________________________________
Cargo: ___________________________________
Fecha: ___________________________________
Firma: ___________________________________

---

**ENCARGADO DEL TRATAMIENTO — A51 · cuakzilla:**

Nombre: ___________________________________
Cargo: ___________________________________
Fecha: ___________________________________
Firma: ___________________________________

---

*DPA-[YYYY]-[NNN] · Memelogía OS · A51 / cuakzilla · 2026*
*Documento legal — Revisar con asesor jurídico especializado en privacidad antes de firmar*
