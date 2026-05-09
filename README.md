# forced_landing_experiment
Validando hipótesis de negocio con pruebas estadísticas
##📊 Introducción
Eres analista de datos en el equipo de marketing digital de una empresa de ecommerce.  

Se ejecutó un experimento A/B en la página de inicio (landing page), comparando dos versiones (A y B) con el objetivo de mejorar la tasa de conversión y el valor económico por usuario.  

La empresa necesita una decisión basada en datos para definir qué versión implementar, considerando la tasa de conversión, el gasto promedio y el comportamiento por canal de tráfico y tipo de usuario.  

Para ello, trabajarás con el dataset:  
- /datasets/landing_experiment.csv: información de usuarios expuestos a las versiones A y B, incluyendo región, dispositivo, fuente de tráfico, tipo de usuario, conversión y gasto.

###🎯 Objetivo:

Explorar, validar y analizar estadísticamente el experimento A/B para identificar diferencias significativas entre las páginas y traducir los resultados en recomendaciones para el negocio.

###💡 Preguntas del negocio
- ¿Existe una diferencia significativa en el gasto promedio por usuario convertido entre ambas versiones?
- ¿Qué versión de la página (A o B) genera mayor tasa de conversión?
- ¿La conversión depende de la fuente de tráfico?
- ¿El tipo de usuario (nuevo o recurrente) influye en la conversión?
- ¿Qué hallazgos o insights permiten optimizar la estrategia de marketing y el diseño de la página de inicio (landing page)?

###🎯 Aprendizaje del proyecto
Al finalizar este proyecto, podrás:
- Explorar y validar un dataset proveniente de un experimento A/B real.
- Comparar métricas de negocio mediante pruebas estadísticas apropiadas.
- Interpretar resultados estadísticos desde una perspectiva de negocio.
- Visualizar resultados para respaldar conclusiones.
- Comunicar hallazgos o insights de forma clara a stakeholders no técnicos.

###📁Dataset
El archivo /datasets/landing_experiment.csv contiene información de usuarios expuestos a dos versiones de la página de inicio (landing page) dentro del experimento A/B.  

Puedes descargarlo aquí.  
https://drive.google.com/uc?export=download&id=15zGd_F-LzxCOcwNc74n_1x_o6OjAWYUV

| Columna | Tipo de dato | Descripción | Ejemplo real |
|:--- |:--- |:--- |:--- |
| user_id | Categórica (UUID) | Identificador único del usuario	|26f3052e-8500-44ea-8fff-06de65258abb |
| date | Fecha (YYYY-MM-DD) | Fecha en la que el usuario fue expuesto a la página | 2026-01-01 |
| landing | Categórica | Versión de la página mostrada al usuario | A, B |
| region | Categórica | Región geográfica del usuario | Norte, Centro, Sur, Occidente, Oriente |
| dispositivo | Categórica | Tipo de dispositivo utilizado por el usuario | Mobile, Desktop |
| traffic_source | Categórica | Canal por el que llegó el usuario | Organic, Ads, Email, Referral |
| user_type | Categórica | Tipo de usuario según historial previo | Nuevo, Recurrente |
| converted | Binaria (0/1) | Indica si el usuario realizó una conversión | 0, 1 |
| gasto | Numérica (float) | Monto gastado por el usuario (0 si no convirtió) | 38.08 |

###🔍 Detalles y consideraciones importantes
- Unidad de análisis: cada fila representa un usuario expuesto a una única versión de la página de inicio.
- La variable landing define los grupos del experimento A/B:
  - A: versión de control (página A)
  - B: versión de prueba (página B)
- converted es la variable objetivo principal del experimento:
  - 1 → El usuario realizó una compra
  - 0 → El usuario no convirtió
- La variable gasto solo tiene valores mayores a cero cuando converted = 1.  

  Esto es importante para:
  - Filtrar correctamente al comparar gasto promedio.
  - Evitar sesgos al incluir usuarios que no convirtieron.
- Las variables region, traffic_source y user_type permiten analizar la conversión por segmentos y validar si existen efectos diferenciales.
- El experimento está balanceado entre las versiones A y B, lo que permite aplicar pruebas estadísticas con confianza.

###📝 Plan de acción (pensamiento programático)
**Contexto del negocio**  
Tu objetivo es evaluar el experimento A/B y recomendar qué versión de la página de inicio debe implementarse, usando evidencia estadística sólida.  

El entregable será un notebook claro, reproducible y orientado a decisiones.

###🔄 Flujo general del proyecto
| Paso | Resultado para el negocio |
|:---|:---|
| 1. Cargar y validar datos | Confianza en la calidad del experimento |
| 2. Comparar gasto promedio (A vs. B) | Identificar qué página genera más valor |
| 3. Comparar tasa de conversión (A vs. B) | Identificar la página más efectiva |
| 4. Analizar tráfico y conversión | Optimizar inversión en canales |
| 5. Analizar tipo de usuario y conversión | Evaluar si segmentar usuarios |
| 6. Visualización | Respaldo visual de conclusiones |
| 7. Insight ejecutivo | Decisión clara para stakeholders |
###✅ Criterios de evaluación del proyecto
- 📊 Análisis estadístico  
  - Prueba estadística adecuada  
  - Verificación de supuestos  
  - Interpretación correcta del valor p (p-value).  
- 🧠 Razonamiento analítico  
  - Hipótesis claras  
  - Coherencia entre pregunta, método y conclusión  
  - Identificación de limitaciones  
- 💬 Comunicación de resultados  
  - Explicaciones claras  
  - Visualizaciones efectivas  
  - Enfoque en impacto de negocio  
- 🧾 Organización y reproducibilidad  
  - Notebook estructurado  
  - Código claro y reproducible  
  - Comentarios precisos y útiles
