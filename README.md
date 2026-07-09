# HIA - Health Insights Agent

**Tu Agente Personal de Insights de Salud con IA**

Aplicación web construida con Streamlit que permite a los usuarios cargar documentos de salud (PDFs) y obtener respuestas e insights personalizados mediante un agente conversacional con IA.

## 🚀 Stack Tecnológico

- **Frontend/App**: [Streamlit](https://streamlit.io/)
- **LLM**: [Groq](https://groq.com/) (inferencia rápida de modelos de lenguaje)
- **Autenticación y Base de Datos**: [Supabase](https://supabase.com/)
- **RAG (Retrieval-Augmented Generation)**: LangChain + FAISS (búsqueda vectorial)
- **Procesamiento de PDFs**: pdfplumber

## 📋 Requisitos previos

- Python 3.10+
- Cuenta gratuita en [Groq Console](https://console.groq.com/keys)
- Cuenta gratuita en [Supabase](https://supabase.com/)

## ⚙️ Instalación

1. **Clona el repositorio**
```bash
   git clone https://github.com/technssoluciones-dev/Agente-de-Salud-Insights.git
   cd Agente-de-Salud-Insights
```

2. **Crea un entorno virtual**
```bash
   python -m venv venv
   venv\Scripts\activate    # Windows
   # source venv/bin/activate   # Linux/Mac
```

3. **Instala las dependencias**
```bash
   pip install -r requirements.txt
```

4. **Configura tus credenciales**

   Crea el archivo `.streamlit/secrets.toml` con el siguiente contenido:
```toml
   GROQ_API_KEY = "tu_groq_api_key_aqui"
   SUPABASE_URL = "https://tu-proyecto.supabase.co"
   SUPABASE_KEY = "tu_anon_key_aqui"
```

5. **Crea las tablas en Supabase**

   Ve al **SQL Editor** de tu proyecto en Supabase y ejecuta el script ubicado en `public/db/script.sql`.

## ▶️ Cómo correr la aplicación

```bash
streamlit run src/main.py
```

La aplicación se abrirá automáticamente en `http://localhost:8501`.

## 📁 Estructura del proyecto

├── src/
│   ├── agents/       # Lógica del agente conversacional (Groq)
│   ├── auth/         # Autenticación de usuarios (Supabase)
│   ├── components/   # Componentes de UI reutilizables
│   ├── config/       # Configuración de la app y prompts
│   ├── services/     # Servicios (AI, PDF, etc.)
│   ├── utils/        # Utilidades generales
│   └── main.py       # Punto de entrada de la app
├── public/
│   └── db/
│       └── script.sql  # Script de creación de tablas en Supabase
└── requirements.txt

## 🚧 Estado del proyecto

Este proyecto está **en desarrollo activo**. Funcionalidades y estructura pueden cambiar.

## 📄 Licencia

_Pendiente de definir._