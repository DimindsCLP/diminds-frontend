# 00_Gobernanza_DIMINDS

**Versión:** v1.1.0  
**Estado:** Aprobado inicial  
**Fecha:** 2026-04-17  
**Proyecto:** DIMINDS  

---

## 1. Propósito

Este documento define la gobernanza base del proyecto DIMINDS.

Su objetivo es establecer las reglas estructurales que deben regir
las decisiones de negocio, arquitectura, datos, frontend, cumplimiento
y evolución del sistema.

Este documento es canónico.

Todo diseño posterior debe alinearse con este marco.

---

## 2. Naturaleza del proyecto

DIMINDS es una plataforma consultiva, financiera y tecnológica
orientada a construir confianza, capturar oportunidades de negocio
y habilitar servicios de análisis y apoyo a decisiones con base
tecnológica escalable.

DIMINDS no debe entenderse solo como un sitio web.

Debe entenderse como una base institucional y tecnológica capaz de sostener:

- presencia pública confiable
- captura ordenada de prospectos y datos
- gestión de consentimiento
- servicios consultivos
- evolución futura hacia servicios financieros más sofisticados
- preparación para integraciones tipo open finance
- operación trazable y audit-ready

---

## 3. Principios obligatorios

Toda decisión dentro de DIMINDS debe respetar los siguientes principios:

### 3.1 Privacy by Design

La protección de datos personales debe integrarse desde el diseño inicial.

No se admite agregar privacidad como ajuste posterior.

### 3.2 Consent-Aware by Default

Ningún dato personal o sensible debe capturarse, procesarse o reutilizarse
sin una base de consentimiento explícita cuando corresponda.

El consentimiento debe poder registrarse, versionarse y auditarse.

### 3.3 Audit-Ready

Toda acción relevante del sistema debe dejar trazabilidad suficiente.

Toda arquitectura, flujo o integración debe poder ser revisada posteriormente.

### 3.4 Human-in-the-Loop

Toda recomendación, evaluación o decisión con impacto relevante
en personas, finanzas o materias sensibles debe mantener validación humana.

No se permitirá automatización cerrada en materias críticas.

### 3.5 Separación de dominios

Debe existir separación estricta entre:

- dominio editorial/comercial
- dominio sensible/financiero

La conveniencia técnica no justifica mezclar ambos dominios.

### 3.6 Minimización de datos

Solo deben capturarse los datos estrictamente necesarios
para la finalidad declarada.

### 3.7 Open Finance Readiness

La arquitectura debe permitir evolución futura hacia integraciones
con ecosistemas financieros y open finance.

Sin embargo, el MVP no debe asumir operación regulada plena.

---

## 4. Reglas de decisión

Las decisiones dentro del proyecto deben regirse por las siguientes reglas:

1. Ninguna decisión nueva puede reemplazar silenciosamente una anterior.
2. Toda contradicción debe marcarse explícitamente.
3. Toda propuesta relevante debe indicar si:
   - mantiene
   - amplía
   - aterriza
   - abre pendiente
   - contradice
4. No se debe privilegiar conveniencia técnica por sobre cumplimiento.
5. Toda captura de datos debe tener finalidad explícita.
6. Toda integración externa debe evaluarse desde riesgo, trazabilidad y consentimiento.

---

## 5. Capas lógicas del sistema

DIMINDS debe estructurarse, como mínimo, en las siguientes capas lógicas:

### 5.1 Capa pública institucional

Responsable de:

- posicionamiento
- confianza
- contenido institucional
- captación inicial

Esta capa no debe almacenar ni procesar información sensible innecesaria.

### 5.2 Capa de captura controlada

Responsable de:

- formularios
- consentimiento
- validación de ingreso
- registro trazable de interacción

### 5.3 Capa de dominio sensible

Responsable de:

- datos financieros
- perfiles sensibles
- análisis
- lógica de evaluación

Debe operar con protección reforzada.

### 5.4 Capa de servicios inteligentes

Responsable de:

- análisis
- apoyo a decisiones
- modelos de recomendación
- automatizaciones controladas

Siempre bajo criterio human-in-the-loop
cuando el caso lo requiera.

### 5.5 Capa de integraciones

Responsable de futuras conexiones con:

- APIs externas
- datos financieros
- motores analíticos
- componentes transversales como JARVIS

---

## 6. Modelo de confianza

Toda expresión de la marca y del sistema debe transmitir:

- criterio
- seriedad
- confianza
- claridad
- control
- profesionalismo

Esto aplica a:

- frontend
- textos
- formularios
- procesos
- mensajes legales
- experiencia de usuario

---

## 7. Entregables y disciplina documental

Todo entregable del proyecto debe:

- ser estructurado
- ser claro
- evitar ambigüedad
- mantener trazabilidad
- indicar estado de aprobación cuando corresponda

Los documentos canónicos del proyecto deben versionarse formalmente.

No deben editarse sin criterio de control.

---

## 8. Documentos canónicos base

DIMINDS debe mantener al menos los siguientes documentos estructurales:

- 00_Gobernanza_DIMINDS.md
- 01_Modelo_Consentimiento.md
- 02_Modelo_Datos_DIMINDS.md
- 03_Arquitectura_Web.md
- 04_Modelo_Servicios.md
- DECISION_LOG_DIMINDS.md

---

# Historial de versiones

## v1.0.0
Versión inicial del documento.

## v1.1.0
- Normalización de formato.
- Alineación con arquitectura web actual.