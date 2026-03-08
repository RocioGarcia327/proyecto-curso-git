# BASICOS TERMINAL
###### $ ls es para ver el listado de carpetas desde donde estamos parados
###### para listar
###### $cd carpeta es para poder acceder a la carpeta
###### $pwd es para mostrarnos que estamos dentro de la carpeta
###### $cd .. es para poder salir de la carpeta, cuando se hace algún tipo de relación de donde esta un archivo, si hacemos ./ es en nuestra propia carpeta y si hacemos ../ es en la carpeta anterior, ./ nombre de la carpeta es dentro de la carpeta
###### $ mkdir proyecto-git (este comando es para crear una carpeta, en Linux se le llama directorio)
###### $ cd proyecto-git (es para acceder a la carpeta creada)
###### $ git init ( con git init se inicializa un repositorio vacio lo vemos a continuacion)
>> Initialized empty Git repository in C:/Users/rocio/OneDrive/Desktop/proyecto-git/.git/
###### $ls -a ./  ../  .git/ (aquí vemos que tiene la carpeta git de forma oculta, si nos vamos a la carpeta en el despliegue de nombres le ponemos /.git nos abrirá la carpeta con todos los archivos ocultos donde estará la configuración de nuestro manejador de versiones )
###### $ code . (nos abre visual directamente en la carpeta del proyecto ya que estábamos dentro de ella)
###### $ mkdir directorio-interno (de esta forma podemos crear una nueva carpeta dentro de la carpeta de nuestro proyecto, también se puede abrir la consola dentro de visual, damos ctrl+ñ nos abre la terminal, en la opcion de + nos da git bash)
# FLUJO DE GIT
###### Vamos a ver como se trabaja en git y como nuestros archivos van a ir pasando de estado a estado hasta llegar a repositorio que es el estado final, la parte local se refiere a nuestra computadora local y dice sin marcar, vamos a inicializar este proceso poniendo git init pero no va hacer nada con los archivos hasta que pongamos git add que ahí va a ser cuando los archivos pasen a estado de stage 
(/C:/Users/rocio/OneDrive/Imágenes/Screenshots/flujo.png)
###### Aquí vemos que los archivos ya están marcados, van a ser observados por git y todos los cambios que hagamos a esos archivos se van a detectar, si modificamos uno y otro lo eliminamos y hacemos git status git se dará cuenta que hicimos una modificacion si volvemos a hacer git add todos los archivos van a pasar a stage pero con el nuevo estado, uno modificado y otro eliminado y ahí va a marcar el nuevo estado en el que se encuentran los archivos, lo que podemos hacer es tomar una fotografía a nuestro proyecto para que quede una versión puntual, un commit ósea comitear es una especie de fotografía del estado en el que esta en ese momento los archivos y nuestro proyecto lo que nos permitirá hacer un historial, una vez que queremos que vaya al servidor hacemos git push se guardara en el servidor en el repositorio remoto.
# ADD - STATUS - COMMIT
###### Generamos una carpeta para nuestro proyecto
###### Git status -s es un comando que nos ayuda a saber en que estado se encuentran los archivos actualmente, si estan en stage  o no
###### Git add se usa para guardar los cambios de nuestros archivos y despues poder hacer un commit y enviarlo a nuestro repositorio
###### Git commit -m "mensaje con lo que se hizo" se usa para guardar los comentarios de lo que hhicimos en nuestros archivos

