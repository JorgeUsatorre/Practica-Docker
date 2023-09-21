# PRÁCTICA  DOCKER 

## 1. Descarga la imagen de Ubunut y comprueba que está en tu equipo:

    Para este paso debemos utilizar el siguiente comando:

    `docker pull ubuntu`

    Este comando le indica a Docker que descargue la imagen de Ubuntu de Docker Hub, que es el repositorio oficial de imagenes de Docke.
    Para comprobar si tenemos la imagen descargada podemos utilizar el comando `docker images`

## 2. Crea un contenedor sin ponerle nombre. ¿Está arrancado? Obtén el nombre.

    Para crea un contenedor de Ubuntu con docker utilizamos el comando: `docker run ubuntu` esto nos creara un contenedor de ubuntu con un nombre generado por docker, para saber el nombre de nuestro contenedor necesitamos acceder a la lista de todos nuestros contenedores con el comando: `docker ps -a` en mi caso el contenedor se  llama "jovial_gauss".

## 3. Crea un contenedor con el nombre 'dam_ubu1'. ¿Como puedes acceder a él?

    Para crear un conetedor utilizamos el comando `docker run -it --name dam_ubu1 ubuntu`. Este comando crea un nuevo contenedor basado en la imagen de Ubuntu y lo nombra como "dam_ubuntu1". El flag -it se utiliza para iniciar el contenedor en modo interactivo para que puedas acceder a la linea de comandos dentro del contenedor. 

    