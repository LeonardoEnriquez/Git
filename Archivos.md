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
$ git push https://github.com/LeonardoEnriquez/Git_Tutorial.git --all
```

## Eliminar archivos de tu directorio de trabajo
```
$ rm PROJECTS.md
$ git status
```

## Eliminar archivos de tu directorio de trabajo
```
$ git rm PROJECT.mdgit
$ git status
```

## Cambiar el nombre de Archivos
```
$ git mv README.md README
$ git status
```

## Actualiza y fusiona
> Para actualizar tu repositorio local al commit mas nuevo 
> git pull opciones...
```
$ git pull origin develop
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