#  Git para **windows**

![GIT](https://git-scm.com/images/logo@2x.png)

## Comandos basicos:

* git init, indica a git que se creara un nuevo o se utilizara uno existente
* git add <file>, permite subir los archivos del working directory al staging area
* git status, permite ver el estado de archivos donde se encuentra
* git commit, subir archivos del staging area al repositorio
* git push,permite subir los archivos a un repositorio remoto o servidor
* git pull, permite traer cambios realizados por otros desarrolladores
* git clone, permite realizar una copia desde el servidor central al computador

## Configurando Git

### Tu identidad

```
$ git config --global user.name "John Doe"
$ git config --global user.email "johndoe@example.com"
```

### Comprobando tu configuracion

```
$ git config --list
$ git config user.name
```

### Obteniendo ayuda
```  
$ git help config
```

### Inicializando un repositorio

```
$ git init
```

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
$ git commit -m 'initial project version'
```

### Mostrar historial del ultimo commit
```
$ git log
```

## Identificar el repositorio de trabajo actual
```console
$ git remote -v
```

## Cambio de repositorio remoto URL
```console
$ git remote set-url origin https://hostname/USERNAME/REPOSITORY.git
```
## Clonando un repositorio
```
$ git clone https://github.com/libgit2/libgit2
$ git clone https://github.com/libgit2/libgit2 mylibgit
```
## Cambios preparados y no preparados
```
$ git satus
$ git diff
$ git diff -staged
$ git diff -cached
```
## Confirmar cambios
```
$ git commit
```
## Eliminar archivos de tu directorio de trabajo
```
$ rm PROJECTS.md
$ git status
```
## Eliminar archivos de tu directorio de trabajo
```
$ git rm PROJECT.md
$ git status
```
## Cambiar el nombre de Archivos
```
$ git mv README.md README
$ git status
```
## Ver historial de las diferencias introduccidas
```
$ git log
```
## Ver historial de las 2 ultimas diferencia introduccidas
```
$ git log
$ git log -p -2
```
## Ver historial formateado ultimas diferencia introduccidas
```
$ git log --pretty=format:"%h - %an, %ar : %s"
```
> %h Hash de la confirmación abreviado
> %an Nombre del autor
> %ar Fecha de auditoria, relativa
> %s Asunto


