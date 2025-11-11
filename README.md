# 🧠 Proyecto: Modelo Predictivo de Score de Crédito Hipotecario

## 🎯 Objetivo y Resumen

Desarrollar y validar un modelo de **Machine Learning** capaz de predecir el riesgo crediticio (probabilidad de incumplimiento) en solicitantes de créditos hipotecarios. El objetivo principal fue automatizar el proceso de validación sobre una base de **más de 50,000 registros**, proporcionando una puntuación objetiva para la toma de decisiones.

---

## 🛠️ Metodología y Herramientas

| Etapa | Descripción | Herramienta Clave |
| :--- | :--- | :--- |
| **Ingesta y Limpieza** | Carga, validación y estandarización de datos. Se utilizó SQL para la limpieza inicial y Pandas para el preprocesamiento en Python. | `SQL`, `Python (Pandas)` |
| **Análisis Exploratorio (EDA)** | Identificación de *features* (variables) críticas y análisis de desbalance de clases. | `Jupyter Notebooks` |
| **Modelado ML** | Implementación, entrenamiento y ajuste fino del modelo. Se optó por **Árboles de Decisión** por su interpretabilidad en el sector financiero. | `Python (Scikit-learn)` |
| **Visualización** | Dashboard ejecutivo para mostrar la distribución de scores de riesgo y las variables de mayor impacto. | `Power BI` |

---

## ✨ Resultados Clave

### 1. Desempeño del Modelo
El modelo basado en Árboles de Decisión demostró una alta capacidad predictiva:

| Métrica | Valor Obtenido |
| :--- | :--- |
| **Precisión (Accuracy)** | **79%** |
| **F1-Score** | 0.77 |
| **Área bajo la curva ROC (AUC)** | 0.81 |

### 2. Impacto Estratégico
El modelo permite a la institución:
* **Mitigar Riesgos:** Mejorar la precisión de evaluación en **+15%** al integrar el modelo con métricas financieras (VAN, TIR, RBC).
* **Eficiencia:** Automatizar una parte significativa del proceso de evaluación manual.


---

## 📚 Estructura y Contenidos del Repositorio

| Archivo/Carpeta | Descripción |
| :--- | :--- |
| **`notebooks/`** | Jupyter Notebooks que contienen el EDA y el código final del modelo (ej: `credit_score_model.ipynb`). |
| **`data/`** | Datos anonimizados utilizados (ej: `base_50000_registros_anonimizada.csv`). **Nota:** La información sensible no está incluida. |
| **`src/`** | Scripts de Python para la limpieza avanzada y funciones reutilizables. |
| **`dashboard.png`** | Captura de pantalla del Dashboard de Power BI con los resultados y *score* de riesgo. |
| **`requirements.txt`** | Lista de librerías necesarias para ejecutar el código (`scikit-learn`, `pandas`, etc.). |

---

## 💡 Lecciones Aprendidas

* **Desbalance de Clases:** Se manejó activamente el desbalance entre clientes de bajo y alto riesgo, optimizando el umbral de clasificación para priorizar la minimización de Falsos Negativos (identificar a un mal pagador como bueno).
* **Interpretabilidad:** Se eligió el Árbol de Decisión sobre otros modelos más complejos para garantizar la **transparencia** ante los reguladores y el comité de créditos, explicando claramente los factores de riesgo.
