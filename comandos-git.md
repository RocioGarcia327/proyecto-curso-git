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
###### 
# ADD - STATUS - COMMIT
# BRANCH
# STAGE
# 
# IGNORE
# DIFF
# LOG
# CHECKOUT
# GITHUB Y VISUAL
# PLUGIN GRAPH
# REMOTE ORIGIN
# PUSH Y PULL
# TAG & SWITCH
# STASH Y STASH POP
# DELETE BRANCH
# FETCH
# RESET Y RESET --HARD
# CLONE
# MERGE
# CONFLICTOS
# FORK & PULL REQUEST
# MARKDOWN & README.md