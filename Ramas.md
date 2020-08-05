#  Git para **windows**
![GIT](https://git-scm.com/images/logo@2x.png)

## Ramas
Las ramas (branches) nos permiten desviarnos de la línea principal de desarrollo para realizar experimentos que después podemos integrar a la línea principal o descartarlos
Por defecto git crea una rama por defecto llamada master
Para ver en qué rama nos encontramos utiliza el comando git status
```
$ git status
On branch master
...
```
### Creando una rama
Para crear una rama utiliza el comando git branch seguido del nombre que le quieres dar a la rama. 
```
$ git branch Develop
```
Para cambiar de rama debes ejecutar el siguiente comando:
git checkout Develop

Sin embargo, la mayoría de veces, cuando uno quiere crear una rama también se quiere ubicar sobre ella, así que existe un atajo
```
$ git checkout -b mi-rama
```
### Cambiando el nombre de una rama
Para cambiar el nombre de la rama debes estar ubicado sobre ella y ejecutar el comando git branch -m seguido del nuevo nombre. 
```
$ git branch -m develop
```
### Integrando una rama
Para integrar los commits de una rama (p.e. Develop) a otra (p.e. master) primero debemos ubicarnos sobre la rama principal (p.e. master) y ejecutar el comando git merge seguido del nombre de la rama:
```
$ git checkout master
git merge Develop
```

### Solucionando conflictos
Es posible que se realicen cambios en las dos ramas que generen conflictos a la hora de integrarlas (p.e. si se crea un archivo con el mismo nombre en las dos ramas o si se cambia la misma línea de un archivo). En este caso es necesario solucionar los conflictos a la hora de hacer el git merge.
> Por ejemplo, suponiendo que en master se creó un archivo llamado prueba.txt con un  texto Hola desde master y en mi-rama se creo otro archivo con el mismo nombre pero  el texto Hola desde mi-rama, al hacer el git merge veríamos lo siguiente en la consola:
```$ git checkout master
1 $ git merge mi-rama
2 Auto-merging prueba.txt
3 CONFLICT (add/add): Merge conflict in prueba.txt
4 Automatic merge failed; fix conflicts and then commit the result.
```
La línea 4 nos dice que existe un conflicto en prueba.txt. Al abrir el archivo veríamos algo así:
```
1 <<<<<<< HEAD
2 Hola desde master
3 =======
4 Hola desde mi-rama
5 >>>>>>> mi-rama
```
Lo que está entre la línea 1 y 3 es lo que está en master y lo que está entre la línea 3 y 5 es lo que está en mi-rama. Para solucionar el conflicto debemos decidir qué vamos a dejar y qué vamos a eliminar. Muy importante es siempre elimianar las líneas que definen los límites (las que comienzan con <<<<<<<, ======= y >>>>>>>).

Una vez solucionado el conflicto debemos indicarle a git que ya lo solucionamos utilizando el comando git add y continuar con el merge.
```
git add prueba.txt
git commit -m 'Merge branch "Develop"'
```
### Eliminando una rama
Para eliminar una rama que ya ha sido integrada en otra utilizamos el comando git branch -d. Para que este comando funcione debemos estar ubicados en la rama a la que fue integrada. Por ejemplo, asumiendo que mi-rama ya fue integrada a master ejecutaríamos el siguiente comando:
```
git checkout master
git branch -d mi-rama
```
Si no hemos integrado la rama pero igual la queremos eliminarla, podemos cambiar la opción -d por -D. Por ejemplo, asumiendo que la rama mi-rama tiene nuevos commits y no ha sido integrada, podemos eliminarla ejecutando el siguiente comando:
```
git branch -D mi-rama
```
