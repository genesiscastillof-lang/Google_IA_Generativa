**EL ROL**

actua como un desarrollador de integraciones postulando a un puesto de especialista de integraciones.

**EL OBJETIVO**

responder a la entrevista para el puesto mencionado con el gerente TI integracion XXXXXXXXX del Banco BCI en chile.

**EL CONTEXTO**

Segun el anuncio del empleo, dice asi:

Diseñar e implementar los microservicios y APIs que permiten habilitar la plataforma de Integración del banco, con el fin de dar soporte al proceso de transformación digital en Bci, permitiendo que la corporación pueda contar con una plataforma basada en componentes independientes, autónomos y escalables, entregados de forma rápida y oportuna, con foco en la excelencia y utilización óptima de recursos.

*Las funciones son:*
- Implementar APIs y microservicios en los distintos proyectos/programas de Transformación Digital, basados en un modelo de referencia para servicios financieros y en estándares de la industria, que posteriormente pasarán a formar parte del catálogo de microservicios del banco.Permitir que nuevos productos y servicios puedan ser entregados de forma ágil, poniendo énfasis en la reutilización de componentes.
- Proveer APIS y microservicios tanto para nuestros clientes internos como externos.
- Participar en la co-creación de un gobierno robusto(procesos, roles, tecnología) que permita entregar en tiempo, forma y calidad los microservicios a nuestros clientes.
- Ser un referente técnico de APIs y microservicios.
- Generar y difundir conocimiento al interior del banco, con el fin de mejorar la competitividad y lograr diferenciación, apropiándose del plan de carrera que permita el desarrollo personal y profesional, de manera que se genere un entorno de motivación y crecimiento laboral de él y de sus pares.
- Resguardar la calidad en el diseño, implementación y rendimiento óptimo de las APIs y microservicios, cumpliendo oportunamente los compromisos del proyecto.
- Adoptar las prácticas de Delivery Continuo.
- Optimizar los tiempos de paso a producción realizando entregas continuas para los clientes internos y externos. Con foco en mejorar el time-to-value y lograr eficiencias mediante la disminución de los esfuerzos de certificación.

**LA ESTRUCTURA**

elaborar 30 principales preguntas posible que pueda hacer para esta entrevista con el gerente.

---

# Preguntas y respuestas — Entrevista Bci (con ejemplos y recursos)

## 1. Motivación y fit

**1. ¿Por qué te interesa este puesto y por qué en Bci?**

Porque Bci lidera la transformación digital en Chile y quiero aportar mi experiencia en integración a una plataforma que impacta a millones de clientes.

**2. ¿Qué entiendes por "plataforma de integración" y cuál es su rol en la transformación digital?**

Es la capa que conecta sistemas heterogéneos (core, canales, terceros) mediante APIs y microservicios estandarizados, habilitando agilidad y reutilización.

**Una plataforma de integración (como iPaaS o un bus de servicios)**
- Es un software centralizado que conecta diferentes aplicaciones, sistemas y datos dispersos para que funcionen como un solo conjunto.

**Rol en la transformación digital**
- **Interoperabilidad:** Permite que sistemas antiguos y modernos compartan información en tiempo real sin romper procesos.
- **Automatización:** Conecta flujos de trabajo entre departamentos para reducir tareas manuales y errores.
- **Visión unificada de datos:** Centraliza la información para mejorar la toma de decisiones y el análisis con herramientas modernas.
- **Agilidad:** Acelera la creación de nuevos servicios digitales y la adaptación a las necesidades del mercado.

**3. Cuéntame tu trayectoria: ¿cómo llegaste a especializarte en integraciones/APIs?**

Empecé en desarrollo backend, migré a integración por SOA/ESB, y con el tiempo me especialicé en APIs REST y microservicios cloud-native.

**4. ¿Qué te atrae de trabajar en un sector regulado como el financiero?**

