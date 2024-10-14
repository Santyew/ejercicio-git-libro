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
pro@jpexposito-VirtualBox:~/Documentos/ejercicio-git-libro$ 
```
## Paso 3
Se hace lo mismo que el paso 2 pero añadiendo el capítulo 2 y poniendo el registro

```code
cat > capitulos/capitulo2.txt
El flujo de trabajo básico con Git consiste en:
 1- Hacer cambios en el repositorio.
 2- Añadir los cambios a la zona de intercambio temporal.
 3- Hacer un commit de los cambios.
pro@jpexposito-VirtualBox:~/Documentos/ejercicio-git-libro$ git add .
pro@jpexposito-VirtualBox:~/Documentos/ejercicio-git-libro$ git commit -m "Añadido capitulo 2."
[main ffbc296] Añadido capitulo 2.
 2 files changed, 5 insertions(+), 1 deletion(-)
 create mode 100644 capitulos/capitulo2.txt
pro@jpexposito-VirtualBox:~/Documentos/ejercicio-git-libro$ git log
commit ffbc296439473acd45c69ef5c411167e3191e028 (HEAD -> main)
Author: Santyew <santiagoruiz5999@gmail.com>
Date:   Mon Oct 14 16:29:11 2024 +0100

    Añadido capitulo 2.

commit 045dd41bcc4f7e649ed1c7d4be983dd86f198100
Author: Santyew <santiagoruiz5999@gmail.com>
Date:   Mon Oct 14 16:20:20 2024 +0100

    Añadido capitulo 1.
pro@jpexposito-VirtualBox:~/Documentos/ejercicio-git-libro$ git diff HEAD~2..HEAD 
diff --git a/README.md b/README.md
index 9a06b52..e99af43 100644
--- a/README.md
+++ b/README.md
```

## Paso 4

Se crea el capitulo 3 y en este caso vamos a verificar el commit, y las diferencias de versiones entre la primera y la última versión

```code
pro@jpexposito-VirtualBox:~/Documentos/ejercicio-git-libro$ cat > capitulos/capitulo3.txt
Git permite la creación de ramas lo que permite tener distintas versiones del mismo proyecto y trabajar de manera simultanea en ellas.^C
pro@jpexposito-VirtualBox:~/Documentos/ejercicio-git-libro$ git add .
pro@jpexposito-VirtualBox:~/Documentos/ejercicio-git-libro$ git commit -m "Añadido capitulo 3."
[main 56fd18b] Añadido capitulo 3.
 2 files changed, 35 insertions(+), 1 deletion(-)
 create mode 100644 capitulos/capitulo3.txt
 ```

 ### Este es el historial del primer capitulo ###

 ```code
 pro@jpexposito-VirtualBox:~/Documentos/ejercicio-git-libro$ git diff 21ba79aa2e8e623c125e68eff45775b2cffe4649..HEAD  
diff --git a/README.md b/README.md
index 9a06b52..cefc2a8 100644
--- a/README.md
+++ b/README.md
```

### Este es el historial del capitulo 3 ###

```code
pro@jpexposito-VirtualBox:~/Documentos/ejercicio-git-libro$ git diff ffbc296439473acd45c69ef5c411167e3191e028..HEAD
diff --git a/README.md b/README.md
index e99af43..cefc2a8 100644
--- a/README.md
+++ b/README.md
@@ -40,4 +40,38 @@ git add
 git add .
 pro@jpexposito-VirtualBox:~/Documentos/ejercicio-git-libro$ 
 ## Paso 3
\ No newline at end of file
+## Paso 3
+Se hace lo mismo que el paso 2 pero añadiendo el capítulo 2 y poniendo el registro
```
## Paso 5


