#  Git para **windows**
![GIT](https://git-scm.com/images/logo@2x.png)
## Comandos basicos:

### Agregando archivos a un repositorio
```
$ git add *.c
$ git add LICENSE
$ git add .
$ git commit -m 'initial project version'
```

### Ver el estado de nuestro archivos
```
$ git status
```

### Subir archivos del stage al repositorio
```
$ git commit -m 'iniciando proyect'
```

### Confirmar cambios
```
$ git commit
```

### Envio de cambios 
Reemplazar origin master por la rama a la que quiere enviar tus cambios
git push origin master
```
$ git push origin master
$ git push https://github.com/LeonardoEnriquez/Git_Tutorial.git --all
```

### Eliminar archivos de tu directorio de trabajo
```
$ rm PROJECTS.md
$ git status
```

### Eliminar archivos de tu directorio de trabajo
```
$ git rm PROJECT.mdgit
$ git status
```

### Cambiar el nombre de Archivos
```
$ git mv README.md README
$ git status
```

### Actualiza y fusiona
Para actualizar tu repositorio local al commit mas nuevo git pull opciones...
```
$ git pull origin develop
```
Para actualizar tu repositorio remote forzado git push -f <remote> <branch>
```
$ git pull -f origin develop
```

### Obtener actualizacion de archivos
```
$ git pull https://github.com/LeonardoEnriquez/Git_Tutorial.git
```

### fusionar todos los cambios que se han hecho en el repositorio local trabajando
```
$ git checkout Develop
$ git branch
$ git checkout master
$ git pull origin Devlop
```

### Agregar archivo gitignore
El archivo .gitignore ignora cualquier archivo cuyo nombre este indicado dentro del archivo
```
$ git add .gitignore
$ git commit -m "add the ignore file"
$ git status
```
En el archivo .gitignore escribimos los nombres de los archivo o carpetas que queremos ignorar (uno por línea). También podemos tener comentarios (utilizando numeral #). Por ejemplo:
```
# esto es un comentario
development.log
build
/development.log
# ignorar todos los archivos que terminen en .log
*.log
# excepto production.log
!production.log
# ignorar los archivos terminados en .txt dentro de la carpeta doc (pero no sus subdirectorios)
doc/*.txt
# ignorar todos los archivos terminados en .pdf dentro de la carpeta doc y sus subdirectorios
doc/**/*.pdf
```

### Historial

Ver historial de las diferencias introducidas
```
$ git log
```

Ver historial de las 2 ultimas diferencia introduccidas
```
$ git log
$ git log -p -2
```
Ver historial formateado ultimas diferencia introduccidas
```
$ git log --pretty=format:"%h - %an, %ar : %s"
```
>%h Hash de la confirmación abreviado
%an Nombre del autor
ar Fecha de auditoria, relativa
s Asunto

### Archivos > 100 mb
> `Corregir el error por envio de archivos incorrectos arriba de >100 mb como videos remote: error: GH001: Large files detected. You may want to try Git Large File storage - https://git-lfs.github.com.
> remote: error: Trace: 7d51855d4f834a90c5a5a526e93d2668
> remote: error: See http://git.io/iEPt8g for more information.
> remote: error: File coverage/sensitivity/simulated.bed is 102.00 MB; this exceeds GitHub's file size limit of 100.00 MB`

```
$ git filter-branch --tree-filter 'rm -rf path/to/your/file' HEAD
$ git push
```
