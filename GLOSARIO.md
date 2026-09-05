## Que son Agentes
los agentes de IA son nuevos tipos de arquitecturas de aplicaciones.
Se basan en un modelo linguistico para razonar.
Poseen una memoria a corto y largo plazo y estan conectados a una fuentes de contexto. 
Planifica y ejecutan tareas complejas coordinando multiples tareas mas pequeñas o incluso  otros agentes.
Su experiencia de usuario puede variar
Puede ser sincrona, atraves de un chat o ejecutarse de forma asincrona. Por ejemplo, al realizar investigaciones o revisiones de codigo, necesitan colaborar con el usuario solicitando mas orientacion, confirmacion y toma de decisiones.

Eso permite la moderacion y el control por parte del usuario, algo que llamamos intervencion humana.
Las tareas pueden realizarse utilizando herramientas.

Las herramientas son:

### Herramientas Basicas 
Las Herramientas Basicas donde Las matematicas y las conversiones son ejercicios de modelos de lenguaje grande.

### Acesso a los datos
Los agentes puede recuperar el contexto antes de llamar a LLM , consulta a una base de datos para obtener detalles especificos. por ejemplo un catalogo de productos.

### APIS
El agente puede leer datos de la APIs ya sean propias o de terceros.Inluso puede tener accceso directo bajo supervision humana.

### Generacion de Imagenes
el agente puede llamar a otra API de generacion de imagenes o generar visualizaciones a partir de los datos generados.

### Browser / Navegadores
Se le puede dar/otorgar  al agente el control de un navegador web , donde puede explorar sitios web utilizando un navegador web real basado en Chromium. este se puede realizar mediante multiples intercambios de informacion entre el LLM y el servicio de navegador.

### Ejecucion de Codigo
EL LLM genera codigo y el agente lo ejecuta en un entorno seguro y aislado

![AI Agente Architecture](./data/IA_ARCHITCTURE.png)

