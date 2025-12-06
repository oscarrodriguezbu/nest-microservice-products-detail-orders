# NOTAS

## Notas generales:
- Para el ejercicio de productos se guarda la data en el file system usando sqlite
- Info sobre micros servicios con Nest https://docs.nestjs.com/microservices/basics
- Al trabajar con micros, ya no sirve el puerto que tenemos, en este caso el 3001
- En el gateway se crean las rutas de los micros y se comunican con el gateway por TCP https://docs.nestjs.com/microservices/basics
- Hay que correr el gateway y los micros para que todo funcione
- Para consultar productos, orders se comunica con el micro de productos
- El servicio de orders se comunica con el de productos y el de payments para la creacion
- El proyecto inició como TCP y se cambió a NATS


## NATS:
- Mejora la comunicacion entre micros. Opcionalmente se puede usar la comunicacion tradicional para algo puntual entre micros.
- Explicacion de Nats https://nats.io/
- La ventaja de trabajar con Nest, es que realmente no tenemos que hacer mayor cambio en nuestros microservicios para que se comuniquen por otro canal de transporte, pero si necesitamos configurar un servidor NATS para que sea quien maneje nuestra mensajería.
- Trabaja con mensajería tipo publicar y suscribir.
- Hay temas (topics/subjects) a los cuales se escucha.
- Puede tener múltiples escuchas (listeners) al mismo topic.
- Pensado en para escalamiento horizontal.
- Seguridad, balanceo de carga incluído.
- Payload agnóstico.
- Rápido y eficiente.


## Docker Network:
- Se usa para:
    1. Crear un único comando para levantar todos los servicios.
    2. Crear un repositorio con sub módulos que nos permitan enlazar todo nuestro trabajo.
- En el proyecto se usa de forma opcional para levantar todos los micros a la vez pero tambien se pueden correr individualmente
- Para correrlo con docker: `https://github.com/oscarrodriguezbu/nest-microservice-like-monorepo-docker`


## Stripe:
Para el micro de payments. Esta pendiente de los pagos y devuelve respuesta rapidamente

## Google Cloud
Es basicamente configurar cosas y subir repos etc.

## Kubernetes
Complemento de Google Cloud

- CI => Google Cloud, CD => Kubernetes
- Permite desplegar, actualuzar y administrar aplicaciones. 
- Es como un orquestador de contenedores por ejemplo
- Brinda replicas atraves de un balanceador de carga
- Cluster: Api server, Controller manaager, Scheduler (asegura el cambio de PODs), ETCD (keyValue storage)
- El cluster controla toda la infraestructura, es el mas importante y puede tener replicas. Accedemos a el con: CLI, UI, API
- Cada POD tiene una IP diferente y es efimera. No se alamcena info en los PODS. Se comunican atraves de Service
- Kubernetes se encuentra en docker. Por ejemplo configurando con el engranaje en docker desktop
