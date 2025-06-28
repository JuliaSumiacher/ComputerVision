# Sistema de Detección y Clasificación de Razas de Perros

Este repositorio implementa un pipeline completo para detección y clasificación de razas de perros en imágenes, incluyendo búsqueda por similitud, clasificación por transferencia y CNN propia, detección en escenas complejas, optimización y exportación de anotaciones.

## Requisitos

- Python 3.9 o superior
- [Google Colab](https://colab.research.google.com/) (recomendado)
- Para entorno local: Linux/MacOS/Windows, preferiblemente con GPU o CPU potente.

## Instalación de dependencias

### Opción 1: Google Colab (Recomendado)

1. Sube el archivo `TP_CV.ipynb` a tu Google Drive.
2. Abre el cuaderno en Colab.
3. Ejecuta las celdas desde el inicio. El propio notebook instalará las dependencias con:
    ```python
    !pip install torch torchvision ultralytics gradio scikit-learn opencv-python matplotlib
    ```
4. Descarga el [dataset de 70 razas de perros de Kaggle](https://www.kaggle.com/datasets/gpiosenka/70-dog-breedsimage-data-set?resource=download) y súbelo a tu Drive, o descarga desde Colab con las instrucciones del notebook.

### Opción 2: Entorno local

1. Clona el repositorio:
    ```bash
    git clone https://github.com/usuario/proyecto-razas-perros.git
    cd proyecto-razas-perros
    ```
2. Crea un entorno virtual (opcional pero recomendado):
    ```bash
    python -m venv venv
    source venv/bin/activate  # o .\venv\Scripts\activate en Windows
    ```
3. Instala las dependencias:
    ```bash
    pip install -r requirements.txt
    ```
    > El archivo `requirements.txt` debe contener:
    ```
    torch
    torchvision
    ultralytics
    gradio
    scikit-learn
    opencv-python
    matplotlib
    ```
4. Descarga y descomprime el dataset de Kaggle en la carpeta `dataset/`.

---

## Ejecución de la aplicación Gradio

### **Versión 1: Búsqueda por similitud (Etapa 1)**

```bash
python gradio_similitud.py

