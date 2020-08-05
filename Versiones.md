## Especificar versiones en Git con tag
 A través del comando "git tag" podemos crear etiquetas, en una operación que se conoce comúnmente con el nombre de **"tagging"**. El etiquetado es una herramienta fundamental para que otros sistemas sepan cuándo un proyecto ha cambiado y se permitan desencadenar procesos a ejecutar cada vez que esto ocurre. 
 Generalmente los cambios se pueden dividir en tres niveles de "importancia": **Mayor, menor y pequeño ajuste**. Si tu versión de proyecto estaba en la 1.1 y haces un cambio que no altera la funcionalidad ni la interfaz de trabajo entonces lo adecuado es versionar tu aplicación como 1.1.1. 

 ### Crear un tag con Git
 Suponiendo que se empieza por el número de versión 1.0, entonces para crear la correspondiente etiqueta lanzarás el subcomando de Git "git tag":

```
git tag v1.0 -m "Primera versión"
```

Generalmente, después de hacer cambios en tu repositorio y subirlos al sistema (después de hacer el commit), podrás generar otro número de versión etiquetando el estado actual.
```
git tag v1.1 -m "Segunda versión, cambios menores"
```

### Ver estados de version en el repositorio con Git tag

Después de haber creado tu primer tag, podrás lanzar el comando "git tag", sin más parámetros, que te informará sobre las versiones que has etiquetado hasta el momento
```
git tag
```

Otro comando interesante en el tema de versionado es "show" que te permite ver cómo estaba el repositorio en cada estado que has etiquetado anteriormente, es decir, en cada versión.
```
git show v1.0
```
Dando el siguiente resultado
```
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
git push --tags
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
git push origin v1.1
```