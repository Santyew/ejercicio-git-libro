# ejercicio-git-libro
<git align = "justify">

## Paso 1
Lo primero será crear un repositorio con archivo README.md llamado  *ejercicio-git-libro* y ejecutamos su **git clone**, un **cd** para volverlo principal y por último un **ls -al**

```code
pro@jpexposito-VirtualBox:~/Documentos$ git clone https://github.com/Santyew/ejercicio-git-libro
Clonando en 'ejercicio-git-libro'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Recibiendo objetos: 100% (3/3), listo.
pro@jpexposito-VirtualBox:~/Documentos$ cd ejercicio-git-libro
pro@jpexposito-VirtualBox:~/Documentos/ejercicio-git-libro$ ls la
ls: no se puede acceder a 'la': No existe el archivo o el directorio
pro@jpexposito-VirtualBox:~/Documentos/ejercicio-git-libro$ ls -la
total 16
drwxrwxr-x 3 pro pro 4096 oct 14 15:44 .
drwxr-xr-x 5 pro pro 4096 oct 14 15:44 ..
drwxrwxr-x 8 pro pro 4096 oct 14 15:44 .git
-rw-rw-r-- 1 pro pro   21 oct 14 15:44 README.md
```

## Paso 2

En la terminal de la Visual Studio hacemos **git log**, luego un **mkdir** llamado **capitulos y añadir cat > capitulos/capitulo1.txt** para añadir un texto a un glosario se añade el texto y para salir *Control C*.

```code
pro@jpexposito-VirtualBox:~/Documentos/ejercicio-git-libro$ git log
commit 21ba79aa2e8e623c125e68eff45775b2cffe4649 (HEAD -> main, origin/main, origin/HEAD)
Author: Santyew <134631502+Santyew@users.noreply.github.com>
Date:   Mon Oct 14 15:42:05 2024 +0100

    Initial commit
pro@jpexposito-VirtualBox:~/Documentos/ejercicio-git-libro$ mkdir capitulos
pro@jpexposito-VirtualBox:~/Documentos/ejercicio-git-libro$ cat > capitulos/capitulo1.txt
Git es un sistema de control de versiones ideado por Linus Torvalds.
git add
git add .
^C
pro@jpexposito-VirtualBox:~/Documentos/ejercicio-git-libro$ 
```
