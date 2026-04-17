# DECISION_LOG_DIMINDS

**Versión:** v1.1.0  
**Estado:** Activo  
**Fecha inicial:** 2026-04-17  
**Proyecto:** DIMINDS  

---

# 1. Propósito

Este documento registra todas las decisiones estructurales
relevantes del proyecto DIMINDS.

Su objetivo es:

- evitar pérdida de acuerdos
- mantener coherencia histórica
- permitir trazabilidad
- reducir contradicciones
- facilitar auditoría técnica y estratégica

Toda decisión relevante debe registrarse aquí.

---

# 2. Qué debe registrarse

Se deben registrar decisiones que afecten:

- arquitectura
- modelo de datos
- consentimiento
- seguridad
- frontend estructural
- integraciones
- cumplimiento regulatorio
- modelo de negocio técnico

No registrar:

- ajustes menores visuales
- cambios triviales
- pruebas temporales

---

# 3. Estructura de cada decisión

Cada decisión debe registrarse con la siguiente estructura:

---

## DECISIÓN D-001

**Fecha:** 2026-04-17  

**Área afectada:**  
Gobernanza  

**Descripción:**  
Se establece el modelo formal de gobernanza DIMINDS
como documento canónico base.

**Motivo:**  
Evitar dispersión de reglas en chats y asegurar
coherencia estructural del sistema.

**Impacto:**  

Documentos afectados:

- 00_Gobernanza_DIMINDS.md  

Sistemas afectados:

- Web institucional  
- Formularios  
- Arquitectura general  

**Tipo de decisión:**  

✔ Nueva  
☐ Actualización  
☐ Corrección  

**Estado:**  

✔ Activa  
☐ Reemplazada  
☐ Obsoleta  

---

## DECISIÓN D-002

**Fecha:** 2026-04-17  

**Área afectada:**  
Consentimiento  

**Descripción:**  
Se adopta modelo de consentimiento explícito,
granular y versionado como base obligatoria.

**Motivo:**  
Garantizar cumplimiento normativo y trazabilidad
del uso de datos personales y financieros.

**Impacto:**  



Documentos afectados:

- 01_Modelo_Consentimiento_DIMINDS.md  

Sistemas afectados:

- Formularios  
- Captura de datos  
- Modelo de datos  
- Auditoría  

**Tipo de decisión:**  

✔ Nueva  
☐ Actualización  
☐ Corrección  

**Estado:**  

✔ Activa  
☐ Reemplazada  
☐ Obsoleta  

────────────────────────────────────────
D-003 — Stack frontend oficial
────────────────────────────────────────

Fecha: 2026-04  
Estado: VIGENTE  

Decisión:

Se adopta Astro como framework frontend
y Vercel como plataforma de despliegue.

Motivo:

Permitir rendimiento alto, control estructural
y despliegue rápido para la web institucional.

Impacto:

Define base técnica del frontend productivo.

Dependencias:

03_Arquitectura_Web_DIMINDS.md


────────────────────────────────────────
D-004 — Formularios con Tally.so (MVP)
────────────────────────────────────────

Fecha: 2026-04  
Estado: VIGENTE (TRANSITORIA)

Decisión:

Se adopta Tally.so como solución
transitoria de formularios.

Configuración:

Standard embed  
transparentBackground

Motivo:

Permitir captura inmediata de contactos
sin construir backend propio.

Impacto:

Introduce dependencia externa controlada.

Nota:

Será reemplazado por backend propio
en fases posteriores.


────────────────────────────────────────
D-005 — Sistema cromático v3.0
────────────────────────────────────────

Fecha: 2026-04  
Estado: VIGENTE  

Decisión:

Se abandona el color verde #1B4D3E
como color primario.

Se adopta:

Azul institucional #1A3F6F
derivado del logo oficial.

Motivo:

Mejor alineación con identidad visual.

Impacto:

Define identidad visual principal.


────────────────────────────────────────
D-006 — Colores secundarios institucionales
────────────────────────────────────────

