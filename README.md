# MICROSERVICES - NEST 
NATS, Webhooks, CI/CD, Git submodules, Gateways, Docker, Kubernetes, GCloud, PosstgreSQL, Mongo, SQLite

## Pasos:

1. Configurar el client-gateway (Seguir instrucciones de su Readme)
2. Configurar los micros (Seguir instrucciones de sus Readme)

## NOTA:
- Lo del comando de Nat solo es necesario correrlo una vez. 
- Para arrancar los micros es necesario que los contedores de docker esten corriendo
- Para correr todos los micros a la vez con docker network: `https://github.com/oscarrodriguezbu/nest-microservice-like-monorepo-docker`
- Para el micro de payments se usa stripe, hay que crear cuenta y sacar el secret y agregar la info en .env. Link: `https://stripe.com/es-us`
- En payments tambien hay que configurar hookdeck `https://hookdeck.com/`