# BRANCH
# STAGE
# 
# IGNORE
###### Es un archivo de configuración en el cual vamos a poner todos los archivos y carpetas que van a ser ignorados por git, no van a ser fotografiados y tampoco se van a subir al repositorio. Se usa por que hay muchos archivos que se generan solos o no queremos que se suban, .env es un arachivo donde se ponen las variables de entorno que no queremos que nadie se entere, suele contener contraseñas o pasword para entrar a las bases de datos
###### node_modules es la carpeta donde vana estar todos los modulos instalados, cuando hacemos npm in sol se va a generar esa carpeta y no la queremos
###### *.jpg <!van a ser todos los archivos de imagenes >
###### *.mp4 <!es para videos>
# DIFF
###### Es para ver un archivo antes y uno después 
**NOTA: Se puede verificar el estado de los archivos de forma mas simple usando git status -s y nos mostrara una m en rojo indicando que esta modificado y no se a agregado y una a de add ósea agregado**
# LOG
###### Vamos a ver toda la información que nos da incluso para salir tenemos que usar un código 
**NOTA: los commit son como fotografías dentro de una película y vamos a ver uno detrás de otro y vamos a saber donde estamos parados en esa película. Al usar git log nos da la información de los archivos, asi como los datos de quien lo modifico**
>> $ git log
commit 8da4fa222a60337130f2fd094e896ea0aedb80f4 (HEAD -> master)
Author: “Rocio <rocioramirez18092@gmail.com>
Date:   Sun Feb 22 14:58:43 2026 -0600
    creamos nuevos documentos
