# Prueba tecnica DOMINA-ENTREGA

## Características

- Se tiene un gateway al cual llegan todas las peticiones y este redirecciona a los microservicios.
- Se tiene 2 microservicios uno para la autenticacion y otro para crear/modificar/eliminar tareas.
- Una pequeña aplicacion de frontend realizado con REACT para el login y gestion de las tareas.
- ORM Prisma para la gestión de la base de datos
- Base de datos PostgreSQL en un contenedor Docker.
- Validación de datos integrada.

## Stack tecnologico

- Node.js
- Nestjs
- Reactjs
- Docker y Docker Compose
- Npm
- Git

## Pre-requisitos

- Node.js (v18 o superior)
- Docker y Docker Compose instalados

## Instalación y ejecucion

1. **Clonar repositorio**:
   Para clonar el repositorio y sus submodulos:

   ```bash
   git clone --recurse-submodules https://github.com/Prueba-Tecnica-Microservicios-Domina/DOWNLOAD_THIS.git
   ```

2. **En cada una de las carpetas Instalar dependencias**:

   ```bash
   npm i
   ```

3. **Configurar variables de entorno**:

   ```bash
   Genera un copia del archivo .env.template y renombrarlo a .env
   En cada una de las carpetas hay un archivo .env a excepcion de '/front-ms'
   Por razones practicas no es necesario cambiar los valores de las vbles
   ```

4. **Crear las db usando el archivo docker-compose en la raiz del proyecto**:

   ```bash
   docker-compose up -d
   ```

5. **Ejecutar las migraciones en las carpetas 'auth-ms' y 'task-ms'**:

   ```bash
   npx prisma migrate dev
   ```

6. **Iniciar cada una de los servicios del API**:
   **Hay que ingresar en cada una de las carpetas (auth,client,task) y en cada una de ellas correr el comando**:

   ```bash
   npm run start:dev
   ```

7. **Comando para inciar el front (La carpeta front-ms)**:
   Las rutas en el front son:

   - `http://localhost:5173/login`
   - `http://localhost:5173/register` (Se me olvido poner un link a esta ruta, perdon)
   - `http://localhost:5173/dashboard`

   ```bash
   npm run dev
   ```

## Link a la documentacion

```bash
https://documenter.getpostman.com/view/11752693/2sAYkErLE4
```
