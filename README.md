# 📊 Análisis de Datos de Llamadas – Telco

![Python](https://img.shields.io/badge/Python-3.9+-blue?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)

Este proyecto presenta el análisis exploratorio y la validación estadística de un dataset de **53.902 llamadas** realizadas por **732 clientes**, con el objetivo de identificar patrones de uso, ineficiencias operativas y diferencias entre planes tarifarios.  

---

## 🚀 Conclusiones principales

### 🔍 1. Exploración de datos (EDA)
- El dataset contiene **53.902 llamadas y 732 clientes**.  
- La mayoría de las llamadas son muy cortas, pero se detectaron **outliers extremos (>100.000 seg)**.  
- **88.5% de las llamadas son externas** vs. 11.5% internas → interacción principalmente con clientes.  
- Se encontraron valores nulos en:
  - `operator_id` (~8.000) → posible registro automático o error.  
  - `internal` (117).  

---

### 👨‍💼 2. Identificación de operadores ineficaces
- Métricas clave calculadas:  
  - **Missed rate** (llamadas perdidas).  
  - **Avg. wait time** (tiempo promedio de espera).  
  - **Out ratio** (proporción de salientes).  
- Algunos operadores con suficiente volumen (30–95 llamadas) presentan:  
  - **Tasa de pérdida del 22–28%**, muy por encima de lo esperado.  
  - Casos críticos con **tiempos de espera >30 seg**, lo que incrementa el abandono.  

---

### 📈 3. Prueba de hipótesis (ANOVA – Planes tarifarios)
- **Resultado:** existen diferencias significativas en duración de llamadas entre planes (p < 0.001).  
- Duración promedio:  
  - Plan **B** → ~415 seg.  
  - Plan **A** → ~379 seg.  
  - Plan **C** → ~371 seg.  
- Implicación: el **Plan B atrae clientes con mayor necesidad de comunicación**.  

---

## 🛠️ Recomendaciones

### 🔧 Tratamiento de outliers y nulos
- Filtrar **outliers en `call_duration`** (ej. percentil 95–99).  
- Revisar origen de `operator_id` nulos → excluir o imputar tras validación con el área técnica.  

### 📞 Gestión de operadores ineficaces
- Monitorear operadores con:  
  - **Missed rate >20%**.  
  - **Avg. wait time >30 seg**.  
- Implementar **capacitaciones y alertas de rendimiento**.  
- Redistribuir carga hacia operadores más eficientes.  

### 💡 Estrategia por planes tarifarios
- **Plan B**: enfocar estrategias de **retención y fidelización** (clientes más activos).  
- **Planes A y C**: investigar motivos de llamadas más cortas → ajustar beneficios.  
- Analizar si **Plan B genera mayor ARPU**, para incentivar migración desde otros planes.  

---

## 📂 Contenido del repositorio
- 📁 `notebooks/` → Jupyter Notebooks con el análisis exploratorio y pruebas estadísticas.  
- 📁 `data/` → Dataset procesado (con anonimización).  
- 📁 `reports/` → Conclusiones y visualizaciones clave.  

---

## ✨ Tecnologías utilizadas
- **Python** 🐍 (pandas, numpy, matplotlib, seaborn, scipy, statsmodels)  
- **Jupyter Notebook** 📓  
- **Git & GitHub** 🔗  

---

## 📌 Autor
**Arnold Joel Jimenez**  
📍 Analista de Datos | Bogotá, Colombia  
🔗 [LinkedIn](www.linkedin.com/in/arnold-joel-jimenez-matallana-64ba051b8) | [GitHub]([https://github.com](https://github.com/ArnoldJimenez))  

