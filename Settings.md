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
> $ git help <verb>
> $ git <verb> --help
> $ man git-<verb>
> Por ejemplo
```  
$ git help config

### Inicializando un repositorio
> git init

```
$ git init
```

### Agregando archivos a un repositorio

> git add <nombre_archivo>
```
$ git add *.c
$ git add LICENSE
```

### Ver el estado de nuestro archivos

```
$ git status
```

### Subir archivos del stage al repositorio

```
$ git commit -m 'initial project version'
```

### Clonando un repositorio

> git clone [url]

```
$ git clone https://github.com/libgit2/libgit2
$ git clone https://github.com/libgit2/libgit2 mylibgit
```