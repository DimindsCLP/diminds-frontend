# 03_Arquitectura_Web_DIMINDS

Versión: v1.2.0
Estado: Activo
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

# 3.1 Página Home

Función:
Posicionamiento institucional, generación
de confianza y captura de prospectos.

Versión canónica: HOME v2.2

Secciones implementadas en orden vertical:

01. Navbar
    Sticky · logo · menú principal
    · CTA Conversemos →

02. Hero
    Título H1 · subtítulo · mensaje
    de autoridad · CTA principal
    · CTA secundario · elemento
    geométrico abstracto en CSS

03. Banda de credibilidad
    Clientes: BID · CORFO · MASISA
    · CGE · SQM
    Estado: placeholders de texto
    Activar al recibir logos en SVG/PNG

04. Problemas reales
    8 problemas en grid 2 columnas

05. Metodología
    Timeline 4 etapas en CSS puro
    Diagnóstico · Diseño estratégico
    · Implementación · Seguimiento

06. Servicios principales
    3 servicios · 2 columnas por línea

07. Casos destacados
    Grid 2×2 · número decorativo
    de fondo en CSS

08. Equipo
    Fotos reales + LinkedIn
    Placeholders de iniciales activos
    hasta recibir fotos

09. Audiencias
    3 tarjetas de perfil

10. CTA Final
    Fondo oscuro · formulario Tally
    embebido · datos de contacto

11. Footer
    4 columnas · LinkedIn institucional
    y personal · datos · legal

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



## 7.1 Implementación actual

Framework:   Astro
Deployment:  Vercel
URL actual:  diminds-frontend.vercel.app
Dominio obj: diminds.cl (pendiente)

Sistema de diseño:
· Tipografía: DM Serif Display (H1/H2)
  + Instrument Sans (resto)
· Color primario:    #1A3F6F
· Color CTA:         #0F2549
· Color acento:      #2B7BC8
· Fondo base:        #F7F9FC
· Fondo alternado:   #E8F0FB
· Guiños de marca:
  Púrpura claro      #C4B5FD (fondos oscuros)
  Púrpura oscuro     #6D28D9 (fondos claros)
  Magenta claro      #E879F9 (fondos oscuros)
  Magenta oscuro     #9E0EB5 (fondos claros)

Documentos de referencia del sistema:
· Color System v3.0
· Typography System v1.0
· Spacing System v1.0
· Icon System v1.0 (Lucide Icons)
· Wireframe estructural v2
· UI Foundation v1.0
· HOME v2.2 (contenido y especificaciones)
· Instrucciones técnicas Opción A v1.0

## 7.2 Formulario de contacto — MVP

Solución:    Tally.so (Standard Embed)
Form ID:     ja7gAR
Config:      transparentBackground · hideTitle
             · alignLeft · dynamicHeight
Destino:     contacto@diminds.cl
Brecha:      ver 01_Modelo_Consentimiento
             sección 8.1

## 7.3 Assets pendientes de activación

Fotos del equipo (carpeta /images/team/):
· foto-nelda-cordova.webp
· foto-carlos-gutierrez.webp

Logos de clientes (carpeta /images/logos/):
· logo-bid.svg
· logo-corfo.svg
· logo-masisa.svg
· logo-cge.svg
· logo-sqm.svg

Activación: eliminar placeholder correspondiente
y descomentar bloque img en el HTML.

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

### v1.2.0

- Actualiza sección 3.1 con componentes
  reales del HOME v2.2
- Agrega 7.1 estado de implementación
  y sistema de diseño
- Agrega 7.2 formulario MVP Tally.so
- Agrega 7.3 assets pendientes