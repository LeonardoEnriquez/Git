# GIT
## Configurando Git
### Tu identidad

```console
$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com
```
### Comprobando tu configuracion

```console
$ git config --list
$ git config user.name
```
### Obteniendo ayuda
> $ git help <verb>
> $ git <verb> --help
> $ man git-<verb>
> Por ejemplo 
  
```console
$ git help config
```
### Inicializando un repositorio
> git add, git commit

```console
$ git init
$ git add *.c
$ git add LICENSE
$ git commit -m 'initial project version'
```

### Clonando un repositorio
> git clone [url]

```console
$ git clone https://github.com/libgit2/libgit2
$ git clone https://github.com/libgit2/libgit2 mylibgit
```
