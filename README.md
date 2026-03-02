# TelecomX_LATAM1
# Telecom X - Análisis de Evasión de Clientes (Churn)

## Descripción del Proyecto

Este proyecto tiene como objetivo analizar los factores asociados a la evasión de clientes (Churn) en Telecom X.

La empresa enfrenta una alta tasa de cancelación de servicios y necesita comprender qué variables influyen en la pérdida de clientes para diseñar estrategias de retención más efectivas.

A través de un proceso completo de ETL (Extracción, Transformación y Limpieza) y un Análisis Exploratorio de Datos (EDA), se identificaron patrones relevantes que pueden servir como base para futuros modelos predictivos.

---

## Objetivos del Análisis

- Comprender la magnitud del churn.
- Identificar variables asociadas con la cancelación.
- Detectar perfiles de clientes con mayor riesgo.
- Generar insights estratégicos para reducir la evasión.
- Explorar correlaciones útiles para futuros modelos de Machine Learning.

---

## Estructura del Proyecto

- TelecomX_Churn/
- TelecomX_LATAM(1)
- TelecomX_Data
- TelecomX_Diccionario
- README.md

---

##  Proceso de Limpieza y Transformación

Durante la preparación de los datos se realizaron las siguientes acciones:

- Eliminación de registros con valores vacíos en la variable objetivo `Churn`.
- Conversión de `account.Charges.Total` a formato numérico.
- Reemplazo de valores faltantes por 0 cuando correspondía (clientes con antigüedad 0).
- Conversión de `Churn` a formato binario (0 = No canceló, 1 = Canceló).
- Transformación de variables binarias (Yes/No) a formato numérico.
- Corrección de valores como `"No internet service"` antes de su transformación.
- Creación de la variable derivada `Cuentas_Diarias`.

Dataset final: **7,043 registros completos y consistentes.**

---

##  Principales Análisis Realizados

###  Distribución de Churn

- 26.54% de los clientes cancelaron.
- 73.46% permanecen activos.

Esto indica que aproximadamente 1 de cada 4 clientes abandona la compañía.

---

###  Tipo de Contrato

| Tipo de Contrato | Tasa de Churn |
|------------------|---------------|
| Month-to-month   | 42.71% |
| One year         | 11.27% |
| Two year         | 2.83% |

La duración contractual es el factor más determinante en la retención.

---

###  Método de Pago

Los clientes que utilizan **Electronic check** presentan la mayor tasa de evasión (45.29%), mientras que los métodos automáticos muestran tasas significativamente menores.

---

###  Variables Numéricas

- Clientes con churn tienen menor antigüedad (17.98 meses vs 37.57).
- Clientes con churn pagan en promedio más mensualmente.
- Mayor vinculación (más servicios contratados) se asocia con menor evasión.

---

###  Análisis de Correlación

Variables con mayor relación con churn:

- `customer.tenure` (correlación negativa más fuerte)
- `account.Charges.Monthly`
- `Cuentas_Diarias`
- `Cantidad_Servicios`

---

##  Recomendaciones Estratégicas

1. Incentivar contratos a largo plazo.
2. Implementar programas de retención durante los primeros 12 meses.
3. Promover métodos de pago automáticos.
4. Revisar estructura de precios en planes de mayor costo.
5. Desarrollar modelos predictivos basados en las variables identificadas.

---

## 🛠 Tecnologías Utilizadas

- Python 3
- Pandas
- Matplotlib
- Seaborn
- Google Colab

---

##  Cómo Ejecutar el Proyecto

1. Clonar el repositorio: git clone

2. Abrir el notebook en Google Colab o Jupyter Notebook.

3. Ejecutar las celdas en orden.

---

##  Autor

Proyecto desarrollado por Maria Jose Rincon Manrique como parte del desafío de análisis de datos – Telecom X.

---

## Conclusión

El análisis permitió identificar patrones claros asociados con la evasión de clientes. La antigüedad, el tipo de contrato y el método de pago son los principales factores que influyen en la cancelación.

Estos hallazgos pueden servir como base para el desarrollo de estrategias de retención y modelos predictivos más robustos.
