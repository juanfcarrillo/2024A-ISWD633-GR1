# Contenedores

### Crear un contenedor
Para crear un nuevo contenedor Docker a partir de una imagen específica, pero sin iniciarlo automáticamente. 

```
docker create --name <nombre contenedor> <nombre imagen>:<tag>
```
Crear el contenedor  **srv-web** usando la imagen nginx version alpine

<img width="707" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/a7767ee3-01e0-4461-985b-1e1eed01b50a">


Si creas un contenedor en Docker sin asignarle un nombre específico utilizando la opción --name, Docker asignará automáticamente un nombre aleatorio al contenedor. Este nombre suele consistir en una combinación de palabras y números.  

Crear el contenedor usando la imagen hello-world

<img width="646" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/6cb865a1-37a9-482a-a5d8-962b2e948b0f">

<img width="461" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/e060fcf5-ba72-4572-8985-df0eba003d3b">

### Listar los contenedores ejecutándose o no

```
docker ps -a
```

### Para iniciar un contenedor

```
docker start <nombre contenedor o identificador>
```
Iniciar el contenedor srv-web 

<img width="1179" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/077f8274-60f6-46fc-9c10-6fea0f1a4756">


### Listar los contenedores ejecutándose
```
docker ps 
docker ps | grep <nombre contenedor>
```

### Para detener un contenedor

```
docker stop <nombre contenedor>
```

### Para crear un contenedor y ejecutarlo inmediatamente

```
docker run --name <nombre contenedor> <nombre imagen>:<tag>
```
![Ecosistema de Docker](imagenes/dockerRun.PNG)

Crear y ejecutar inmediatamente el contenedor **srv-web2** usando la imagen nginx:alpine
<img width="856" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/30abb4d4-725e-4a51-9931-f1bf8e2f30b9">

**¿Qué sucede luego de la ejecución del comando?**

Se ejecuta el server web de nginx

Cuando ejecutas un contenedor en primer plano sin la opción -d (modo detach), el contenedor captura la entrada estándar (stdin) del terminal, lo que significa que el terminal queda "atrapado" y no puedes introducir más comandos hasta que detengas el contenedor.

### Para crear un contenedor y ejecutarlo inmediatamente sin estar vinculados al mismo
-d: Es la opción que indica a Docker que ejecute el contenedor en segundo plano (en modo "detach").
Cuando un contenedor se ejecuta en segundo plano, Docker devuelve el control al terminal inmediatamente después de iniciar el contenedor, lo que permite al usuario seguir ejecutando otros comandos en el mismo terminal sin que el contenedor detenga la interacción.

```
docker run -d --name <nombre contenedor> <nombre imagen>:tag
```
Crear y ejecutar inmediatamente el contenedor **srv-web3** en modo detach usando la imagen nginx:alpine

<img width="543" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/65fea3e2-1da6-4964-8147-07f848849b1d">


### Para eliminar un contenedor

```
docker rm <nombre contenedor>
```
Eliminar el contenedor que se creó a partir de la imagen hello-world 
<img width="449" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/57478306-6289-4ebe-be87-64ae8269ed63">

Verificar que el contenedor que se eliminó
<img width="380" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/ffd9e872-090b-4e2f-9dcf-c79a685ad655">

### Para eliminar un contenedor que esté ejecutándose

```
docker rm -f <nombre contenedor>
```
Eliminar el contenedor **srv-web3** 
<img width="459" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/0f423a36-64be-4fe2-8ff3-626dbb23e546">

Verificar que el contenedor que se eliminó
<img width="414" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/209dc0f2-4538-496d-b682-519426400e44">

### Para inspecionar un contenedor 

Inspeccionar el contenedor **srv-web** 
<img width="880" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/e97ea244-db2d-45cf-8480-42152a598710">
