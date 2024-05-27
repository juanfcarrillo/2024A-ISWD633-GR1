### Crear contenedor de Postgres sin que exponga los puertos. Usar la imagen: postgres:11.21-alpine3.17

<img width="677" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/748faeb7-ba1e-44d6-a47f-f41e4747d9d3">


### Crear un cliente de postgres. Usar la imagen: dpage/pgadmin4

<img width="594" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/94ff2189-0e88-43c7-8813-970bf5bef2ea">


La figura presenta el esquema creado en donde los puertos son:
- a: 80
- b: 80
- c: 5432

![Imagen](imagenes/esquema-ejercicio3.PNG)

## Desde el cliente
### Acceder desde el cliente al servidor postgres creado.
<img width="1450" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/667b486a-6c33-49d9-bd0b-025769720d22">

<img width="1446" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/127edeb2-e7a1-4272-92fa-04b57a3705c2">

<img width="1451" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/cbb637a6-1b05-4c77-9b62-74477ca6bbd4">


### Crear la base de datos info, y dentro de esa base la tabla personas, con id (serial) y nombre (varchar), agregar un par de registros en la tabla, obligatorio incluir su nombre.

## Desde el servidor postgresl
### Acceder al servidor
### Conectarse a la base de datos info

<img width="1457" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/4fe46f49-b251-4020-b062-5511566c2741">


### Realizar un select * from personas

<img width="433" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/aa90fbc8-522e-48e9-a661-fe7b50466ab2">
