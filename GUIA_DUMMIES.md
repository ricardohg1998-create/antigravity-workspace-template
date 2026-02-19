# 🪐 Guía de Uso para Dummies - Google Antigravity Workspace

¡Bienvenido! Esta es tu guía paso a paso para convertir tu ordenador en un potente sistema de Agentes de IA. No necesitas ser un experto, solo sigue las instrucciones.

---

## 🧐 ¿Qué es esto?

Imagina que tienes un empleado virtual muy inteligente (una IA) que vive en tu ordenador.
- **Tiene Memoria Infinita:** Recuerda lo que le dices.
- **Usa Herramientas:** Puede ejecutar código Python, buscar archivos, y mucho más.
- **Es Extensible:** Puedes enseñarle nuevas habilidades simplemente copiando archivos.

Este proyecto es la "casa" donde vive ese empleado.

---

## 🛠️ Requisitos Previos (Antes de empezar)

Necesitas tener instaladas dos cosas básicas en tu ordenador. Si no las tienes, descárgalas e instálalas:

1.  **Python (Versión 3.8 o superior)**
    *   Descarga: [python.org/downloads](https://www.python.org/downloads/)
    *   🚨 **IMPORTANTE:** Al instalar, marca la casilla **"Add Python to PATH"**.

2.  **Git**
    *   Descarga: [git-scm.com/downloads](https://git-scm.com/downloads)
    *   Lo usaremos para descargar este proyecto.

3.  **Visual Studio Code (Recomendado)**
    *   Descarga: [code.visualstudio.com](https://code.visualstudio.com/)
    *   Es el mejor editor para ver y modificar los archivos de tu agente.

---

## 🚀 Instalación (Solo la primera vez)

1.  **Descarga el proyecto (Clonar):**
    *   Abre una terminal (o PowerShell) en la carpeta donde quieras guardar el proyecto.
    *   Escribe:
        ```bash
        git clone https://github.com/study8677/antigravity-workspace-template.git mi-agente
        ```
    *   Entra en la carpeta:
        ```bash
        cd mi-agente
        ```

2.  **Ejecuta el instalador automático:**
    *   En Windows, simplemente haz doble clic en el archivo `install.bat` o ejecútalo desde la terminal:
        ```cmd
        install.bat
        ```
    *   Este script creará un entorno virtual e instalará todas las librerías necesarias por ti.

---

## 🔑 Configuración (La Llave Maestra)

Para que la IA funcione, necesitas darle una "llave" (API Key) de Google Gemini.

1.  **Consigue tu API Key:**
    *   Ve a [Google AI Studio](https://aistudio.google.com/app/apikey).
    *   Crea una API Key gratuita.

2.  **Configura el proyecto:**
    *   En la carpeta del proyecto, verás un archivo llamado `.env` (si no está, renombra `.env.example` a `.env`).
    *   Abre el archivo `.env` con el Bloc de notas o VS Code.
    *   Busca la línea que dice:
        ```ini
        GOOGLE_API_KEY=your_api_key_here
        ```
    *   Cambia `your_api_key_here` por tu clave real que copiaste antes.
    *   Guarda el archivo.
    *   **Nota:** Si vas a usar otros modelos (como OpenAI), también puedes configurarlo aquí.

---

## 🤖 ¡A Jugar! (Cómo usar el Agente)

Ahora viene lo divertido. Vamos a dar órdenes a tu agente.

1.  **Abre la terminal en la carpeta del proyecto.**
    *   En VS Code: Ve al menú `Terminal` -> `New Terminal`.

2.  **Ejecuta al agente:**
    Escribe el siguiente comando (puedes cambiar el texto entre comillas por lo que tú quieras):

    ```bash
    python src/agent.py "Escribe un poema sobre un robot que ama el café"
    ```

3.  **¿Qué pasará?**
    *   El agente "pensará" (verás el proceso de pensamiento en la pantalla).
    *   Si necesita herramientas, las usará.
    *   Te dará una respuesta final.

---

## 🧠 Personalización (Hazlo tuyo)

### 1. Enseñarle nuevas Herramientas
¿Quieres que tu agente pueda hacer algo nuevo, como "Calcular el ROI de una inversión"?
*   Ve a la carpeta `src/tools/`.
*   Crea un archivo Python nuevo, por ejemplo `calculadora.py`.
*   Escribe una función normal de Python dentro:
    ```python
    def calcular_roi(inversion: float, ganancia: float) -> str:
        """Calcula el Retorno de Inversión dado un costo inicial y ganancia final."""
        resultado = (ganancia - inversion) / inversion * 100
        return f"El ROI es del {resultado}%"
    ```
*   ¡Listo! La próxima vez que ejecutes el agente, él **automáticamente sabrá** que tiene esa herramienta y cómo usarla. No necesitas registrar nada más.

### 2. Darle Conocimiento (Contexto)
¿Quieres que el agente sepa sobre tu empresa o proyecto específico sin tener que explicárselo cada vez?
*   Ve a la carpeta `.context/`.
*   Crea un archivo Markdown nuevo, por ejemplo `mi_empresa.md`.
*   Escribe toda la información que quieras que el agente sepa.
    ```markdown
    # Reglas de Mi Empresa
    Siempre respondemos con tono amable y profesional.
    Nuestro producto principal es "SuperWidget 3000".
    ```
*   ¡Listo! El agente leerá esto antes de responderte cualquier cosa.

---

## ❓ Solución de Problemas Frecuentes

*   **Error: "Python no se reconoce..."**
    *   Seguro que no marcaste "Add Python to PATH" al instalar Python. Reinstala y marca esa casilla.

*   **Error: "ModuleNotFoundError"**
    *   Asegúrate de haber ejecutado `install.bat`. Si sigue fallando, intenta instalar las dependencias manualmente:
        ```bash
        pip install -r requirements.txt
        ```

*   **El agente no hace nada o da error de API:**
    *   Revisa tu archivo `.env`. Asegúrate de que `GOOGLE_API_KEY` es correcta, no tiene espacios extra y el archivo se llama `.env` (no config.env ni nada parecido).

---

¡Disfruta creando tu ejército de agentes autónomos! 🚀
