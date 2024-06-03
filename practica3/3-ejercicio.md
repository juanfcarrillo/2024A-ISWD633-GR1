## Esquema para el ejercicio
![Imagen](imagenes/esquema-ejercicio3.PNG)

### Crear red net-wp

<img width="485" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/15c89bc3-0e04-41ce-86f1-cc497b24d92e">

### Para que persista la información es necesario conocer en dónde mysql almacena la información.
# COMPLETAR LA SIGUIENTE ORACIÓN. REVISAR LA DOCUMENTACIÓN DE LA IMAGEN EN https://hub.docker.com/)
En el esquema del ejercicio la carpeta contenedor (a) es /Users/juancarrillo/2024A-ISWD633-GR1/practica3/ejercicio3/db
Ruta carpeta host: .../ejercicio3/db

### ¿Qué contiene la carpeta db del host?

<img width="244" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/a10ea146-a00f-4a5b-bb3a-6c9e67d4770b">


### Crear un contenedor con la imagen mysql:8  en la red net-wp, configurar las variables de entorno: MYSQL_ROOT_PASSWORD, MYSQL_DATABASE, MYSQL_USER y MYSQL_PASSWORD

<img width="972" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/0f0dfdd9-b995-44a2-b51b-ad13c96d420b">

### ¿Qué observa en la carpeta db que se encontraba inicialmente vacía?

Los archivos de configuracion de datos de MySQL

### Para que persista la información es necesario conocer en dónde wordpress almacena la información.
# COMPLETAR LA SIGUIENTE ORACIÓN. REVISAR LA DOCUMENTACIÓN DE LA IMAGEN EN https://hub.docker.com/)
En el esquema del ejercicio la carpeta contenedor (b) es /Users/juancarrillo/2024A-ISWD633-GR1/practica3/ejercicio3/www
Ruta carpeta host: .../ejercicio3/www

### Crear un contenedor con la imagen wordpress en la red net-wp, configurar las variables de entorno WORDPRESS_DB_HOST, WORDPRESS_DB_USER, WORDPRESS_DB_PASSWORD y WORDPRESS_DB_NAME (los valores de estas variables corresponden a los del contenedor creado previamente)

<img width="846" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/0e131700-8d9d-4da1-b970-1dc15982d6fd">


### Personalizar la apariencia de wordpress y agregar una entrada

### Eliminar el contenedor y crearlo nuevamente, ¿qué ha sucedido?

# COMPLETAR CON LA RESPUESTA A LA PREGUNTA



