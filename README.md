Análisis de Churn de Clientes 
✅ Descripción del Proyecto
Este proyecto presenta un análisis exploratorio de datos (EDA) completo para identificar los factores clave que contribuyen a la cancelación de servicios (churn) por parte de los clientes en una empresa de telecomunicaciones. El objetivo es transformar datos brutos en insights accionables que puedan guiar las estrategias de retención de clientes.

El análisis abarca todo el proceso, desde la carga y limpieza de datos extraídos en formato JSON, hasta la ingeniería de características, la visualización de patrones y la formulación de recomendaciones estratégicas basadas en evidencia.

✅ Problema de Negocio
La pérdida de clientes, o churn, es uno de los desafíos más críticos para las empresas con modelos de suscripción. Adquirir un nuevo cliente es significativamente más costoso que retener a uno existente. Este proyecto aborda directamente este problema al responder preguntas clave como:

¿Cuál es el perfil de un cliente que es propenso a cancelar el servicio?

¿Qué características del servicio o del contrato están más fuertemente asociadas con el churn?

¿Qué acciones estratégicas podemos implementar para reducir la tasa de cancelación?

✅ Fuente de Datos
Los datos utilizados para este análisis provienen de un archivo JSON (TelecomX_Data.json) que simula la extracción de información desde una API. Este archivo contiene datos anidados sobre clientes, incluyendo:

Información demográfica: Género, si son adultos mayores, si tienen socios o dependientes.

Detalles de la cuenta: Antigüedad (tenure), tipo de contrato, método de pago y facturación.

Servicios contratados: Telefonía, múltiples líneas, servicio de internet (Fibra Óptica, DSL), y servicios adicionales como seguridad online, backup, etc.

Variable objetivo: La columna Churn (Sí/No), que indica si el cliente canceló el servicio.

✅ Metodología
El análisis se estructuró siguiendo los siguientes pasos, detallados en el Jupyter Notebook Analisis_Churn.ipynb:

Carga y Transformación (ETL): Se cargaron los datos desde el archivo JSON y se aplanó la estructura anidada utilizando pandas.json_normalize para convertirla en un DataFrame tabular.

Limpieza de Datos: Se manejaron valores ausentes (en TotalCharges para clientes nuevos), se corrigieron tipos de datos inconsistentes y se verificó la ausencia de duplicados.

Ingeniería de Características (Feature Engineering): Se creó una nueva columna, DailyCharges (Cuentas_Diarias), para obtener una perspectiva más granular de los gastos del cliente.

Análisis Exploratorio de Datos (EDA): Se realizaron visualizaciones para entender la distribución del churn y su relación con diversas variables:

Variables Categóricas: Se utilizaron gráficos de barras para analizar el churn por tipo de contrato, método de pago, servicio de internet, etc.

Variables Numéricas: Se emplearon diagramas de caja (box plots) para comparar la distribución de la antigüedad (tenure) y los cargos mensuales entre clientes que cancelaron y los que no.

Análisis de Correlación: Se generó una matriz de correlación (heatmap) para identificar las relaciones lineales entre las variables numéricas y la variable de churn.

✅ Insights Clave y Hallazgos
El análisis reveló patrones claros que definen el riesgo de churn:

Tipo de Contrato: Los clientes con contratos mes a mes tienen una tasa de cancelación drásticamente superior a los clientes con contratos anuales. La falta de compromiso a largo plazo es el principal factor de riesgo.

Antigüedad (Tenure): Los clientes que cancelan son, en su mayoría, clientes nuevos. La probabilidad de churn disminuye significativamente a medida que aumenta la antigüedad.

Cargos Mensuales: Clientes con cargos mensuales más altos son más propensos a cancelar, especialmente aquellos con servicios de Fibra Óptica.

Método de Pago: El pago a través de cheque electrónico está fuertemente asociado con una mayor tasa de churn, lo que puede indicar fricción en el proceso de facturación.


✅ Recomendaciones Estratégicas
Basado en los hallazgos, se proponen las siguientes acciones para mejorar la retención:

Fomentar Contratos a Largo Plazo: Diseñar campañas de marketing y ofrecer descuentos para incentivar la migración de planes mensuales a planes anuales.

Programa de Retención para Clientes Nuevos: Implementar un programa de "onboarding" y seguimiento proactivo durante los primeros 3 meses para mejorar la experiencia inicial y construir lealtad.

Revisar Precios de Fibra Óptica: Analizar la competitividad de los precios del servicio de Fibra Óptica y considerar la creación de paquetes con mejor relación valor-precio.

Optimizar Métodos de Pago: Incentivar el uso de métodos de pago automáticos (débito directo, tarjeta de crédito) mediante pequeños descuentos para reducir la fricción asociada al cheque electrónico.

✅ Tecnologías Utilizadas
Lenguaje de Programación: Python 3.x

Librerías de Análisis:

Pandas: Para la manipulación y análisis de datos.

NumPy: Para operaciones numéricas eficientes.

Librerías de Visualización:

Matplotlib: Para la creación de gráficos básicos y personalizados.

Seaborn: Para la generación de visualizaciones estadísticas atractivas.

Entorno de Desarrollo: Jupyter Notebook


