# GIT
##  Instalación de Git para **windows**

![GIT](https://git-scm.com/images/logo@2x.png)

Git es un sistema de control de versiones libre y codigo abierto diseñado para pequeños y grandes proyectos. Git tiene tres estados principales en los que se puede encontrar tus archivos: confirmado (committed), modificado (modified(, y preparado (staged).
- **Confirmado:** Significa que los datos estan almacenados de manera segura en tu base de datos local.
- **Modificado:** significa que has modificado el archivo pero todavia no lo has confirmado a tu base de datos.
- **Preparado:** Significa que has 

![GIT_Estados](https://git-scm.herokuapp.com/book/en/v2/images/areas.png)


### A continuación se muestran algunos enlaces de interés
### Sitio Oficial 
>- Git-SCM: [Sitio oficial de GIT](https://git-scm.herokuapp.com/book/es/v2)
>
### Tutorial y documentacion
>- Git-Book: [Sitio oficial de GIT](https://git-scm.com/)
>
>- Video Tutorial: [Como Instalar Git](https://www.youtube.com/watch?v=1PiYqxog8mc&list=PLTd5ehIj0goMCnj6V5NdzSIHBgrIXckGU&index=2)
>- Video Tutorial Fazt: [Como utilizar Git](https://www.youtube.com/watch?v=HiXLkL42tMU)

>
### Instalacion en Windows
>- Instalacion: [Download git-scm](https://git-scm.com/download/win)
>
### Interface visual 
>- Interface visual para Usuario: [GitHub Desktop](https://desktop.github.com/)
>
>- Comando para uso en terminal: [Git Cheat Sheet:](https://education.github.com/git-cheat-sheet-education.pdf)
>
### Interface por comandos
#### Ejemplo de la terminal Gitbash
>![Terminal Gitbash ](https://rm-rf.es/wp-content/uploads/2019/04/git_bash_windows.png)


## Configurando Git
### Tu identidad

```console
$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com
```

### Inicializando un repositorio
```console
$ git init
$ git add *.c
$ git add LICENSE
$ git commit -m 'initial project version'
```
### Clonando un repositorio
```console
$ git clone https://github.com/libgit2/libgit2
$ git clone https://github.com/libgit2/libgit2 mylibgit
```