[▶️ AI Agente](https://www.youtube.com/watch?v=8rlNdKywldQ)

[▶️ AI Agente](https://www.youtube.com/watch?v=Zqno_vux6d8)

---
### Grounding / fundamentación
En el contexto de la IA generativa, la fundamentación se refiere al proceso de vincular las respuestas de un modelo con una fuente de información fidedigna, como documentos internos o resultados de búsquedas web. Esto ayuda a reducir las ilusiones y garantiza que los resúmenes o respuestas generados sean precisos y directamente rastreables a los informes financieros proporcionados, lo cual es fundamental para una base de conocimiento en un sector regulado como el de los servicios financieros. De esta manera, se asegura que la IA no invente información y, en cambio, utilice las fuentes autorizadas disponibles.

### Model Tuning (e.g., fine-tuning)

El ajuste de modelos adapta un modelo preentrenado para realizar tareas específicas con mayor precisión y exactitud en un conjunto de datos particular. Si bien el ajuste fino en los informes financieros podría mejorar la comprensión del modelo sobre ese dominio, no garantiza que sus respuestas se ajusten estrictamente a la información contenida en los informes. Un modelo ajustado aún podría generar información plausible pero incorrecta. La vinculación con datos reales conecta explícitamente las respuestas con una fuente de información fidedigna.

### Function Calling
La llamada a funciones permite que un modelo de IA generativa interactúe con API externas para obtener información en tiempo real o realizar acciones. Si bien es útil para la integración con otros sistemas (por ejemplo, para obtener precios de acciones en tiempo real), no resuelve directamente el problema de garantizar que el contenido resumido generado se base en documentos específicos y autorizados, como una "fuente de verdad", para evitar confusiones. Se trata de las acciones que el modelo puede realizar, no de la fuente de información para generar el texto.

### Prompt Management
La gestión de indicaciones ayuda a organizar y administrar las indicaciones para diferentes casos de uso. Si bien es importante para la coherencia y el control de versiones de las indicaciones, no aborda directamente el problema de garantizar que la salida de la IA sea objetivamente precisa y se derive de datos internos específicos, que es la función de la validación.

### App Engine
App Engine es una plataforma para crear y alojar aplicaciones web. No ofrece herramientas nativas para el entrenamiento, la monitorización o la gestión del ciclo de vida de los modelos.

### Cloud Composer
Cloud Composer es una herramienta de orquestación basada en Apache Airflow, útil para gestionar flujos de trabajo, pero insuficiente por sí sola para completar las tareas del ciclo de vida de la IA/ML.

### Gemini for Workspace
Gemini mejora la productividad en aplicaciones de Google Workspace como Docs y Sheets, pero no está diseñado para la gestión de modelos de aprendizaje automático empresariales.

### Document AI
La IA aplicada al análisis de documentos se centra en extraer datos estructurados de documentos no estructurados (por ejemplo, facturas, formularios) y no está diseñada para unificar sistemas de datos en tiempo real ni para habilitar flujos de trabajo conversacionales.

### Looker Studio
Looker Studio es una herramienta web que transforma tus datos en paneles e informes informativos. Se trata de una herramienta de inteligencia empresarial y visualización de datos, no de una herramienta para extraer datos de documentos.

# Locker
Looker es una herramienta de inteligencia empresarial (BI) y exploración de datos, no una plataforma para crear o gestionar modelos de aprendizaje automático (ML).

### Vertex AI
Vertex AI está diseñado específicamente para brindar soporte a operaciones de aprendizaje automático de extremo a extremo a gran escala, incluyendo entrenamiento, ajuste, implementación, control de versiones, monitoreo y detección de desviaciones de modelos. Es la opción más completa y escalable para el caso de uso descrito.

### Vertex AI Codey
Vertex AI Codey está especializado en la generación de código y el desarrollo de software. Es útil para desarrolladores, no para usuarios empresariales en general, y no incluye la interfaz de la aplicación Gemini ni la funcionalidad Gems para flujos de trabajo de productividad como la creación de resúmenes o diapositivas.

### Vertex AI Workbench
Vertex AI Workbench proporciona cuadernos Jupyter gestionados y preconfigurados con los marcos y bibliotecas de aprendizaje automático más populares. Esto ofrece un entorno altamente flexible y colaborativo para que los científicos de datos escriban código (Python, R, etc.), realicen limpiezas de datos complejas, lleven a cabo análisis exploratorios de datos e implementen técnicas personalizadas de ingeniería de características de forma iterativa. Su integración con otros servicios de Google Cloud lo convierte en un centro neurálgico para los científicos de datos. Es la herramienta ideal para la preparación interactiva e iterativa de datos.

### Vertex AI Search
Vertex AI Search es eficaz para indexar y buscar datos empresariales, pero no proporciona la experiencia conversacional ni la orquestación basada en agentes que ofrece Agentspace.

### Vertex AI Vision
Vertex AI Vision es una plataforma diseñada específicamente dentro de Vertex AI que permite a los usuarios crear e implementar aplicaciones de visión artificial, incluyendo la clasificación de imágenes, con un mínimo o ningún código. A menudo utiliza modelos preentrenados y ofrece una interfaz intuitiva para tareas como el etiquetado de imágenes y el entrenamiento de modelos para tareas de visión específicas, lo que la hace ideal para usuarios con conocimientos técnicos y presupuesto limitados.

### Vertex AI Pipelines
Vertex AI Pipelines, se utilizan para orquestar y automatizar flujos de trabajo de aprendizaje automático. Si bien son potentes para las operaciones de aprendizaje automático, requieren experiencia en la creación y definición de canalizaciones, lo cual está fuera del alcance de una "solución sin código" para un usuario que "no cuenta con especialistas internos en IA".

### Vertex AI Model Garden
Vertex AI Model Garden Proporciona acceso a una amplia gama de modelos preentrenados y de código abierto que se pueden descubrir, probar, personalizar e implementar. Si bien ofrece opciones para diversos modelos, su uso, especialmente su personalización, suele requerir cierto nivel de programación y conocimientos de aprendizaje automático. Representa un paso hacia la democratización, pero no es estrictamente "sin código" para tareas personalizadas como la clasificación de imágenes específicas sin conocimientos técnicos previos.
### Google Agentspace
Google Agentspace permite la creación de agentes con IA que pueden acceder y gestionar datos en múltiples sistemas empresariales. Facilita la interacción de los usuarios mediante una interfaz conversacional, mejorando la toma de decisiones y la eficiencia operativa.

Google Agentspace permite crear agentes seguros con IA capaces de comprender consultas, recuperar información de diversas fuentes de datos y proporcionar respuestas contextuales en tiempo real, lo que resulta ideal para el entorno bancario.

### Cloud Data Fusion
Cloud Data Fusion es un servicio de integración de datos nativo de la nube, totalmente administrado, que ayuda a los usuarios a crear y gestionar flujos de trabajo ETL/ELT. Si bien es excelente para la transformación de datos, se centra más en la creación y orquestación visual de flujos de trabajo para tareas repetibles por lotes o en tiempo real, en lugar de la exploración interactiva e iterativa de datos y la ingeniería de características que suelen realizar los científicos de datos en un entorno de notebook. Se enfoca menos en la manipulación exploratoria de datos ad hoc y más en la creación estructurada de flujos de trabajo.

### Veo
Veo genera vídeos de alta calidad a partir de textos, lo que lo hace ideal para crear contenido breve y atractivo para campañas sin necesidad de grabaciones.

Veo es un modelo de la Fundación Google diseñado específicamente para la generación de vídeo, capaz de producir vídeos con calidad cinematográfica a partir de texto o imágenes.

Veo es el modelo de última generación de Google para la generación de vídeo a partir de texto. Está diseñado específicamente para crear videoclips de alta calidad y alta resolución a partir de textos, con un control avanzado sobre elementos cinematográficos como movimientos de cámara, iluminación y composición de escena. Esto se ajusta perfectamente a la necesidad de las productoras de cine de previsualizar escenas de películas.

### AudioLM
AudioLM es un modelo para generar audio, como voz o música, a partir de diversas entradas. No tiene ninguna relación con la generación de vídeo.

### Duet AI
Mejora la productividad, pero se centra en el conjunto de herramientas de Google en lugar de en la compatibilidad multiplataforma..

## Duet AI for Google Workspace
Duet AI (ahora Gemini para Google Workspace) está diseñado específicamente para integrar capacidades de IA generativa directamente en las aplicaciones de Google Workspace, como Docs, Gmail, Slides y Sheets. Esto permite a los usuarios generar texto (borradores de correo electrónico, textos de marketing), crear imágenes para presentaciones, resumir contenido y organizar datos mediante indicaciones en lenguaje natural, lo que facilita enormemente las tareas diarias de los usuarios sin conocimientos técnicos.

### Google Cloud Contact Center AI
- Contact Center AI es un conjunto de servicios enfocado en mejorar las operaciones de atención al cliente, principalmente a través de agentes virtuales y asistencia a agentes. Su propósito es la interacción con el cliente, no la creación de contenido interno para equipos de marketing dentro de aplicaciones de productividad.

- Contact Center AI (CCAI) permite a las empresas implementar agentes virtuales inteligentes, brindar asistencia a agentes en vivo con sugerencias en tiempo real y gestionar transiciones fluidas, todo ello manteniendo una experiencia de cliente consistente en canales de voz y digitales.

- Esta es la solución integral de Google Cloud para modernizar las operaciones de atención al cliente. Integra canales de voz, chat y mensajería, e incluye funciones como agentes virtuales, asistencia a agentes y análisis de llamadas, todo ello diseñado pensando en la seguridad y la escalabilidad.


### AI Hub
AI Hub es un repositorio para compartir componentes y soluciones de IA, pero no proporciona soporte directo al cliente ni capacidades conversacionales.

### Codey
Codey está diseñado específicamente para casos de uso de programación, incluyendo la respuesta a preguntas técnicas de codificación, la depuración y la generación de código en lenguajes como Python, JavaScript y Go. Es el modelo más adecuado para escenarios de asistencia a desarrolladores.

### Gemma
Gemma es una familia de modelos abiertos y ligeros optimizados para tareas generales, no específicamente para asistencia en codificación o generación de código.

Gemma es un modelo de texto ligero y de código abierto, adecuado para uso local y con baja latencia, pero no admite el procesamiento multimodal ni las grandes ventanas de contexto necesarias para resumir conversaciones largas.

### Bard
Bard es una IA conversacional impulsada por Gemini, pero no está específicamente entrenada ni optimizada para tareas relacionadas con la programación como lo está Codey.

### Imagen
Imagen is a text-to-image generation model and not applicable for coding or chatbot support.

### Metadata
Metadata refers to data about data (e.g., timestamps, authorship), not the primary features or labels used for training.

### Datos etiquetados
Los datos etiquetados incluyen características de entrada (notas del paciente) y sus etiquetas de salida correspondientes (diagnósticos), lo que los hace adecuados para el aprendizaje supervisado.

### Aprendizaje supervisado
El aprendizaje supervisado requiere pares de entrada-salida etiquetados. El sistema no se entrena con datos históricos etiquetados, sino que aprende a partir de la retroalimentación en tiempo real mediante interacciones.

### Datos sin etiquetar
Los datos sin etiquetar carecen de la variable objetivo (en este caso, el diagnóstico). Dado que se proporcionan diagnósticos, los datos están etiquetados.

### Datos sintéticos
Los datos sintéticos se generan artificialmente en lugar de recopilarse a partir de interacciones del mundo real. En este caso, el conjunto de datos proviene de notas de pacientes reales, por lo que esta regla no aplica.

---

### Data Poisoning Attack
This is the correct answer. Data poisoning involves introducing malicious or carefully crafted data into the training dataset of an AI model. The goal is to compromise the integrity, performance, or introduce backdoors into the model, making it behave unpredictably or maliciously when presented with specific inputs in production. The adversary's method of "injecting imperceptible malicious examples" directly points to this threat.

### Data leakage
Data leakage occurs when future or unintended information is included in training, allowing the model to “cheat” by using data unavailable in real time.

### Few-shot prompting
Few-shot prompting is a highly effective and direct method for guiding a generative model to produce outputs that adhere to a specific format or style. By providing a few examples of desired input-output pairs in the prompt, the model learns the intended pattern and is more likely to generate consistent summaries. This is often the first and most efficient step for improving format consistency before considering more resource-intensive methods.

### RLHF
Si bien RLHF es una técnica poderosa, depender únicamente de la retroalimentación de la fase de producción es demasiado reactivo. La IA responsable requiere mitigación proactiva, incluyendo auditorías de sesgo y explicabilidad durante las fases de desarrollo y prueba.

---
### Generative Pretrained Transformer (GPT)
GPT es un tipo de modelo de lenguaje a gran escala (LLM, por sus siglas en inglés) optimizado para generar texto en lenguaje natural coherente y relevante a partir de indicaciones. Es ideal para tareas como la generación automática de descripciones de productos a partir de palabras clave o datos estructurados.

### Aprendizaje por refuerzo
El aprendizaje por refuerzo es la opción correcta: aprender mediante recompensas y penalizaciones para optimizar la toma de decisiones secuenciales es una configuración clásica del aprendizaje por refuerzo.

### Aprendizaje supervisado
El aprendizaje supervisado utiliza datos previamente etiquetados. En este caso, el robot interactúa con el entorno, no aprende a partir de ejemplos etiquetados.

### Aprendizaje generativo
El aprendizaje generativo se refiere normalmente al aprendizaje de distribuciones o a la generación de contenido nuevo (por ejemplo, imágenes o texto), no al comportamiento basado en recompensas.

### Aprendizaje por transferencia
El aprendizaje por transferencia implica reutilizar el conocimiento de un dominio en una tarea relacionada. No implica aprender mediante retroalimentación y recompensa en tiempo real.

---
### Image Generation
Image generation creates new images based on prompts or existing data. While it could be used for creating personalized visuals in marketing, it doesn't directly address the text-based nature of product recommendations and marketing campaign content as broadly implied. The primary need is for textual personalization.

### Text Generation for Personalized User Needs
Este tipo de solución de IA generativa está diseñada específicamente para crear textos con un lenguaje natural que se adaptan a las preferencias individuales del usuario, a sus datos históricos y a contextos específicos. Esto se alinea directamente con la generación de recomendaciones de productos personalizadas (por ejemplo, «Según tus compras recientes, te recomendamos…») y mensajes de campañas de marketing a medida (por ejemplo, contenido dinámico para correos electrónicos, textos publicitarios personalizados).

### Data Augmentation
Data augmentation involves creating new synthetic data points from existing ones to expand datasets for training other AI models. While it can indirectly support the development of personalization models by providing more training data, it is not a direct solution for generating personalized content for end-users.

### Code Generation
Code generation focuses on automating the creation of programming code. While valuable for developer productivity, it directly addresses the business objective of personalized customer engagement through product recommendations and marketing content.

--- 
## Los parámetros de generación de contenido
Los parámetros de generación de contenido son valores de configuración que controlan el comportamiento, la creatividad y la longitud de las respuestas de los modelos de lenguaje.

## Creatividad y Aleatoriedad
- **Temperatura:** Controla el nivel de sorpresa o variedad en las palabras elegidas. Valores bajos generan respuestas predecibles y directas; valores altos producen textos más creativos e inesperados.

- **Top-P (Muestreo de Núcleo):** Limita las opciones de palabras a un porcentaje acumulativo de probabilidad. Un valor bajo restringe el vocabulario a los términos más probables.

- **Top-K:** Restringe la selección de la siguiente palabra solo a las "K" opciones con mayor probabilidad matemática.

## Longitud y Control de Salida
- **Máximo de tokens:** Define el límite superior de longitud para la respuesta generada (un token equivale aproximadamente a 3/4 de una palabra en inglés).

- **Penalización de frecuencia:** Reduce la probabilidad de repetir exactamente las mismas palabras o frases ya usadas en el texto.

- **Penalización de presencia:** Penaliza el uso de términos basándose en si ya aparecieron antes, fomentando la introducción de temas nuevos.

---
### top-p
El muestreo top-p (muestreo de núcleo) selecciona tokens del conjunto más pequeño posible cuya probabilidad acumulada supera el valor top-p. Un valor top-p más alto implica que el modelo considera un conjunto mayor de tokens menos probables (y, por lo tanto, más diversos) para la generación, lo que aumenta la variabilidad y la creatividad del resultado. Para la lluvia de ideas, esto es muy conveniente para obtener una gama más amplia de ideas.

### Temperature
Temperature controls the randomness of the token selection. A lower temperature (closer to 0) makes the model more deterministic and less likely to pick lower-probability tokens, resulting in more predictable, conservative, and often generic outputs. This would counteract the goal of generating diverse and innovative taglines.


#### EJEMPLO:
17.- *Un equipo está desarrollando una aplicación de IA generativa para la creación de resúmenes de documentos legales. Es fundamental garantizar que los resúmenes sean concisos, aborden directamente los puntos legales clave y eviten detalles superfluos. ¿Qué combinación de parámetros de muestreo sería la más eficaz para lograrlo manteniendo la precisión factual?*

Temperatura baja: Esto reduce la aleatoriedad y hace que el modelo sea más determinista, favoreciendo los tokens de alta probabilidad. Esto es crucial para la precisión de los datos y para asegurar que el modelo se ciña a la información principal del documento legal, reduciendo el riesgo de inventar detalles.

Top-p bajo: De forma similar a la temperatura baja, un valor de top-p más bajo restringe las opciones de tokens a las más probables, reduciendo aún más la diversidad y asegurando que el resultado sea conciso y directo, evitando detalles superfluos.

MaxOutputTokens adecuado: Esto permite al equipo controlar la longitud del resumen, asegurando la concisión sin omitir información esencial. Esta es una configuración práctica para gestionar la longitud del resultado. Esta combinación garantiza que el resultado sea preciso, objetivo y se ajuste al contenido del documento.


---
### Límite de conocimiento / Knowledge Cutoff
El límite de conocimiento se refiere a la incapacidad del modelo para acceder a información anterior a su fecha de entrenamiento. El problema descrito (estereotipos de género, lenguaje excluyente) no radica en hechos obsoletos, sino en sesgos inherentes presentes en los datos de entrenamiento, independientemente de su antigüedad.

### Casos extremos / Edge Cases
Los casos extremos son entradas inusuales o poco frecuentes que provocan un rendimiento deficiente del modelo. La descripción sugiere un problema más generalizado (estereotipos sutiles y lenguaje excluyente) que puede aparecer en diversas salidas, lo que indica un sesgo sistémico en lugar de un fallo en una entrada específica y poco frecuente.

### Alucinaciones / Hallucinations
Las alucinaciones implican que el modelo invente información que no es verdadera o que no se deriva lógicamente. Si bien el lenguaje sesgado puede ser "incorrecto" en un sentido social, no es una invención fáctica como lo es una alucinación. El modelo refleja patrones que aprendió, aunque indeseables, de sus datos de entrenamiento.

### Sesgo / Bias
Los modelos de Foundation se entrenan con conjuntos de datos masivos extraídos de internet, que inevitablemente contienen sesgos sociales, estereotipos y prejuicios históricos presentes en el lenguaje y el contenido humanos. Cuando el modelo aprende de estos datos sesgados, puede perpetuar e incluso amplificar estos sesgos en sus resultados, lo que da lugar a un lenguaje injusto, discriminatorio o excluyente.

---

### Indicaciones de una sola muestra / One-shot prompting
Las indicaciones de una sola muestra incluyen un ejemplo para guiar el comportamiento del modelo. Mejoran el rendimiento al demostrar la relación esperada entre entrada y salida, especialmente cuando las indicaciones de cero muestras son insuficientes.

### Indicaciones de rol / Role prompting
Las indicaciones de rol implican definir un perfil (por ejemplo, «Eres un agente de atención al cliente servicial»), lo cual no es la técnica principal utilizada aquí.
 
### Indicaciones de cero muestras / Zero-shot prompting
Las indicaciones de cero muestras no proporcionan ejemplos y esperan que el modelo generalice basándose únicamente en las instrucciones. No son adecuadas cuando se requiere una salida más clara y estructurada.

### Encadenamiento de indicaciones / Prompt chaining
El encadenamiento de indicaciones divide una tarea compleja en una secuencia de indicaciones interdependientes. Este escenario implica solo un ejemplo, no indicaciones secuenciales.

### Indicación con pocos ejemplos / Few-shot prompting
Al proporcionar algunos ejemplos de líneas de asunto de correo electrónico altamente efectivas en la indicación, el modelo aprende el tono, el estilo, la longitud y la concisión deseados. 
Aprovecha el aprendizaje contextual, lo que permite al modelo reconocer patrones a partir de un número limitado de ejemplos y generar nuevas respuestas coherentes con las proporcionadas. 
Esto es ideal cuando se dispone de ejemplos específicos para guiar la respuesta del modelo.

---

### Unimodal generative model
Unimodal models are limited to a single data type (e.g., text-only or image-only). The scenario explicitly requires multiple data types, ruling this out.

### Diffusion model
Diffusion models are typically used for image generation from noise through denoising processes, not for processing multiple modalities like video and text together.

### Reinforcement learning model
**El aprendizaje por refuerzo** se utiliza para la toma de decisiones y acciones secuenciales, no principalmente para generar resúmenes a partir de entradas multimodales.

- EJEMPLO: El dron interactúa con el entorno, recibe recompensas diferidas y ajusta su estrategia para maximizar la recompensa acumulada, características fundamentales del aprendizaje por refuerzo.

El aprendizaje por refuerzo (RL) implica aprender comportamientos óptimos mediante señales de recompensa. El sistema explora acciones (ajustes), observa los resultados y utiliza la retroalimentación (como la eficiencia energética) para mejorar con el tiempo.

### Multimodal foundation model
This model type is specifically designed to handle inputs from multiple modalities, such as video, text, and audio. It's the best choice for generating summaries from multimodal input like spoken content in videos.

---

### Data agent
Los agentes de datos se especializan en gestionar tareas de datos como la ingesta, la transformación, la limpieza y la estructuración, lo que se ajusta perfectamente al escenario descrito.
Los agentes de datos ayudan a procesar y organizar los datos de entrada, pero no son responsables de generar el contenido creativo de las campañas.

### Workflow agent
Los agentes de flujo de trabajo gestionan la ejecución y la orquestación de procesos de varios pasos, pero no generan el contenido de marketing propiamente dicho.

### Code agent
Los agentes de código se centran en tareas de desarrollo de software, como escribir o analizar código fuente, lo cual no es el caso de uso que nos ocupa.

### Content agent
Los agentes de contenido se especializan en crear y gestionar contenido generativo, como textos de marketing, publicaciones en redes sociales, imágenes o vídeos, lo que encaja perfectamente con este caso de uso.

---

### Vertex AI Model Registry
Vertex AI Model Registry es un repositorio centralizado para gestionar el ciclo de vida de los modelos de aprendizaje automático, incluyendo el control de versiones, los metadatos y la gestión de fases (p. ej., desarrollo, producción). Es donde se almacenan y gestionan los modelos entrenados antes de su implementación, pero no facilita el proceso de entrenamiento en sí.

### Vertex AI Custom Training
Vertex AI Custom Training permite a los usuarios ejecutar su código de entrenamiento personalizado en la infraestructura gestionada de Google Cloud. Esto incluye especificar los tipos de máquinas (con GPU), configurar el entrenamiento distribuido e integrarse con servicios de ajuste de hiperparámetros. Ofrece la flexibilidad necesaria para entrenar prácticamente cualquier arquitectura de modelo, incluidos grandes modelos de IA generativa, aprovechando los recursos informáticos escalables de Google Cloud. Este es el servicio principal para ejecutar trabajos de entrenamiento personalizados.

### Vertex AI Experiments
Vertex AI Experiments se utiliza para realizar el seguimiento y la gestión de experimentos de aprendizaje automático, incluyendo parámetros, métricas y modelos generados. Si bien es fundamental para llevar un registro de las ejecuciones de entrenamiento y sus resultados, no realiza el entrenamiento en sí; simplemente registra los metadatos de las tareas de entrenamiento. Es una herramienta de gestión y seguimiento, no un motor de ejecución para el entrenamiento.

### Vertex AI Prediction
Vertex AI Prediction se centra en el despliegue y la prestación de servicios a modelos entrenados para la inferencia. Esto incluye la gestión de puntos finales, el procesamiento de solicitudes de predicción (por lotes o en línea) y la configuración del escalado automático. Se utiliza después de que un modelo haya sido entrenado y evaluado, no durante el proceso de entrenamiento en sí.

---

### TPU
Esto resalta con precisión la principal ventaja de las TPU. 
El aprendizaje profundo, y especialmente la IA generativa, depende en gran medida de multiplicaciones y convoluciones de matrices a gran escala. 
Las TPU son aceleradores de hardware diseñados específicamente para este fin, cuya arquitectura (por ejemplo, Unidades de Multiplicación de Matrices) está diseñada precisamente para acelerar estas operaciones con un alto rendimiento y eficiencia energética. 
Esta especialización suele traducirse en tiempos de entrenamiento significativamente más rápidos y un menor coste por operación de entrenamiento/inferencia para modelos de IA generativa grandes y complejos, en comparación con las GPU de propósito general, especialmente a gran escala (TPU Pods).

Las TPU en la arquitectura de hipercomputación de Google Cloud ofrecen computación densa, interconexiones personalizadas (por ejemplo, conmutación de circuitos ópticos) y software integrado como XLA (Álgebra Lineal Acelerada), lo que las hace ideales para entrenar modelos LLM basados ​​en transformadores y otros modelos generativos.



---

### Vertex AI Model Garden, Vertex AI Search, and AutoML

Este trío de herramientas responde directamente a las necesidades de los desarrolladores en este escenario:

**Model Garden** ofrece modelos base preentrenados (p. ej., Gemini, PaLM, Imagen) que se pueden ajustar fácilmente, lo que permite a los desarrolladores crear modelos de aprendizaje automático potentes listos para usar.

**Vertex AI Search** proporciona capacidades de búsqueda de nivel empresarial con comprensión del lenguaje natural y generación aumentada de recuperación (RAG), lo que la hace ideal para navegar por documentos médicos o bases de conocimiento.

**AutoML** permite a usuarios sin experiencia entrenar modelos personalizados con un mínimo de código, utilizando técnicas avanzadas como el aprendizaje por transferencia. Abstrae gran parte de la complejidad del entrenamiento y la evaluación de modelos, lo que resulta ideal para equipos con conocimientos limitados en aprendizaje automático.

En conjunto, estas herramientas aceleran el desarrollo de IA, reducen el tiempo de obtención de valor y disminuyen las barreras técnicas, lo que las hace perfectamente adecuadas para este escenario.

---
### Relevance
Relevance pertains to whether the data is applicable to the task at hand. The focus here is on accessibility and technical usability, not topical alignment.
This is the most critical factor. If the training data contains information that is outdated, unrelated to customer preferences, or includes topics that are considered sensitive or inappropriate for marketing, the generative AI model will learn from this irrelevant information. This can lead to the generation of marketing emails that are not only ineffective but potentially alienating or even offensive to the customer, directly addressing the "irrelevant or off-putting content" aspect of the question.


### Confidentiality
Confidentiality deals with security and privacy concerns. While important, it’s not relevant to the formatting and accessibility issue raised in this scenario.

### Format
Format impacts accessibility — whether the data is in machine-readable formats (e.g., JSON, CSV, or structured PDFs). Uniform encoding and structure are critical for preprocessing and ingestion in AI pipelines.

### Completeness
Completeness is about the presence of all necessary data fields. The question does not mention missing fields but rather structure and readability.

---

### XAI tools
XAI tools (e.g., SHAP, LIME, attention visualizations) provide transparency into AI decisions, addressing compliance needs without removing the model's generative benefits.


---

## Model management 
Model management (often referred to as MLOps) is the overarching stage that encompasses monitoring the deployed model's performance, detecting issues like data drift and concept drift, analyzing model behavior, and implementing strategies for retraining, versioning, and updating models to maintain their effectiveness in production. It is a continuous, iterative process crucial for the long-term success of ML systems.

## Model training
Model training is where the algorithm learns patterns from the prepared data to build the model. While retraining is a common response to model degradation, the act of detecting performance issues and drift occurs after training and deployment, in the management phase. Training is about building the model, not monitoring it in production.

## Model deployment 
Model deployment is the act of making the trained model available for inference. This stage ensures the model is accessible and can serve predictions. However, it doesn't encompass the ongoing monitoring, maintenance, and retraining activities needed to keep the model healthy in the long term. It's the launch point, not the ongoing operations center.

## Data preparation
Data preparation involves cleaning, transforming, and engineering features from raw data. Issues in data preparation can lead to poor model performance, but this stage focuses on getting the data ready for training, not on monitoring the deployed model's performance or addressing post-deployment drift.