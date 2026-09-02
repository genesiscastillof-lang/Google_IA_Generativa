# Cuestionario 4

1.- *Un departamento de marketing desea utilizar IA generativa para crear anuncios dinámicos y personalizados para diversas líneas de productos. Los datos disponibles incluyen segmentación de clientes (estructurados), descripciones de productos (texto no estructurado) y campañas publicitarias exitosas anteriores (semiestructuradas, con etiquetas para métricas de rendimiento). ¿Cuál es la principal implicación empresarial de combinar eficazmente estos diversos tipos de datos para la IA generativa en este contexto?*


- Mayor supervisión humana para la validación de contenido.
- Reducción de los costos de almacenamiento de datos gracias a la unificación de formatos.
- Creación de contenido más rápida con mayor personalización y relevancia, lo que se traduce en mayores tasas de conversión.
- Cumplimiento simplificado de las normativas de privacidad de datos.

2.- *Un analista de datos necesita utilizar un modelo de IA generativa para resumir una serie de informes financieros complejos. Los resúmenes deben extraer métricas financieras clave y proporcionar un breve análisis de las tendencias, sin necesidad de ejemplos previos de este tipo de resúmenes. ¿Qué técnica de solicitud es la más adecuada para este escenario, suponiendo que el modelo ha sido preentrenado con una gran cantidad de texto financiero?*

Few-shot prompting
Role prompting
Zero-shot prompting
Prompt chaining

3.- *Su empresa está lanzando un asistente de marketing generativo impulsado por IA. Para garantizar la alineación con los valores de la IA responsable, el Director de IA propone añadir un sistema de intervención humana (HITL). ¿Cuál es la razón más estratégica para integrar HITL desde una perspectiva de IA responsable?*

Para agilizar el lanzamiento al mercado sorteando las restricciones regulatorias y de cumplimiento mediante la intervención humana.

Para garantizar la trazabilidad y la rendición de cuentas en la toma de decisiones de la IA, especialmente en situaciones delicadas o que impactan la marca.

Para que la IA parezca más humana simulando empatía mediante intervenciones predefinidas.

Para aumentar la exposición del modelo a datos reales durante la inferencia, mejorando así la personalización a largo plazo.


4.- *Una empresa de comercio electrónico está lanzando un nuevo motor de recomendación de productos basado en aprendizaje automático. Buscan una plataforma totalmente gestionada que abarque todo el ciclo de vida del aprendizaje automático —desde la preparación de datos y el entrenamiento del modelo hasta la implementación y la monitorización—, integrándose a la perfección con otros servicios de Google Cloud. ¿Qué producto de Google Cloud deberían adoptar?*

Gemini for Workspace
Cloud Run
Vertex AI
Looker

5.- *Un equipo de IA quiere entrenar un modelo de clasificación que identifique tipos de documentos como contratos, facturas e informes. Han recopilado un conjunto de datos de archivos PDF, cada uno etiquetado con el tipo de documento correcto por expertos en la materia. ¿Con qué tipo de datos están trabajando?*

Labeled data
Reinforced data
Unstructured data
Metadata

6.- *Tras identificar un caso de uso de alto impacto para una solución de IA generativa, Google Cloud recomienda construir una "base de datos sólida". ¿Cuál es la razón principal por la que se enfatiza este paso, especialmente para la IA generativa?*

Para garantizar que el modelo de IA generativa pueda entrenarse con un conjunto de datos masivo y sin filtrar.

Para facilitar el ajuste fino, la fundamentación y las prácticas responsables de la IA mediante el suministro de datos de calidad, relevantes y controlados.

Para monetizar inmediatamente los activos de datos vendiéndolos a desarrolladores de IA externos.

Para reducir la necesidad de supervisión humana en los resultados de la IA.

7.- *Una empresa de servicios financieros está implementando una solución de IA generativa para automatizar la comunicación con sus clientes. El equipo directivo está preocupado por el acceso no autorizado a los modelos y el uso indebido de datos confidenciales de los clientes. ¿Qué herramienta de seguridad de Google Cloud es la más adecuada para controlar quién puede acceder y gestionar las cargas de trabajo de IA?*

