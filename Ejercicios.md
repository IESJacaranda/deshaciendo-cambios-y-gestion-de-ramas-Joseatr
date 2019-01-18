1. Tienes que modificar la escena 5 de Hamlet en el fichero scene-5.txt. En dicha escena Hamlet encuentra al fantasma de su padre. Añade este texto al fichero:
> Ghost: 
> My hour is almost come,
> When I to sulphurous and tormenting flames
> Must render up myself.
2. Añade scene-5.txt al área de preparación.
3. Haz un commit con los cambios con un buen mensaje de commit.
4. Modifica las palabras del fantasma. Aquí tienes una sugerencia divertida:
> Ghost: 
> My hour is almost come,
> When I to sulphurous and tormenting balloons
> Must render up myself.
5. Devuelve el fichero al estado del último commit.
6. Cambia el nombre de LARRY por LAERTES en los ficheros scene-3.txt y scene-7.txt.
7. Añade los ficheros al área de preparación usando un único comando git.
8. Vamos a cometer un error a propósito. Borra cualquier línea del fichero scene-2.txt.
9. Añade scene-2.txt al área de preparación.
10. Comprueba el estado del repositorio. 
11. Devuelve scene-2.txt al directorio de trabajo.
12. Haz un commit para guardar los cambios realizados en el nombre de Larry por Laertes.
13. Busca el primer commit que has hecho y vuelve a dicho commit. Indica como has buscado el commit anterior y como has vuelto a él.
14. Crea una nueva rama llamada **reinventando_hamlet**
15. Cámbiate a dicha rama
16. Mejora la escena 2 como creas conveniente.
17. Haz un commit con los cambios con un mensaje adecuado.
18. Vuelve a la rama master.
19. Elimina la rama **reinventando_halet**
20. Crea una nueva rama, modifica algo en la rama master, haz commit y llévate los cambios a la rama que has creado.
21. Provoca un conflicto entre la rama master y la rama que has creado (indica lo que has hecho). Une la rama a la rama master resolviendo el conflicto.


1. 
- mkdir Examen
- cd Examen/
- git init
- git config --global user.name "joseatr"
- git config --global user.email "joseatr.93@gmail.com"
- nano scene-5.txt
- git remote add origin https://github.com/IESJacaranda/deshaciendo-cambios-y-gestion-de-ramas-Joseatr
- git pull origin master

2. 
- git nano scene-5.txt (pego el texto)

3.
- git commit -m "Subiendo scene-5.txt modificado"

4.
- nano scene-5.txt (vuelvo a pegar el texto debajo del anterior)

5.
- git log --oneline
- git reset --hard

6.
- nano scene-3.txt
- CONTROL W 
- CONTROL R (Introduzco el nombre a buscar y seguidamente me pregunta por cual reemplazar y lo introduzco)
- nano scene-7.txt
- CONTROL W 
- CONTROL R (Introduzco el nombre a buscar y seguidamente me pregunta por cual reemplazar y lo introduzco)

7. 
- git add scene-3.txt scene-7.txt

8.
- nano scene-2.txt (Borro la primera linea)

9. 
- git add scene-2.txt

10.
- git status

11.
- git rm --cached scene-2.txt

12.
- git commit -m "Nombre de Larry cambiado"

13.
- git log --oneline (Busco el primer commit)
- git reset --hard 0da6009

14.
- git branch reinventando_hamlet

15.
- git checkout reinventando_hamlet

16.
- nano scene-2.txt (Escribo al final "At that moment, Hamlet raised his hand and said "I CAN!" ")

17.
- git add scene-2.txt
- git commit -m "Añado nueva linea al final"

18.
- git checkout master

19.
- git branch -D reinventando_hamlet

20.
- git branch conf

21.
- nano scene-3.txt (Modifico borrando unas lineas)
- git add scene-3.txt
- git commit -m "modificando scene-3.txt"
- git checkout conf
- nano scene-3.txt (Modifico borrando distintas lineas a als de la rama master)
- git add scene-3.txt
- git commit -m "Creando conflicto"
- git checkout master
- git merge conf (CONFLICTO)
- nano scene-3.txt (Modifico para que no haya errores y quede igual a la de la rama conf)
- git add scene-3.txt
- git commit -m "Arreglado"
- git merge conf
