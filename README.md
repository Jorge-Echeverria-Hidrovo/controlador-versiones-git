# Tarea 1

## Controlador-versiones-git

Tarea 1 de la materia de controladores de versiones de la Maestría en Diseño Web y Desarrollo de Apps

---

### Git

---

Es un controlador de versiones que registra los cambios que se realizan a un conjunto de archivos en una línea de tiempo llamada master o main, en el desarrollo de un proyecto y se almacenan en un repositorio.

* Repositorio: un contenedor de almacenamiento de archivos.
* Repositorio local: los que se crean en la computadora local
* Repositorio remoto: los que se crean en la web (git/hub)
* Master o Main: línea de tiempo principal
* HEAD`se refiere al commit en el que está tu repositorio posicionado en cada momento. Es un puntero que señala el lugar donde estamos.`

$ git log
commit d96b53834879fdc8bb13e50508d728b6b49b4e62 (HEAD -> main, origin/main, origin/HEAD)
Author: Jorge Echeverria <jorge_echeverria_mdw@espam.edu.ec>
Date:   Sun Oct 22 17:39:04 2023 -0500

```
Agrega archivo prueba1
```

commit f919d532bd0068abced7cf7a22b5f82bd12991eb
Author: Jorge-Echeverria-Hidrovo <148644315+Jorge-Echeverria-Hidrovo@users.noreply.github.com>
Date:   Sun Oct 22 10:15:37 2023 -0500

```
Initial commit

```

---

#### **Instalación de Git**

---

1. Descargar el archivo instalador desde la URL: https://git-scm.com/download/
2. Instalar (Git) en el equipo local
3. Abrir un terminal (CMD, Git Bash)
4. Verificamos la instalación

   * **git** --version
     * `git version 2.42.0.windows.2`
5. Crear una carpeta (repositorio local) de manera manual o a traves del terminal

   * **mkdir** (crea la carpeta "repositorio")
     * `$ mkdir mi-primer.repo`
   * **cd** (te ubica en el directorio "repositorio local")
     * `ASUS@DESKTOP-CDA5FCM MINGW64 ~/mi-primer-repo (main)$ cd mi-primer.repo`
6. Configurar el usuario

   * git config --global user.name$ git config --global user.name "Jorge Echeverria"
   * git config --global user.email$ git config --global user.email "jorge_echeverria_mdw@espam.edu.ec"
7. Damos inicio a Git

   * git init
   * `Initialized empty Git repository in /Users/ASUS/mi-primer-repo/.git/`

---

#### Comandos

---

ls `enumera los archivos en el directorio`

---

git status `verifica el estado actual del lugar donde estamos en la línea de trabajo(ubicación, branch, archivos modificados o no)`

* *$ git status
  On branch main
  Your branch is up to date with 'origin/main'.*
* $ git status
  On branch main
  Your branch is up to date with 'origin/main'.

Changes not staged for commit:
(use "git add `<file>`..." to update what will be committed)
(use "git restore `<file>`..." to discard changes in working directory)
modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

---

git log `muestra el historial de los cambios realizados (commit)`

commit 69ddaeb9f7b164385bd5f27906885c7cf80082c4 (HEAD -> main, origin/main)

Author: Jorge-Echeverria-Hidrovo <148644315+Jorge-Echeverria-Hidrovo@users.noreply.github.com>
Date:   Sun Oct 22 09:56:47 2023 -0500

```
agregar-archivo2
```

commit 6bf524543f749a830dcdaab8082749c35ae53ccd
Merge: f7bd6df 7650bb2
Author: Jorge-Echeverria-Hidrovo <148644315+Jorge-Echeverria-Hidrovo@users.noreply.github.com>
Date:   Sun Oct 22 09:31:56 2023 -0500

```
Merge branch 'main' of https://github.com/Jorge-Echeverria-Hidrovo/Mi-Proyecto-Git
```

commit f7bd6dfe8ba6052dfc947e2f7920bd7534db245d
Author: Jorge-Echeverria-Hidrovo <148644315+Jorge-Echeverria-Hidrovo@users.noreply.github.com>
Date:   Sun Oct 22 09:24:35 2023 -0500

