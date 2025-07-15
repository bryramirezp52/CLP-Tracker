# CLP Tracker - Automatización de Finanzas Personales con IA

Sistema de automatización que transforma el registro manual de gastos en una experiencia conversacional inteligente, utilizando análisis conductual impulsado por IA.

---

## 🚀 Descripción del Proyecto

**CLP Tracker** es una solución automatizada que captura, procesa y analiza gastos personales a través de simples mensajes de Telegram. Utilizando Google Gemini AI, el sistema no solo registra en qué gastas tu dinero, sino que revela por qué lo haces y qué patrones de comportamiento subyacen a tus decisiones, culminando en un reporte de análisis estratégico semanal.

---

## 🔧 Arquitectura del Sistema

### Stack Tecnológico

- **Automatización**: n8n  
- **Interfaz de Usuario**: Telegram Bot API  
- **Inteligencia Artificial**: Google Gemini API  
- **Base de Datos**: Google Sheets API  

### Flujos de Trabajo

1. **Registro de Gastos en Tiempo Real**  
   📱 Telegram → 🤖 n8n → 🧠 Gemini AI (Registro) → ✅ Validación → 📊 Google Sheets → 📤 Confirmación  
   
   ![Flujo CLP Tracker](imagenes/flujo_clp_tracker)

2. **Análisis Estratégico Semanal**  
   🗓️ Disparador Semanal → 🤖 n8n → 📊 Google Sheets (Lectura) → 🧠 Gemini AI (Análisis) → 📤 Reporte a Telegram  
   
   ![Flujo Analista Financiero](imagenes/flujo_analista_financiero)

3. **Interacción con el Bot de Telegram**  
   ![Funcionamiento Telegram](imagenes/funcionamiento_telegram)
---

## 🛠️ Funcionalidades Principales

### 1. Registro Conversacional en Tiempo Real

**Input**: Mensajes en lenguaje natural enviados a un bot de Telegram.  
_Ejemplo_: `"12 lucas en pizza; estaba demasiado cansado para cocinar"`

**Procesamiento Inteligente (Gemini AI)**:

- **Extracción de Monto**: Normaliza expresiones chilenas ("lucas", "k", etc.) a un valor numérico.  
- **Categorización Funcional**: Asigna una taxonomía estricta y anidada (ej: Alimentación → Delivery).  
- **Análisis Conductual**: Infiere la motivación detrás del gasto (ej: Confort / Evasión Emocional).  

**Validación y Persistencia**:

- Verifica la coherencia de los datos extraídos (monto > 0, categoría válida).  
- Almacena cada gasto en Google Sheets, enriquecido con las clasificaciones de la IA.  
- Envía una notificación de éxito al usuario.  

### 2. Analista Financiero Semanal (IA)

- **Activación**: Se ejecuta automáticamente cada domingo por la noche.  
- **Generación de Reporte**: Consolida todos los gastos de la semana, calculando totales, subtotales y porcentajes por categoría.  

**Análisis Estratégico (Gemini AI)**:  
Un segundo agente de IA, actuando como "Asesor Estratégico", recibe el reporte numérico y, sin repetirlo, entrega un análisis cualitativo que incluye:

- **Insight Central**: La conclusión más potente sobre el comportamiento de la semana.  
- **Preguntas Críticas**: Cuestionamientos profundos sobre los gastos más reveladores.  
- **Proyección y Riesgo**: Una evaluación del impacto financiero a futuro.  
- **Desafío Semanal**: Una pregunta accionable para mejorar la semana siguiente.  

---

## 📊 Valor Agregado

### Problema Resuelto

El registro manual de gastos es tedioso y carece de contexto. Una hoja de cálculo muestra que gastaste $15.000 en delivery, pero no revela si fue por comodidad, un impulso o una celebración. Sin el "porqué", los datos no generan aprendizaje.

### Solución Implementada

- **Automatización sin Fricción**: Elimina la tarea manual de registrar gastos.  
- **Datos Contextuales**: Captura las motivaciones y circunstancias reales de cada transacción.  
- **Insights Conductuales**: Transforma cifras en información accionable, revelando patrones de comportamiento.  

---

## 🎯 Competencias Técnicas Demostradas

- **Ingeniería de Prompts**: Diseño avanzado de prompts para dirigir LLMs hacia resultados estructurados y análisis cualitativos.  
- **Integración de APIs**: Conexión cohesiva y robusta entre múltiples servicios (Telegram, Google, n8n).  
- **Automatización de Workflows**: Implementación de pipelines de datos complejos, lógicos y programados.  
- **Arquitectura de Sistemas**: Diseño de un sistema multiagente con flujos de datos para registro y análisis.  
- **Procesamiento de Lenguaje Natural (PLN)**: Aplicación práctica de LLMs para extraer, clasificar e inferir información de texto no estructurado.  

---

## 🔍 Casos de Uso

- **Análisis de Patrones**: Identificar los *triggers* conductuales que impulsan los gastos (ej: estrés, aburrimiento, celebración).  
- **Optimización Financiera**: Detectar áreas de mejora en hábitos de consumo basadas en motivaciones, no solo en categorías.  
- **Reportes Automatizados**: Generar insights estratégicos semanales sin ninguna intervención manual.  
- **Seguimiento en Tiempo Real**: Monitorear continuamente el comportamiento financiero para una mayor autoconciencia.  

---

## 📈 Resultados

Este sistema trasciende el simple tracking de gastos para convertirse en una herramienta de análisis conductual financiero. Proporciona la base para tomar decisiones más informadas y conscientes sobre el manejo del dinero personal, conectando los gastos con las emociones y contextos que los originan.

> **Nota**: Este proyecto representa una aplicación práctica y de punta a punta de automatización e IA para resolver un problema real, demostrando capacidades de integración de sistemas, PLN y la generación de insights verdaderamente accionables.
