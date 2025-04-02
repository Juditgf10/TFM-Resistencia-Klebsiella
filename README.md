# Predicción de Resistencia a Carbapenémicos en *Klebsiella pneumoniae* mediante Machine Learning

## 📌 Descripción del Proyecto
Este proyecto forma parte del Trabajo Final de Máster (TFM) y tiene como objetivo el desarrollo de un modelo de aprendizaje automático para predecir la resistencia a antibióticos en *Klebsiella pneumoniae*. Utilizando datos genómicos y fenotípicos de bases de datos públicas, aplicaremos técnicas de bioinformática y machine learning para identificar patrones en la resistencia a carbapenémicos.

## 📂 Estructura del Repositorio
```
📂 TFM-Resistencia-AMR
├── 📁 data/               # Conjunto de datos utilizados en el estudio (FASTA, Excel, etc.)
├── 📁 notebooks/          # Notebooks de Jupyter con el preprocesamiento y análisis
├── 📁 src/               # Código Python modularizado (opcional)
├── 📁 docs/              # Documentación del proyecto
├── 📄 README.md          # Descripción del proyecto e instrucciones
└── 📄 .gitignore         # Archivos a excluir del repositorio
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
- **Scikit-learn & XGBoost**: Implementación de modelos de machine learning.
- **Matplotlib & Seaborn**: Visualización de datos.
- **GitHub**: Control de versiones y almacenamiento del código.

## 🚀 Instalación y Uso
1. Clona el repositorio:
   ```bash
   git clone https://github.com/tu-usuario/TFM-Resistencia-AMR.git
   cd TFM-Resistencia-AMR
   ```
2. Crea un entorno virtual (opcional pero recomendado):
   ```bash
   python -m venv env
   source env/bin/activate  # En Windows: env\Scripts\activate
   ```
3. Instala las dependencias:
   ```bash
   pip install -r requirements.txt
   ```
4. Abre Jupyter Notebook y ejecuta los análisis:
   ```bash
   jupyter notebook
   ```

## 📌 Próximos Pasos
✅ Carga y preprocesamiento de datos  
🔄 Análisis exploratorio y visualización  
📈 Entrenamiento y evaluación de modelos  
📢 Publicación de resultados y documentación  

## 📜 Licencia
Este proyecto es de uso académico y se publica bajo la licencia [MIT](LICENSE).
