# Interconnect – Predicción de Cancelación de Clientes (Churn)

## Descripción

Este proyecto utiliza técnicas de machine learning para ayudar a la empresa de telecomunicaciones **Interconnect** a predecir qué clientes podrían cancelar su servicio.
Anticipar el churn permite ofrecer **promociones personalizadas**, mejorar la atención y reducir la pérdida de usuarios valiosos.

Interconnect ofrece:

- Telefonía fija (incluyendo múltiples líneas)
- Internet (DSL o fibra óptica)
- Seguridad en línea (antivirus y bloqueador de sitios)
- Soporte técnico
- Backup en la nube
- Streaming de TV y películas

El objetivo es construir un modelo que identifique clientes en riesgo de cancelar.

---

## Objetivos del Proyecto

- Predecir la probabilidad de cancelación de cada cliente.
- Comparar el desempeño entre distintos modelos.
- Identificar factores clave asociados al churn.
- Permitir a Interconnect aplicar estrategias de retención basadas en datos.

---

## Descripción de los Datos

Los datos provienen de cuatro archivos:

- **contract.csv** — detalles del contrato (duración, método de pago, cargos, tipo de contrato).
- **personal.csv** — información personal del cliente.
- **internet.csv** — servicios de Internet (tipo de conexión, seguridad, backup, streaming).
- **phone.csv** — servicios telefónicos.

Todos incluyen la columna **customerID**, usada como identificador único.

La información del contrato es válida desde **el 1 de febrero de 2020**.

---

## Tecnologías Utilizadas

- Python 3
- pandas, numpy
- seaborn, matplotlib
- scikit-learn (Gradient Boosting, métricas, preprocesamiento, balanceo)

---

## Metodología

- Análisis exploratorio de datos (EDA).
- Integración de datasets mediante `customerID`.
- Preprocesamiento:
  - Codificación de variables categóricas.
  - Escalado cuando es necesario.
  - Balanceo del dataset para mejorar el recall.
- Entrenamiento de modelos de clasificación:
  - Árboles de decisión
  - Random Forest
  - Gradient Boosting
- Evaluación mediante:
  - Accuracy
  - Precision
  - Recall
  - F1-score
- Análisis de importancia de características.

---

## Resultados

- El mejor modelo fue **Gradient Boosting con datos balanceados**.
- Las variables más influyentes en la cancelación fueron:
  - **Tiempo como cliente** (tenure)
  - **Método de pago**
  - **Tipo de servicio de Internet**
- Otros hallazgos:
  - Clientes que **no usan soporte técnico** tienen mayor probabilidad de cancelar.
  - Usuarios con **StreamingTV** muestran mayor riesgo de churn.

Estos resultados permiten implementar mejores estrategias de retención y personalizar promociones.

---

## Cómo Ejecutar

1. Clona el repositorio:
   ```bash
   git clone https://github.com/ely00carmen/Proyecto_13.git
2. Instala las dependencias:

   pip install -r requirements.txt

3. Ejecuta el notebook principal:

   jupyter notebook