Identity and Access Management (IAM)
Cloud Armor
BigQuery ML
Vertex AI Pipelines

8.- *Una ventaja clave de utilizar la Generación Aumentada por Recuperación (RAG) frente al simple ajuste de un modelo de lenguaje extenso (LLM) para un conocimiento de dominio específico es su capacidad para manejar información que evoluciona rápidamente. ¿Qué escenario ilustra mejor esta ventaja?*

Un LLM encargado de responder preguntas sobre el precio diario de las acciones de una empresa y sus comunicados de prensa recientes.

Un LLM que proporciona resúmenes históricos de eventos bien documentados sin información nueva.

Un LLM que necesita generar eslóganes de marketing altamente creativos basados ​​en el conocimiento general del producto.

Un LLM que traduce textos entre dos idiomas con reglas lingüísticas estables.

9.- *Un equipo de marketing está planificando una campaña que consiste en generar vídeos cortos y cinematográficos de presentación de productos, basados ​​en datos estructurados de productos, perfiles de clientes y mensajes de marketing. Quieren aprovechar un modelo de Google que pueda transformar textos en vídeos de alta calidad con efectos visuales dinámicos y cinematográficos. ¿Qué modelo deberían usar?*

Bard
Veo
Gemini
Imagen

10.- *Un modelo de IA generativa implementado en producción muestra signos de degradación del rendimiento y desviación conceptual. ¿Qué etapa del ciclo de vida del aprendizaje automático se centra principalmente en detectar y abordar estos problemas para garantizar que el modelo siga funcionando eficazmente a lo largo del tiempo?*

Model management 
Model training
Model deployment 
Data preparation


11.- *Una firma de asesoría financiera utiliza un asistente de IA generativa para resumir el rendimiento de diferentes fondos mutuos. Al consultar sobre un fondo recién lanzado, el asistente genera un historial de rendimiento detallado, incluyendo las rentabilidades trimestrales de los dos últimos años. Sin embargo, el fondo se lanzó hace tan solo tres meses y no existen datos históricos. ¿Qué limitación del modelo LLM ilustra esta situación?*


Training latency
Hallucinations
Data freshness
Overfitting

12.- *Un equipo de ciencia de datos está experimentando con un nuevo modelo de IA generativa multimodal capaz de generar tanto texto como imágenes. Quieren asegurarse de que el modelo produzca imágenes que se ajusten a estilos y temas artísticos específicos. Más allá de simplemente describir la imagen deseada, ¿qué estrategia avanzada de ingeniería de indicaciones podrían emplear para garantizar una producción artística consistente?*

- Implementación de metadatos para refinar dinámicamente las instrucciones de generación de imágenes.
- Uso exclusivo de palabras clave en el mensaje.
- Proporcionar un mensaje muy breve y general.
- Confiar en la configuración predeterminada del modelo.

13.- *Un equipo de marketing quiere que su modelo de IA genere correos electrónicos con el tono de un consultor de marca profesional. Para ello, introducen la frase "Eres un consultor de marketing experto..." antes de proporcionar la tarea. ¿Qué técnica de introducción de preguntas se está utilizando?*

Role prompting
Meta prompting
Prompt chaining
Few-shot prompting

14.- *Una agencia de marketing busca crear contenido altamente específico y atractivo para diversas campañas publicitarias, a menudo necesitando generar texto, imágenes e incluso breves fragmentos de video a partir de un único briefing. ¿Qué tipo de solución de IA generativa sería la más eficaz para este requisito tan complejo?*

Multimodal Generative AI
Robotic Process Automation (RPA)
Reinforcement Learning
Unimodal Generative AI

