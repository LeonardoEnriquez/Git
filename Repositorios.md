#  Git para **windows**

![GIT](https://git-scm.com/images/logo@2x.png)

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
$ git status
$ git diff
$ git diff -staged
$ git diff -cached
```

## Conectando un repositorio local a uno remoto
> Reemplazar origin master por la rama a la que quiere enviar tus cambios
```
$ git remote add origin <server>
```

## Configurar proxy
```
$ git config --global -l
$ git config --global --unset http.proxy
$ git config --global -l
```

## Eliminar la configuracion de proxy
```
$ git config --global http.proxy 10.12.1.163:3128
```


## Obtener actualizacion de archivos
```
$ git pull https://github.com/LeonardoEnriquez/Git_Tutorial.git
```
## fusionar todos los cambios que se han hecho en el repositorio local trabajando
```
$git checkout sesion-8
$git branch
$git checkout master
$git pull origin sesion-8
```


