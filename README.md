# Proyecto-1-LSA-con-SVD

Este proyecto aplica técnicas de procesamiento de lenguaje natural (NLP) y álgebra lineal para identificar estructuras temáticas latentes en un corpus de reseñas de la plataforma Steam. Utilizando la **Descomposición en Valores Singulares (SVD)**, se logra reducir la dimensionalidad de los datos para descubrir tópicos comunes entre miles de documentos.

## Instrucciones de Ejecución

Este proyecto fue desarrollado íntegramente en **Google Colab**, por lo que se recomienda su uso para asegurar la compatibilidad de las librerías y el entorno de ejecución.

1. **Subir el Notebook**: Carga el archivo `Proyecto.ipynb` a tu unidad de Google Drive o ábrelo directamente en Colab.
2. **Entorno de Hardware**: No se requiere GPU; el entorno estándar de CPU de Colab es suficiente para procesar los 15,000 documentos.
3. **Ejecución en Orden**: Ejecuta las celdas de forma secuencial. El script está diseñado para instalar y configurar las dependencias necesarias automáticamente.

## Dataset

El conjunto de datos utilizado es el **Steam Reviews Dataset**, disponible en Kaggle. 

* **Enlace al Dataset**: [Kaggle - Steam Reviews Dataset](https://www.kaggle.com/datasets/luthfim/steam-reviews-dataset)
* **Descarga Automática**: El código utiliza la librería `kagglehub` para descargar los datos directamente al entorno de ejecución. No es necesario descargar el archivo manualmente ni subirlo al repositorio.

## Requisitos e Instalación

Para reproducir los resultados localmente o en Colab, se requieren las siguientes librerías de Python:

```python
import kagglehub
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import re
from sklearn.feature_extraction.text import TfidfVectorizer
from sklearn.metrics.pairwise import cosine_similarity