Fecha: 2026-04  
Estado: VIGENTE  

Decisión:

Se incorporan colores secundarios:

Púrpura  
#6D28D9  
#C4B5FD  

Magenta  
#9E0EB5  
#E879F9  

Motivo:

Mantener coherencia visual
con degradados del logo.


────────────────────────────────────────
D-007 — Sistema tipográfico oficial
────────────────────────────────────────

Fecha: 2026-04  
Estado: VIGENTE  

Decisión:

Se adopta sistema tipográfico:

DM Serif Display  
Instrument Sans  

Motivo:

Transmitir formalidad institucional
y legibilidad profesional.


────────────────────────────────────────
D-008 — Arquitectura HOME v2.2
────────────────────────────────────────

Fecha: 2026-04  
Estado: VIGENTE  

Decisión:

Se adopta HOME v2.2
como arquitectura canónica.

Componentes:

Navbar  
Hero  
Credibilidad  
Problemas  
Metodología  
Servicios  
Casos  
Equipo  
Audiencias  
CTA Final  
Footer

Impacto:

Define orden estructural permanente.


────────────────────────────────────────
D-009 — Política visual sin imágenes stock
────────────────────────────────────────

Fecha: 2026-04  
Estado: VIGENTE  

Decisión:

No utilizar:

- imágenes stock
- imágenes generadas por IA

Sistema visual basado en:

CSS puro  
Fotos reales del equipo


────────────────────────────────────────
D-010 — Placeholders de equipo
────────────────────────────────────────

Fecha: 2026-04  
Estado: VIGENTE  

Decisión:

Se utilizan placeholders:

NC  
CG  

Mientras llegan fotos reales.

Motivo:

Permitir continuidad del diseño.


────────────────────────────────────────
D-011 — Placeholders de logos
────────────────────────────────────────

Fecha: 2026-04  
Estado: VIGENTE  

Decisión:

Se utilizan placeholders:

BID  
CORFO  
MASISA  
CGE  
SQM  

Hasta disponer de logos SVG.


────────────────────────────────────────
D-012 — Uso de anclas internas
────────────────────────────────────────

Fecha: 2026-04  
Estado: VIGENTE  

Decisión:

Las páginas no implementadas
redirigen a:

#contacto

Secciones:

Servicios  
Casos  
Insights


────────────────────────────────────────
D-013 — Catálogo oficial de servicios
────────────────────────────────────────

Fecha: 2026-04  
Estado: VIGENTE  

Decisión:

Se aprueba catálogo de:

18 servicios reales.

Divididos en:

Línea financiera  
Línea organizacional

Impacto:

Base del modelo comercial.


────────────────────────────────────────
D-014 — Estructura de liderazgo
────────────────────────────────────────

Fecha: 2026-04  
Estado: VIGENTE  

Decisión:

Carlos actúa como:

Socio Director

Responsable de línea financiera.


────────────────────────────────────────
D-015 — Estrategia de crecimiento
────────────────────────────────────────

Fecha: 2026-04  
Estado: VIGENTE  

Decisión:

Se adopta estrategia en:

3 fases

0–12 meses  
12–24 meses  
24–36 meses  

Objetivo:

$10M CLP mensuales.


────────────────────────────────────────
D-016 — Separación estructural de ecosistemas
────────────────────────────────────────

Fecha: 2026-04  
Estado: VIGENTE  

Decisión:

Se separa:

DIMINDS  
y ecosistema personal de Carlos:

Visado  
Nexelo  
Jarvis  

Bajo razón social futura independiente.

Impacto:

Define propiedad intelectual
y gobernanza futura.




---

# 4. Numeración de decisiones

Las decisiones deben numerarse en forma secuencial:

```text
D-001
D-002
D-003
D-004


Historial de  versiones 

### v1.1.0

- Agrega D-003 a D-012
- Cubre stack técnico · paleta · tipografía
  · Home v2.2 · fotografía · assets
  · navegación · modelo de servicios