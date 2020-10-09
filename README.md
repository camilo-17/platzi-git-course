Para añadir a staging
´´´bash
git add 
´´´
para remover archivos de staging:

´´´bash
git rm archivo.txt 
´´´

Para enviar al commit 
´´´bash
git commit -m "comentario" 
´´´

para traer los cambios 
´´´bash
git checkout 
´´´

Acceder a la configuración 
´´´bash
git config list 
´´´

Cambiar variables de configuracion
´´´bash
git config --global name.user "Camilo"
´´´
Para ver los cambios realizados entre commit
´´´bash
git show

git show historia.txt
´´´

Para comparar dos commit
´´´bash
git diff 1234 3211
´´´

Para volver a la version anterior
´´´bash
git reset
´´´
Para volver a la version anterior sin perder los archivos en staging
´´´bash
git reset 1234 --soft
´´´
Para ver en resumen las lineas cambiadas en el log
´´´bash
git log --stat 
´´´
Para ver como era el proyecto antes 

´´´bash
git checkout 1234

git checkout 1234 historia.txt
´´´
Para volver a master (Los cabmios actuales, ultimo commit)

´´´bash
git checkout master
git checkout master historia.txt
´´´

git log --oneline - Te muestra el id commit y el título del commit.
git log --decorate- Te muestra donde se encuentra el head point en el log.
git log --stat - Explica el número de líneas que se cambiaron brevemente.
git log -p- Explica el número de líneas que se cambiaron y te muestra que se cambió en el contenido.
git shortlog - Indica que commits ha realizado un usuario, mostrando el usuario y el titulo de sus commits.
git log --graph --oneline --decorate y
git log --pretty=format:"%cn hizo un commit %h el dia %cd" - Muestra mensajes personalizados de los commits.
git log -3 - Limitamos el número de commits.
git log --after=“2018-1-2” ,
git log --after=“today” y
git log --after=“2018-1-2” --before=“today” - Commits para localizar por fechas.
git log --author=“Name Author” - Commits realizados por autor que cumplan exactamente con el nombre.
git log --grep=“INVIE” - Busca los commits que cumplan tal cual está escrito entre las comillas.
git log --grep=“INVIE” –i- Busca los commits que cumplan sin importar mayúsculas o minúsculas.
git log – index.html- Busca los commits en un archivo en específico.
git log -S “Por contenido”- Buscar los commits con el contenido dentro del archivo.
git log > log.txt - guardar los logs en un archivo txt


Hacer una rama de desarrollo
´´´bash
git branch cabecera
´´´

pasar a otra rama
´´´bash
git checkout cabecera
´´´

Volver a master
´´´bash
git checkout master
´´´