# BRANCH Y CHECKOUT
###### Una rama son como los distintos caminos que se pueden crear dentro de algun proyecto, donde podria trabajar cada persona haciendo cosas diferentes
###### Branch master se refiere a la rama principal donde se encuentra  nuestro codigo, las ramas es donde tenemos caracteristicas distintas de lo que hara nuestro codigo
###### Un merge commit se usa para unir las ramas alternativaws con la master, normalmente el lider se encarga de unirlo
###### Para crear ramas se usa el comando git checkout -b(nombre de la nueva rama) o en visual click en master en la parte inferior, git branch nos indica la rama en la que nos encontramos, en la consola nos aparece como HEAD>(seguido del nombre de la rama en que nos encontramos)
###### El comando git checkout master nos lleva de vuelta a la rama principal (se puede usar master o main dependiendo del caso)
###### El comando git branch se usa para saber en que rama estamos parados, de igual forma podemos verificarlo en la parte izquierda inferior de visual
###### Para unir las ramas primero nos vamos a la rama principal con el comando git checkout master, seguido de git branch para  verificar la branch master, hacemos un git merge (nombre de la rama a unir), lo comprobamos con un git log --oneline y nos tiene que poner en el HEAD>master(rama principal),nombre rama agregada
# GITHUB Y VISUAL
###### Creamos un repositorio en GitHub, lo dejamos publico, siguen instrucciones que ya hemos realizado como git init, copiamos la liga de git remote add origin en la consola de visual, esto para agregar el origen de nuestro repositorio y esten conectados 
###### Hacemos un git push master (origin, dependiendo si tenemos nuestra rama principal como main o master), push es como enviar al repositorio 
###### Cuando ya tenemos nuestro trabajo en el repositorio (GitHub) y queremos subir otra rama, nos colocamos en la parte inferior izquierda y damos click en la nube que aparece, esta es una forma de enviar nuestros archivos al repositorio
# PLUGIN GRAPH
###### Solo es instalar el plugin para observar de forma grafica la creacion de las ramas
# REMOTE ORIGIN
# PUSH Y PULL
###### Al trabajar con un equipo se maneja una carpeta compartida, al hacer cambios estos solo se guardan en mi carpeta local, para que todos puedan acceder a estos cambios y trabajar con ellos, se hace un git push, primero hacemos git add, git commit para que se pueda subir con todas las actualizaciones que ya hemos realizado, esto es mas como para subirlo al final del dia de trabajo o cuando se nos pidan
###### Cada vez que una persona hace cambios en esa carpeta compartida como tal no aparecen directo en mi carpeta local, para sincronizar esos cambios se debe hacer un git pull, esto podria hacerse al inicio del dia para comenzar a trabajar con todas las actualizaciones que se realizaron el dia anterior 
###### En este caso nos puede marcar un error indicando que no estan unidos nuestra carpeta local y el repositorio, en ese caso hacemos un git branch -u origin / master, despues hacemos el git pull y nos debe traer los archivos que se crearon de forma remota, es para que quede seteado que es el origen con el que estamos trabajando
# TAG & SWITCH
###### Nos va a permitir tagear o etiquetar uno de los commit como importante, se utiliza normalmente cuando se va a sacar una version a produccion o se va a hacer publico, se tagea por que es una version estable y queda la etiqueta por si se modifica despues y se quiere regresar a ese estado estable
###### Se usa el comando git tag nombre del archivo (depende nuestra forma de trabajo, se puede manejar por versiones como v1.0 o algun nombre definido con el que se pueda identifica)
###### El comando switch se usa para moverse sobre los archivos que tenemos de forma local
# STASH Y STASH POP
###### Es una especie de guardado temporal donde se puede volver para seguir haciendo cambios, un ejemplo es si nos quedo algun error pero nos pidieron trabajar sobre otra rama o archivo y no lo enviamos al repositorio para que si alguien jala los archivos (git pull) no se jalen con ese error que aun no solucionamos
###### git stash se guardan los cambios hechos en los archivos pero al regresar no se pueden ver tal cual las modificaciones que realizamos bajo este comando, es decir, nos mostraria el ultimo commit sin los errores
###### git stash pop nos trae los archivos con los cambios que no se veian para que podamos seguir trabajando sobre ellos y correguir lo necesario
# DELETE BRANCH
###### El comando git branch -d nombre de la rama nos elimina las ramas de forma local
###### El comando git push origin --delete nombre de la rama nos eimina las ramas de forma remota
# FETCH
###### Este comando nos trae el historial con los cambios que se hicieron de forma remota pero no trae los archivos en si, se usa como git fetch
###### git log --oneline --all nos va a permitir ver todas las modificaciones que se hicieron de forma remota
###### git tree solo se usa en apple o linux
# RESET Y RESET --HARD
###### git checkout (nombre del archivo) nos regresa al ultimo cambio realizado
###### git reset sirve para volver atras en los cambios y los saca de changes
###### git reset --hard es para que los archivos vuelvan al estado del commit anterior, se pone tambien el hash o numero que identifican al commital que vamos a regresar
# CLONE
###### Para tratar de re cuperar una carpeta o descargarla para trabajar en otro equipo, entramos en nuestro github, usando git clone quedara linkeadolo que se descargara con el repositorio
###### damos click en https donde se copiara el link del repositorio, abrimos la terminal en la pantalla y usamos git bash, ponemos git clone y pegamos el link copiado, de esta forma aparecen los archivos y ramas que tenemos de forma remota para que podamos trabajar de forma local
###### si se hace un clone ccon otro repositorio se tiene que pedir permiso
# MERGE
###### Aqui copio un codigo de su repositorio, lo inicializo con git init y luego git add, despues un git commit -m(descripcion), agrega el origen con git remote add origin (url) luego git push origin master para mergear una rama nos vamos a master y agregamos la rama, se la trae y mezcla sobre la rama master (git merge nombre de la rama)
# CONFLICTOS
# FORK & PULL REQUEST
###### Fork es para hacer un clonado de algun repositorio que no es de nosotros, hacer modificaciones y pedir que se tomen en cuenta, en el apartado sing up es para crear un nuevo usuario
###### La idea no es crear un nuevo repositorio sino ir al que ya tenemos o sobre el que queremos trabajar  y vamos a forkear
###### Nos metemos al repositorio que elegimos y vamos al apartado fork, nos da la opcion create a new fork, es basicamente como crear un nuevo repositorio, lo modificamos, en este caso se hace en la version web, si se hiciera de forma local tendriamos que configurar todo como el nuevo usuarioque esta haciendo las modificaciones
###### una vez modificado nos da el mensaje this branch ist commit a head of (usuario dueño del repositorio), le damos en contribute luego open pull request, esto es para pedirle al dueño que haga los cambios sin tener acceso total al codigo, el dueño decide si los aplica o no son de ayuda
# MARKDOWN & README.md