# Apuntes básicos de comandos Linux

Estos son algunos comandos y apuntes relacionados, especialmente con el uso de la consola de linux.

un diredtorio en linux en realidad un archivo con información que lo convierte en directorio

En linux las extensiones de los archivos no son tan necesarias como si lo son en windows

La carpeta root es la carpeta de inicion (home) del usuario root, no confundir con la dirección root   `/`

Los archivos y carpetas de los demás usuarios estaran en la carpeta `home`

el directorio 
~/archivo.txt
es acceder a /home/usuario/archivo.txt
***
## Algunos comandos básicos


Lista archivos y directorios, usar 

    ls -l -p -a -R --color

- -p marca los directorios con /
- -a muestra los archivos ocultos (los que inician con .)
- -l lo muestra conn muchas especificaciones
- -R recursivo, muestra todos los archivos y directorios interiores


crear un archivo

      touch file.txt

crear y/o editar un archivo (editor vim)

    vim file.txt



leer el contenido de un archivo desde la consola
```
cat file
```

Ejecucion en segundo plano
La ejecucion en segundo plano consiste en que se puede mantenr la ejecucion de algo en el background y se puede volver a esa ejecucion cuando se desee. Se usa el simbolo & para indicar que es una ejecucion en la cola
```
vim archivo.txt &
```

si algo se estpa ejectando y se quiere llevar a segundo plano se logra con la combinación `ctrl+z`

Detener un programa de manera forzada se logra con `ctrl+c`

Elegir cual ejecucion se coloca de foregruod (primer plano)
```
fg #  (siendo # el numero de la pila de ejecucion del programa, si se quiere el ultimo proframa en ejecucion solo entonces se tipea fg)
```

Estudiar que hace bg (background)




ver directorio actual
```
pwd
```

Ver las rutas globales
```
echo $PATH
```

copiar un archivo

    cp file-origin file-new
    cp file-origin directorio/file-origin

mover un archivo (si la carpeta de destino es el mismo, este comando sirve para cambiar el nombre del arcivo)

    mv file-origen directorio/
    mv file-origen new-nama

Borrar un archivo o carpeta

        rm file

Borrar un directorio con todos sus archivos
        rm -r dir
-r significa recursive

Enlaces fuertes: son uno o mas archivos que apuntan al mismo origen de datos, de tal manera que si uno cambia el otro tambien lo hace, se puede asociar al concepto de sincronización, por lo tanto todos los archivos enlazados ocupan la misma cantida de espacio

        ln file-origin file-linked

Enlaces simbolicos: este se relaciona o asocia coo un enlace directo de windows, es decir el enlace debil guarda el nombre del archivo base, acceder al enlace debil te llva directamente al archivo origem. los enlaces debiles son de pequeño tamaño.

        ln -s file-origen file-linked


**Variables de entorno**
Estas se crean en el archivo ~/.bashrc
una variable de entorno se crea en el archivo .bashrc de la siguiente manera

        export NAME_VARIABLE=valor
valor puede ser numerico, string bolleano etc

Luego de editar el archivo se debe o bien reiniciar linux o pedir que se cargue el archivo de esta manera en consola

        $ source ~/.bashrc

Un uso por ejemplo de una variable de entorno es imprimirla en pantalla

        $ echo $NAME_VARIABLE




