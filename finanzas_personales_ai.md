# CLP Tracker - Automatización de Finanzas Personales con IA

Sistema de automatización que transforma el registro manual de gastos en una experiencia conversacional inteligente, utilizando análisis conductual impulsado por IA.

## 🚀 Descripción del Proyecto

CLP Tracker es una solución automatizada que captura, procesa y categoriza gastos personales a través de mensajes de Telegram en lenguaje natural. Utilizando Google Gemini AI, el sistema no solo registra **qué** gastas, sino **por qué** lo haces, proporcionando insights conductuales para mejorar la toma de decisiones financieras.

## 🔧 Arquitectura del Sistema

### Stack Tecnológico
- **Automatización**: n8n
- **Interfaz de Usuario**: Telegram Bot API
- **Inteligencia Artificial**: Google Gemini API
- **Base de Datos**: Google Sheets API

### Flujo de Trabajo

```
📱 Telegram → 🤖 n8n → 🧠 Gemini AI → ✅ Validación → 📊 Google Sheets → 📤 Confirmación
```

## 🛠️ Funcionalidades Principales

### 1. Captura Conversacional
- **Input**: Mensajes en lenguaje natural via Telegram
- **Ejemplo**: `"12 lucas en pizza; estaba demasiado cansado para cocinar"`

### 2. Procesamiento Inteligente (Gemini AI)
- **Extracción de montos**: Normaliza expresiones chilenas ("lucas", "k", etc.)
- **Categorización funcional**: Asigna taxonomía estructurada (`Alimentación → Delivery`)
- **Análisis conductual**: Infiere motivaciones (`Confort / Evasión Emocional`)
- **Descripción limpia**: Genera texto estructurado

### 3. Validación y Almacenamiento
- **Validación de datos**: Verifica coherencia (monto > 0, categoría válida)
- **Persistencia**: Almacena en Google Sheets con enriquecimiento de datos
- **Confirmación**: Notifica éxito al usuario

## 📊 Valor Agregado

### Problema Resuelto
El registro manual de gastos carece de contexto. Una hoja de cálculo muestra que gastaste `$15.000` en delivery, pero no revela si fue por:
- Comodidad tras un día agotador
- Compra impulsiva
- Celebración

### Solución Implementada
- **Datos contextuales**: Captura motivaciones y circunstancias
- **Automatización completa**: Elimina fricción del registro manual
- **Insights conductuales**: Transforma datos en información accionable

## 🎯 Competencias Técnicas Demostradas

- **Ingeniería de Prompts**: Diseño de prompts para resultados estructurados y precisos
- **Integración de APIs**: Conexión cohesiva entre múltiples servicios (Telegram, Google, n8n)
- **Automatización de Workflows**: Implementación de pipelines complejos y lógicos
- **Procesamiento de Lenguaje Natural**: Aplicación práctica de LLMs para análisis de texto
- **Arquitectura de Sistemas**: Diseño de flujos de datos robustos y escalables

## 🔍 Casos de Uso

1. **Análisis de Patrones**: Identificar triggers conductuales de gastos
2. **Optimización Financiera**: Detectar áreas de mejora en hábitos de consumo
3. **Reportes Automatizados**: Generación de insights sin intervención manual
4. **Seguimiento en Tiempo Real**: Monitoreo continuo de comportamiento financiero

## 📈 Resultados

Este sistema trasciende el simple tracking de gastos para convertirse en una herramienta de **análisis conductual financiero**, proporcionando la base para decisiones más informadas y conscientes sobre el manejo del dinero personal.

---

> **Nota**: Este proyecto representa una aplicación práctica de automatización e IA para resolver problemas reales, demostrando capacidades de integración de sistemas, procesamiento de lenguaje natural y generación de insights accionables.