 📱 Análisis de comportamiento de usuarios en app de alimentos 
 
Este proyecto analiza el comportamiento de los usuarios dentro de una aplicación móvil de una empresa emergente de productos alimenticios. Se estudia el embudo de conversión y los resultados de un experimento A/A/B para evaluar el impacto de un rediseño tipográfico en la experiencia del usuario.


## 🧰 Tecnologías usadas

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-Data%20Analysis-blueviolet?logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-Numerical%20Computing-orange?logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-yellow?logo=matplotlib&logoColor=black)
![Seaborn](https://img.shields.io/badge/Seaborn-Statistical%20Plots-teal?logo=python&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-Statistical%20Tests-darkgreen?logo=scipy&logoColor=white)
![Statsmodels](https://img.shields.io/badge/Statsmodels-Hypothesis%20Testing-darkred?logo=python&logoColor=white)

## 🧪 Metodología

Este proyecto sigue una metodología de análisis exploratorio y validación estadística, estructurada en cinco etapas:

### 1. Preparación de datos
- Lectura del archivo `logs_exp_us.csv`
- Renombrado de columnas y conversión de tipos
- Extracción de fechas (`event_date`) y timestamps (`event_timestamp`)
- Identificación del período confiable de datos y exclusión de registros incompletos

### 2. Análisis del embudo de conversión
- Identificación de eventos clave:
  - `MainScreenAppear`
  - `OffersScreenAppear`
  - `CartScreenAppear`
  - `PaymentScreenSuccessful`
- Cálculo de proporciones de usuarios que avanzan entre etapas
- Evaluación de pérdidas por etapa
- Cálculo del porcentaje de usuarios que completan todo el recorrido

### 3. Prueba A/A entre grupos de control (246 vs 247)
- Comparación de proporciones de usuarios por evento
- Aplicación de prueba Z para dos proporciones
- Corrección por comparaciones múltiples:
  - Bonferroni
  - Holm-Bonferroni
  - Benjamini-Hochberg

### 4. Prueba A/B entre grupo experimental (248) y controles
- Comparación de cada evento entre grupo 248 y controles
- Evaluación de significancia estadística
- Análisis del impacto del rediseño tipográfico (fuentes nuevas)

### 5. Conclusiones y recomendaciones
- Identificación de etapas críticas en el embudo
- Validación de consistencia entre grupos de control
- Evaluación del efecto del nuevo diseño sobre el comportamiento del usuario

---

## ▶️ Cómo ejecutar el proyecto

1. **Clona este repositorio**:
   ```bash
   git clone https://github.com/tu-usuario/nombre_repo.git
2. - Instala las dependencias necesarias:
   ```bash
   pip install pandas numpy matplotlib seaborn scipy statsmodels
- 
3. Coloca el archivo de datos logs_exp_us.csv en la carpeta /datasets/.
4. Abre el notebook archivo.ipynb en Jupyter Notebook o VS Code
5. Ejecuta las celdas en orden para reproducir el análisis completo:
- Filtrado de datos incompletos
- Análisis del embudo de conversión
- Comparación A/A y A/B con pruebas estadísticas
- Corrección de p-valores y conclusiones


