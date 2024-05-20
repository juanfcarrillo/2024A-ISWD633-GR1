# Imagen
Es un archivo único que contiene todos los programas, librerías, dependencias y configuraciones necesarias para instalar y/o ejecutar una aplicación o un conjunto de aplicaciones.
![Imagen](imagenes/imagen.PNG)


## ¿Cuál es la relación entre una imagen y un contenedor? 

Imagen:

Una imagen es un archivo estático e inmutable que contiene todas las instrucciones necesarias para crear un contenedor.
Es una plantilla o modelo a partir del cual se crean los contenedores.
Las imágenes se componen de una serie de capas apiladas, cada una representando una instrucción en el archivo Dockerfile utilizado para construir la imagen.

Contenedor:

Un contenedor es una instancia en ejecución de una imagen.
Cuando se ejecuta una imagen, se crea un contenedor con su propio sistema de archivos, recursos y espacios de nombres aislados.
Los contenedores son entornos livianos y portátiles que permiten ejecutar aplicaciones de manera aislada y consistente en diferentes entornos.

![Imagen y contenedores](imagenes/imagenYcontenedores.JPG)
## Comandos para imágenes

### Descargar imagen
Descarga la última versión de la imagen disponible en el registro de Docker.

```
docker pull <nombre imagen> 
```

Descarga una versión específica de la imagen, cada imagen tiene etiquetas (tags) para diferentes versiones.
Una imagen puede tener la etiqueta latest para representar la última versión, si no se especifica una etiqueta se hará referencia a la versión latest.

```
docker pull <nombre imagen>:<tag>
```

Descargar la imagen **hello-world**


<img width="1206" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/07d8b2d7-a94f-4b86-ac3e-ba6b087951cc">


**¿Qué es nginx**
# COMPLETAR 

Nginx (pronunciado "engine-x") es un servidor web de código abierto y de alto rendimiento.

Descargar la imagen  **nginx** en la versión **alpine**
# COMPLETAR

### Listar imágenes

<img width="955" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/1fcbd6d5-e636-4ca5-b90c-89cb8b6702ce">


```
docker images
```

<img width="783" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/1bc37c6b-0132-4f8b-ab01-7004eeb757b7">

**Identificadores**
En Docker, se utilizan varios identificadores para diferenciar de manera única los elementos del sistema, como imágenes, contenedores, volúmenes y redes. Estos identificadores son generados automáticamente por Docker y son únicos dentro del contexto del sistema Docker en el que se encuentran. 

### Inspeccionar una imagen
El comando docker inspect se utiliza para obtener información detallada sobre un objeto de Docker específico, como un contenedor, una imagen, un volumen o una red.  Proporciona información en formato JSON sobre el objeto especificado.

```
docker inspect <nombre imagen>
docker inspect <nombre imagen>:<tag>
```

Inspeccionar la imagen hello-world 
<img width="911" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/76e409b3-c39a-4651-aaa2-8c4bddf74123">

**¿Con qué algoritmo se está generando el ID de la imagen**

SHA256
 
### Filtrar imágenes

```
docker images | grep <termino a buscar>

```

### Para eliminar una imagen
Eliminar permanentemente la imagen de tu sistema Docker.

```
docker rmi <nombre imagen>:<tag>
```

Eliminar la imagen hello-world 

<img width="788" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/4b0cf4db-cd44-4644-929c-3d51e7a3d381">


-f: Es la opción para forzar la eliminación de la imagen incluso si hay contenedores en ejecución que utilizan esa imagen.
Cuando eliminas una imagen Docker, Docker no elimina automáticamente los contenedores que se han creado a partir de esa imagen. Esto significa que, aunque hayas eliminado la imagen, el contenedor seguirá ejecutándose normalmente.  
**Considerar**
Eliminar una imagen no afecta a los contenedores que se han creado a partir de esa imagen, a menos que esos contenedores dependan de archivos o configuraciones específicas de la imagen eliminada. En ese caso, es posible que los contenedores se comporten de manera inesperada después de eliminar la imagen.
Es una buena práctica detener y eliminar todos los contenedores que dependan de una imagen antes de eliminar la imagen en sí.

```
docker rmi -f <nombre imagen>:<tag>
```

