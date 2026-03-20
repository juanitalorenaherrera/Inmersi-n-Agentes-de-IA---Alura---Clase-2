# 🤖 Inmersión en Agentes de IA — RAG & Agente Autónomo

Proyecto práctico donde evoluciono desde un sistema RAG clásico hasta un agente capaz de **decidir cómo responder** según el contexto.

No es solo consulta de documentos… es inteligencia aplicada 🧠⚡

---

## 🧠 ¿Qué hace este proyecto?

Este repositorio implementa un sistema de IA que:

- Procesa documentos (PDFs)
- Genera embeddings semánticos
- Almacena información en un vector store (FAISS)
- Recupera contexto relevante
- Genera respuestas con modelos LLM
- Decide dinámicamente entre usar **datos internos o información web**

---

## 🚀 Evolución del sistema

### 🔹 Clase 2 — RAG (Retrieval-Augmented Generation)

Pipeline base:

Datos → Embeddings → Vector Store → Retrieval → LLM → Respuesta

Incluye:

- 📄 Carga de PDFs  
- ✂️ Chunking (fragmentación de texto)  
- 🔍 Generación de embeddings  
- ⚡ Almacenamiento en FAISS  
- 📚 Recuperación de contexto  
- 🤖 Generación con LLM  

👉 Resultado: un sistema que responde usando conocimiento interno

---

### 🔹 Clase 3 — Agente Inteligente

El sistema evoluciona a un agente que toma decisiones:

Pregunta → Clasificación → (RAG 🧠 | Web 🌐) → Contexto → LLM → Respuesta

Ahora el modelo:

- Analiza la intención de la pregunta  
- Decide la mejor fuente de información  
- Combina múltiples entradas  

👉 Resultado: un agente más flexible, preciso y útil

---

## 🧭 Arquitectura del agente

```mermaid
flowchart TD

A[Usuario] --> B[Agente]

B --> C{¿Fuente?}

C -->|RAG| D[Buscar en PDFs]
C -->|Web| E[Buscar en Internet]

D --> F[FAISS Vector Store]
F --> G[Contexto relevante]

E --> H[Resultados Web]

G --> I[LLM - Gemini]
H --> I

I --> J[Respuesta]

🧠 Lógica de decisión

El agente clasifica cada pregunta:

📄 RAG → si la información está en los documentos

🌐 Web → si requiere conocimiento externo

Ejemplos

“¿Dónde se concentró el mix de productos?” → RAG

“¿Cuántos mundiales tiene Brasil?” → Web

.
├── Inmersión_Agentes_de_IA_Alura_Clase_2_+3_Orli.ipynb
├── Inmersión_Agentes_de_IA_Alura_Clase_2_Orli.ipynb
├── README.md
└── LICENSE
⚙️ Tecnologías utilizadas

LangChain

FAISS

Google Gemini

SerpAPI

LangGraph

🛠️ Requisitos

Python 3.10+

Google Colab (recomendado)

API Keys:

Google Gemini

SerpAPI

▶️ Uso
git clone https://github.com/Orliluq/Inmersion_Agentes_de_IA_Alura_Clase_2.git
cd Inmersion_Agentes_de_IA_Alura_Clase_2

Abre el notebook en Colab

Ejecuta las celdas en orden

Realiza tus propias consultas

⚠️ Consideraciones

Puede haber límites de uso en APIs (errores 429)

Se recomienda trabajar con datasets pequeños en pruebas

Para producción: usar embeddings locales o planes pagos

🎯 ¿Qué demuestra este proyecto?

Implementación de RAG real

Uso de búsqueda semántica

Integración con APIs externas

Diseño de agentes con toma de decisiones

Arquitectura moderna de sistemas de IA

📜 Licencia

MIT

✨ Autor

Juanita Lorena Herrera Herrera 🧠⚡
Desarrolladora Web & Software | Explorando el futuro de la inteligencia artificial

