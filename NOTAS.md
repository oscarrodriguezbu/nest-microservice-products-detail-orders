# NOTAS

- Para el ejercicio de productos se guarda la data en el file system usando sqlite
- Info sobre micros servicios con Nest https://docs.nestjs.com/microservices/basics
- Al trabajar con micros, ya no sirve el puerto que tenemos, en este caso el 3001
- En el gateway se crean las rutas de los micros y se comunican con el gateway por TCP https://docs.nestjs.com/microservices/basics
- Hay que correr el gateway y los micros para que todo funcione