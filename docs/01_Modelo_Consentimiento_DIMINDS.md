# 01_Modelo_Consentimiento_DIMINDS

**Versión:** v1.0.0  
**Estado:** Aprobado inicial  
**Fecha:** 2026-04-17  
**Proyecto:** DIMINDS  

---

# 1. Propósito

Este documento define el modelo de consentimiento del sistema DIMINDS.

Su objetivo es asegurar que toda captura, uso y procesamiento de datos
se realice bajo un esquema explícito, trazable y auditable.

Este modelo es obligatorio para cualquier flujo que involucre:

- captura de datos personales
- análisis de datos
- uso de información financiera
- contacto con clientes o prospectos
- integración con sistemas externos

---

# 2. Principios del modelo de consentimiento

El consentimiento en DIMINDS debe cumplir los siguientes principios:

## 2.1 Consentimiento explícito

El usuario debe aceptar activamente el uso de sus datos.

No se permite:

- consentimiento implícito
- consentimiento por omisión
- casillas pre-marcadas

---

## 2.2 Consentimiento informado

El usuario debe conocer:

- qué datos se capturan
- para qué finalidad
- cómo se usarán
- quién los usará
- cuánto tiempo se conservarán

---

## 2.3 Consentimiento granular

El consentimiento debe registrarse por finalidad.

Ejemplo:

- contacto comercial
- análisis financiero
- envío de información
- elaboración de diagnósticos

No se permite un consentimiento genérico único.

---

## 2.4 Consentimiento versionado

Cada consentimiento debe registrar:

- versión del texto legal
- fecha de aceptación
- fuente de captura
- usuario asociado

Esto permite trazabilidad histórica.

---

## 2.5 Consentimiento revocable

El usuario debe poder retirar su consentimiento.

La revocación debe:

- registrarse
- detener usos futuros
- mantener trazabilidad histórica

---

# 3. Tipos de consentimiento

DIMINDS debe soportar al menos los siguientes tipos:

---

## 3.1 Consentimiento de contacto

Finalidad:

Permitir contacto inicial con el usuario.

Ejemplo:

- responder formularios
- agendar reuniones
- enviar respuestas

---

## 3.2 Consentimiento de análisis

Finalidad:

Permitir análisis de información proporcionada.

Ejemplo:

- diagnóstico financiero
- evaluación estratégica
- análisis consultivo

---

## 3.3 Consentimiento de comunicación

Finalidad:

Permitir envío de información relevante.

Ejemplo:

- newsletters
- actualizaciones
- información institucional

---

## 3.4 Consentimiento financiero sensible (futuro)

Finalidad:

Permitir tratamiento de información financiera.

Ejemplo:

- cuentas
- ingresos
- deudas
- inversiones

Este tipo requiere controles adicionales.

---

# 4. Eventos que deben registrarse

Todo consentimiento debe generar eventos auditables.

Eventos mínimos:

- consentimiento otorgado
- consentimiento actualizado
- consentimiento revocado
- consentimiento consultado

Cada evento debe registrar:

- fecha
- origen
- tipo de consentimiento
- versión legal asociada

---

# 5. Componentes del registro de consentimiento

Cada consentimiento debe almacenar:

- identificador único
- usuario asociado
- finalidad
- versión legal
- fecha de aceptación
- origen de captura
- estado actual
- fecha de revocación (si aplica)

---

# 6. Flujo general de consentimiento

El flujo estándar debe seguir este orden:

1 — Mostrar información legal  
2 — Mostrar finalidades  
3 — Solicitar aceptación explícita  
4 — Registrar consentimiento  
5 — Permitir uso de datos  

Nunca al revés.

---

# 7. Separación por finalidad

Cada finalidad debe ser independiente.

Ejemplo:

Un usuario puede aceptar:

✔ contacto  
✔ análisis  

Pero rechazar:

✖ comunicación comercial  

El sistema debe respetar esa separación.

---

# 8. Integración con formularios

Todo formulario debe:

- mostrar consentimiento asociado
- registrar aceptación
- registrar versión legal
- bloquear envío si no se acepta cuando corresponda

Esto aplica a:

- formulario web
- captura interna
- integraciones externas

---

# 9. Integración con modelo de datos

El consentimiento debe existir como entidad independiente.

Nunca debe mezclarse directamente con:

- datos comerciales
- datos financieros

Debe existir relación lógica entre:

Usuario ↔ Consentimiento

---

# 10. Auditoría del consentimiento

El sistema debe permitir:

- consultar historial completo
- identificar versión aceptada
- identificar fecha de aceptación
- identificar cambios posteriores

Esto es obligatorio para:

- cumplimiento
- defensa legal
- trazabilidad

---

# 11. Preparación para Open Finance

El modelo debe permitir evolución futura hacia:

- consentimiento granular por entidad
- consentimiento por fuente externa
- consentimiento temporal

Esto permitirá integraciones financieras futuras.

---

# 12. Historial de versiones

## v1.0.0

- Definición inicial del modelo de consentimiento DIMINDS
- Incluye principios, tipos, eventos y estructura base