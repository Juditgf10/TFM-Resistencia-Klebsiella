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

## 🚀 Instalación rápida

```bash
# 1. Clonar el repositorio
git clone https://github.com/<usuario>/TFM-Resistencia-Klebsiella.git
cd TFM-Resistencia-Klebsiella

# 2. (Opcional) Crear y activar un entorno virtual
python -m venv venv
# Linux / macOS
source venv/bin/activate
# Windows PowerShell
.\venv\Scripts\Activate.ps1

# 3. Instalar dependencias
pip install -r requirements.txt

## 📈 Resultados Principales

Se han entrenado y evaluado tres modelos de clasificación para predecir la resistencia a carbapenémicos en *K. pneumoniae*. La optimización se realizó mediante `GridSearchCV` utilizando validación cruzada estratificada (`StratifiedKFold`) y técnicas para el desbalance de clases.

Los resultados en el conjunto de prueba son los siguientes:

* **Random Forest:**
    * Optimizado por: *Recall + ADASYN*
    * AUC: **0.506**
    * Accuracy general: 77%
* **Support Vector Machines (SVM):**
    * Optimizado por: *Recall* (con `class_weight='balanced'`)
    * AUC: **0.512**
    * Accuracy general: 77%
* **XGBoost:**
    * Optimizado por: *Recall*
    * AUC: **0.502**
    * Accuracy general: 77%

Las matrices de confusión y las curvas ROC detalladas para cada modelo se han generado y se encuentran en la carpeta `figures/`.

## 🔍 Análisis y Discusión de Resultados

Los valores de AUC obtenidos para los tres modelos son cercanos a 0.5, lo que indica que, a pesar de la optimización y el uso de técnicas de balanceo, los modelos tienen una capacidad limitada para discriminar de forma robusta entre las cepas resistentes y sensibles. Este resultado sugiere la alta complejidad en la relación genotipo-fenotipo de la resistencia a carbapenémicos, que podría no ser capturada completamente por las características o los modelos empleados en esta fase.

La *accuracy* general, aunque moderada, es engañosa en contextos de desbalance de clases, y el bajo *recall* para la clase minoritaria (resistente) confirma la dificultad para identificar correctamente los casos de interés clínico. Sin embargo, el análisis de importancia de características (disponible en `figures/`) del modelo XGBoost ha permitido identificar genes clave que son influyentes en la predicción, lo que puede proporcionar valiosa información para futuras investigaciones biomédicas.

## ✅ Conclusiones

Este Trabajo Final de Máster ha sentado las bases para el desarrollo de modelos predictivos de resistencia a carbapenémicos en *Klebsiella pneumoniae*. A pesar de las limitaciones observadas en el rendimiento predictivo actual de los modelos (reflejado en los valores AUC), se ha establecido un pipeline para el preprocesamiento de datos genómicos y la evaluación de modelos de Machine Learning. Los hallazgos subrayan la necesidad de enfoques más complejos y un conocimiento más profundo de los mecanismos moleculares de resistencia.

## ➡️ Trabajos futuros

Para avanzar en esta línea de investigación, se proponen las siguientes mejoras:

* **Ingeniería de Características Avanzada:** Explorar características más allá de la presencia/ausencia de genes, como polimorfismos de un solo nucleótido (SNPs), análisis de promotores, y la integración de datos de expresión génica.
* **Exploración de Modelos Más Complejos:** Investigar el potencial de modelos de Deep Learning para capturar patrones más intrincados en secuencias genómicas.
* **Validación Externa:** Evaluar los modelos con conjuntos de datos independientes y de diferentes orígenes para asegurar su generalización.

---

## 📜 Licencia
Este proyecto es de uso académico y se publica bajo la licencia [MIT](LICENSE).