15.- *Una gran empresa está emprendiendo una iniciativa de IA generativa para crear un chatbot de atención al cliente. Planean utilizar décadas de registros de interacción con clientes, almacenados en diversos sistemas heredados, depósitos de almacenamiento en la nube y archivos de texto no estructurados. Muchas de estas fuentes de datos presentan diferentes esquemas de codificación y de datos, así como permisos de acceso restringidos para los distintos departamentos. ¿Qué aspecto de la accesibilidad a los datos representa el mayor desafío en este escenario?*

- Volumen de datos y capacidad de procesamiento
- Relevancia de los datos y mitigación de sesgos
- Interoperabilidad y complejidad de la integración
- Costo del almacenamiento y recuperación de datos

16.- *Una empresa utiliza un modelo de IA generativa para ayudar a sus empleados con preguntas relacionadas con el cumplimiento normativo. Sin embargo, los empleados han informado que las respuestas suelen hacer referencia a políticas obsoletas u omitir actualizaciones importantes de los cambios regulatorios recientes. ¿Qué debería hacer la empresa para garantizar que las respuestas se ajusten a la documentación más reciente?*

- Use grounding techniques to anchor answers in up-to-date policy documents
- Increase the model’s parameter count to improve accuracy
- Reduce the maximum context length during inference
- Retrain the model from scratch using regulatory compliance data only

17.- *Una agencia de marketing está preparando una campaña de vídeo y quiere generar automáticamente clips cinematográficos de texto a vídeo para presentar ideas conceptuales rápidamente. Las imágenes deben ser dinámicas y realistas para impresionar a las partes interesadas durante la preproducción. ¿Qué modelo de la Fundación Google debería usar el equipo?*

Gemini
Codey
Imagen
Veo

18.- *Un equipo interno de soporte de TI se ve desbordado por consultas repetitivas sobre problemas comunes de software y resolución de problemas de hardware. Desean implementar una solución de IA que pueda responder automáticamente a estas preguntas, proporcionar artículos de conocimiento relevantes y liberar a los agentes para que se enfoquen en problemas más complejos. ¿Qué oferta preconfigurada de IA generativa de Google Cloud se adapta específicamente a este caso de uso interno impulsado por IA?*

Vertex AI Pipelines
Cloud Healthcare API
Cloud Storage
Contact Center AI (CCAI)

19.- *Una startup está desarrollando una aplicación innovadora que utiliza IA generativa para ayudar a los profesionales del derecho en la redacción de contratos y escritos legales. La aplicación debe garantizar la máxima precisión y el cumplimiento de los precedentes legales, con especial énfasis en la reducción de errores fácticos (ilusiones). ¿Qué característica de un modelo de base es crucial para este caso de uso empresarial específico?*

-Compatibilidad con la generación de imágenes y audio junto con la generación de texto.
- Alta coherencia factual, menor tendencia a las alucinaciones y aptitud para el ajuste fino específico del dominio o RAG.
- Rentabilidad y facilidad de implementación, incluso si la precisión se ve comprometida ocasionalmente.
- Amplio conocimiento general proveniente de diversas fuentes de internet para abarcar una amplia gama de temas.

20.- *Se utiliza un dron autónomo para el monitoreo de cultivos. Ajusta su trayectoria de vuelo dinámicamente según las condiciones del terreno y los datos meteorológicos. Inicialmente ineficiente, el dron aprende mediante misiones repetidas al recibir retroalimentación: obtiene puntuaciones altas por escaneos completos y de bajo consumo energético, y penalizaciones por zonas no exploradas o por el agotamiento de la batería. ¿Qué tipo de enfoque de aprendizaje automático se aplica en este caso?*

Supervised learning
Unsupervised learning
Reinforcement learning
Semi-supervised learning

21.- *Una empresa global de comercio electrónico está experimentando un aumento en el volumen de llamadas y una atención al cliente inconsistente en todas sus regiones. La empresa busca mejorar la satisfacción del cliente y la eficiencia de sus agentes de soporte mediante las soluciones de IA generativa de Google Cloud. ¿Qué producto o función de Google Cloud proporcionaría mejor asistencia en tiempo real a los agentes de soporte, ayudándoles a resolver las consultas de los clientes con mayor rapidez?*

