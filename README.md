Interconnect – Operador de telecomunicaciones
📌 Descripción

Interconnect es un operador de telecomunicaciones que ofrece servicios de telefonía fija e Internet (por DSL o fibra óptica), junto con servicios adicionales como seguridad en línea, soporte técnico, almacenamiento en la nube y streaming de TV y películas.

Con el fin de mejorar la retención de clientes, surge la necesidad de predecir qué usuarios tienen mayor probabilidad de cancelar su contrato. Esto permite ofrecer promociones personalizadas y planes especiales antes de que abandonen la compañía.

🎯 Objetivos del Proyecto

Construir un modelo capaz de predecir la tasa de cancelación (churn) de los clientes de Interconnect.

Identificar las características que más influyen en la cancelación.

Apoyar al equipo de marketing para tomar acciones preventivas mediante ofertas, mejoras de servicio o contacto oportuno.

Evaluar diferentes modelos y determinar cuál proporciona el mejor balance entre precisión y capacidad de identificar clientes en riesgo.

📊 Descripción de los Datos

El proyecto utiliza información proveniente de varias fuentes, cada una relacionada con aspectos distintos del servicio:

contract.csv — información del contrato.

personal.csv — datos personales de cada cliente.

internet.csv — información sobre servicios de Internet.

phone.csv — detalles sobre servicios telefónicos.

Todos los archivos incluyen la columna customerID, que identifica de manera única a cada cliente.

El dataset contiene información relevante para clasificación, junto con variables personales que han sido previamente ofuscadas para proteger la privacidad.
Los datos del contrato son válidos a partir del 1 de febrero de 2020.

⚙️ Tecnologías Utilizadas

Python 3

Librerías de análisis y visualización:

pandas, numpy

seaborn, matplotlib

Librerías de machine learning:

scikit-learn (Gradient Boosting, métricas de evaluación, preprocesamiento, balanceo)

🧪 Metodología

Exploración y limpieza de datos, integrando las diferentes tablas mediante customerID.

Análisis exploratorio (EDA) para identificar patrones, correlaciones y distribución de variables relevantes.

Preprocesamiento:

Codificación de variables categóricas.

Estandarización de valores numéricos.

Tratamiento de datos faltantes.

Balanceo del dataset para mejorar la detección de clientes que cancelan.

Entrenamiento de múltiples modelos para comparar desempeño:

Modelos lineales

Árboles de decisión

Random Forest

Gradient Boosting

Selección del mejor modelo basándose en métricas como:

Accuracy

Recall (especialmente para clase “cancelación”)

F1-score

Interpretación de características importantes para comprender los factores que influyen en la cancelación.

📈 Resultados

El modelo con mejor desempeño fue Gradient Boosting utilizando datos balanceados, logrando el mejor equilibrio entre precisión y capacidad de identificar clientes que cancelan.

Principales hallazgos:

El tiempo como cliente es uno de los factores más influyentes: quienes llevan menos tiempo tienden a cancelar con mayor frecuencia.

El método de pago tiene un impacto notable en la probabilidad de churn.

El tipo de servicio de Internet también influye significativamente, especialmente en clientes con fibra óptica.

Usuarios que no utilizan soporte técnico muestran una mayor tasa de cancelación.

Clientes con StreamingTV presentan una probabilidad más alta de cancelar.

Estos insights permiten orientar estrategias de retención, como mejorar la calidad del servicio, ajustar la oferta de planes y personalizar promociones para clientes en riesgo.

▶️ Cómo Ejecutar

Clona el repositorio:

git clone https://github.com/ely00carmen/Proyecto_13.git


Instala las dependencias:

pip install -r requirements.txt


Ejecuta el script o notebook principal:

jupyter notebook
