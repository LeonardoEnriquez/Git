#  Git para **windows**

![GIT](https://git-scm.com/images/logo@2x.png)

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

## Confirmar cambios
```
$ git commit
```

## Envio de cambios 
> Reemplazar origin master por la rama a la que quiere enviar tus cambios
> git push origin master
```
$ git push origin master
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