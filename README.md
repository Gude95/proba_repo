# Guión 1 Git
## Comandos:
'''bash
git init
'''
>Inicialización do repo local
# Como crear proba_git 
## inicio
    '''
    Para nuestra practica utilizaremos Git en Visual Code Studio.
     Crearemos una carpeta donde se almaceran los html que usaremos.
    En visual accederemos a ella y crearemos los documentos
     y los rellenaremos con  información usando emmet
    una vez listo abriremos una terminal en el propio visual 
    y en ella utilizaremos una serie comandos de Git. 
    Con los comandos (git config --global user.name "nombre")
     y con (git config --global user.email "correo").
    ahora comprobaremos que la ruta del terminal es la misma
     que la carpeta con la que estamos trabajando.
      Posteriormente añadiremos al git nuestro documentos 
      con el comando (git add .) Este subira todo el contenido de la carpeta. 
      Luego utilizaremos un commit y le añadiremos un mensaje (git commit -m "mensaje").
    Con el comando git log --oneline --graph --decorate --all 
    comprobaremos todos los commit que hayamos echo. Una vez
     echo todos los cambios procederemos a acceder a Github 
     (crear una cuenta si no tenemos) para poder subir nuestro
      repositorio a la plataforma. 
      Para esto usaremos el comando git push -u origin --all.
    Lo siguiente que haremos sera crear otra carpeta para
     clonar el contenido que hemos subido a git hub para
     ello cambiaremos la ruta del terminal a la nueva carpeta
      y alli utilizar el comando git clone y el enlace de
       git hub que conseguiremos aqui:
    ![copiar_codigo](\Repo git\Captura.PNG)
    Otra forma para conseguir el codigo es con el 
    comando git pull --all para cargar que se haya echo
     en el propio git hub en el repositorio local.
    '''
# Guia paso a paso
 1. **Empezar a usar y crear el repositorio local**
    * Instalaremos Git en nuestro ordenador (comandos o via web).
    * Creamos una carpeta para nuestro repositorio y la abrimos en visual code studio
    * Utilizaremos la terminal de visual code studio y comprobaremos que la ruta sea la de la carpeta creada
    * Para utilizar de ejemplo crearemos dos html y los rellenaremos con ! (emmet)
    * Ahora usamos "git add ." para añadir todos las modificaciones del repositorio (guardar antes los cambios)
    * Con (git commit -m "mensaje") guarderos un comentario de lo que hemos añadido/modificado
    * Con el comando git log --oneline --graph --decorate --all comprobaremos todos los commit que hayamos echo
2. **Git hub** 
    * Accederemos o crearemos una cuenta de Git Hub
    * Una vez crearemos un nuevo repositorio publico dentro tenemos una pequeña guia de como subir nuestro repositorio
    * Crearemos un Readme en formato md (mark down) lo añadiremos y commiteamos
    * Utilizaremos (git branch -M main) para cambiar el master a main, ya que es lo mas recomendable
    * Ahora lo subiremos con (git push -u origin --all ) al repositorio de Git Hub
3. **Clonación**
    * Creamos otra carpeta en la ruta de nuestra repo y accedemos a ella en la terminal
    * ahora copiaremos el enlace de nuestra repo y la pegaremos en el siguiente comando (git clone enlace)
    * Ahora tendremos en esta carpeta todo lo que habiamos subido a Git Hub
4. **Pull**
    * Crearemos en Git Hub un CSS de ejemplo
    * Ahora lo añadiremos a nuestro repositorio local con el comando (git pull --all)

# Guión 2 Git:
## Nuevos comandos
1. **git config --global color.ui auto**
    * Controla los colores de salida.
2. **git diff**
    * muestra las diferencias en el repositorio, si has modificado o añadido una nueva linea
3. **git show**
    * Similar a git diff pero este muestra las diferencias entre commits
4. **git commit --amend -m "texto"**
    * Modifica el ultimo commit añadido
# Guión 3 Git:
## Nuevos comandos
1. **git reset --hard**
    * Este comando añadiendole el codigo de un commit nos permite posicionar nuestro Head en el.
2. **git remote remove origin** 
    * Basicamente elimina todo la información posterior al commit que apunta HEAD
3. **git log**
    * git log muestra toda la información sobre los commmit realizados.
4. **git diff HEAD~2..HEAD**
    * con este comando podemos ver las diferencias entre el head actual y el de hace 2 commits, (el 2 del comando puedo ser cualquier numero)
5. **git diff &lt;codigo hash de la primera version>..HEAD**
    * Muestra las diferencias desde el commit seleccionado hasta el actual
6. **git annotate**
    * este comando te permite ver las modificaciones que han echo los usuarios en un archivo, muiestra el usuario la fecha y la modificación/ contenido añadido.

## Practica 4: Desfacer cambios

### Comandos empregados

``` bash 
git clean -f
```
> Sirve para eliminar un arquivo que ainda non esta para commitear.

``` bash 
git reset --soft HEAD~1
```
> Sirve para eliminar solo o commit pero non os cambios no stage.

``` bash 
git reset --hard HEAD~1
```
> Sirve para volver o repo o estado anterior.

```bash 
git reset "archivo"
```
> Git mixed. Restablece o indice pero non o arbol de traballo e indica o que non se actualizou.

``` bash 
git restore "arquivo"
```
> Sirve para desfacer os cambios que se acaban de facer nun arquivo.

``` bash
git restore --stage
```
> Sirve para desfacer os cambios que se acaban de facer no stage.


### Pasos a seguir na práctica.

1. Eliminamos a ultima linea de indice.txt e executamos o comando git status para comprobar o estado do repo.
2. Executamos o comando git restore para desfacer os cambios que acabamos de realizar. 
3. Volvemos a eliminar a ultima linea de indice.txt e executamos o comando "git add ." para añdilo o stage.
4. Desfacemos o ultimo git add . executando o comando "git restore --stage" e comprobamos o estado do repo.
5. Volvemos eliminar a ultima linea de indice.txt, eliminamos capitulo3.txt e engadimos o arquivo capitulo4.txt.
6. Facemos un git add . para engadir os cambios e revisamos o estado do repo.
7. Facemos un git restore --stage * para desfacer todos os cambios no stage e revisamos o estado do repo.
8. Facemos un git restore * para desfacer todos os cambios e revisamos o estado do repo.
9. Facemos git clean -f para eliminar o arquivo novo "capitulo4.txt" 
10. Eliminamos a ultima linea de indice.txt e o capitulo3.txt
11. Facemos git add * para engadir todos os cambios e despois git commit -m "borrado accidental" e revisamos o estado do repo.
12. Facemos un git reset --soft para desfacer o commit pero non o git add . nin os cambios e revisamos o estado do repo vendo que o git add ainda se conserva.
13. Facemos de novo git commit -m "borrado accidental" e un git log para ver o estado do repo.
14. Volvemos a ultima version anterior do repo utilizando o comando git reset --hard e vemos que o repo volveu o estado anterior.


## Practica 5: Ramas
1. **git brach**
    *Este es el comando para añadir ranas
2. **git branch -av
    *Muestra las ramas del repositorio
3. **git checkout master**
    *Fusionar la rama con la rama master.
4. **git branch -d
    *elimina la rama
