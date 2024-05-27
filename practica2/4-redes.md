# Redes
Las redes son un componente fundamental que permite la comunicación entre contenedores, así como la comunicación de los contenedores con el mundo exterior. 
![Imagen](imagenes/redes.PNG)
- Bridge: Esta es la red por defecto en Docker. Permite la comunicación entre contenedores en el mismo host. Cada contenedor conectado a la red bridge tiene una IP propia en la subred de la red bridge.
    -  Brige por default: Cuando se ejecuta un contenedor, Docker crea automáticamente una red de tipo bridge por default. Esta red se utiliza para permitir la comunicación entre contenedores en el mismo host. Cada contenedor conectado a esta red obtiene su propia dirección IP en la subred de la red bridge.
    - Bridge creada por nosotros: Un usuario también puede crear sus propias redes de tipo bridge en Docker. Esto puede ser útil para organizar y segmentar los contenedores de una aplicación de manera más controlada. Al crear una red bridge personalizada, se puede especificar un rango de direcciones IP y otras configuraciones de red específicas. Los contenedores conectados a esta red utilizarán las direcciones IP de la subred definida por el usuario.
- Host: Con esta red, los contenedores comparten la red del host en lugar de tener su propia interfaz de red. Esto puede mejorar el rendimiento de red, pero los contenedores pueden entrar en conflicto con los puertos del host si intentan utilizar los mismos puertos.
- None: Con esta red, se deshabilita la configuración de red. Los contenedores que usan esta red tienen su propia red de bucle invertido y no pueden comunicarse con otros contenedores a menos que se conecten explícitamente a una red.

### Crear una red de tipo bridge

```
docker network create <nombre red> -d bridge
```

### Crear un contenedor vinculado a una red

```
docker run -d --name <nombre contenedor> --network <nombre red> <nombre imagen>
```

### Para saber a qué red está conectado un contenedor

```
docker inspect <nombre contenedor>
```
ó
```
docker network inspect <nombre red> 
```

### Vincular contenedor a una red
```
docker network connect <nombre red> <nombre contenedor>
```

### Para desvincular un contenedor de una red
```
docker network disconnect <nombre red> <nombre contenedor>
```

### Para listar las redes existentes
```
docker network ls
```

### Crear los contenedores y las redes que se presentan en el esquema. Usar para todos los contenedores la imagen de nginx:alpine

![Imagen](imagenes/esquema-ejercicio-redes.PNG)

<img width="407" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/b487ac86-4f12-4ca6-9c38-10cc2b562f3e">

# COLOCAR UNA(S) CAPTURAS(S) DE LOS CONTENEDORES CREADOS EN DONDE SE EVIDENCIE A QUÉ RED ESTÁN VINCULADOS

<img width="708" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/9ce415b7-e959-4304-bd45-0092272fc3f3">
<img width="804" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/69cb8252-adc0-4c72-9186-17145c8272f3">


# Eliminar las redes creadas

<img width="346" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/d6132f1d-c699-44ff-acbf-b242c009302e">

<img width="343" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/5d75ca56-c115-49e1-855a-7ecdffc1e47f">

