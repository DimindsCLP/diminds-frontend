# 02_Modelo_Datos_DIMINDS

Versión: v1.1.0
Estado: Activo
**Fecha:** 2026-04-17  
**Proyecto:** DIMINDS  

---

# 1. Propósito

Este documento define el modelo lógico de datos base
del sistema DIMINDS.

Su objetivo es establecer:

- las entidades principales
- sus atributos clave
- sus relaciones
- la clasificación de datos
- las dependencias con consentimiento

Este modelo debe respetar:

- Privacy by Design
- Minimización de Datos
- Separación de dominios
- Auditabilidad

---

# 2. Principios del modelo de datos

El modelo de datos debe cumplir:

## 2.1 Separación por dominios

Se deben separar:

DOMINIO PÚBLICO  
DOMINIO COMERCIAL  
DOMINIO SENSIBLE  

Nunca mezclar directamente.

---

## 2.2 Minimización de datos

Solo almacenar:

datos estrictamente necesarios.

Evitar duplicación.

---

## 2.3 Trazabilidad

Todo dato relevante debe permitir:

- saber cuándo fue creado
- saber quién lo creó
- saber su origen

---

## 2.4 Consentimiento dependiente

Ningún dato sensible puede existir
sin consentimiento asociado.

---

# 3. Entidades principales

Las siguientes entidades forman
la base del sistema.

---

# 3.1 Usuario

Representa a una persona registrada
o capturada en el sistema.

Campos base:

- usuario_id (UUID)
- nombre
- apellido
- email
- telefono
- fecha_creacion
- origen_registro

Clasificación:

Datos personales.

Requiere consentimiento.

---

# 3.2 Consentimiento

Representa autorización explícita
para uso de datos.

Campos base:

- consentimiento_id (UUID)
- usuario_id
- finalidad
- version_legal
- fecha_otorgamiento
- estado
- fecha_revocacion

Clasificación:

Dato crítico.

Entidad obligatoria.

---

# 3.3 Prospecto

Representa un contacto potencial.

Campos base:

- prospecto_id
- usuario_id
- estado_prospecto
- fecha_creacion
- canal_origen

Clasificación:

Dato comercial.

---

# 3.4 Caso

Representa una interacción formal
con el usuario.

Ejemplo:

- diagnóstico
- análisis financiero
- evaluación estratégica

Campos base:

- caso_id
- usuario_id
- tipo_caso
- estado_caso
- fecha_inicio
- fecha_cierre

Clasificación:

Dato operativo.

Puede contener información sensible.

---

# 3.5 Documento

Representa documentos asociados
a un caso.

Ejemplo:

- informes
- archivos financieros
- antecedentes

Campos base:

- documento_id
- caso_id
- tipo_documento
- fecha_carga
- version

Clasificación:

Dato potencialmente sensible.

---

# 3.6 Evento_Auditoria

Registra eventos críticos.

Ejemplo:

- creación
- modificación
- consulta
- eliminación

Campos base:

- evento_id
- tipo_evento
- entidad_afectada
- usuario_responsable
- fecha_evento
- origen_evento

Clasificación:

Dato técnico obligatorio.

---

# 4. Relaciones principales

Relaciones clave:

Usuario → Consentimiento  
Usuario → Prospecto  
Usuario → Caso  
Caso → Documento  
Usuario → Evento_Auditoria  

Estas relaciones permiten trazabilidad completa.

---

# 5. Clasificación de datos

Los datos deben clasificarse en:

---

## 5.1 Datos públicos

Ejemplo:

- contenido web
- información institucional

No sensibles.

---

## 5.2 Datos personales

Ejemplo:

- nombre
- email
- teléfono

Requieren consentimiento.

---

## 5.3 Datos sensibles

Ejemplo:

- información financiera
- antecedentes económicos
- análisis financieros

Requieren controles estrictos.

---

# 6. Control de acceso a datos

El sistema debe permitir:

- control por roles
- control por tipo de dato
- registro de acceso

Nunca permitir acceso abierto.

---

# 7. Versionamiento de datos

Las siguientes entidades deben permitir versiones:

- Consentimiento
- Documento
- Caso

Esto permite:

trazabilidad histórica.

---

# 8. Preparación para crecimiento

El modelo debe permitir:

- integración con servicios externos
- incorporación de nuevas entidades
- expansión modular

Sin rediseño total.

---

# 9. Dependencias críticas

Este modelo depende de:

- 00_Gobernanza_DIMINDS.md
- 01_Modelo_Consentimiento_DIMINDS.md

---

## 10. Estado de implementación

### 10.1 Fase MVP

El MVP opera sin backend propio.
La captura se realiza mediante Tally.so.
Las entidades de este modelo no están
implementadas en base de datos aún.
Los datos capturados llegan por correo
a contacto@diminds.cl.

### 10.2 Pendiente — Fase 2

Implementar backend con:
· Base de datos relacional
· Entidades según este modelo
· API controlada
· Registro de consentimiento
· Auditoría de eventos

### 10.3 Orden de implementación sugerido

1. Usuario
2. Consentimiento
3. Prospecto
4. Caso
5. Documento
6. Evento_Auditoria

Referencia: DECISION_LOG D-004

---
# 11. Historial de versiones

## v1.0.0

Definición inicial del modelo lógico
de datos base del sistema DIMINDS.

### v1.1.0

- Agrega sección 10 con estado de
  implementación MVP y pendientes Fase 2