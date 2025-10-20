# My Course Agent 🤖

Un agente inteligente construido con LangGraph que proporciona información meteorológica utilizando herramientas personalizadas.

## 📋 Descripción

Este proyecto es un agente conversacional desarrollado como parte del curso de LangGraph en Platzi. El agente utiliza OpenAI GPT-4o-mini y está equipado con una herramienta personalizada para consultar el clima de diferentes ciudades.

## ✨ Características

- 🌤️ **Consulta meteorológica**: Obtén información del clima para cualquier ciudad
- 🤖 **Agente inteligente**: Basado en LangGraph con capacidades de ReAct
- 🔧 **Herramientas personalizadas**: Funciones especializadas para tareas específicas
- 🌐 **API REST**: Interfaz HTTP para interactuar con el agente
- 🎨 **Interfaz gráfica**: Studio UI para visualización y debugging

## 🚀 Inicio Rápido

### Prerrequisitos

- Python 3.8 o superior
- Cuenta de OpenAI con API key

### 📦 Instalación

1. **Clona el repositorio**
   ```bash
   git clone https://github.com/dmarmijosa/first-langgrapfh.git
   cd my_course_agent
   ```

2. **Crea un entorno virtual**
   ```bash
   python -m venv .venv
   source .venv/bin/activate  # En Windows: .venv\Scripts\activate
   ```

3. **Instala las dependencias**
   ```bash
   pip install -r requeriment.txt
   ```

4. **Configura las variables de entorno**
   
   Crea un archivo `.env` en la raíz del proyecto:
   ```env
   OPENAI_API_KEY=tu_api_key_de_openai_aqui
   ```

### 🏃‍♂️ Ejecución

Ejecuta el servidor de desarrollo de LangGraph:

```bash
langgraph dev
```

El servidor estará disponible en:
- 🚀 **API**: http://127.0.0.1:2024
- 🎨 **Studio UI**: https://smith.langchain.com/studio/?baseUrl=http://127.0.0.1:2024
- 📚 **Documentación API**: http://127.0.0.1:2024/docs

## 🛠️ Estructura del Proyecto

```
my_course_agent/
├── main.py              # Definición del agente principal
├── langgraph.json       # Configuración de LangGraph
├── requeriment.txt      # Dependencias del proyecto
├── .env                 # Variables de entorno (no incluido en git)
├── .gitignore          # Archivos ignorados por git
└── README.md           # Este archivo
```

## 📝 Uso

### Ejemplo de consulta

Una vez que el servidor esté ejecutándose, puedes interactuar con el agente:

```python
# Ejemplo de invocación
response = agent.invoke({
    "messages": [
        {"role": "user", "content": "¿Cómo está el clima en Madrid?"}
    ]
})
```

### Herramientas disponibles

#### 🌤️ get_weather
- **Descripción**: Obtiene información meteorológica para una ciudad específica
- **Parámetros**: `city` (str) - Nombre de la ciudad
- **Retorna**: Información del clima (actualmente simulada)

## 🔧 Configuración

### langgraph.json
```json
{
  "dependencies": ["."],
  "graphs": {
    "agent": "./main.py:agent"
  },
  "env": ".env"
}
```

### Variables de entorno requeridas
- `OPENAI_API_KEY`: Tu clave API de OpenAI

## 🤝 Contribuir

1. Fork el proyecto
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## 📚 Recursos de Aprendizaje

- [Documentación de LangGraph](https://langchain-ai.github.io/langgraph/)
- [Curso de LangGraph en Platzi](https://platzi.com)
- [OpenAI API Documentation](https://platform.openai.com/docs/)

## 🐛 Solución de Problemas

### Error: "The api_key client option must be set"
- Asegúrate de que tu archivo `.env` contenga `OPENAI_API_KEY=tu_api_key`
- Verifica que el archivo `.env` esté en la raíz del proyecto

### Error: "create_react_agent() got unexpected keyword arguments"
- Verifica que estés usando la sintaxis correcta para `create_react_agent`
- Consulta la documentación de LangGraph para parámetros válidos

## 📄 Licencia

Este proyecto está bajo la Licencia MIT. Ver el archivo `LICENSE` para más detalles.

## 👨‍💻 Autor

**Danny Armijos** - [@dmarmijosa](https://github.com/dmarmijosa)

---

⭐ ¡Si este proyecto te fue útil, no olvides darle una estrella!