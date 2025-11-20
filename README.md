📡 Interconnect – Predicción de Cancelación de Clientes (Churn)
📌 Descripción

Este proyecto utiliza técnicas de machine learning para ayudar a la empresa de telecomunicaciones Interconnect a predecir qué clientes podrían cancelar su servicio.
Anticipar el churn permite que la empresa ofrezca promociones personalizadas, mejore su atención y reduzca la pérdida de usuarios valiosos.

Interconnect ofrece servicios de:

Telefonía fija (incluyendo líneas múltiples)

Internet (DSL o fibra óptica)

Seguridad en línea (antivirus, bloqueador de sitios)

Soporte técnico

Backup en la nube

Streaming de TV y películas

El objetivo del proyecto es analizar estos datos y construir un modelo capaz de identificar clientes en riesgo de cancelar.

🎯 Objetivos del Proyecto

Predecir la probabilidad de cancelación de cada cliente mediante modelos supervisados.

Comparar el desempeño entre múltiples algoritmos y técnicas de balanceo.

Determinar los factores más influyentes en la cancelación del servicio.

Proveer a Interconnect una herramienta que permita aplicar estrategias de retención basadas en datos.

📊 Descripción de los Datos

El proyecto utiliza cuatro archivos principales:

contract.csv — detalles del contrato (duración, método de pago, cargos, tipo de contrato).

personal.csv — información personal del cliente.

internet.csv — servicios relacionados con Internet (tipo de conexión, seguridad, backup, streaming).

phone.csv — información sobre servicios telefónicos.

Todos incluyen la columna customerID, usada para unificarlos.
La información del contrato está vigente desde el 1 de febrero de 2020.

⚙️ Tecnologías Utilizadas

Python 3

pandas, numpy

seaborn, matplotlib

scikit-learn (Gradient Boosting, métricas, validación, preprocesamiento, balanceo)

🧪 Metodología

Exploración de datos (EDA) para comprender patrones y distribución de variables.

Integración de los cuatro datasets mediante customerID.

Preprocesamiento:

Codificación de variables categóricas.

Escalado de datos cuando fue necesario.

Balanceo del dataset para mejorar la detección de churn.

Pruebas con diversos modelos, enfocándonos en:

Árboles de decisión

Random Forest

Gradient Boosting

Selección del mejor modelo según métricas como Accuracy, Recall y F1-Score.

Análisis de importancia de características para entender qué factores influyen en la cancelación.

📈 Resultados

El modelo Gradient Boosting con datos balanceados presentó el mejor desempeño global.

Variables más influyentes en la cancelación:

Tiempo como cliente (tenure)

Método de pago

Tipo de servicio de Internet

Hallazgos adicionales:

Clientes que no usan soporte técnico tienen mayor riesgo de cancelar.

Usuarios con StreamingTV muestran mayor probabilidad de churn.

Estos insights permiten a Interconnect optimizar acciones de retención, mejorar su servicio y personalizar promociones.

▶️ Cómo Ejecutar

Clona el repositorio:

git clone https://github.com/ely00carmen/Proyecto_13.git


Instala las dependencias:

pip install -r requirements.txt


Ejecuta el proyecto:

jupyter notebook