Cloud Run
Gemini for Google Workspace
Vertex AI Search
Cloud Contact Center AI (CCAI) Agent Assist

22.- *¿Cuál de las siguientes opciones describe mejor el papel de los modelos fundamentales en el panorama de la IA generativa?*

- Son motores sencillos basados ​​en reglas que se utilizan para simular respuestas humanas en chatbots básicos.
- Son modelos preentrenados a gran escala, capaces de comprender y generar datos en diversas modalidades.
- Son modelos ligeros diseñados para ejecutarse exclusivamente en dispositivos periféricos.
- Se utilizan únicamente durante la etapa de etiquetado de datos en los flujos de trabajo de aprendizaje automático.

23.- *Un líder en IA generativa está explicando la importancia de la ingeniería de instrucciones a un nuevo miembro del equipo. ¿Qué afirmación define mejor la ingeniería de instrucciones en el contexto de los modelos de lenguaje grande (LLM)?*

- Es el proceso de ajustar con precisión los pesos y sesgos internos de un modelo de lenguaje natural (LLM) para mejorar su rendimiento en tareas específicas.
- Implica diseñar y refinar las entradas (indicadores) para guiar al LLM a generar las salidas deseadas de forma eficaz y eficiente.
- Se centra en el desarrollo de nuevas arquitecturas de LLM para mejorar sus capacidades generativas.
- Se refiere al posprocesamiento de las salidas del LLM para corregir errores y filtrar contenido no deseado.

24.- *¿Cuál de las siguientes opciones describe mejor cómo un modelo de IA generativa produce contenido?*

- Realiza búsquedas web y resume contenido externo en tiempo real.
- Aplica reglas deterministas para generar resultados predecibles.
- Recupera respuestas preescritas de una base de datos fija.
- Genera contenido nuevo aprendiendo patrones de datos de entrenamiento y prediciendo posibles resultados.

25.- *Un equipo global de recursos humanos utiliza una herramienta de IA generativa para responder preguntas internas sobre las políticas de la empresa. Recientemente, la herramienta ha proporcionado información precisa, pero solo hasta una fecha determinada, omitiendo los cambios posteriores. El equipo desea que el asistente incluya de forma consistente las actualizaciones recientes de una base de datos central de políticas. ¿Cuál es la mejor solución?*

- Utilice la generación aumentada por recuperación (RAG) para proporcionar información actualizada durante la inferencia.
- Entrene el modelo con un conjunto de datos de internet más amplio.
- Utilice la instrucción de aprendizaje cero para guiar la salida del modelo.
- Aumente el tamaño del modelo para mejorar su capacidad.

26.- *Un analista de inversiones consulta un modelo de IA generativa lanzado en enero de 2024 para resumir los resultados del lanzamiento de un producto de una importante empresa tecnológica, anunciado en noviembre de 2024. La IA proporciona proyecciones vagas, pero no incluye resultados ni métricas reales del evento, a pesar de responder con seguridad. ¿Qué refleja esta limitación?*

- Alucinación de datos
- Fallo de generalización con pocos ejemplos
- Desalineación
- Límite de conocimiento

27.- *Una empresa minorista ha implementado una solución de IA generativa para automatizar la creación de descripciones de productos para su sitio web de comercio electrónico. Antes de la implementación de la IA generativa, un equipo de redactores escribía manualmente todas las descripciones. ¿Cuál de las siguientes es la métrica cuantitativa más eficaz para medir el impacto inmediato en la eficiencia operativa de esta iniciativa de IA generativa?*

- Aumento de la tasa de conversión de clientes para productos con descripciones generadas por IA
- Mejora del Net Promoter Score (NPS)
- Reducción del tiempo promedio para crear una descripción de producto
- Aumento del tráfico web

28.- *Una empresa de servicios financieros tiene equipos de atención al cliente que cambian con frecuencia entre herramientas como CRM, registros de transacciones y documentación de cumplimiento normativo. Esto ralentiza los tiempos de respuesta y genera un servicio inconsistente. Buscan una solución que permita a los agentes de soporte interactuar con una interfaz centralizada que utilice IA generativa para obtener información relevante de todos estos sistemas en tiempo real. ¿Qué producto de Google Cloud satisface mejor esta necesidad?*

