# CERTUS Protocol

El protocolo Certus Protocol es una implementación de una cadena de bloques basada en Substrate que proporciona servicios de datos seguros y confiables para el ecosistema Polkadot.

## Descripción

Certus es un protocolo verificado en cadena que proporciona servicios de datos seguros y confiables para el ecosistema Polkadot. Es un oráculo híbrido descentralizado que realiza completamente la verificación en cadena y en cadena de los datos del oráculo. Utiliza un modelo desafiante innovador para garantizar la precisión de los datos.

## Diseño Detallado

El protocolo se basa en Substrate y se utiliza como una cadena relay chain para que diferentes parachains se conecten y se beneficien de la interoperabilidad. El proceso específico es el siguiente:

1. **Conexión a Parachains:** A través de la integración de la plataforma CDT Oraculo, envía solicitudes de datos.
2. **Escáner y Agregador:** El escáner obtiene datos de solicitudes externas y los envía al agregador. CDT Chain selecciona aleatoriamente un agregador a través del algoritmo VRF.
3. **Procesamiento y Agregación de Datos:** El agregador llama al procesador para agregar datos de múltiples fuentes de datos y enviarlos a la cadena de bloques CDT.
4. **Verificación y Desafío:** El nodo de verificación verifica los datos del agregador y desafía.
5. **Arbitraje:** El Comité de Reputación verifica los datos presentados por el impugnador y realiza un arbitraje.

## Participantes

- **Agregador:** Se encarga de obtener datos de solicitudes externas y agregarlos para proporcionar una fuente de datos precisa y confiable en la cadena de bloques.
- **Desafiador:** Verifica la integridad y validez de los datos enviados por el agregador y envía transacciones fraudulentas del agregador y datos correctos al Comité de Reputación para obtener recompensas.
- **Comité de Reputación:** Garantiza la seguridad de la red del Área al motivar a los retadores y castigar a los agregadores maliciosos.
- **Consumidor de Datos:** Obtiene datos fuera de la cadena de forma segura y eficaz para utilizarlos en contratos inteligentes, parachains, etc.
- **Operador de Nodo:** Verifica los datos para garantizar la seguridad de la red CDT y proporcionar el servicio Oráculo RPC.

## Resolución de Disputas

La seguridad de la red Certus está garantizada por un TPV muy estricto y con penalizaciones. Si un operador de nodo es identificado como un atacante, todos los tokens CVX prometidos por él se asignarán al comité de reputación, al retador y a la tesorería.

Para evitar manipulaciones maliciosas, CDT ha diseñado un mecanismo de desafío en el que el retador puede oponerse a la información. Iniciar un desafío requiere pagar una pequeña cantidad de tokens CVX y transmitirlos al Comité de Reputación. Si los nodos del Comité de Reputación son auditados como maliciosos, se marcará como un nodo malicioso y se tomarán medidas para congelar sus tokens.

En casos extremos, cuando los consumidores de datos sufren pérdidas debido a que los nodos maliciosos informan datos, pueden iniciar una propuesta para solicitar una compensación al tesoro estatal y votar a través de la comunidad para aprobar la compensación.

## Contribución

¡Las contribuciones son bienvenidas! Si deseas contribuir al protocolo CDT, sigue estos pasos:

1. Crea un fork del repositorio.
2. Realiza tus cambios en una nueva rama.
3. Envía un pull request.

## Licencia

Este proyecto está bajo la Licencia MIT. Consulta el archivo [LICENSE](LICENSE) para obtener más detalles.
