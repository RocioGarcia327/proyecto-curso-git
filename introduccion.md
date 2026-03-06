# GIT

###### es un sistema de control de versiones distribuido, lo que significa que un clon local del proyecto es un repositorio de control de versiones completo. Estos repositorios permiten trabajar sin conexión o de forma remota con facilidad. Los desarrolladores confirman su trabajo localmente y a continuación, sincronizan su copia del repositorio con la copia del servidor. En pocas palabras en nuestra computadora podemos crear nuestra versión y luego subirla y sincronizarla, todas las versiones estarán en un solo servidor y luego una persona se encarga de que funcionen todas.
###### Usando un control de versiones la versión nueva no sustituye la versión anterior, la versión 0.1 sigue existiendo de igual forma que la versión 0.2, si hubiese un error en la nueva versión siempre se puede volver a la versión anterior haciendo rollback para corregir sin tanto problema.
###### Si no se trabajara con versiones se podrían generar conflictos y si se elimina por error no se puede recuperar, si se trabaja con versiones se trabaja en torno a un repositorio en el cual se sincronizan todas las versiones haciendo que todos converjan. Al trabajar en equipo y con varias versiones puede que algún conflicto genere un error, detectar el momento exacto nos ahorra tiempo y nos permite focalizar esfuerzo. 

**NOTA: En el link gist.github.com/sergiecode se encuentra toda la documentación necesaria sobre el curso, así como las herramientas necesarias para realizarlo.**

# CONFIGURACION
###### Damos click derecho y en open git bash here abrimos la consola y ponemos la siguiente información para realizar la configuración y el servidor nos reconozca.
>> rocio@Rocio MINGW64 ~/OneDrive/Desktop 
 $ git config --global user.name “Rocio Garcia”
 rocio@Rocio MINGW64 ~/OneDrive/Desktop
 $ git config --global user.email 
 rocioramirez18092@gmail.com (este email tiene 
 que ser el mismo que usemos en nuestro repositorio remoto)
 rocio@Rocio MINGW64 ~/OneDrive/Desktop
 $ git config --global core.editor "code --wait" (code es la palabra clave de visual studio, si es
 diferente hay que buscar la palabra, wait quiere
 decir que la terminal de git va a esperar hasta que
 nosotros cerremos el archivo en el editor de código
 para poder seguir con las instrucciones)
rocio@Rocio MINGW64 ~/OneDrive/Desktop
 $ git config --global -e (este comando es para
 verificar que tenemos nuestra configuración y nos
 va abrir un archivo con la información)
 El salto de línea se trata de una forma, en mac o
 Linux es otra la siguiente configuración es muy
 importante

rocio@Rocio MINGW64 ~/OneDrive/Desktop
$ git config --global core.autocrlf true (esta
palabra es para Windows, para Linux o mac es input)  rocio@Rocio MINGW64 ~/OneDrive/Desktop
$ git config --global -h (esto nos va a traer una ayuda de todas las cosas que podemos hacer, desde configurarlo e forma local y no global y demás cosas, para limpiar la terminal solo se escribe clear y se da click)

