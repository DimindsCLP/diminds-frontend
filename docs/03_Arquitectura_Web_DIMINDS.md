# 03_Arquitectura_Web_DIMINDS

**Versión:** v1.0.0  
**Estado:** Inicial  
**Fecha:** 2026-04-17  
**Proyecto:** DIMINDS  

---

# 1. Propósito

Este documento define la arquitectura lógica
de la web institucional DIMINDS.

La web no debe entenderse únicamente como
una interfaz visual.

Debe entenderse como:

un sistema de entrada controlada
hacia el dominio interno del negocio.

La web cumple funciones estratégicas:

- posicionamiento institucional
- generación de confianza
- captura estructurada de prospectos
- activación de flujos consultivos
- preparación para integración futura

---

# 2. Principios arquitectónicos web

Toda arquitectura web debe respetar:

---

## 2.1 Web como capa pública

La web es:

CAPA PÚBLICA CONTROLADA

No es:

- repositorio de datos sensibles
- sistema de análisis
- motor financiero

Debe limitar su responsabilidad.

---

## 2.2 Separación frontend/backend

Debe existir separación clara entre:

Frontend público  
Backend de datos  

Nunca mezclar lógica sensible
directamente en el frontend.

---

## 2.3 Formularios controlados

Todo formulario debe:

- capturar consentimiento
- validar información
- registrar origen
- enviar datos a backend controlado

Nunca almacenar localmente.

---

## 2.4 Experiencia centrada en confianza

Toda interfaz debe transmitir:

- criterio
- claridad
- profesionalismo
- seguridad

Esto es parte de la arquitectura.

No solo diseño.

---

# 3. Componentes principales de la web

La web DIMINDS debe organizarse en módulos.

---

# 3.1 Página Home

Función:

Posicionamiento inicial
y presentación institucional.

Componentes:

- Hero principal
- Propuesta de valor
- Problemas que resolvemos
- Metodología
- Equipo
- Llamado a acción
- Contacto

---

# 3.2 Página Servicios

Función:

Explicar capacidades consultivas.

Componentes:

- Tipos de servicio
- Áreas de intervención
- Beneficios
- Casos de uso

---

# 3.3 Página Nosotros

Función:

Generar credibilidad institucional.

Componentes:

- Equipo
- Trayectoria
- Experiencia
- Filosofía

---

# 3.4 Página Contacto

Función:

Captura de prospectos.

Componentes:

- Formulario
- Consentimiento
- Validación
- Registro

---

# 3.5 Formularios

Los formularios representan:

punto crítico de captura.

Responsabilidades:

- mostrar consentimiento
- capturar datos mínimos
- registrar aceptación
- enviar a backend

Nunca almacenar localmente.

---

# 4. Flujo general de información

El flujo base debe seguir:

Usuario → Web → Formulario → Consentimiento → Backend → Registro

Nunca:

Usuario → Web → Base de datos directa

Debe existir backend intermedio.

---

# 5. Integración con consentimiento

Todo formulario debe:

- incluir consentimiento explícito
- registrar versión legal
- asociar consentimiento a usuario

Dependencia directa:

01_Modelo_Consentimiento_DIMINDS.md

---

# 6. Integración con modelo de datos

Los datos capturados deben alimentar:

Usuario  
Prospecto  
Consentimiento  

Dependencia directa:

02_Modelo_Datos_DIMINDS.md

---

# 7. Arquitectura técnica esperada

La web debe operar bajo:

Frontend:

- Astro / HTML / CSS / JS

Deployment:

- Vercel

Backend futuro:

- API controlada
- Registro auditable
- Gestión de consentimiento

---

# 8. Seguridad básica

La web debe implementar:

- validación de formularios
- protección contra spam
- control de origen
- registro de intentos

Nunca permitir envíos anónimos
sin validación.

---

# 9. Escalabilidad futura

La arquitectura debe permitir:

- agregar nuevos formularios
- integrar nuevos servicios
- conectar sistemas externos
- incorporar analítica

Sin rediseño completo.

---

# 10. Dependencias críticas

Este documento depende de:

- 00_Gobernanza_DIMINDS.md
- 01_Modelo_Consentimiento_DIMINDS.md
- 02_Modelo_Datos_DIMINDS.md

---

# 11. Historial de versiones

## v1.0.0

Definición inicial de arquitectura web
para la plataforma DIMINDS.