Me atrae el nivel de exigencia técnica y de seguridad que exige el rubro financiero; es un entorno donde la calidad del diseño realmente importa.

## 2. Diseño de APIs y microservicios

**5. ¿Qué principios sigues al diseñar una API REST?**

Contract-first, diseño orientado a recursos, versionado semántico y documentación con OpenAPI/Swagger. 

Como referencia, suelo recomendar estos dos videos:
- [Deep Dive into REST API Design and Implementation Best Practices](https://www.youtube.com/watch?v=7nm1pYuKAhY)
- [9 Must-Know REST API Design Principles for Developers](https://www.youtube.com/watch?v=pJ83mmqcvoQ)

**6. ¿Cómo diseñarías una API para que sea reutilizable por múltiples equipos?**

Definiendo contratos genéricos y desacoplados del consumidor, con capacidades configurables (parámetros, filtros) en vez de endpoints ad-hoc. 

    Por ejemplo: en vez de crear `/clientes/activos` y `/clientes/inactivos`, diseñaría un único endpoint `/clientes?estado=activo` que cualquier equipo (canal web, app, un tercero) pueda consumir ajustando solo los parámetros, sin duplicar lógica de negocio.

Video de referencia: [Microservices Best Practices](https://www.youtube.com/watch?v=Ljj166lMj4s).

**7. ¿Diferencias entre microservicios y monolito, y cuándo elegir cada uno?**

- Monolito para dominios simples o equipos pequeños; 
- Microservicios cuando se necesita escalar, desplegar independiente y aislar fallas.

**8. ¿Cómo abordas el versionado de APIs sin romper a los consumidores?**

Versionado en la URL o header, manteniendo compatibilidad hacia atrás y períodos de convivencia antes de deprecar. 
    Ejemplo: si `/v1/transferencias` cambia su estructura de respuesta, publico `/v2/transferencias` con el nuevo contrato, mantengo `/v1` operativo y monitoreado durante un período de transición (ej. 6 meses), notifico a los consumidores vía changelog y solo deprecio `/v1` cuando confirmo que ya no recibe tráfico relevante.

**9. ¿Qué patrones usas para la comunicación entre microservicios?**

Síncrono (REST) para consultas en tiempo real; eventos/colas (Kafka, RabbitMQ) para desacoplar procesos y mejorar resiliencia.

**10. ¿Cómo garantizas idempotencia y manejo de errores en transacciones distribuidas?**

    Uso de idempotency keys, patrones saga/compensación y manejo explícito de reintentos con backoff. 

*la idempotencia*
- Garantizo la idempotencia mediante la implementación de Identificadores Únicos de Transacción (Idempotency Keys) generados por el cliente. 
- Al recibir una petición, el sistema verifica en una base de datos centralizada o caché distribuida (como Redis) si ese ID ya fue procesado. 
- Si el ID ya existe, se retorna directamente el resultado almacenado de la primera ejecución sin duplicar la lógica de negocio. 
- Si no existe, se procesa la transacción y se registra el ID junto con su resultado en una operación atómica.

Video tutorial recomendado: [Saga Pattern: Mastering Distributed Transactions](https://m.youtube.com/watch?v=iJT8ehN8A_I).

**11. ¿Qué experiencia tienes con API Gateways?**

    He trabajado con Apigee para gestión de tráfico, seguridad, rate limiting y analítica de consumo.

*APIGEE*
Tengo un conocimiento sólido y teórico sobre el funcionamiento y la arquitectura de los API Gateways, aunque todavía no me ha tocado implementarlos en un entorno de producción real.
Entiendo perfectamente que actúan como un punto de entrada único para microservicios, encargándose de tareas críticas como la gestión de tráfico (rate limiting), autenticación (OAuth/JWT), enrutamiento de peticiones y abstracción de la arquitectura interna.

He estudiado y seguido de cerca soluciones populares del mercado como Apigee, comprendiendo sus casos de uso. 

**12. ¿Cómo diseñarías un microservicio expuesto a clientes internos y externos?**

Un mismo backend con dos "fachadas" (gateway interno y externo), políticas de seguridad y throttling diferenciadas por audiencia.

## 3. Arquitectura e integración bancaria

**13. ¿Experiencia integrando sistemas core bancarios o legados?**

He integrado sistemas legados vía adaptadores/middleware, exponiendo sus funcionalidades como APIs modernas sin tocar el core.

**14. ¿Cómo aseguras una API que expone datos financieros sensibles?**

OAuth2/OIDC, mTLS, cifrado en tránsito y reposo, tokenización de datos sensibles y validación estricta de scopes.

OAuth2/OIDC, mTLS, cifrado, tokenización, scopes
Seguridad en capas: transporte, autenticación, autorización y datos.

    Para asegurar una API que maneja datos financieros sensibles, se debe implementar una estrategia de defensa en profundidad. Esto significa aplicar múltiples capas de seguridad tanto en la autenticación, la infraestructura como en el ciclo de vida del dato.

**15. ¿Qué sabes sobre Open Banking, ISO 20022 o BIAN?**

Conozco los principios de Open Banking (consentimiento, APIs estandarizadas) y modelos de referencia tipo BIAN para dominios financieros.

Consentimiento, APIs estandarizadas, modelo de referencia BIAN
Estándares clave para interoperabilidad en servicios financieros.

**Open Banking, ISO 20022 o BIAN en BCI**

- **Open Banking (Banca Abierta):** Bci es pionero y referente en Chile en la implementación de este modelo. Cuenta con herramientas como el Bci API Market y su plataforma 360 Connect, que permite a las empresas integrar saldos y movimientos de otros bancos de forma centralizada.
- **ISO 20022:** Es el estándar mundial para el intercambio electrónico de datos entre instituciones financieras. Los bancos modernos, incluido Bci, lo adoptan para homologar pagos internacionales y locales con mayor cantidad de datos y seguridad.
- **BIAN (Banking Industry Architecture Network):** Es un marco global de arquitectura de microservicios para la banca. Muchas entidades que realizan transformaciones digitales profundas —como la estrategia de innovación de Bci— usan BIAN como guía para estructurar sus sistemas internos.

**16. ¿Cómo manejas alta disponibilidad en un microservicio crítico?**

Con redundancia, circuit breakers, timeouts, health checks y diseño stateless para escalar horizontalmente.

**17. ¿Qué consideraciones de cumplimiento normativo tomas en cuenta?**

- Trazabilidad de datos, 
- minimización de información sensible expuesta y 
- cumplimiento de normativa de protección de datos vigente.

## 4. Delivery continuo y DevOps

**18. ¿Qué experiencia tienes con pipelines de CI/CD?**

He implementado pipelines con Jenkins/GitLab CI: build, test automatizado, análisis estático y despliegue automatizado por ambiente.

**19. ¿Cómo reduces los tiempos de paso a producción sin sacrificar calidad?**

Automatizando pruebas y certificación, usando feature flags y despliegues progresivos (canary/blue-green).

**20. ¿Qué prácticas de testing automatizado aplicas?**

Pruebas unitarias, contract testing (Pact) e integración automatizada en el pipeline antes de cada release.

**Pruebas de Contrato (Contract Testing)**
- **Objetivo:** Asegurar que los cambios en el proveedor de la API no rompan la integración con el consumidor.
- **Pact / OpenAPI:** Definir acuerdos formales sobre la estructura exacta de los endpoints, encabezados y payloads.
- **Detección temprana:** Automatizar la validación del contrato en el pipeline de CI/CD para detectar cambios disruptivos (breaking changes) antes del despliegue.

**21. ¿Experiencia con contenedores y orquestadores?**

Sí, uso Docker para empaquetar servicios y Kubernetes para orquestación, escalado y auto-healing.

**22. ¿Cómo manejas el rollback de un microservicio que falla en producción?**

Con versionado de artefactos y despliegues blue-green/canary que permiten revertir rápido al estado anterior estable.

## 5. Gobierno y calidad

**23. ¿Qué entiendes por "gobierno de APIs"?**

**El gobierno de APIs (API Governance)**
El gobierno de APIs (API Governance) es el conjunto de normas, prácticas y herramientas que utiliza una organización para gestionar todo el ciclo de vida de sus APIs de forma centralizada.

*Sus objetivos principales son:*
- **Estandarizar:** Garantizar que todas las APIs sigan las mismas reglas de diseño, documentación y seguridad.
- **Evitar duplicidad:** Asegurar que no se creen APIs que hagan lo mismo, optimizando recursos.
- **Garantizar seguridad:** Controlar quién accede a los datos y proteger la información de la empresa.
- **Facilitar el uso:** Lograr que sean fáciles de descubrir y reutilizar por otros desarrolladores.

En resumen, es poner orden, control y calidad al ecosistema de APIs de una empresa para que crezca de forma segura y eficiente.




**24. ¿Cómo aseguras que un microservicio cumpla estándares antes de sumarse al catálogo?**

Con checklists de certificación automatizados: seguridad, documentación, pruebas y cumplimiento de convenciones de diseño.

**25. ¿Cómo mides la calidad y rendimiento de una API en producción?**

Con métricas de disponibilidad, latencia, tasa de error y dashboards de observabilidad (APM, logs centralizados).

**26. ¿Qué harías si un equipo quiere saltarse el proceso de certificación?**

Explicaría el riesgo de saltarse el proceso y buscaría una vía rápida pero segura, priorizando junto al equipo qué controles son innegociables.

## 6. Liderazgo y equipo

**27. ¿Cómo has liderado técnicamente o mentorizado a colegas?**

He liderado documentación de buenas prácticas y sesiones de mentoría técnica para nivelar a desarrolladores junior en diseño de APIs.

**28. Cuéntame de una vez que convenciste a un equipo de adoptar una buena práctica.**

Usé datos concretos (incidentes, deuda técnica) para mostrar el costo de no adoptar la práctica, y logré consenso gradual.

**29. ¿Cómo manejas el desacuerdo técnico dentro de un equipo?** 

*(respuesta alternativa)*

Priorizo separar el desacuerdo de la persona: pido que cada postura se sustente con un prototipo rápido o un caso de prueba (spike técnico) en vez de debatir solo en abstracto, así la decisión se basa en evidencia y no en jerarquía ni en quién argumenta mejor. Si el spike no despeja la duda, documento el trade-off (rendimiento vs. mantenibilidad, por ejemplo) y escalo la decisión al arquitecto o al dueño del dominio, dejando registro para futuras decisiones similares.

## 7. Situacional / cierre

**30. Cuéntame de un proyecto de integración desafiante que hayas liderado.**

Lideré la integración de un canal digital con el core bancario vía una capa de microservicios REST con caché y circuit breakers, reduciendo tiempos de respuesta en más de 40% y eliminando acoplamiento directo al legado.

---
# Otras Preguntas

## Contract-first

El enfoque Contract-first (o contrato primero) es una metodología de desarrollo de software donde se diseña y define la interfaz o el contrato de una API antes de escribir cualquier código de programación o lógica de negocio.

## Qué es Contract-first
- **Definición previa:** Se establece cómo se comunicarán el cliente y el servidor (URLs, métodos HTTP, datos de entrada y salida, códigos de error) usando lenguajes estándar como OpenAPI/Swagger (para REST) o WSDL (para SOAP).
- **Inversión del orden:** A diferencia del desarrollo tradicional (code-first), donde la interfaz surge automáticamente del código ya programado, aquí el documento del contrato es la fuente única de la verdad.
- **Trabajo en paralelo:** Una vez aprobado el contrato, los equipos de frontend y backend pueden trabajar al mismo tiempo. El frontend usa simuladores (mocks) basados en el contrato y el backend programa la lógica real sabiendo qué datos entregar.

## diseño de la API 

### cumple 3 caracteristicas mas comunes:*
- Una API facil de leer y usar 
- dificil de malinterpretar
- completa y concisa

### Aspecto mas importante del diseño de la API*
- que es la Nomenclatura (Naming)
    - declarar o usar siempre sustantivos para representar los recursos, NO VERBOS.
        - example.com/v1/store/items/{id}
        - example.com/1/store/employees/{id}

- Aprovechar la agrupación lógica reflejando la relación entre objetos.
    - es decir si un objeto puede contener otro object, debes diseñar el endpoint para que refleje esa condicion. 
        - Customer -> Orders 
            - ..../customers/orders
        - otro dato Spring HATEOAS
            Spring HATEOAS es una librería de Spring que ayuda a crear APIs REST que incluyen enlaces en sus respuestas, permitiendo que los clientes naveguen por la API de forma dinámica.HATEOAS significa Hypermedia As The Engine Of Application State (Hipermedia como motor del estado de la aplicación). En lugar de que el cliente deba conocer de antemano todas las URLs de la aplicación, el servidor le entrega enlaces junto con los datos para indicarle qué acciones puede realizar a continuación.
- Definir los nombres de sus endpoints, utilice sustantivos en plural para los recursos.
    - example.com/v1/store/items/{id}
    - example.com/v1/store/employees/{id}

- Collection es un grupo de recursos.
    - /orders    --> es una coleccion de pedidos.
    - /orders/99 --> es un recurso con la informacion sobre un pedido especifico.

- Utilzar GUIONES para mejorar la legibilidad de las URLs.  

- utilizar VERSIONAMIENTO ya sea en :
    - puntos finales  : /exampleo.com/v1/stores
    - como parametros : /example.com/stores?version=2

- Para filtering, sorting and pagination: 
    - filtrar datos por pares clave-valor específicos
        -   /customers?lastname=Smith&age=38
    - recuperar solo campos específicos por clave
        -   /customers?fields=projectId,quantity
    - limitar el número de elementos para los datos devueltos
        -   /customers?limit=50   
    - paginar los datos por bloques en lugar de consultarlos todos a la vez
        -   /customers?start=50&limit=100
    - ordenar los datos por un valor clave específico.
        -   /customers?sort=author,datepublished
        -   /customers?sort=+author,-datepublished
    - route controllers should not rely on side-effects
    - same request repeated for the same resource should result in same state
    - HTTP status codes im the response may differ
    - first  DELETE request: 204 (No Content)
    - second DELETE request: 404 (Not Found)

- Operaciones Asincronas
    - POST {orderId:99} -> /orders/create  ::  202 (Accepted)
    - GET ->  /orders/status/99 :: 200 (OK) { status: 'IN Progress' ... timeToCompleted: 3000 }
    - GET ->  /orders/status/99 :: 300 (See Other) {status: 'Completed'}
    - GET ->  /orders/99 :: 200 (OK) { orderId: 99 ,  description: 'Order 99' , ....}

    - Para mejorar la velocidad de carga de esos recursos, los usuarios deberían poder volver a intentarlo en fragmentos.
    - Los usuarios de los endpoints necesitan saber qué falló para poder corregir la solicitud.
    - Pero asegúrate también de no exponer la mecánica interna del controlador.
    - Asegúrate de devolver el código de estado HTTP correcto; existen muchos.
    - Por ejemplo, un cuerpo vacío de una solicitud GET debería devolver 204 (Sin contenido) en lugar de 200 (OK).

- Seguridad
    - Establezca el cifrado SSL/TLS como predeterminado para los endpoints de su API.
    - Autorización.
    - Implementación de ACL (Listas de Control de Acceso).
    - Limitación de velocidad, control de ancho de banda, bloqueo de IP, prevención de XSS.

- Documentacion
    - Open API (Swagger) Es un estandar codigo abierto para describir, documentar y visualizar los endpoints RESTful.
    - Permite a los desarrolladores definir la estructura, los endpoints, los formatos de solicitud y respuesta y otros detalle inmportantes de una API. 

## MONOLITO VS MICROSERVICIO

Aquí tienes 5 diferencias clave y breves entre ambas arquitecturas:

**Estructura:**
   - El monolito es un único bloque de código; 
   - los microservicios son componentes independientes.

**Despliegue:** 
   - El monolito se despliega todo junto; 
   - los microservicios se despliegan por separado.
** Escalabilidad:** 
   - El monolito escala todo el sistema; 
   - los microservicios escalan solo la parte necesaria.
** Tecnología:** 
   - El monolito usa una misma tecnología; 
   - los microservicios permiten usar diferentes lenguajes.
**Fallas:** 
   - Si el monolito falla, cae todo; 
   - si un microservicio falla, los demás siguen funcionando.

# La resiliencia

La resiliencia en software es la capacidad de un sistema para soportar fallos, recuperarse rápidamente y mantener su funcionamiento principal ante interrupciones, errores o picos de tráfico inesperados.

## Características Principales

- **Tolerancia a fallos:** El sistema no se desploma por completo si un componente secundario deja de funcionar.
- **Recuperación automática:** Vuelve a la normalidad en poco tiempo tras un error.
- **Degradación elegante:** Si una parte falla, reduce funciones específicas en vez de apagar todo el servicio.

## Patrones Comunes de Resiliencia
- **Reintento (Retry):** Vuelve a intentar una conexión fallida de forma automática.
- **Cortafuegos de circuitos (Circuit Breaker):** Detiene peticiones a un servicio dañado para evitar que colapse todo el sistema.
- **Tiempo de espera (Timeout):** Cancela una tarea si tarda demasiado en responder para liberar recursos.

----


# rate limiting 
rate limiting (o limitación de velocidad) es una técnica que controla el número máximo de peticiones que un cliente puede hacer a un servidor o API en un periodo de tiempo determinado.

    APIS

    es un mecanismo que permiten a 2 componentes de softwares comunicarse entre si mediante un conjunto de definiciones y protocolos.

- **API (Interfaz de Programación de Aplicaciones):** El canal de comunicación que permite a una aplicación pedir datos o servicios a otra.

- **REST (Transferencia de Estado Representacional):** Un estilo arquitectónico que hace que las APIs sean ligeras, rápidas y usen la estructura estándar de internet.

---
 # SOA vs ESB

- **SOA** es un enfoque de diseño de software donde los servicios se comunican de forma independiente, 
- **ESB** es la herramienta o bus central que ayuda a conectar esos servicios.


## ¿Qué es SOA?
- **Concepto:** Es la Arquitectura Orientada a Servicios (Service-Oriented Architecture).
- **Función:** Define cómo organizar los componentes de software en servicios independientes y reutilizables.
- **Objetivo:** Permitir que distintos sistemas de una empresa intercambien datos y funciones mediante interfaces comunes.

## ¿Qué es ESB?
- **Concepto:** Es el Bus de Servicio Empresarial (Enterprise Service Bus).
- **Función:** Es un patrón de software o middleware centralizado.
- **Objetivo:** Conectar aplicaciones para que se comuniquen entre sí, transformando datos y adaptando protocolos sin que los sistemas se conecten de forma directa.

## Diferencias Principales
- **Naturaleza:** SOA es un concepto de diseño (el "qué" hacer), y ESB es un componente tecnológico o infraestructura (el "cómo" implementarlo).
- **Alcance:** Puedes aplicar principios de SOA sin usar un ESB, pero un ESB se creó específicamente para cumplir con las necesidades de integración de una SOA.
- **Dependencia:** SOA existe por sí misma como estilo arquitectónico; un ESB depende de las aplicaciones y servicios que debe comunicar.

