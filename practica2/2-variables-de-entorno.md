# Variables de Entorno
### ¿Qué son las variables de entorno

Las variables de entorno son variables que se presentan dentro del sistema operativo que corre y se usan para determinar valores que vamos a poder usar en nustra aplicacion en distintos ambientes 

### Para crear un contenedor con variables de entorno

```
docker run -d --name <nombre contenedor> -e <nombre variable1>=<valor1> -e <nombre variable2>=<valor2>
```

### Crear un contenedor a partir de la imagen de nginx:alpine con las siguientes variables de entorno: username y role. Para la variable de entorno rol asignar el valor admin.

<img width="798" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/0440aa57-f240-48fa-b9d8-640058fa327f">


<img width="442" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/7c82c7ea-4942-4b17-a650-29628de14f08">


### Crear un contenedor con mysql:8 , mapear todos los puertos

<img width="907" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/fcee376d-b8d0-4fc4-b57b-91b86c660f23">

### ¿El contenedor se está ejecutando?
No

### Identificar el problema
Falta setear varibles de entorno especificadas

### Eliminar el contenedor creado con mysql:8 
<img width="661" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/67e65409-6962-496f-8a1a-443580d29547">

### Para crear un contenedor con variables de entorno especificadas
- Portabilidad: Las aplicaciones se vuelven más portátiles y pueden ser desplegadas en diferentes entornos (desarrollo, pruebas, producción) simplemente cambiando el archivo de variables de entorno.
- Centralización: Todas las configuraciones importantes se centralizan en un solo lugar, lo que facilita la gestión y auditoría de las configuraciones.
- Consistencia: Asegura que todos los miembros del equipo de desarrollo o los entornos de despliegue utilicen las mismas configuraciones.
- Evitar Exposición en el Código: Mantener variables sensibles como contraseñas, claves API, y tokens fuera del código fuente reduce el riesgo de exposición accidental a través del control de versiones.
- Control de Acceso: Los archivos de variables de entorno pueden ser gestionados con permisos específicos, limitando quién puede ver o modificar la configuración sensible.

Previo a esto es necesario crear el archivo y colocar las variables en un archivo, **.env** se ha convertido en una convención estándar, pero también es posible usar cualquier extensión como **.txt**.
```
docker run -d --name <nombre contenedor> --env-file=<nombreArchivo>.<extensión> <nombre imagen>
```
**Considerar**
Es necesario especificar la ruta absoluta del archivo si este se encuentra en una ubicación diferente a la que estás ejecutando el comando docker run.

### Crear un contenedor con mysql:8 , mapear todos los puertos y configurar las variables de entorno mediante un archivo

<img width="577" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/4ca0e2f7-fd62-4af1-87d2-dbbd33f45d00">
<img width="310" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/cefbc775-aaa1-4653-a0ea-5c6cf09fa8ab">

<img width="730" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/5eae196e-cea4-4bee-854c-a11d8aa39c30">

### ¿Qué bases de datos existen en el contenedor creado?
Mysql
