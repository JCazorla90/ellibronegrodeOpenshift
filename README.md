# El libro Negro de Openshift 🐱‍👤
![](https://i2.wp.com/becloudready.com/wp-content/uploads/2020/09/Screen-Shot-2020-09-30-at-9.02.29-AM.png?resize=1024%2C558&ssl=1)

![](https://img.shields.io/github/stars/jcazorla90) ![](https://img.shields.io/github/forks/jcazorla90/editor.svg) ![](https://img.shields.io/github/tag/jcazorla90/editor.svg) ![](https://img.shields.io/github/v/release/jcazorla90/editor.svg) ![](https://img.shields.io/github/issues/jcazorla90/editor.md.svg) ![](https://img.shields.io/bower/v/editor.md.svg)

*En Construcción*🚧
### Antes de empezar

- Este recopilatorio aún esta en construcción y pueden faltar apartados.
- Las recomendaciones y ejemplos que encuentre son de uso personal, siempre revise la documentación oficial de los productos mencionados, no me hago responsable del mal uso de la guia.
- En proximas actualizaciones se añadirán ejemplos y diagramas explicativos.
- Tome esta información como una opinión personal.
- 🚩 Esta información es información general sobre teoria de Kubernetes y OpenShift





**Contenidos**

-  El libro Negro de Openshift 🐱‍👤
    -   Antes de empezar

[OpenShift & Kubernetes](https://github.com/JCazorla90/ellibronegrodeOpenshift/blob/main/README.md#openshift--kubernetes)
-  [¿Qué es Kubernetes y cómo funciona?](https://github.com/JCazorla90/ellibronegrodeOpenshift/blob/main/README.md#qu%C3%A9-es-kubernetes-y-c%C3%B3mo-funciona)
-   [¿Qué es OpenShift y cómo se diferencia de Kubernetes?](https://github.com/JCazorla90/ellibronegrodeOpenshift/blob/main/README.md#qu%C3%A9-es-openshift-y-c%C3%B3mo-se-diferencia-de-kubernetes)
-   [¿Cómo se implementa la alta disponibilidad en un clúster de Kubernetes?](https://github.com/JCazorla90/ellibronegrodeOpenshift/blob/main/README.md#c%C3%B3mo-se-implementa-la-alta-disponibilidad-en-un-cl%C3%BAster-de-kubernetes)
-  [¿Cómo se realizamos el escalado automático en un clúster de Kubernetes?](https://github.com/JCazorla90/ellibronegrodeOpenshift/blob/main/README.md#c%C3%B3mo-se-implementa-la-alta-disponibilidad-en-un-cl%C3%BAster-de-kubernetes)
-   [¿Cómo se manejan las actualizaciones y las rollbacks en un clúster de Kubernetes?](https://github.com/JCazorla90/ellibronegrodeOpenshift/blob/main/README.md#c%C3%B3mo-se-manejan-las-actualizaciones-y-las-rollbacks-en-un-cl%C3%BAster-de-kubernetes)
-   [¿Cómo se realiza la monitoreo y el diagnóstico de problemas en un clúster de Kubernetes?](https://github.com/JCazorla90/ellibronegrodeOpenshift/blob/main/README.md#c%C3%B3mo-se-realiza-la-monitoreo-y-el-diagn%C3%B3stico-de-problemas-en-un-cl%C3%BAster-de-kubernetes)
-   [¿Cómo se implementan los despliegues continuos en un clúster de Kubernetes?](https://github.com/JCazorla90/ellibronegrodeOpenshift/blob/main/README.md#c%C3%B3mo-se-implementan-los-despliegues-continuos-en-un-cl%C3%BAster-de-kubernetes)
-   [Redes en Kubernetes y OpenShift](https://github.com/JCazorla90/ellibronegrodeOpenshift/blob/main/README.md#redes-en-kubernetes-y-openshift)
[-   Consideraciones para diseño de la arquitectura de OpenShift](https://github.com/JCazorla90/ellibronegrodeOpenshift/blob/main/README.md#consideraciones-para-dise%C3%B1o-de-la-arquitectura-de-openshift)
-   [¿Cómo se implementa la seguridad en un clúster de Kubernetes?](https://github.com/JCazorla90/ellibronegrodeOpenshift/blob/main/README.md#c%C3%B3mo-se-implementa-la-seguridad-en-un-cl%C3%BAster-de-kubernetes)
-   [¿Cómo se integran los servicios externos con un clúster de Kubernetes?](https://github.com/JCazorla90/ellibronegrodeOpenshift/blob/main/README.md#c%C3%B3mo-se-integran-los-servicios-externos-con-un-cl%C3%BAster-de-kubernetes)
    -   [Pasos para añadir seguridad a nuestro entorno](https://github.com/JCazorla90/ellibronegrodeOpenshift/blob/main/README.md#pasos-para-a%C3%B1adir-seguridad-a-nuestro-entorno-utilizando-un-servidor-externo-de-wazuh-puedes-seguir-los-siguientes-pasos)
    -  ⚡Siguiente actualización el uso de ArgoCD y ejemplos.



# OpenShift & Kubernetes

## ¿Qué es Kubernetes y cómo funciona?
Kubernetes es un sistema de orquestación de contenedores que permite automatizar la implementación, escalamiento y gestión de aplicaciones en contenedores.
Funciona creando y administrando clústeres de nodos que ejecutan los contenedores.
## ¿Qué es OpenShift y cómo se diferencia de Kubernetes?
OpenShift es una plataforma de aplicaciones en contenedores basada en Kubernetes que proporciona herramientas adicionales para el desarrollo y la implementación de aplicaciones. Se diferencia de Kubernetes en que es más fácil de usar y proporciona una experiencia más integrada para los desarrolladores.

 **¿Cómo se administran los recursos en un clúster de Kubernetes?**

Los recursos en un clúster de Kubernetes se administran mediante la asignación de recursos y la gestión de los mismos a través de objetos como los pods y los nodos.

Controlador de recursos: Controla y gestiona los recursos de manera automática mediante la creación de objetos de recursos en el clúster.

Límites de recursos: Configura límites de recursos en cada contenedor para asegurarte de que ningún contenedor consuma demasiados recursos y afecte el desempeño del clúster.

Asignación de recursos: Asigna recursos a diferentes aplicaciones y contenedores mediante la creación de objetos de recursos y la asignación de recursos específicos a cada contenedor.

Monitoreo de recursos: Monitorea el uso de recursos en el clúster para detectar cualquier problema y ajustar los límites y la asignación de recursos en consecuencia.

Balanceo de carga: Balancea la carga en el clúster mediante la asignación de recursos y el monitoreo de los mismos para asegurarte de que todas las aplicaciones y contenedores tengan acceso a los recursos necesarios.

Autoescalado: Automáticamente aumenta o disminuye la cantidad de recursos disponibles en el clúster en función del uso de recursos.

Estos componentes y técnicas trabajan juntos para garantizar que los recursos en el clúster se utilicen de manera eficiente y equilibrada para asegurar el desempeño óptimo del clúster y de las aplicaciones que se ejecutan en el mismo.

**¿Y en OpenShift?**

En un clúster de OpenShift, la administración de recursos se puede hacer utilizando las siguientes herramientas y técnicas:

Controladores de recursos: OpenShift incluye controladores de recursos integrados que pueden asignar y gestionar los recursos de manera automática en el clúster.

Quotas y limitaciones de recursos: OpenShift permite establecer límites y cuotas de recursos para cada proyecto y usuario para asegurarse de que ninguno consuma demasiados recursos.

Prioridades de recursos: OpenShift permite establecer prioridades de recursos para diferentes aplicaciones y contenedores, lo que garantiza que las aplicaciones críticas tengan acceso a los recursos antes que las aplicaciones no críticas.

Monitoreo y diagnóstico de recursos: OpenShift incluye herramientas integradas de monitoreo y diagnóstico de recursos para detectar y solucionar problemas de recursos en el clúster.

Autoescalado de recursos: OpenShift permite configurar el autoescalado de recursos para aumentar o disminuir la cantidad de recursos disponibles en el clúster en función del uso de recursos.

Asignación de recursos: OpenShift permite asignar recursos específicos a cada contenedor y aplicación mediante la creación de objetos de recursos.

CLI de OpenShift: se pueden crear objetos de recursos utilizando la línea de comandos de OpenShift (oc) y los comandos de recursos.

Dashboard de OpenShift: se pueden crear objetos de recursos utilizando el Dashboard de OpenShift, que es una interfaz gráfica de usuario en la nube que permite crear y gestionar objetos de recursos de manera intuitiva.

API de OpenShift: se pueden crear objetos de recursos utilizando la API de OpenShift, que es una interfaz de programación de aplicaciones que permite crear y gestionar objetos de recursos mediante la invocación de llamadas REST.

Estas herramientas y técnicas trabajan juntas para garantizar una administración eficiente y equilibrada de los recursos en el clúster de OpenShift y para asegurar el desempeño óptimo de las aplicaciones que se ejecutan en el clúster.

##¿Cómo se implementa la alta disponibilidad en un clúster de Kubernetes?
 La alta disponibilidad se puede lograr en un clúster de Kubernetes mediante la implementación de múltiples replicas de una aplicación y la configuración de los recursos y los objetos del clúster para tolerar la falla de nodos y otros problemas.
 
 Uso de múltiples nodos: Utiliza varios nodos para tu clúster de Kubernetes para asegurarte de que existen varios puntos de falla en caso de que algún nodo falle.

Uso de múltiples controladores: Utiliza múltiples controladores para tu clúster para garantizar que la información del clúster se mantiene en sincronía y se mantienen varios puntos de falla.

Uso de réplicas de pod: Utiliza múltiples réplicas de tus pods para garantizar que hay varios puntos de falla y para asegurarte de que tus aplicaciones siguen funcionando aun cuando un pod falle.

Uso de balanceo de carga: Utiliza un equilibrador de carga para distribuir la carga de tus aplicaciones entre varios pods y garantizar que tu clúster siga funcionando aun cuando algún pod falle.

##¿Cómo se realiza el escalado automático en un clúster de Kubernetes?
 El escalamiento automático en un clúster de Kubernetes se puede lograr mediante la configuración de los recursos y los objetos del clúster para responder a los cambios en la demanda y la utilización de los recursos.
 
 Definición de reglas de autoescalado: Define reglas de autoescalado que indiquen cuándo debes aumentar o disminuir el número de replicas de un pod basándote en una métrica, como la CPU o la memoria.

Configuración de límites de recursos: Configura los límites de recursos para tus pods para asegurarte de que no consuman más recursos del clúster de lo que necesitan.

Monitoreo de la métrica de autoescalado: Monitorea la métrica que has definido en las reglas de autoescalado para determinar cuándo debes aumentar o disminuir el número de replicas.

Ejecución de acciones de autoescalado: Ejecuta acciones de autoescalado para aumentar o disminuir el número de replicas de tus pods basándote en las reglas de autoescalado.

Estos pasos te permitirán implementar autoescalado en tu clúster de Kubernetes y garantizar que tus aplicaciones tengan el número adecuado de replicas en todo momento, optimizando el uso de recursos y mejorando la disponibilidad y el rendimiento de tus aplicaciones.

## ¿Cómo se manejan las actualizaciones y las rollbacks en un clúster de Kubernetes?
 Las actualizaciones y los rollbacks en un clúster de Kubernetes se pueden realizar mediante la gestión de las versiones de las aplicaciones y la utilización de técnicas como la implementación canary y blue/green.
 
 Uso de objetos de despliegue: Se crea un objeto de despliegue con la nueva imagen de contenedor y se actualiza el despliegue actual. Se puede hacer un rollback simplemente actualizando el objeto de despliegue con la versión anterior.

Uso de comandos de CLI: Kubernetes ofrece comandos de CLI para realizar actualizaciones y rollbacks, como kubectl rollout.

Uso de herramientas de gestión de versiones: Herramientas como Helm, GitOps o Weave Flux pueden automatizar el proceso de actualización y rollback, permitiendo un control centralizado y un seguimiento fácil de las versiones.

Uso de estrategias de actualización: Kubernetes ofrece diferentes estrategias de actualización, como "rolling update" o "recreate", que se pueden elegir en función de tus requisitos de disponibilidad y capacidad.

Es importante realizar pruebas exhaustivas en entornos de prueba antes de realizar actualizaciones en producción y tener un plan de contingencia en caso de problemas. También es recomendable tener una estrategia de monitorización y diagnóstico en caso de que surjan problemas durante una actualización o un rollback.
##¿Cómo se realiza la monitoreo y el diagnóstico de problemas en un clúster de Kubernetes?
 El monitoreo y el diagnóstico de problemas en un clúster de Kubernetes se pueden realizar mediante la utilización de herramientas de monitoreo y la revisión de los registros y los informes de estado del clúster.
 
 Monitoreo y alertas: Monitorea tu clúster para detectar problemas y configura alertas para recibir notificaciones cuando se produzcan eventos críticos.

Estos pasos te permitirán implementar alta disponibilidad en tu clúster de Kubernetes y garantizar que tus aplicaciones continúen funcionando incluso en caso de fallas en el clúster.

Monitoreo de los recursos del sistema: Monitorea los recursos del sistema, como la CPU, la memoria y el almacenamiento, para detectar cuellos de botella y posibles problemas de rendimiento.

Monitoreo de la salud de los nodos: Monitorea la salud de los nodos para detectar nodos fallidos o problemas de conectividad.

Monitoreo de las aplicaciones: Monitorea las aplicaciones para detectar posibles problemas de disponibilidad, rendimiento o errores de aplicación.

Análisis de logs: Analiza los logs de los componentes del clúster, como los controladores y los nodos, para identificar posibles problemas.

Debugging en tiempo real: Utiliza herramientas de debugging en tiempo real, como kubectl describe, kubectl logs y kubectl exec, para solucionar problemas en tiempo real.

Análisis post-mortem: Realiza un análisis post-mortem de los problemas ocurridos para identificar la causa raíz y prevenir futuros problemas.

Recopilación de datos: Reúne información relevante, como logs de los componentes del clúster, estadísticas de recursos y datos de monitoreo.

Identificación de la causa raíz: Utiliza los datos recopilados para identificar la causa raíz del problema, ya sea un error en la aplicación, un problema de hardware o una configuración incorrecta.

Revisión y mejora de procesos: Revisa los procesos actuales y determina si hay áreas que deban mejorarse para prevenir futuros problemas.

Documentación: Documenta los hallazgos y las soluciones implementadas para futuras referencias.

Verificación de solución: Verifica que la solución implementada resuelva efectivamente el problema y no cause nuevos problemas.

El análisis post-mortem te permitirá mejorar la estabilidad y disponibilidad de tu clúster de Kubernetes, identificar áreas que deban mejorarse y prevenir futuros problemas.

Estos pasos te permitirán realizar un monitoreo y diagnóstico efectivo de problemas en tu clúster de Kubernetes, asegurándote de que tus aplicaciones estén disponibles, funcionando correctamente y optimizando su rendimiento.
## ¿Cómo se implementan los despliegues continuos en un clúster de Kubernetes?
Los despliegues continuos en un clúster de Kubernetes se pueden implementar utilizando herramientas de automatización de construcción y despliegue, como Jenkins, Travis CI, CircleCI, entre otros. El proceso básico consiste en lo siguiente:

1. Integración continua: compila y prueba el código cada vez que se realiza un cambio en el repositorio de control de versiones.
2. Creación de imágenes: crea una imagen de contenedor a partir del código compilado y probado.
3. Almacenamiento de imágenes: guarda la imagen en un registro de contenedores, como Docker Hub o Google Container Registry.
4. Despliegue: utiliza objetos de despliegue de Kubernetes para definir y realizar el despliegue de la nueva imagen en el clúster.
5. Validación: realiza pruebas para validar el despliegue y verificar que la nueva versión funciona correctamente.
6. Rollback: en caso de un fallo, se puede revertir fácilmente a una versión anterior utilizando objetos de despliegue en Kubernetes.

Estos pasos se pueden automatizar y ejecutar de forma continua y sin interrupciones para lograr un despliegue continuo eficiente en un clúster de Kubernetes.
## Redes en Kubernetes y OpenShift
En Kubernetes y OpenShift, la configuración de redes se puede realizar a través de los siguientes objetos y herramientas:

1. Servicio: define un punto de acceso de red para los contenedores en un pod.

      Se puede utilizar para exponer los contenedores a Internet o para conectarlos entre sí            dentro del clúster.

1. ConfigMap: permite la definición de configuraciones de red, como los nombres de los servidores DNS.
2. NetworkPolicy: permite controlar el flujo de tráfico de red entre los pods en un clúster.
3. Add-ons de red: Kubernetes y OpenShift incluyen add-ons de red, como Calico o Flannel, que se encargan de implementar la capa de red y proporcionar características avanzadas, como enrutamiento y seguridad.
4. Plugins de red: OpenShift permite la implementación de plugins de red, que son soluciones de terceros que proporcionan características adicionales, como la integración con herramientas de firewall o la gestión de direcciones IP.

Para configurar las redes en un clúster de Kubernetes o OpenShift, se deben definir los objetos de red necesarios y utilizar las herramientas adecuadas para implementarlos y administrarlos. Esto permitirá que los contenedores comuniquen entre sí y con el exterior de forma eficiente y segura.
## Consideraciones para diseño de la arquitectura de OpenShift
1. Infraestructura: se requiere una infraestructura sólida y escalable para soportar el clúster de OpenShift. Esto puede incluir servidores físicos o virtuales, almacenamiento compartido y redes de alta disponibilidad.
2. Nodos: los nodos son los servidores que ejecutan los contenedores y proporcionan los recursos necesarios para ejecutar aplicaciones. Deben ser escalables y distribuidos en diferentes zonas de disponibilidad para garantizar la alta disponibilidad y la tolerancia a fallos.
3. Clúster de control: el clúster de control administra y coordina los nodos y los recursos en el clúster. Debe ser altamente disponible y tolerante a fallos.
4. Registro de contenedores: el registro de contenedores almacena las imágenes de contenedor que se utilizan para implementar aplicaciones en el clúster. Debe ser escalable y seguro.
5. Integración con herramientas externas: OpenShift puede integrarse con herramientas externas, como herramientas de monitoreo, sistemas de autenticación y control de acceso, entre otros.
6. Despliegues y gestión de aplicaciones: el diseño de la arquitectura debe contemplar la forma en que se realizarán los despliegues y la gestión de aplicaciones en el clúster, incluidas las políticas de seguridad y las prácticas de automatización y monitoreo.

Es importante considerar cuidadosamente cada uno de estos factores al diseñar la arquitectura de OpenShift para garantizar una implementación eficiente, escalable y segura.

## ¿Cómo se implementa la seguridad en un clúster de Kubernetes?

La seguridad en un clúster de Kubernetes se puede implementar a través de la gestión de los roles y los permisos de los usuarios, la encriptación de los datos en tránsito y en reposo, y la configuración de políticas de seguridad.

Control de acceso: Configura la autenticación y autorización para restringir el acceso a los recursos del clúster.

Cifrado de datos: Cifra la información sensibles y los datos de red en tránsito y en reposo.

Seguridad de la red: Implementa políticas de seguridad en la red para controlar el flujo de datos y prevenir ataques.

Monitoreo de seguridad: Implementa herramientas de monitoreo de seguridad para detectar y responder a posibles amenazas.

Validación de imágenes: Verifica la integridad y seguridad de las imágenes de los contenedores antes de su uso en producción.

Configuración segura por defecto: Configura el clúster con valores seguros por defecto para prevenir posibles vulnerabilidades.

Actualizaciones de seguridad: Mantén actualizado el clúster y los componentes relacionados con la seguridad con las últimas correcciones y parches de seguridad.

Es importante tener en cuenta que la seguridad es un proceso continuo y debes monitorear y mejorar la seguridad de tu clúster de Kubernetes en todo momento.
##¿Cómo se integran los servicios externos con un clúster de Kubernetes?
 Los servicios externos se pueden integrar con un clúster de Kubernetes mediante la utilización de objetos como los servicios y los ingress.
 
 Uso de servicios de nube pública: Integra servicios como bases de datos, almacenamiento y monitoreo en la nube utilizando proveedores como AWS, Google Cloud o Azure.

Uso de servicios internos: Integra servicios internos existentes, como bases de datos o aplicaciones, en el clúster de Kubernetes utilizando técnicas como servicios ClusterIP o LoadBalancer.

Creación de puentes: Crea puentes entre servicios externos y el clúster de Kubernetes mediante la creación de contenedores personalizados que actúen como intermediarios entre los servicios.

Uso de API y SDKs: Utiliza API y SDKs de servicios externos para integrarlos en el clúster de Kubernetes y permitir su uso por parte de tus aplicaciones.

Uso de enrutamiento externo: Configura el enrutamiento externo para permitir la integración con servicios externos, como bases de datos o aplicaciones.

El método de integración depende de tus requisitos y preferencias de arquitectura y seguridad. Es importante evaluar cuidadosamente los servicios externos antes de integrarlos en un clúster de Kubernetes para asegurarte de que cumplen con tus requisitos de seguridad y disponibilidad.

### Pasos para añadir seguridad a nuestro entorno, utilizando un servidor externo de Wazuh, puedes seguir los siguientes pasos:

1. Instala y configura el servidor Wazuh: Instala el servidor Wazuh en un servidor externo a tu clúster OpenShift y configúralo según tus necesidades.
2. Configura los agentes Wazuh en los nodos de OpenShift: Configura los agentes Wazuh en cada uno de los nodos de OpenShift para permitir que el servidor Wazuh recopile información de seguridad.
3. Configura los contenedores para monitoreo: Configura tus contenedores en OpenShift para que los agentes Wazuh los monitoreen y recopilen información sobre su seguridad.
4. Verifica la integración: Verifica la integración de Wazuh con OpenShift para asegurarte de que estás recopilando la información correcta sobre la seguridad de tus contenedores.
5. Configura las alertas en Wazuh: Configura las alertas en Wazuh para recibir notificaciones cuando se produzcan eventos relacionados con la seguridad de tus contenedores.

Estos pasos te permitirán configurar un servidor externo de Wazuh para monitorear la seguridad de tus contenedores en OpenShift y recibir información valiosa sobre posibles amenazas y vulnerabilidades.

Estos pasos son similares a los que seguiríamos para monitorear desde un servidor externo utilizando Zabbix.




----
                    







### Siguiente actualización el uso de ArgoCD y ejemplos.🔮
