# Product Microservice



## Dev

1. Clonar el repositorio
2. Instalar dependencias
3. Crear un archivo `.env` basado en el `env.template`
4. Ejecutar migración de prisma `npx prisma migrate dev`
5. Levantar el servidor de NATS
```
docker run -d --name nats-server -p 4222:4222 -p 8222:8222 nats
```
6. Ejecutar `npm run start:dev`
7. Abrir el archivo prisma\dev.db en tablePlus por ejemplo (Puede que se requiera conexion manual a la base de datos si no abre directamente el archivo)
8. Cargar la data de data\products.sql y oprimir CTRL + ENTER. Esta carpeta solo esta con fines educativos