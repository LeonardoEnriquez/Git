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
## Conectando un repositorio local a uno remoto
> Reemplazar origin master por la rama a la que quiere enviar tus cambios
```
$ git remote add origin <server>
```
## Cambio de repositorio remoto URL
```console
$ git remote set-url origin https://hostname/USERNAME/REPOSITORY.git
```
## Clonando un repositorio
git clone -b <branch> <remote_repo>
```
$ git clone https://github.com/libgit2/libgit2
$ git clone https://github.com/libgit2/libgit2 mylibgit
```
### Clonando una rama especifica de un repositorio
```
$ git clone -b Develop git@github.com:user/myproject.git 
```
## Eliminando un remote
### Ver los remotos actuales:
```
$ git remote -v
```
> origin  https://github.com/OWNER/REPOSITORY.git (fetch)  
> origin  https://github.com/OWNER/REPOSITORY.git (push)
> destination  https://github.com/FORKER/REPOSITORY.git (fetch)
> destination  https://github.com/FORKER/REPOSITORY.git (push)
```
$ git remote rm destination
```

## Diferencias entre ramas
```
$ git status
$ git diff master..Develop
```

## Eliminar proxy
```
$ git config --global -l
$ git config --global --unset http.proxy
```

## Colocar la configuracion de proxy
```
$ git config --global -l
$ git config --global http.proxy xx.xx.1.163:3128
```



