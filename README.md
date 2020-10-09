# Curso de git y github 📋

Este curso enseña como manejar git y git hub pongo aca los comandos que aprendi 


Para añadir a staging
```sh
git add 
```
para remover archivos de staging:
```sh
git rm archivo.txt 
```

Para enviar al commit 
```sh
git commit -m "comentario" 
```

para traer los cambios 
```sh
git checkout 
```

Acceder a la `configuración`
```sh
git config list 
```

Cambiar variables de configuracion
```sh
git config --global name.user "Camilo"
```
Para ver los cambios realizados entre commit
```sh
git show

git show historia.txt
```

Para comparar dos commit
```sh
git diff 1234 3211
```

Para volver a la version anterior
```sh
git reset
```
Para volver a la version anterior sin perder los archivos en staging
```sh
git reset 1234 --soft
```
Para ver en resumen las lineas cambiadas en el log
```sh
git log --stat 
```
Para ver como era el proyecto antes 
```sh
git checkout 1234
git checkout 1234 historia.txt
```
Para volver a master (Los cabmios actuales, ultimo commit)
```sh
git checkout master
git checkout master historia.txt
```

* ```sh git log --oneline ``` - Te muestra el id commit y el título del commit.
* ```sh git log --decorate ``` - Te muestra donde se encuentra el head point en el log.
* ```sh git log --stat ``` - Explica el número de líneas que se cambiaron brevemente.
* ```sh git log -p ```- Explica el número de líneas que se cambiaron y te muestra que se cambió en el contenido.
* ```sh git shortlog ``` - Indica que commits ha realizado un usuario, mostrando el usuario y el titulo de sus commits.
* ```sh git log --graph --oneline --decorate ``` y
* ```sh git log --pretty=format:"%cn hizo un commit %h el dia %cd" ``` - Muestra mensajes personalizados de los commits.
* ```sh git log -3 ``` - Limitamos el número de commits.
* ```sh git log --after=“2018-1-2” ``` ,
* ```sh git log --after=“today” ``` y
* ```sh git log --after=“2018-1-2” --before=“today” ``` - Commits para localizar por fechas.
* ```sh git log --author=“Name Author” ``` - Commits realizados por autor que cumplan exactamente con el nombre.
* ```sh git log --grep=“INVIE” ``` - Busca los commits que cumplan tal cual está escrito entre las comillas.
* ```sh git log --grep=“INVIE” –i ``` - Busca los commits que cumplan sin importar mayúsculas o minúsculas.
* ```sh git log – index.html``` - Busca los commits en un archivo en específico.
* ```sh git log -S “Por contenido”``` - Buscar los commits con el contenido dentro del archivo.
* ```sh git log > log.txt``` - guardar los logs en un archivo txt

 ```sh
Ver las ramas existentes
```sh
git branch
```
Fusionar las ramas (SIEMPRE SE DEBE HACER EN MASTER).
```sh
git merge cabecera1
```


Hacer una rama de desarrollo
```sh
git branch cabecera
```

pasar a otra rama
```sh
git checkout cabecera
```

Volver a master
```sh
git checkout master
```

cambiar la URL del repo
```sh 
git remote set-url origin git@github.com:camilo-17
```

ver a que URL le ha apuntado
```sh 
git remote -v
```

Crear un tag:
```sh 
git tag -a v0.1 -m "resultado"
```
Mostrar tags
```sh 
git show-ref --tags
```

Enviar tag
```sh 
git push origin --tags
```

log de ramas
```sh 
git show-branch --all
```

## Pull Request

Es una funcionalidad de github (en gitlab llamada merge request y en bitbucket push request), en la que un colaborador pide que revisen sus cambios antes de hacer merge a una rama, normalmente master.

Al hacer un pull request se genera una conversación que pueden seguir los demás usuarios del repositorio, así como autorizar y rechazar los cambios.

El flujo del pull request es el siguiente

* Se trabaja en una rama paralela los cambios que se desean: 

```sh 
git checkout -b <rama>
```

* Se hace un commit a la rama:

```sh 
git commit -am '<Comentario>'
```

* Se suben al remoto los cambios:

```sh 
git push origin <rama>
```
 
 * En GitHub se hace el pull request comparando la rama master con la rama del fix.

 * Uno, o varios colaboradores revisan que el código sea correcto y dan **feedback** (en el chat del pull request)

 * El colaborador hace los cambios que desea en la rama y lo vuelve **a subir** al remoto (automáticamente jala la historia de los cambios que se hagan en la rama, en remoto)

 * Se aceptan los cambios en GitHub

 * Se hace merge a master desde GitHub

**Importante:** Cuando se modifica una rama, también se modifica el pull request.


### Forks o Bifurcaciones

Es una característica única de GitHub en la que se crea una copia exacta del estado actual de un repositorio directamente en GitHub, éste repositorio podrá servir como otro origen y se podrá clonar (como cualquier otro repositorio), en pocas palabras, lo podremos utilizar como un git cualquiera
.
Un fork es como una bifurcación del repositorio completo, tiene una historia en común, pero de repente se bifurca y pueden variar los cambios, ya que ambos proyectos podrán ser modificados en paralelo y para estar al día un colaborador tendrá que estar actualizando su fork con la información del original.
.
Al hacer un fork de un poryecto en GitHub, te conviertes en dueñ@ del repositorio fork, puedes trabajar en éste con todos los permisos, pero es un repositorio completamente diferente que el original, teniendo alguna historia en común.
.
Los forks son importantes porque es la manera en la que funciona el open source, ya que, una persona puede no ser colaborador de un proyecto, pero puede contribuír al mismo, haciendo mejor software que pueda ser utilizado por cualquiera.
.
Al hacer un fork, GitHub sabe que se hizo el fork del proyecto, por lo que se le permite al colaborador hacer pull request desde su repositorio propio.

***Trabajando con más de 1 repositorio remoto***

Cuando trabajas en un proyecto que existe en diferentes repositorios remotos (normalmente a causa de un fork) es muy probable que desees poder trabajar con ambos repositorios, para ésto puedes crear un remoto adicional desde consola.

```sh 
git remote add <nombre_del_remoto> <url_del_remoto> 
```

```sh 
git remote upstream https://github.com/freddier/hyperblog
```

Al crear un remoto adicional podremos, hacer pull desde el nuevo origen (en caso de tener permisos podremos hacer fetch y push)

```sh 
git pull <remoto> <rama>
git pull upstream master
```

Éste pull nos traerá los **cambios del remoto**, por lo que se estará al día en el proyecto, el flujo de trabajo cambia, en adelante se estará trabajando haciendo **pull desde el upstream y push al origin para pasar a hacer pull request**.


```sh 
git pull upstream master
git push origin master
```
