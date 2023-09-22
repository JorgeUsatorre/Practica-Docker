# PRÁCTICA  DOCKER 

## 1. Descarga la imagen de Ubunut y comprueba que está en tu equipo:

    Para este paso debemos utilizar el siguiente comando:

    `docker pull ubuntu`

    Este comando le indica a Docker que descargue la imagen de Ubuntu de Docker Hub,
    que es el repositorio oficial de imagenes de Docke.
    Para comprobar si tenemos la imagen descargada podemos utilizar el comando `docker images`

## 2. Crea un contenedor sin ponerle nombre. ¿Está arrancado? Obtén el nombre.

    Para crea un contenedor de Ubuntu con docker utilizamos el comando: `docker run ubuntu` esto nos creara
    un contenedor de ubuntu con un nombre generado por docker, para saber el nombre de nuestro contenedor 
    necesitamos acceder a la lista de todos nuestros contenedores con el comando:
    `docker ps -a` 
    en mi caso el contenedor se  llama "jovial_gauss".

## 3. Crea un contenedor con el nombre 'dam_ubu1'. ¿Como puedes acceder a él?

    Para crear un conetedor utilizamos el comando `docker run -it --name dam_ubu1 ubuntu`. 
    Este comando crea un nuevo contenedor basado en la imagen de Ubuntu y lo nombra como "dam_ubuntu1". 
    El flag -it se utiliza para iniciar el contenedor en modo interactivo para que puedas acceder 
    a la linea de comandos dentro del contenedor. 


## 4. Comprueba que ip tiene y si puedes hacer un ping a google.com

    El primer paso que necesitamos hacer es descargar el net-tools para combrobar la ip. 
    `apt update` Actualiza la lista de paquetes
    `apt install net-tools` Instala el net-tools 
    `ipconfig` Para comprobar la ip
    
    Dentro del contenedor, intentamos hacer ping a google con el siguiente comando: `ping google.com`
    Para cancelar el ping tenemos que presionar Ctr + C

## 5. Crea un contenedor con el nombre 'dam_ubu2'. ¿Puedes hacer ping entre los contenedores?

    Para crear un contenedor con el nombre 'dam_ubu2' utilizamos el comando:
    `docker run -it --name dam_ubu2 ubuntu`
    Una vez creado el segundo contenedor para hacer ping entre el primer y el segundo contenedor debemos 
    utilizar el comando `Ping +ip del otro contenedor`

## 6. Sal del terminal, ¿que ocurrió con el contenedor?

    Una vez cerrada la terminal el contenedor sigue funcionando correctamente esto lo podemos comprobar 
    poniendo en el tenminal el comando `docker ps` este comando nos dara toda la informcion de todos los 
    contenedores que tenemos.

## 7. ¿Cuanta memoria en el disco duro ocupaste?

    Para ver cuanta memoria del disco se esta utilizando cada contenedor utilizamos podemos utiliza el comando
    `docker sysytem df -v` este nos proporcionara bastante informacion sobre los contenedores.


## 8. ¿Cuanta RAM ocupan los contenedores? ¿Hay algún comando docker para saber esto?.

    Si, Docker nos proporciona el comando `docker stats`, este comando nos va a proporcionar diferente 
    informacion de la cantidad de cpu, memoria ram... que estan utilizando los contenedores.
    En mi caso en el primer contenedor me ocupa un 0.00% tando de CPU como deMemoria Ram.  
    El segundo contenedor ocupa un 0.00% tando de CPU como de Memoria Ram.

