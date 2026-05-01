# Calendario de Feriados Perú & Chile

## Descripción del Proyecto
Este proyecto tiene como objetivo la construcción de un pipeline de generación y análisis de calendarios de feriados para Perú y Chile, permitiendo su uso en modelos analíticos, forecasting y planificación operativa.

Se desarrollaron scripts en Python para la generación, integración y exportación de datasets estructurados en formato CSV, los cuales pueden ser utilizados en procesos de Data Science y Data Engineering.

---

## Objetivos
- Generar calendarios de feriados por país
- Integrar datasets de múltiples geografías (Perú y Chile)
- Facilitar su uso en modelos de:
  - Forecasting
  - Análisis de demanda
  - Modelos de series de tiempo
  - Feature engineering

---

## 🏗️ Estructura del Proyecto

📁 calendario/
│
├── calendario_pais.py # Generación de calendario por país
├── calendario_per_cl.py # Integración Perú + Chile
├── calendario_per_cl.ipynb # Análisis exploratorio
├── feriados_chile.csv
├── feriados_perú.csv
├── feriados_chile_peru.csv # Dataset consolidado


---

## ⚙️ Tecnologías Utilizadas

- Python 3.x
- Pandas
- Jupyter Notebook
- CSV (Data Storage)

---

## 🔄 Flujo del Proyecto

1. Generación de feriados por país
2. Limpieza y estructuración de datos
3. Integración de datasets
4. Exportación a CSV
5. Uso potencial en modelos analíticos

---

## Casos de Uso (Data Science)

Este tipo de dataset es clave para:

- Modelos de **forecasting de demanda**
- Identificación de **efectos calendario**
- Feature engineering en modelos de:
  - XGBoost
  - LightGBM
  - Modelos de series de tiempo (ARIMA, Prophet)

Ejemplo de features:
- `is_holiday`
- `holiday_type`
- `country`
- `lag_holiday_effect`

---

## Ejemplo de Uso

```python
import pandas as pd

df = pd.read_csv("feriados_chile_peru.csv")

# Crear variable dummy para feriados
df["is_holiday"] = 1
