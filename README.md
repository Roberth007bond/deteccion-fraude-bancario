# 🔍 Detección de Fraude en Tarjetas de Crédito

![Python](https://img.shields.io/badge/Python-3.14-blue?style=for-the-badge&logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.8-orange?style=for-the-badge&logo=scikit-learn&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-3.0-150458?style=for-the-badge&logo=pandas&logoColor=white)

Pipeline completo de detección de fraude bancario usando Machine Learning sobre 284,807 transacciones reales de tarjetas de crédito europeas.

---

## 🎯 Problema de negocio

Los bancos pierden millones anuales por fraude en tarjetas de crédito. El reto principal es detectar el 0.17% de transacciones fraudulentas sin generar falsas alarmas que afecten a clientes legítimos.

---

## 📊 Hallazgos principales

| Métrica | Resultado |
|---|---|
| Total transacciones analizadas | 284,807 |
| Fraudes detectados correctamente | 73 de 98 (74%) |
| Falsas alarmas generadas | 3 de 56,864 (0.005%) |
| ROC-AUC Score | 0.9529 |
| Monto promedio fraude | €122.21 vs €88.29 legítimas |

---

## 📈 Visualizaciones

### 1. Distribución de clases y montos
![Distribución](graficas/01_distribucion_clases.png)

### 2. Análisis temporal y correlaciones
![Temporal](graficas/02_analisis_temporal_correlacion.png)

### 3. Resultados del modelo
![Modelo](graficas/03_resultados_modelo.png)

---

## 🛠️ Stack técnico

| Herramienta | Uso |
|---|---|
| Python 3.14 | Lenguaje principal |
| pandas | Carga y manipulación de datos |
| scikit-learn | Modelo Random Forest + métricas |
| matplotlib / seaborn | Visualizaciones |
| StandardScaler | Normalización de Amount y Time |

---

## ⚙️ Metodología

1. **Carga e inspección** — 284,807 registros, 0 valores nulos
2. **Análisis de desbalance** — 99.83% legítimas vs 0.17% fraudes
3. **Preprocesamiento** — escalado de Amount y Time con StandardScaler
4. **Modelado** — Random Forest con `class_weight='balanced'`
5. **Evaluación** — ROC-AUC 0.9529, matriz de confusión, curva ROC

---

## 📁 Estructura del proyecto

| Archivo | Descripción |
|---|---|
| `Notebook/eda_fraude.ipynb` | Notebook completo con EDA y modelo |
| `graficas/01_distribucion_clases.png` | Distribución de clases y montos |
| `graficas/02_analisis_temporal_correlacion.png` | Análisis temporal y correlaciones |
| `graficas/03_resultados_modelo.png` | Resultados del modelo |
| `data/creditcard.csv` | Dataset (no incluido por tamaño) |

---

## 📂 Dataset

- **Fuente:** [Credit Card Fraud Detection — Kaggle](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
- **Registros:** 284,807 transacciones · septiembre 2013
- **Features:** 28 variables PCA anonimizadas + Time + Amount
- **Desbalance:** 492 fraudes (0.172%) vs 284,315 legítimas

---

## 👤 Autor

**Robert Alexis Robles Sánchez**  
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/robert-robles-sanchez)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Robe
