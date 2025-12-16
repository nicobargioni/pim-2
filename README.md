============================================================
============================================================

🧠 Monitor de Atención Visual en Tiempo Real

Este proyecto implementa un sistema de monitoreo de atención en tiempo real utilizando visión por computadora con MediaPipe, visualización con Streamlit y procesamiento con OpenCV.

============================================================
============================================================

🎯 Objetivo

Detectar si un usuario está prestando atención frente a la cámara, evaluando la posición del rostro y la orientación de la mirada, con validación adicional mediante segmentación semántica para asegurar que hay una persona real en escena.

============================================================
============================================================

🔍 Funcionalidad

Detección facial en vivo con MediaPipe FaceMesh

Segmentación de personas con MediaPipe SelfieSegmentation, para validar que haya una persona real frente a cámara

Evaluación del índice de atención con criterios de posición de nariz y ojos

Penalizaciones si la cabeza está baja o la mirada desviada

Visualización del análisis en tiempo real con OpenCV + gráfico de atención con matplotlib

Al detener el monitoreo, generación de un gráfico final de resumen.

============================================================
============================================================

🗂️ Estructura del proyecto

monitor_atencion/
├── main.py                 # Interfaz principal con Streamlit
├── detector.py             # Lógica de atención y landmarks faciales
├── segmentacion.py         # Validación de presencia humana por segmentación
├── graficos.py             # Visualización del índice de atención
├── requirements.txt        # Lista de dependencias
└── README.md               # Documentación del proyecto

============================================================
============================================================

▶️ Instrucciones de uso

Instalar dependencias:

pip install -r requirements.txt

Ejecutar el sistema:

streamlit run main.py

Si no funciona, ejecutar python -m streamlit run main.py

============================================================
============================================================

⚙️ Dependencias principales

- streamlit: Interfaz web interactiva
- opencv-python: Captura y procesamiento de video
- mediapipe: Detección facial y segmentación
- numpy: Cálculos numéricos
- matplotlib: Gráficos en tiempo real

============================================================
============================================================

🧩 Contenidos de Clases Aplicados

✅ Clase 7: Reconocimiento de patrones

Concepto aplicado: Detección de patrones faciales mediante landmarks.

En el proyecto: Se utiliza MediaPipe FaceMesh para detectar 468 puntos clave del rostro, permitiendo identificar la posición de nariz, ojos, frente y barbilla para evaluar la orientación facial.

✅ Clase 8: Visión por computadora

Concepto aplicado: Procesamiento de imágenes y video con OpenCV.

En el proyecto: Se captura video de la webcam frame a frame, se convierte de BGR a RGB para MediaPipe, se aplica flip horizontal (efecto espejo), y se dibujan anotaciones visuales sobre cada frame.

✅ Clase 9: Inteligencia artificial aplicada

Concepto aplicado: Redes neuronales convolucionales y aprendizaje profundo.

En el proyecto: MediaPipe FaceMesh utiliza internamente modelos de deep learning para detectar landmarks faciales. MediaPipe SelfieSegmentation usa CNNs para segmentación semántica persona/fondo.

✅ Clase 10: Librerías especializadas

Concepto aplicado: Uso de librerías de visión por computadora.

En el proyecto: Se integran OpenCV (captura de video, procesamiento de frames), MediaPipe (detección facial y segmentación), NumPy (operaciones con arrays) y Matplotlib (visualización de gráficos).

✅ Clase 11: Detección en tiempo real

Concepto aplicado: Análisis continuo frame a frame con feedback inmediato.

En el proyecto: El sistema procesa la webcam en vivo, evaluando la atención en cada frame y actualizando el indicador visual y el gráfico en tiempo real.

✅ Clase 12: Análisis de comportamiento

Concepto aplicado: Métricas de atención y evaluación conductual basada en imágenes.

En el proyecto: Se implementa un índice de atención (0-100%) basado en la posición centrada de nariz y ojos, con penalizaciones por cabeza baja o mirada desviada. Se genera un resumen estadístico al finalizar.

============================================================
============================================================

👤 Autor

Desarrollado por Nicolás Bargioni | Año 2025
ISSD: Inteligencia Artificial y Ciencia de Datos
Materia: Procesamiento de Imágenes

============================================================
============================================================# pim-2