---

git add `agrega el o los archivos que hemos trabajado para que se reseñe los cambios en el repositorio.`

$ git add `Prueba1`

---

git commit -m `"Agregando título para el trabajo": crea una confirmación de la reseña en el repositorio de los cambios que realicemos a o los archivo.`

###### $ git commit -m "Agrega archivo prueba1"

[main d96b538] Agrega archivo prueba1
2 files changed, 9 insertions(+), 2 deletions(-)
create mode 100644 Prueba1

---

git tag `es una etiqueta que permite mostrar la version del proyecto (trabajo realizado).`

ASUS@DESKTOP-CDA5FCM MINGW64 ~/Mi-primer-repo ((558debe...))

$ git tag 0.0.1

ASUS@DESKTOP-CDA5FCM MINGW64 ~/Mi-primer-repo ((0.0.1))

---

branch: rama; es una línea de tiempo del trabajo de un proyecto la cual nos permite regresar a éste estado si se es necesario.

git branch nombre-branch `crea una rama de trabajo`

git branch -m `cambia-nombre-branch`

git branch -d nombre-branch `elimina un branch`

ASUS@DESKTOP-CDA5FCM MINGW64 ~/Mi-primer-repo ((0.0.1))
$ git branch

* (HEAD detached at 558debe)
  main

---

git checkout `es el comando utilizado para verificar un branch y pasarnos del actual a otro que especificamos al final del comando o a un commit.`

ASUS@DESKTOP-CDA5FCM MINGW64 ~/Mi-primer-repo ((0.0.1))
$ git checkout main
Previous HEAD position was 558debe cambios-prueba1
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 1 commit.
(use "git push" to publish your local commits)

ASUS@DESKTOP-CDA5FCM MINGW64 ~/Mi-primer-repo (main)
$ git checkout 558debe6edc40abbeda027f7fdb1fb39943eca5c
Note: switching to '558debe6edc40abbeda027f7fdb1fb39943eca5c'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

git switch -c `<new-branch-name>`

Or undo this operation with:

git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 558debe cambios-prueba1

git checkout -b `se creará una nueva rama y se posicionará en ella.`

$ git branch rama1

ASUS@DESKTOP-CDA5FCM MINGW64 ~/Mi-primer-repo (main)

$ git checkout rama1
Switched to branch 'rama1'

ASUS@DESKTOP-CDA5FCM MINGW64 ~/Mi-primer-repo (rama1)

---

$ git push `actualiza el repositorio remoto con los archivos de trabajo del repositorio local.`
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 438 bytes | 438.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/Jorge-Echeverria-Hidrovo/controlador-versiones-git.git
f919d53..d96b538  main -> main

---

.gitignore `es un archivo donde se almacenan datos (tipos de archivos) que no deseamos visualisar. No se sube al repositorio.`

secrets.yml `iarchivos que se desea mantener su información en secreto /no se sube al repositorio.`

---

git diff master nombre-branch `muestra los archivos que se trabajaron en el branch; es decir, compara entre el main o master y el branch los archivos que se trabajaron que contienen`

git diff `muestra el archivo modificado`

---

git reset --hard `regresa al cambio anterior`

---

git push -u origin `para llevar a git-hub desde local al repositorio remoto nuestro trabajo`

$ git push
Everything up-to-date

---

git pull `para lo inverso; traer desde git-hub a local los cambios realizados.`

---

diff --git ruta o nombre del archivo.html `mostrará los cambios realizados`

---

git merge nombre-branch master `pasa todos los archivos de un branch al master`

---

git remote add origin "url-del-repositorio-remoto"

---

git --list `muestra la configuraciones que he realizado`

---

.gitignore `es un archivo que nos permite oculatar ciertos arhivos que queremos que sean visibles.`

---

git revert `revierte el cambio`

---

hooks `script que se va ejecutar con el lanzamiento de alguna acción`

---

-------------------------

git merge

add y commit

staggin  -  commit

clonar

colaborador

forkear