Vertex AI Agent Builder
BigQuery Studio
Gemini for Google Cloud Console
Google Agentspace

29.- *Una empresa minorista con experiencia limitada en aprendizaje automático interno desea implementar IA generativa para mejorar el servicio al cliente y la generación de contenido interno. Necesitan una plataforma que permita a los analistas de negocio y al personal no técnico crear soluciones sin escribir código complejo. ¿Cuál de las siguientes opciones ilustra mejor cómo la plataforma de IA de Google Cloud democratiza el desarrollo de IA para este tipo de casos de uso?*

- Google Cloud solo ofrece pesos de modelos sin procesar para una personalización avanzada, lo que obliga a todos los usuarios a crear modelos desde cero.

- Google Cloud proporciona modelos preentrenados, acceso a la API a través de Vertex AI y herramientas de bajo código/sin código como Generative AI Studio para acelerar el desarrollo.

- Las herramientas de IA generativa de Google Cloud están restringidas a usuarios con experiencia en desarrollo con Python o Java debido a restricciones de seguridad.

- Google Cloud exige a los usuarios que implementen su propia infraestructura de entrenamiento, lo que limita su uso para usuarios empresariales.

30.- *Un equipo utiliza un modelo generativo para crear resúmenes legales a partir de contratos extensos. El modelo suele incluir datos o términos legales ficticios que no aparecen en el documento original. ¿Qué estrategia de ingeniería de mensajes sería la más adecuada para mitigar este problema?*

- Utilizar múltiples generaciones de autocompletado y promediarlas
- Integrar la lógica RAG directamente en la pregunta
- Pedirle al modelo que “imagine el contenido legal más probable”
- Incluir instrucciones explícitas para que solo utilice el contexto proporcionado

31.- *Un agente de IA generativa necesita acceder y procesar información de una vasta colección de conjuntos de datos internos y estructurados, almacenados de forma altamente escalable y eficiente para realizar consultas analíticas. ¿Qué servicio de Google Cloud es la opción más adecuada para almacenar y consultar estos datos según las necesidades analíticas del agente?*

Cloud Storage
Cloud SQL
BigQuery
Firestore

32.- *Un proveedor de atención médica está desarrollando un asistente de IA multimodal y seguro capaz de resumir conversaciones con pacientes, interpretar imágenes de rayos X e integrarse de forma segura con sistemas internos. El asistente debe ser personalizable para cumplir con las estrictas políticas de datos sanitarios y contar con una ventana de contexto amplio para gestionar transcripciones extensas. ¿Qué modelo de la Fundación Google se ajusta mejor a estos requisitos?*


Gemini
Imagen
Gemma
PaLM 2

33.- *Una empresa de logística está explorando el uso de agentes de IA para optimizar las operaciones de entrega. El equipo prevé agentes capaces de evaluar los retrasos en las entregas, acceder a API externas para obtener datos meteorológicos y de tráfico, y redirigir los envíos de forma dinámica. ¿Qué capacidad caracteriza mejor a un agente de IA en este contexto?*

- Analiza de forma autónoma las condiciones, utiliza herramientas y toma decisiones para alcanzar los objetivos.
- Es responsable de generar paneles visuales para las métricas de ruta.
- Ejecuta scripts preescritos sin intervención ni razonamiento externo.
- Genera automáticamente respuestas de texto basadas en datos logísticos históricos.

34.- *Una empresa está desarrollando una nueva aplicación de IA generativa para ayudar a los agentes de atención al cliente resumiendo los tickets de soporte y sugiriendo respuestas. El equipo de seguridad insiste en implementar medidas de seguridad en cada etapa del ciclo de vida del aprendizaje automático. ¿En qué etapa serían más cruciales el entrenamiento adversario y las pruebas de robustez para integrar la seguridad?*



