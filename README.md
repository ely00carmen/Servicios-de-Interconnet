📡 Interconnect – Predicción de Cancelación de Clientes (Churn) --
-- Descripción --

Este proyecto utiliza técnicas de machine learning para ayudar a la empresa de telecomunicaciones Interconnect a predecir qué clientes podrían cancelar su servicio.
Anticipar el churn permite ofrecer promociones personalizadas, mejorar la atención y evitar pérdidas de clientes.

Interconnect ofrece:

Telefonía fija (incluyendo múltiples líneas)

Internet (DSL o fibra óptica)

Seguridad en línea (antivirus y bloqueador de sitios)

Soporte técnico

Backup en la nube

Streaming de TV y películas

-- Objetivos del Proyecto --

Predecir la probabilidad de cancelación de cada cliente.

Comparar múltiples modelos y estrategias de balanceo.

Identificar los factores más influyentes en el churn.

Apoyar estrategias de retención basadas en datos.

-- Descripción de los Datos --

Los datos provienen de cuatro archivos:

contract.csv — detalles del contrato (duración, cargos, método de pago, tipo de contrato).

personal.csv — datos personales del cliente.

internet.csv — tipo de conexión, seguridad, backup, streaming.

phone.csv — servicios de telefonía fija.

Todos los archivos incluyen customerID como identificador único.

La información del contrato es válida desde el 1 de febrero de 2020.

-- Tecnologías Utilizadas --

Python 3

pandas, numpy

seaborn, matplotlib

scikit-learn (Gradient Boosting, preprocesamiento, métricas, balanceo)

-- Metodología --

Análisis exploratorio (EDA).

Unificación de datasets usando customerID.

Preprocesamiento:

Codificación de variables categóricas.

Escalado cuando fue necesario.

Balanceo de clases para mejorar el recall.

Entrenamiento de diferentes modelos:

Árboles de decisión

Random Forest

Gradient Boosting

Evaluación mediante Accuracy, Recall, Precision y F1-score.

Análisis de importancia de características.

-- Resultados --

Gradient Boosting con datos balanceados fue el modelo con mejor desempeño.

Factores clave asociados al churn:

Tiempo como cliente (tenure)

Método de pago

Tipo de servicio de Internet

Hallazgos relevantes:

Clientes que no usan soporte técnico cancelan más.

Usuarios con StreamingTV muestran más probabilidad de churn.

Estos resultados permiten a Interconnect optimizar estrategias de retención y ofrecer promociones más efectivas.

-- Cómo Ejecutar --

Clona el repositorio:

git clone https://github.com/ely00carmen/Proyecto_13.git


Instala las dependencias:

pip install -r requirements.txt


Ejecuta el notebook o script principal:

jupyter notebook
