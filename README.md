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


