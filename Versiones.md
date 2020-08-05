## Especificar versiones en Git con tag

A través del comando "git tag" podemos crear etiquetas, en una operación que se conoce comúnmente con el nombre de "tagging". El etiquetado es una herramienta fundamental para que otros sistemas sepan cuándo un proyecto ha cambiado y se permitan desencadenar procesos a ejecutar cada vez que esto ocurre. Generalmente los cambios se pueden dividir en tres niveles de "importancia": Mayor, menor y pequeño ajuste. Si tu versión de proyecto estaba en la 1.1 y haces un cambio que no altera la funcionalidad ni la interfaz de trabajo entonces lo adecuado es versionar tu aplicación como 1.1.1.

### Crear un tag con Git
Hay dos tipos de etiquetas: ligeras (lightweight) y anotadas (annotated). Una etiqueta ligera almacena únicamente el commit sobre el que se creó la etiqueta, mientras que una etiqueta anotada almacena también la información de la persona que la creó, la fecha y un mensaje. Nuestra recomendación es siempre crear etiquetas anotadas.

Etiqueta Ligera:
```
git tag v1.4.2
```
Etiqueta anotada:
```
$ git tag -a v1.0 -m 'Version 1.0'
```

### Listando etiquetas
Para listar las etiquetas de un repositorio utiliza el siguiente comando:
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
+++ b/Versiones
@@ -0,0 +1,2 @@
+## Especificar versiones en Git con tag
+
~
```

### Eliminando etiquetas
Para eliminar una etiqueta utiliza el comando git tag -d seguido del nombre de la etiqueta. Por ejemplo, para eliminar una etiqueta llamada v1.4.2 ejecuta el siguiente comando:
git tag -d v1.4
```
$ git tag -d v1.4.2
```
## Repositorios remotos
### Subiendo etiquetas
Para compartir una etiqueta con un repositorio remoto ejecuta el comando git push pasándo explicitamente el nombre de la etiqueta. Por ejemplo, para compartir una etiqueta llamada v1.4.2 a un repositorio remoto llamado origin, ejecutaríamos el siguiente comando:
```
$ git push origin v1.4.2
```
Si tienes varias etiquetas por compartir puedes utilizar el siguiente comando:
```
git push origin --tags
```
### Eliminando etiquetas
Para eliminar una etiqueta de un repositorio remoto utiliza el comando git push con la opción --delete. Por ejemplo, para eliminar la etiqueta v1.4.2 del remoto origin ejecutaríamos el siguiente comando:
```
$ git push --delete origin v1.4.2
```