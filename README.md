# Conexión a la API de Gemini

Script en Python que se conecta a la API de Google Gemini (Google AI Studio) usando la librería oficial `google-genai`, envía un prompt de prueba y muestra la respuesta del modelo en consola.

> Proyecto realizado para la asignatura ** Desarrollo de aplicaciones con IA**.

## Requisitos previos

- Python 3.10 o superior instalado
- Una cuenta de Google
- Una API Key de Gemini (gratuita), obtenida desde [Google AI Studio](https://aistudio.google.com/)

## Instalación y configuración

### 1. Clonar el repositorio

```bash
git clone https://github.com/<tu-usuario>/<nombre-del-repo>.git
cd <nombre-del-repo>
```

### 2. Crear y activar el entorno virtual

**Windows:**
```bash
python -m venv venv
.\venv\Scripts\Activate
```

**macOS / Linux:**
```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Instalar las dependencias

```bash
pip install -r requirements.txt
```

Esto instala `google-genai` (SDK oficial de Google para Gemini) y `python-dotenv` (para leer variables de entorno desde un archivo `.env`).

### 4. Configurar la API Key

1. Ingresa a [Google AI Studio](https://aistudio.google.com/) con tu cuenta de Google.
2. En el menú lateral, haz clic en **"Get API key"** → **"Create API key"**.
3. Asigna la clave a un proyecto (o crea uno nuevo) y cópiala.
4. En la raíz del proyecto, crea un archivo llamado `.env` (puedes copiar `.env.example` y renombrarlo) y pega tu clave así:

```
GEMINI_API_KEY=tu_clave_aqui
```

## Ejecución

Con el entorno virtual activado, ejecuta:

```bash
python app_gemini.py
```

El script:
1. Carga la API Key desde el archivo `.env`.
2. Inicializa el cliente de conexión con `genai.Client()`.
3. Envía un prompt al modelo `gemini-3-flash-preview` pidiéndole que se presente como asistente del curso.
4. Imprime en consola la respuesta generada por el modelo.

### Salida esperada

```
🚀 Conectando con el motor de Gemini ...

--- Respuesta Recibida ---
[Aquí aparece el texto generado por Gemini]
--------------------------
```

## Evidencia de ejecución

Captura de pantalla de la ejecución exitosa del script, mostrando la conexión con la API y la respuesta recibida de Gemini:

<img width="1606" height="1029" alt="ConexiónAPI" src="https://github.com/user-attachments/assets/7b3cc5f9-8e5c-46d1-9528-19ecf0520a35" />


## Estructura del proyecto

```
├── app_gemini.py       # Script principal de conexión con la API de Gemini
├── requirements.txt    # Dependencias del proyecto
├── .env.example        # Plantilla de variables de entorno (sin clave real)
├── .gitignore           # Archivos/carpetas excluidos del control de versiones
└── README.md            # Este archivo
```

## Tecnologías utilizadas

- [Python](https://www.python.org/)
- [google-genai](https://pypi.org/project/google-genai/) — SDK oficial de Google para la API de Gemini
- [python-dotenv](https://pypi.org/project/python-dotenv/) — Gestión de variables de entorno

## Autor

Jose Luis Patiño | 506232065
Ingeniería de Sistemas
Fundación Universitaria Konrad Lorenz
