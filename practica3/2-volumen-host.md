# VOLUMEN TIPO HOST
Un volumen host (o bind mount) es un tipo de volumen donde se monta un directorio o archivo específico del sistema de archivos del host en un contenedor.

```
docker run -d --name <nombre contenedor> -v <ruta carpeta host>:<ruta carpeta contenedor> <imagen> 
```

### Crear un volumen tipo host con la imagen nginx:alpine, para la ruta carpeta host: directorio en donde se encuentra la carpeta html en tu computador y para la ruta carpeta contenedor: /usr/share/nginx/html esta ruta se obtiene al revisar la se obtiene desde la documentación
![Volúmenes](imagenes/volumen-host.PNG)

<img width="923" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/c9169de8-08a5-4868-b931-0a7f640acb6c">

### ¿Qué sucede al ingresar al servidor de nginx?

El servidor retorna: <img width="1457" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/7567c43e-3033-466d-99b9-9e79a9c9959a">


### ¿Qué pasa con el archivo index.html del contenedor?

No existe un archivo index.html

### Ir a https://html5up.net/ y descargar un template gratuito, descomprirlo dentro de nginx/html
### ¿Qué sucede al ingresar al servidor de nginx?

Se carga la plantilla:
<img width="958" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/82e061f8-e4d1-4df1-b180-bf1061cea60e">


### Eliminar el contenedor

<img width="160" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/a4156396-83ca-4065-a26f-3322f0653850">

### ¿Qué sucede al crear nuevamente el mismo contenedor con volumen de tipo host a los directorios definidos anteriormente?

La plantilla cargada anteriormente se conserva 

### ¿Qué hace el comando pwd?

Indica el directorio actual
<img width="217" alt="image" src="https://github.com/juanfcarrillo/2024A-ISWD633-GR1/assets/78522923/4de94133-74aa-47e7-831a-2a19b285f250">



Si quieres incluir el comando pwd dentro de un comando de Docker, lo puedes hacer de diferentes maneras dependiendo del shell que estés utilizando.


### Volumen tipo host usando PWD y PowerShell
```
docker run -d --name <nombre contenedor> --publish published=<valorPuertoHost>,target=<valor> -v ${PWD}/<ruta relativa>:<ruta absoluta> <nombre imagen>:<tag> 
```

### Volumen tipo host usando PWD (Git Bash)

```
docker run -d --name <nombre contenedor> --publish published=<valorPuertoHost>,target=<valor> -v $(pwd -W)/html:/usr/share/nginx/html <nombre imagen>:<tag> 
```

### Volumen tipo host usando PWD (en Linux)

```
docker run -d --name <nombre contenedor> --publish published=<valorPuertoHost>,target=<valor> -v $(pwd)/html:/usr/share/nginx/html <nombre imagen>:<tag> 
```

