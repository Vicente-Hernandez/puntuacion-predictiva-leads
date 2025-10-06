# Sistema de Lead Scoring Predictivo 🎯

![Python](https://img.shields.io/badge/python-3.9+-blue.svg)
![Scikit-learn](https://img.shields.io/badge/scikit--learn-1.x-orange)
![Pandas](https://img.shields.io/badge/pandas-2.x-yellow)
![License](https://img.shields.io/badge/license-MIT-green.svg)

Este repositorio, **`puntuacion-predictiva-leads`**, contiene un proyecto de Machine Learning diseñado para predecir la probabilidad de conversión de leads de ventas. El objetivo es optimizar los esfuerzos del equipo comercial, permitiéndoles priorizar los leads con mayor potencial de compra.

El sistema entrena y evalúa múltiples modelos de clasificación, selecciona el de mejor rendimiento y proporciona insights clave sobre los factores que más influyen en la decisión de compra.

---

## 🚀 Características Principales

* **Análisis Exploratorio de Datos (EDA):** Genera visualizaciones automáticas para entender la distribución de los datos y la relación entre las variables y la conversión.
* **Ingeniería de Características:** Realiza la limpieza de datos, imputación de valores faltantes y creación de variables relevantes como la `capacidad_pago`.
* **Modelado Comparativo:** Entrena, evalúa y compara tres modelos de clasificación robustos:
    1.  Regresión Logística
    2.  Random Forest
    3.  Gradient Boosting
* **Optimización de Hiperparámetros:** Utiliza `GridSearchCV` para encontrar la mejor configuración de parámetros para los modelos más complejos, maximizando su rendimiento.
* **Evaluación Robusta:** Mide el rendimiento de los modelos utilizando métricas clave como Accuracy, F1-Score y **ROC-AUC**, e incluye validación cruzada.
* **Análisis de Importancia:** Identifica y cuantifica las variables más influyentes en la predicción, ofreciendo insights de negocio accionables.
* **Dashboard de Resultados:** Genera un dashboard visual (`lead_scoring_dashboard.png`) que resume el rendimiento de los modelos, la matriz de confusión y las curvas ROC.

---

## 🛠️ Tecnologías Utilizadas

* **Python 3.9+**
* **Pandas:** para la manipulación y análisis de datos.
* **NumPy:** para operaciones numéricas.
* **Scikit-learn:** para el preprocesamiento, modelado y evaluación.
* **Matplotlib & Seaborn:** para la generación de gráficos y visualizaciones.
* **Openpyxl:** como motor para leer archivos `.xlsx`.

---

## ⚙️ Instalación y Configuración

Para ejecutar este proyecto en tu entorno local, sigue estos pasos:

1.  **Clona el repositorio:**
    ```bash
    git clone [https://github.com/tu-usuario/puntuacion-predictiva-leads.git](https://github.com/tu-usuario/puntuacion-predictiva-leads.git)
    cd puntuacion-predictiva-leads
    ```

2.  **Crea un entorno virtual (recomendado):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # En Windows: venv\Scripts\activate
    ```

3.  **Instala las dependencias:**
    El proyecto requiere las librerías listadas en `requirements.txt`.
    ```bash
    pip install -r requirements.txt
    ```
    *(Si no tienes un archivo `requirements.txt`, puedes crearlo con `pip freeze > requirements.txt` después de instalar las librerías manualmente).*

---

## 📈 Cómo Ejecutar el Notebook

1.  **Prepara tus datos:**
    Asegúrate de tener tu conjunto de datos, llamado **`simulacion_ventas.xlsx`**, en la raíz del proyecto.

    > **Nota Importante:** El script debe estar configurado para leer un archivo Excel. Asegúrate de que la línea de carga de datos en el código utilice `pd.read_excel('simulacion_ventas.xlsx')` en lugar de `pd.read_csv()`.

2.  **Abre y ejecuta el notebook:**
    El análisis se encuentra en el archivo **`sistema_lead_scoring_predictivo.ipynb`**. Ábrelo en un entorno compatible como **Google Colab**, **Jupyter Lab** o **VS Code**. Una vez abierto, puedes ejecutar todas las celdas para replicar el análisis.

3.  **Revisa los resultados:**
    Al finalizar la ejecución, encontrarás lo siguiente:
    * **Salida en el notebook:** Un reporte detallado de cada etapa del proceso.
    * **Carpeta `eda_plots/`:** Gráficos del análisis exploratorio de datos.
    * **Archivo `lead_scoring_dashboard.png`:** Un dashboard visual con la evaluación completa de los modelos.

---

## 📂 Estructura del Repositorio

```
puntuacion-predictiva-leads/
├── .gitignore
├── README.md
├── sistema_lead_scoring_predictivo.ipynb
├── simulacion_ventas.xlsx
├── requirements.txt
├── eda_plots/
│   ├── conversion_por_gse.png
│   └── ...
└── lead_scoring_dashboard.png
```

---

## 📄 Licencia

Este proyecto se distribuye bajo la Licencia MIT. Consulta el archivo `LICENSE` para más detalles.
