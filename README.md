# Tutorial Nginx - Docker en Ubuntu Linux

## **Indice**   
1. [Resumen](#id1)
2. [Introducción](#id2)
3. [Instalación](#id3)
4. [Conclusiones](#id4)


## Resumen <a name="id1"></a>
En esta guía aprenderás a como crear un contenedor de Docker en el sistema operativo Linux que incluya el servicio Nginx.
Lo que aprenderás:
*	Como crear una imagen de Docker.
*	Como incluir el servicio de Nginx sobre un contenedor.\

Lo que necesitarás: 
*	Un ordenador con conexión a internet y sistema operativo Linux.
*	Tener instalado Docker.

* Sino tiene instalado Docker por favor revisar la sección Instalación de Docker 
## Introducción <a name="id2"></a>

### ¿Qué es Docker?
Docker es una plataforma que permite desarrollar, implementar y ejecutar aplicaciones dentro de contenedores.

### ¿Qué es Nginx?
Es un servidor web/proxy muy ligero que permite un alto rendimiento que también funciona solo como proxy para diferentes protocolos de correo electrónico.

## Instalación <a name="id3"></a>
Existen una gran cantidad y variedad de imágenes Docker de servidor Nginx, pero para este tutorial se utilizará la imagen oficial de Nginx.

1.	Descargamos la imagen Docker de Nginx desde los repositorios en línea.\
``` $ sudo docker pull nginx ```

![image](https://user-images.githubusercontent.com/73547550/192417454-3a9a05dd-3db8-4fe8-a3a3-78b8e998321d.png)

2.	Para más información de las opciones y parámetros del comando docker pull, ejecute el siguiente comando: \
``` $ sudo docker pull –help ```

3.	Procedemos a listar todas las imágenes de Docker que se encuentran en nuestro sistema con el comando: \
``` $ sudo docker images ```
![image](https://user-images.githubusercontent.com/73547550/192417521-406c0365-0ba6-40a2-b8d1-2b7c1a7334a9.png)

4.	Para ejecutar un contenedor desde una imagen extraída, ejecute el siguiente comando:\
``` $ sudo docker run -d --name nginx-server -p 8080:80 nginx ```

Parametros:
* **d**:  Ejecutar el contenedor en modo detached.
* **name**: Nombre del contenedor que va a ser creado
* **p**: Puerto con el que se mapeara el contenedor.
Tendrás una salida similar a:

![image](https://user-images.githubusercontent.com/73547550/192417626-09fa3ec9-6e75-40af-b24f-fceb258962e2.png)

Este resultado es el id del contenedor creado con la imagen de Nginx.

5.	También puede probar el contenido por defecto del servidor nginx usando el navegador de su preferencia para acceder a la dirección URL http://localhost:8080/ como se muestra a continuación:\
![image](https://user-images.githubusercontent.com/73547550/192417690-2ff3dfc5-1ae3-4619-8ecf-b44a0d7ee22c.png)

## Conclusiones <a name="id4"></a>
En nuestro ejemplo:

* La imagen de Docker se usó para iniciar un nuevo contenedor.
* El nuevo contenedor está utilizando el puerto local 8080.
* El ID del contenedor es: **4744150be374b84f6c86e1f4c0bba0d34afd1a212f974f8d6d9abaf6575061c0**


¡Felicidades! Ha finalizado la instalación de Nginx Docker en Ubuntu Linux.



