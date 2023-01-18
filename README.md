# Guión 1 Git
## Comandos:
'''bash
git init
'''
>Inicialización do repo local
# Como crear proba_git 
## inicio
    ''' para nuestra practica utilizaremos Git en Visual Code Studio
    crearemos una carpeta donde se almaceran los html que usaremos 
    es visual accederemos a ella y crearemos los documentos y los rellenaremos con 
    información usando emmet
    una vez listo abriremos una terminal en el propio visual y en ella utilizaremos una serie 
    comando de Git. Con los comandos (git config --global user.name "nombre") y con (git config --global user.email "correo").
    ahora comprobaremos que la ruta del terminal es la misma que la carpeta con la que estamos trabajando. Posteriormente añadiremos al git nuestro documentos con el comando (git add .) este subira todo el contenido de la carpeta. Luego utilizaremos un commit y le añadiremos un mensaje (git commit -m "mensaje").
    Con el comando git log --oneline --graph --decorate --all comprobaremos todos los commit que hayamos echo.
    Una vez echo todos los cambios procederemos a acceder a Github (crear una cuenta si no tenemos) para poder subir nuestro repositorio a la plataforma. Para esto usaremos el comando git push -u origin --all.
    Lo siguiente que haremos sera crear otra carpeta para clonar el contenido que hemos subido a git hub para ello cambiaremos la ruta del terminal a la nueva carpeta y alli utilizar el comando git clone y el enlace de git hub que conseguiremos aqui:
    ![copiar_codigo](\Repo git\Captura.PNG)
    Otra forma para conseguir el codigo es con el comando git pull --all para cargar que se haya echo en el propio git hub en el repositorio local.
    '''
# Guia paso a paso
 1. Empezar a usar y crear el repositorio local
    * Instalaremos Git en nuestro ordenador (comandos o via web).
    * Creamos una carpeta para nuestro repositorio y la abrimos en visual code studio
    * Utilizaremos la terminal de visual code studio y comprobaremos que la ruta sea la de la carpeta creada
    * Para utilizar de ejemplo crearemos dos html y los rellenaremos con ! (emmet)
    * Ahora usamos "git add ." para añadir todos las modificaciones del repositorio (guardar antes los cambios)
    * Con (git commit -m "mensaje") guarderos un comentario de lo que hemos añadido/modificado
    * Con el comando git log --oneline --graph --decorate --all comprobaremos todos los commit que hayamos echo
2. Git hub 
    * Accederemos o crearemos una cuenta de Git Hub
    * Una vez crearemos un nuevo repositorio publico dentro tenemos una pequeña guia de como subir nuestro repositorio
    * Crearemos un Readme en formato md (mark down) lo añadiremos y commiteamos
    * Utilizaremos (git branch -M main) para cambiar el master a main, ya que es lo mas recomendable
    * Ahora lo subiremos con (git push -u origin --all ) al repositorio de Git Hub
3. Clonación
    * Creamos otra carpeta en la ruta de nuestra repo y accedemos a ella en la terminal
    * ahora copiaremos el enlace de nuestra repo y la pegaremos en el siguiente comando (git clone enlace)
    * Ahora tendremos en esta carpeta todo lo que habiamos subido a Git Hub
4. Pull
    * Crearemos en Git Hub un CSS de ejemplo
    * Ahora lo añadiremos a nuestro repositorio local con el comando (git pull --all)

#Guión 2 Git:
## Nuevos comandos
1.git config --global color.ui auto
    * Controla los colores de salida.
2.git diff
    * muestra las diferencias en el repositorio, si has modificado o añadido una nueva linea
3.git show
    * Similar a git diff pero este muestra las diferencias entre commits
4.git commit --amend -m "texto"
    * Modifica el ultimo commit añadido




