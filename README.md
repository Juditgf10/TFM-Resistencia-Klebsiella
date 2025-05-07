# Predicción de Resistencia a Carbapenémicos en *Klebsiella pneumoniae* mediante Machine Learning

## 📌 Descripción del Proyecto
Este proyecto forma parte del Trabajo Final de Máster (TFM) y tiene como objetivo el desarrollo de un modelo de aprendizaje automático para predecir la resistencia a antibióticos en *Klebsiella pneumoniae*. Utilizando datos genómicos y fenotípicos de bases de datos públicas, se aplican técnicas de bioinformática y machine learning para identificar patrones en la resistencia a carbapenémicos.

## 📂 Estructura del Repositorio
```
📂 TFM-Resistencia-Klebsiella
├── 📁 data/               # Conjunto de datos utilizados en el estudio (FASTA, Excel, etc.)
├── 📁 notebooks/          # Notebooks de Jupyter con el preprocesamiento y análisis
├── 📁 docs/              # Documentación del proyecto
└── 📄 README.md          # Descripción del proyecto e instrucciones
```

## 📊 Datos Utilizados
Los datos utilizados en este proyecto provienen de la plataforma **BVBRC (PATRIC)** e incluyen:
- **BVBRC_genome_amr.xlsx**: Datos de resistencia a antibióticos.
- **BVBRC_sp_gene.xlsx**: Genes de resistencia identificados en *Klebsiella pneumoniae*.
- **BVBRC_genome_feature.fasta**: Secuencias genómicas de los genes de resistencia.

## 🛠️ Herramientas y Tecnologías
- **Python**: Lenguaje principal para el desarrollo.
- **Jupyter Notebook**: Entorno de análisis y experimentación.
- **Pandas & NumPy**: Manipulación y procesamiento de datos.
- **Biopython**: Análisis de secuencias genómicas.
- **Scikit-learn:** Implementación de modelos de *machine learning* (Random Forest, SVM), división de datos y métricas de evaluación.
- **XGBoost:** Implementación del modelo de *gradient boosting* XGBoost.
- **imblearn:** Biblioteca para técnicas de manejo de desbalance de clases (ADASYN).
- **Matplotlib & Seaborn**: Visualización de datos.
- **GitHub**: Control de versiones y almacenamiento del código.

## 📌 Estado Actual del Proyecto (Mayo 2025)

En la fase actual del proyecto, se han completado las siguientes etapas:

1.  **Obtención y Preprocesamiento de Datos:** Se han descargado, limpiado y preparado los datos genómicos y fenotípicos de *Klebsiella pneumoniae* para el modelado. Se ha generado la matriz de características (presencia/ausencia de genes) y se ha dividido el dataset para entrenamiento y prueba.
2.  **Entrenamiento Inicial de Modelos:** Se han entrenado tres modelos de clasificación para predecir la resistencia a carbapenémicos:
    * **Random Forest:** Entrenado con datos sobremuestreados utilizando ADASYN y optimizado por *recall*.
    * **Support Vector Machines (SVM):** Entrenado con el parámetro `class_weight='balanced'` para abordar el desbalance de clases, optimizado por F1-score.
    * **XGBoost:** Entrenado y optimizado por la métrica *recall*.

Los resultados preliminares en el conjunto de prueba indican una *accuracy* general alrededor del 77-78% para los tres modelos. Sin embargo, el *recall* para la clase resistente (el objetivo principal) es bajo en todos los modelos, lo que sugiere una dificultad para identificar correctamente las cepas resistentes.


## 📌 Próximos Pasos
🔄 **Análisis de Resultados Detallado:** Evaluar en profundidad los resultados obtenidos, incluyendo el análisis de la importancia de las características (genes).
📈 **Experimentación con Mejoras:** Explorar técnicas avanzadas para el manejo del desbalance de clases, ingeniería de características (e.g., combinaciones de genes), y métodos de selección de características más informados.
 **Ajuste Fino de Modelos:** Realizar un ajuste más exhaustivo de los hiperparámetros de los modelos.
📢 **Documentación:** Continuar documentando el proceso y los hallazgos en los notebooks y en el informe del TFM. 

## 📜 Licencia
Este proyecto es de uso académico y se publica bajo la licencia [MIT](LICENSE).
