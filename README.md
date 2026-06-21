# Apuntes de Git y GitHub

Repositorio con apuntes, prácticas y comandos vistos durante las clases de Git, GitHub y control de versiones.

---

# Índice

* Clase 1 - Git Bash y creación de directorios
* Clase 2 - Archivos, historial y primer repositorio Git
* Clase 4 - Análisis de cambios y commits
* Clase 5 - Git Ignore, Merge, Tag y Stash
* Clase 6
* Clase 7
* Clase 8 - Clone, Push, Fetch y Pull
* Clase 9 - Claves SSH

---

# Clase 1 - Git Bash y creación de directorios

## Lo que vimos en la clase anterior

```bash
pwd
cd
cd /
cd ~
ls
ls -al
ls -l
ls -a
clear
cd ..
cd U + tab
cd /D
df -h
cd /mnt/d
```

## Creación de carpetas

```bash
cd ..
cd ..
cd /mnt/c

cd ~

mkdir Tecnicatura

cd tecnicatura

mkdir Python
mkdir Java
mkdir JavaScript
```

### Notas

* Revisar y ejecutar cada comando.
* Realizar las prácticas indicadas durante la clase.

**Profesor:** Ariel Betancud

---

# Clase 2 - Archivos, historial y primer repositorio Git

## Comandos básicos

```bash
touch vacio.txt
cat vacio.txt
history
!72
history -c
rm vacio.txt
rm --help
```

### Referencias

```text
./   -> Carpeta actual
../  -> Carpeta anterior
```

## Crear un repositorio Git y realizar el primer commit

```bash
cd tecnicatura

mkdir class-git

cd class-git

git init

code .

git status

git add historia.txt

git status

git rm --cached historia.txt

git config

git config --list

git config --list --show-origin
```

## Configuración de Git

```bash
git config --global user.name "Ariel Betancud"

git config --global user.email "betancudariel@gmail.com"

git config --list
```

## Primer commit

```bash
git add .

git commit -m "Mensaje importante del commit"
```

## Segundo commit

```bash
code .

git status

git add .

git commit -m "Mi segundo commit"
```

## Historial

```bash
git log historia.txt
```

---

# Clase 4 - Análisis de cambios y commits

## Preparación

```bash
cd tecnicatura

cd class-git

ls

touch historia.txt

code .
```

## Confirmar cambios

```bash
git status

git add .

git status

git commit
```

## Salir de Vim

```bash
Esc

:wq!
```

o

```bash
Esc + Shift + Z + Z
```

## Ver cambios realizados

```bash
git show

git log historia.txt
```

## Comparar commits

```bash
git diff hash_commit_viejo hash_commit_nuevo
```

---

# Clase 5 - Git Ignore, Merge, Tag y Stash

## git ignore

Permite ignorar archivos pasados como argumentos.

```bash
git ignore archivo.py
```

## git merge

Fusiona dos ramas.

```bash
git switch main

git merge auxiliar
```

### Opciones

```bash
git merge --continue
git merge --abort
```

## git tag

Crear etiquetas.

```bash
git tag v1.0 hash_commit
```

### Opciones

```bash
git tag -a v1.0 -m "mensaje"

git tag -d version_2.4
```

## git show

```bash
git show
```

## git stash

Guardar cambios temporales.

```bash
git stash
```

### Opciones

```bash
git stash pop

git stash push -m "mensaje"

git stash -u

git stash list

git stash apply stash@{n}

git stash drop stash@{n}

git stash clear
```

---

# Clase 6

Nada nuevo.

---

# Clase 7

Nada nuevo.

---

# Clase 8 - Repositorios remotos

## git clone

```bash
git clone <url-del-repo>
```

## git push

```bash
git push

git push -u origin <rama>
```

### Opciones

```bash
git push --all

git push --tags

git push -f

git push --force-with-lease

git push origin --delete <rama>
```

## git fetch

```bash
git fetch origin
```

### Opciones

```bash
git fetch origin -p
```

## git pull

```bash
git pull

git pull origin <rama>
```

## git shortlog

```bash
git shortlog
```

---

# Clase 9 - Claves SSH

## Generar una clave SSH

```bash
ssh-keygen -t ed25519 -C "<email>"
```

### Opciones

```bash
-t <algoritmo>

-C <email>

-b <bits>
```

---

# Autor

Tato

# Profesor

Ariel Betancud
