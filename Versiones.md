## Especificar versiones en Git con tag
 A través del comando "git tag" podemos crear etiquetas, en una operación que se conoce comúnmente con el nombre de **"tagging"**. El etiquetado es una herramienta fundamental para que otros sistemas sepan cuándo un proyecto ha cambiado y se permitan desencadenar procesos a ejecutar cada vez que esto ocurre. 
 Generalmente los cambios se pueden dividir en tres niveles de "importancia": **Mayor, menor y pequeño ajuste**. Si tu versión de proyecto estaba en la 1.1 y haces un cambio que no altera la funcionalidad ni la interfaz de trabajo entonces lo adecuado es versionar tu aplicación como 1.1.1. 

 ### Crear un tag con Git
 Suponiendo que se empieza por el número de versión 1.0, entonces para crear la correspondiente etiqueta lanzarás el subcomando de Git "git tag":

```
$ git tag v1.0 -m "Primera versión"
```

Generalmente, después de hacer cambios en tu repositorio y subirlos al sistema (después de hacer el commit), podrás generar otro número de versión etiquetando el estado actual.
```
$ git tag v1.1 -m "Segunda versión, cambios menores"
```

### Ver estados de version en el repositorio con Git tag

Después de haber creado tu primer tag, podrás lanzar el comando "git tag", sin más parámetros, que te informará sobre las versiones que has etiquetado hasta el momento
```
$ git tag
```
También puedes buscar etiquetas con un patrón particular. El repositorio del código fuente de Git, por ejemplo, contiene más de 500 etiquetas. Si sólo te interesa ver la serie 1.8.5, puedes ejecutar:
```
$ git tag -l 'v1.8.5*'
v1.8.5
v1.8.5-rc0
v1.8.5-rc1
v1.8.5-rc2
v1.8.5-rc3
v1.8.5.1
v1.8.5.2
v1.8.5.3
v1.8.5.4
v1.8.5.5
```

Otro comando interesante en el tema de versionado es "show" que te permite ver cómo estaba el repositorio en cada estado que has etiquetado anteriormente, es decir, en cada versión.
```
$ git show v1.0

tag v1.0
Tagger: leonardoenriquez@gmail.com <leonardoenriquez@gmail.com>
Date:   Wed Aug 5 10:41:56 2020 -0700

Primera version

commit 2f618e1ae08f22405da7c80a9ccc2194e9eebe98
Author: Leonardo Enriquez <leonardoenriquez@gmail.com>
Date:   Wed Aug 5 10:42:06 2020 -0700

    Create Versiones

diff --git a/Versiones b/Versiones
new file mode 100644
index 0000000..c11ecc0
--- /dev/null
```

### Enviar tags a GitHub
Si quieres que tus tags creados en local se puedan enviar al repositorio en GitHub
```
$ git push --tags
```
resultado el siguiente mensaje
```
$ git push --tags
Counting objects: 1, done.
Writing objects: 100% (1/1), 168 bytes | 0 bytes/s, done.
Total 1 (delta 0), reused 0 (delta 0)
To https://github.com/LeonardoEnriquez/Git_Tutorial.git
 * [new tag]         v1.0 -> v1.0
```

Tambien se puede enviar un tag en especifico, a traves del siguiente comando:
```
$ git push origin v1.1
```

#### Enviar tags y hacer push de los commit al mismo tiempo

Si queremos hacer un push de una rama en concreto, por ejemplo la rama master, y enviar los tags al mismo tiempo, entonces podríamos lanzar el siguiente comando.
```
$ git push origin master --tags
```
### Etiquetado Tardío
También puedes etiquetar commits mucho tiempo después de haberlos hecho. Supongamos que tu historial luce como el siguiente:
```
$ git log --pretty=oneline
15027957951b64cf874c3557a0f3547bd83b3ff6 Merge branch 'experiment'
a6b4c97498bd301d84096da251c98a07c7723e65 beginning write support
0d52aaab4479697da7686c15f77a3d64d9165190 one more thing
6d52a271eda8725415634dd79daabbc4d9b6008e Merge branch 'experiment'
0b7434d86859cc7b8c3d5e1dddfed66ff742fcbc added a commit function
4682c3261057305bdd616e23b64b0857d832627b added a todo file
166ae0c4d3f420721acbb115cc33848dfcc2121a started write support
9fceb02d0ae598e95dc970b74767f19372d61af8 updated rakefile
964f16d36dfccde844893cac5b347e7b3d44abbc commit the todo
8a5cbc430f1a9c3d00faaeffd07798508422908a updated readme
```
Suponiendo que se olvido etiquetar el proyecto en su versión v1.2, la cual corresponde al commit “updated rakefile”. Igual puedes etiquetarlo. Para etiquetar un commit, debes especificar el checksum del commit (o parte de él) al final del comando
```
$ git tag -a v1.2 9fceb02
```

### Etiquetas anotadas
La forma más fácil de hacerlo es especificar la opción -a cuando ejecutas el comando git tag:
```
$ git tag -a v1.4 -m 'my version 1.4'
$ git tag
v0.1
v1.3
v1.4
```
La opción -m especifica el mensaje de la etiqueta, el cual es guardado junto con ella.

Fuentes: 
[git-scm.com](https://git-scm.com/book/es/v2/Fundamentos-de-Git-Etiquetado)
[desarrolloweb.com](https://desarrolloweb.com/articulos/trabajar-ramas-git.html)

