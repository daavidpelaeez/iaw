# Tutorial: Jekyll con Docker por David Pelaez

## Instalacion Docker en Ubuntu
En primer lugar tendremos que instalar dockers en el ubuntu que vamos a realizar la practica.

Con los siguientes comandos procederemos a la instalación de dockers.

![Ejemplo de imagen](/img/instalar1.png)
![Ejemplo de imagen](/img/instalar2.png)
![Ejemplo de imagen](/img/instalar3.png)

Una vez hecho esto con docker run hello-world nos saldra si la instalación se ha completado correctamente.

![Ejemplo de imagen](/img/helloworld.png)

# Instalación Jekyll en Ubuntu con Dockers
## PASO 1:
Descargar la versión indicada de la imagen Jeylll, si aún no la tenemos en local.

Crear un contenedor basado en esa imagen llamado mi-blog.
Montar la carpeta actual local en la carpeta /srv/jekyll del contenedor.

Ejecutar en el contenedor el comando jekyll new mi-blog, lo que creará un nuevo proyecto Jekyll en la carpeta ./mi-blog/.

Abrir la carpeta del nuevo proyecto.

Con el siguiente comando haremos esto:
![Ejemplo de imagen](/img/Paso1.png)

## PASO 2:

Hasta ahora, solo hemos dado inicio al contenedor y generado los archivos del proyecto, los cuales puedes ver, editar o añadir en la carpeta recién creada ./mi-blog.

Para dar forma al sitio web, ahora necesitamos ejecutar la siguiente orden:

![Ejemplo de imagen](/img/Paso2.png)

## PASO 3:

Una vez construido el sitio (alojado en la carpeta _site), podremos levantar el servidor para comprobar su funcionamiento.

Tambien deberemos añadir al fichero GEMFILE la gema de webrick para que funcione correctamente.

![Ejemplo de imagen](/img/Gemfile.png)

Ahora con el siguiente comando levantaremos el servidor:

![Ejemplo de imagen](/img/Paso3.png)

Para visualizar la página web, necesitas abrir la siguiente dirección en tu navegador: http://localhost:3000 Mientras el sitio esté en proceso, cualquier cambio que realices en los archivos se mostrará automáticamente en el navegador; solo necesitas actualizar la página para ver las modificaciones.


## PASOS ADICIONALES

![Ejemplo de imagen](/img/adicional.png)

Podemos comprobar que el contenedor esta en ejecución con el siguiente comando:

![Ejemplo de imagen](/img/Paso5.png)
