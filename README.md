# Curso de git y github

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