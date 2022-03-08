# Linux Cheatsheet

## Comandos básicos.
* `ls` - listado de los archivos en la ruta actual.
* `ls -l` o bien `ll` - listado detallado de los archivos en la ruta actual.
* `ls -la` - listado detallado (incluye archivos ocultos) de los archivos en la ruta actual.
* `cd X` - nos movemos de un directorio al indicado como X (por ejemplo cd /home).
* `cd _` - nos movemos al directorio padre.
* `cd _/X` - nos movemos a la carpeta especificada dentro del directorio padre.
* `cd` - nos movemos al directorio raíz.
* `pwd` - muestra el directorio actual.
* `mkdir X` - crea la carpeta X en el directorio actual.
* `rm X` - borra el archivo X.
* `rmdir X` - borra la carpeta X (si la carpeta tiene archivos, debemos usar rmdir -r).
* `rm -f X` - borra forzadamente el archivo X.
* `rmdir -r X` - borra la carpeta X al completo.
* `rm -rf /` - despídete de tu sistema.
* `cp X Y` - copia el archivo X llamándolo ahora Y.
* `mv X Y` - renombra el archivo X a Y.
* `mv X /home/Y` - mueve y renombra el archivo a /home/Y.
* `touch X` - crea o actualiza el archivo X.
* `cat X` - muestra el contenido del archivo X.
* `cat > X` - creamos el archivo X y añadimos contenido. 
* `cat >> X` - agregamos contenido al archivo X.
* `tail -f X` - muestra el contenido del archivo X desde el final.
* `locate X` - muestra todas las instancias de X.
* `whereis app` - muestra la posible ubicación de la app indicada.
* `man command` - muestra el manual del comando especificado.

## Redes
* `ping X` - ping a X.
* `whois dominio` - muestra info del dominio indicado. 
* `dig dominio` - muestra el DNS del dominio indicado.
* `wget X` - descarga el archivo X
* `wget -c X` - retoma la descarga pausada
* `wget -r url` - descarga archivos de la url indicada.
* `curl url` - herramienta de línea de comandos para obtener o enviar datos utilizando la sintaxis de URL
* `curl -o hola.html url` - nombra hola.html a la url indicada. 
* `ssh usuario@host` - nos conectamos al host con el usuario indicado.
* `ssh -p puerto user@host` - especificamos el puerto para conectarnos.

## Procesos
* `ps` - muestra los procesos activos.
* `ps aux` - muestra los procesos detallados.
* `kill pid` - mata el proceso indicado por su pid.
* `killall X` - mata todos los procesos llamados X.

## Info del sistema
* `date` - muestra la fecha y hora actual. 
* `uptime` - muestra el tiempo de la sesión actual. 
* `whoami` - muestra el usuario actual.
* `w` - muestra todos los usuarios conectados.
* `cat /proc/cpuinfo` - muestra info de la cpu
* `cat /proc/meminfo` - muestra info de la memoria.
* `free` - muestra el uso de la memoria
* `du` - muestra el espacio libre del directorio actual.
* `du -sh` - muestra el espacio en GB de los archivos.
* `df` - muestra el espacio del disco.
* `uname -a` - muestra configuración del kernel.

## Compresión
* `tar cf X.tar Y` - comprime Y en X.tar
* `tar xf X.tar` - descomprime X.tar
* `tar tf X.tar` - muestra el contenido de X.tar

## Permisos
* `chmod X Y` - cambia los permisos de Y según lo especificado en X.
    * X puede ser:
        * 4 - lectura (r)
        * 2 - escritura (w)
        * 1 - ejecución (x)
    * El orden va de la siguiente manera: creador/grupo/otros
        * `chmod 777` - rwx para todos
        * `chmod 751` - r todos, rx grupo, x otros
