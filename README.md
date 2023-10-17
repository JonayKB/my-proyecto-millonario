<div align="justify">

# Manipulación Avanzada en Git (trabajo con tags y ramas)

## Índice
 - [README.md](#readmemd)
 - [Commit inicial](#commit-inicial)
 - [Push inicial](#push-inicial)
 - [Ignorar archivos](#ignorar-archivos)
 - [Añadir fichero 1.txt](#añadir-fichero-1txt)
 - [Crear el tag v0.1](#crear-el-tag-v01)
 - [Subir el tag v0.1](#subir-el-tag-v01)
 - [Crear una rama v0.2](#crear-una-rama-v02)
 - [Añadir fichero 2.txt](#añadir-fichero-2txt)
 - [Crear una rama remota v0.2](#crear-ramma-remota-v02)
 - [Merge directo](#merge-directo)
 - [Merge con conflicto](#merge-con-conflicto)
 - [Listado de ramas](#listado-de-ramas)
 - [Arreglar conflicto](#arreglar-conflicto)
 - [Borrar rama](#borrar-rama)
 - [Listado de cambios](#listado-de-cambios)

## README.md

```code
touch README.md
```

 <details>
 <summary><strong>Explicación</strong></summary>

- touch README.md
```code
No es necesario la creación del README.md ya que seleccione la opción de crearlo por defecto
```
</details>
<details>
<summary><strong>Salida</strong></summary>

- touch README.md
```code

```
</details>


---



## Commit inicial

```code
git add .
git commit -m "commit inicial"
```
 <details>
 <summary><strong>Explicación</strong></summary>

- git add .

    ```code
    Añade los ficheros 
    ```

- git commit -m "commit inicial"

    ```code
    Creamos un commit con el nombre de commit inicial
    ```

</details>

<details>
<summary><strong>Salida</strong></summary>

- git add .
    ```code

    ```
- git commit -m "commit inicial"
    ```code
    [main 3cea8f5] commit inicial
    1 file changed, 93 insertions(+), 1 deletion(-)
    rewrite README.md (100%)
    ```

</details>

---



## Push inicial

```code
git push origin master
```
 <details>
 <summary><strong>Explicación</strong></summary>

- git push origin master

    ```code
    El push realiza una subida de los ficheros al repositorio, en la rama master, estos dos últimos argumentos lo podemos ignorar y los subira en la rama que estemos asignado 
    ```
    >WARNING: Si ignoramos el argumento en el push de "master" y estamos en otra rama, la subiremos a esa, pudiendo ocasionar equivocaciones


</details>

<details>
<summary><strong>Salida</strong></summary>

- git push origin main
    ```code
        Enumerando objetos: 5, listo.
    Contando objetos: 100% (5/5), listo.
    Compresión delta usando hasta 4 hilos
    Comprimiendo objetos: 100% (2/2), listo.
    Escribiendo objetos: 100% (3/3), 747 bytes | 747.00 KiB/s, listo.
    Total 3 (delta 0), reusados 0 (delta 0), pack-reusados 0
    To https://github.com/JonayKB/my-proyecto-millonario.git
    aaaff10..3cea8f5  main -> main

    ```


</details>

---


## Ignorar archivos

```code
touch privado.txt
mkdir privada
echo "privado.txt" >> .gitignore
echo "/privada" >> .gitignore
git add .
git commit -m "añadido fichero .gitignore"
```
 <details>
 <summary><strong>Explicación</strong></summary>

- touch privado.txt

    ```code
    Crea un archivo llamado privado.txt
    ```
- mkdir privada

    ```code
    Crea una carpeta llamada privada
    ```

- echo "privada.txt"/"/privada" >> .gitingnore

    ```code
    Añade el contenido de la carpeta y el archivo privado.txt a un archivo nuevo llamado .gitignore
    ```

</details>

<details>
<summary><strong>Salida</strong></summary>

- touch privado.txt

    ```code

    ```
- mkdir privada

    ```code

    ```

- echo "privada.txt"/"/privada" >> .gitingnore

    ```code
    
    ```

- git commit -m "añadido fichero .gitignore"

    ```code
        [main 9ebd13a] añadido fichero .gitignore
    2 files changed, 112 insertions(+), 1 deletion(-)
    create mode 100644 .gitignore
    ```
</details>
 <details>

 <summary><strong>Pregunta</strong></summary>
 
```code
Un fichero o directorio añadido a .gitignore sera ignorado por git al subirlo al repositorio
```

</details>


---


## Push inicial

```code
git push origin master
```
 <details>
 <summary><strong>Explicación</strong></summary>

- git push origin master

    ```code
    Envia los archivos añadidos al repositiorio de la nube
    ```

</details>

<details>
<summary><strong>Salida</strong></summary>

- git push origin main
    ```code
        Enumerating objects: 6, done.
    Counting objects: 100% (6/6), done.
    Delta compression using up to 16 threads
    Compressing objects: 100% (3/3), done.
    Writing objects: 100% (4/4), 475 bytes | 475.00 KiB/s, done.
    Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
    remote: Resolving deltas: 100% (1/1), completed with 1 local object.
    To https://github.com/JonayKB/my-proyecto-millonario
    3cea8f5..e09d1a5  main -> main
    ```


</details>

<details>
<summary><strong>Pregunta</strong></summary>

- Respuesta:
    ```code
    Esos dos argumentos el origin indica que es la nube, y el master es la rama, pero estos son opcionales
    ```

>WARNING: Sino ponemos estos argumentos, puede ocurrir el error de estar en la rama equivocada y subir los archivos a donde no debemos
</details>

---




## Ignorar archivos

```code
touch privado.txt
mkdir privada
echo "privado.txt" >> .gitignore
echo "/privada" >> .gitignore
git add .
git commit -m "añadido fichero .gitignore"
```
 <details>
 <summary><strong>Explicación</strong></summary>

- touch privado.txt

    ```code
    Crea un archivo llamado privado.txt
    ```

- mdkir privada

    ```code
    Crea una carpeta llamada privada
    ```
    
- echo "privado.txt" / "/privada" >> .gitignore

    ```code
    Añade "privado.txt" y "/privada" o crea un archivo llamado .gitignore y los añade 
    ```


</details>

<details>
<summary><strong>Salida</strong></summary>

- touch privado.txt

    ```code
    
    ```

- mdkir privada

    ```code
    
    ```
    
- echo "privado.txt" / "/privada" >> .gitignore

    ```code
     
    ```


</details>

<details>
<summary><strong>Pregunta</strong></summary>

- Respuesta:
    ```code
    El .gitignore indica los archivos que no hay que subir, por ende ni la carpeta ni el archivo seran subidos
    ```


</details>

---



## Añadir fichero 1.txt

```code
touch 1.txt
git add .
git commit -m "añadido 1.txt"
```
 <details>
 <summary><strong>Explicación</strong></summary>

- touch 1.txt

    ```code
    Crea un archivo llamado 1.txt
    ```

- git add .

    ```code
    Añade los ficheros de los que hacer commit
    ```

- git commit -m "añadido 1.txt"

    ```code
    Crea un puntero llamado "añadido 1.txt" en local
    ```



</details>

<details>
<summary><strong>Salida</strong></summary>

- touch 1.txt

    ```code

    ```

- git add .

    ```code

    ```

- git commit -m "añadido 1.txt"

    ```code
        [main 9b7df7b] añadido 1.txt
    2 files changed, 160 insertions(+), 5 deletions(-)
    create mode 100644 1.txt
    ```




</details>

<details>
<summary><strong>Pregunta</strong></summary>

- Respuesta:
    ```code
    El git add . añade los archivos al próximo commit, y el commit crea un marcador en locar, que despues se puede subir con un push
    ```


</details>

---



## Crear el tag v0.1

```code
git tag v0.1
```
 <details>
 <summary><strong>Explicación</strong></summary>

- git tag v0.1

    ```code
    Crea un tag llamado v0.1
    ```





</details>

<details>
<summary><strong>Salida</strong></summary>

- git tag v0.1

    ```code

    ```






</details>


---



## Subir el tag v0.1

```code
git push --tag origin master
```
 <details>
 <summary><strong>Explicación</strong></summary>

- git push --tag origin master

    ```code
    Envia la información de la versiñon a un tag
    ```

</details>

<details>
<summary><strong>Salida</strong></summary>

- git push --tag origin main

    ```code
        Enumerating objects: 6, done.
    Counting objects: 100% (6/6), done.
    Delta compression using up to 16 threads
    Compressing objects: 100% (3/3), done.
    Writing objects: 100% (4/4), 1.52 KiB | 1.52 MiB/s, done.
    Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
    To https://github.com/JonayKB/my-proyecto-millonario
    e09d1a5..9b7df7b  main -> main
    * [new tag]         v0.1 -> v0.1
    ```






</details>

<details>
<summary><strong>Pregunta</strong></summary>

- Respuesta:
    ```code
    Los tags son versiones estables guardadas, es como una rama que solo guarda los punteros, no todos los archivos en si
    ```


</details>

---


## Crear una rama v0.2

```code
git branch v0.2
git checkout v0.2
```
 <details>
 <summary><strong>Explicación</strong></summary>

- git branch v0.2

    ```code
    Crea una rama llamada v0.2
    ```

- git checkout v0.2

    ```code
    Te posiciona en la rama v0.2
    ```

</details>

<details>
<summary><strong>Salida</strong></summary>

- git branch v0.2

    ```code

    ```

- git checkout v0.2

    ```code
    Switched to branch 'v0.2'
    M       README.md
    ```

</details>

---

## Añadir fichero 2.txt

```code
touch 2.txt
git add .
git commit -m "añadido 2.txt"
```
 <details>
 <summary><strong>Explicación</strong></summary>

- touch 2.txt

    ```code
    Crea un fichero llamado 2.txt
    ```

- git add .

    ```code
    Añade los ficheros al siguiente commit
    ```

- git commit -m "añadido 2.txt"

    ```code
    Creamos una marca llamada "añadido 2.txt"
    ```

</details>

<details>
<summary><strong>Salida</strong></summary>

- touch 2.txt

    ```code
    
    ```

- git add .

    ```code

    ```

- git commit -m "añadido 2.txt"

    ```code
        [v0.2 19f966a] añadido 2.txt
    2 files changed, 225 insertions(+), 20 deletions(-)
    create mode 100644 2.txt
    ```






</details>

<details>
<summary><strong>Pregunta</strong></summary>

- Respuesta:
    ```code
    El fin del uso de ramas es el trabajo conjunto en distintas ramas, para que los trabajadores no se molesten entre ellos, ademas de mantener en la rama main una versión estable
    ```


</details>

---



</div>




## Crear ramma remota v0.2

```code
git push origin v0.2
```
 <details>
 <summary><strong>Explicación</strong></summary>

- git push origin v0.2

    ```code
    Sube la información a la rama v0.2
    ```



</details>

<details>
<summary><strong>Salida</strong></summary>

- git push origin v0.2

    ```code
        [v0.2 19f966a] añadido 2.txt
    2 files changed, 225 insertions(+), 20 deletions(-)
    create mode 100644 2.txt
    PS B:\Repositorios Clase\my-proyecto-millonario> git push origin v0.2
    Enumerating objects: 5, done.
    Counting objects: 100% (5/5), done.
    Delta compression using up to 16 threads
    Compressing objects: 100% (3/3), done.
    Writing objects: 100% (3/3), 1.24 KiB | 1.24 MiB/s, done.
    Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
    remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
    remote:
    remote: Create a pull request for 'v0.2' on GitHub by visiting:
    remote:      https://github.com/JonayKB/my-proyecto-millonario/pull/new/v0.2
    remote:
    To https://github.com/JonayKB/my-proyecto-millonario
    * [new branch]      v0.2 -> v0.2
    ```


</details>

---



## Merge directo

```code
git checkout master
git merge v0.2 -m "merge v0.2 sin conflictos"
```
 <details>
 <summary><strong>Explicación</strong></summary>

- git checkout master

    ```code
    Nos posicionamos en la rama master
    ```

- git merge v0.2 -m "merge v0.2 sin conflictos"

    ```code
    Unimos la rama v0.2 a la rama main
    ```



</details>

<details>
<summary><strong>Salida</strong></summary>

- git checkout master

    ```code
    
    ```

- git merge v0.2 -m "merge v0.2 sin conflictos"

    ```code

    ```


</details>

<details>
<summary><strong>Pregunta</strong></summary>

- Respuesta:
    ```code
    No deben surgir conflictos, ya que el archivo que se ha creado no existe en la rama principal, en caso de haberse modificado uno de los archivos ya creados si lo existira (En este caso si lo hay por el README, pero en lo explicado no debería de suceder)
    ```


</details>

---



## Merge con conflicto

```code
git checkout master
echo "Hola" >> 1.txt
git add .
git commit -m "hola en 1.txt"

git checkout v0.2
echo "Adios" >> 1.txt
git add .
git commit -m "adios en 1.txt"

git checkout master
git merge v0.2
vim 1.txt
git add .
git commit -m "arreglado merge en 1.txt"
```
 <details>
 <summary><strong>Explicación</strong></summary>

- git commit -m "hola en 1.txt"

    ```code
    Despues de haber modificado la información de 1.txt y añadirla, hacemos un commit a la rama main
    ```

- git commit -m "adios en 1.txt"

    ```code
    Despues de haber modificado la información de 1.txt y añadirla, hacemos un commit a la rama v0.2
    ```

- git commit -m "arreglado merge en 1.txt"

    ```code
    Despues de haber modificado la información de 1.txt y añadirla, realizamos un merge  y realizamos un commit (Creara un error y tendremos que resolverlo eligiendo con que quedarnos, si la versión actual, la entrante o una combinación)
    ```

</details>

<details>
<summary><strong>Salida</strong></summary>

- git commit -m "hola en 1.txt"

    ```code
        [main 95051ed] hola en 1.txt
    2 files changed, 77 insertions(+), 4 deletions(-)
    ```

- git commit -m "adios en 1.txt"

    ```code
    [v0.2 580fe21] adios en 1.txt
    1 file changed, 1 insertion(+)
    ```

- git merge v0.2

    ```code
    Auto-merging 1.txt
    CONFLICT (content): Merge conflict in 1.txt
    Automatic merge failed; fix conflicts and then commit the result.
    ```

- git commit -m "arreglado merge en 1.txt"

    ```code
    error: Committing is not possible because you have unmerged files.
    hint: Fix them up in the work tree, and then use 'git add/rm <file>'
    hint: as appropriate to mark resolution and make a commit.
    fatal: Exiting because of an unresolved conflict.
    U       1.txt
    ```

</details>

---

## Listado de ramas

```code
git branch --merged
git branch --no-merged
```
 <details>
 <summary><strong>Explicación</strong></summary>

- git branch --merged

    ```code
    Nos enseña las ramas que estan unidas a la rama main
    ```

- git branch --no-merged

    ```code
    Nos enseña las ramas que NO estan unidas a la rama main
    ```


</details>

<details>
<summary><strong>Salida</strong></summary>

- git branch --merged

    ```code
    * main
    ```

- git branch --no-merged

    ```code
      v0.2
    ```

</details>

---

## Arreglar conflicto

```code
vim 1.txt
git add .
git commit -m "arreglado merge en 1.txt"
```
 <details>
 <summary><strong>Explicación</strong></summary>

- git commit -m "arreglado merge en 1.txt"

    ```code
    Después de arreglar el conflicto modificando el archivo y añadir los ficheros realizamos un commit
    ```


</details>

<details>
<summary><strong>Salida</strong></summary>

- git commit -m "arreglado merge en 1.txt"

    ```code
    [main af6ce90] arreglado merge en 1.txt
    ```


</details>

---

## Borrar rama

```code
git tag v0.2
git branch -D v0.2
```
 <details>
 <summary><strong>Explicación</strong></summary>

- git tag v0.2

    ```code
    Crea una rama llamada v0.2
    ```

- git branch -D v0.2

    ```code
    Borra la rama llamada v0.2
    ```

</details>

<details>
<summary><strong>Salida</strong></summary>

- git tag v0.2

    ```code
    
    ```

- git branch -D v0.2

    ```code
    Deleted branch v0.2 (was 580fe21).
    ```

</details>

---


## Listado de cambios

```code
git config --global alias.list 'log --oneline --decorate --graph --all'
git list
```
 <details>
 <summary><strong>Explicación</strong></summary>

- git config --global alias.list 'log --oneline --decorate --graph --all'

    ```code
    Crea una "función" que al llamarla ejecuta "log --oneline --decorate --graph --all" 
    ```

- git list

    ```code
    Enseña git config --global alias.list 'log --oneline --decorate --graph --all'
    ```


</details>

<details>
<summary><strong>Salida</strong></summary>

- git config --global alias.list 'log --oneline --decorate --graph --all'

    ```code

    ```

- git list

    ```code
    *   af6ce90 (HEAD -> main, tag: v0.2) arreglado merge en 1.txt
    |\
    | * 580fe21 adios en 1.txt
    * | 7f8904b hola en 1.txt
    * | 95051ed hola en 1.txt
    |/
    * 19f966a (origin/v0.2) añadido 2.txt
    * 9b7df7b (tag: v0.1, origin/main, origin/HEAD) añadido 1.txt
    * e09d1a5 commit inicial
    * 3cea8f5 commit inicial
    * aaaff10 Initial commit
    ```

</details>

---

# Manipulación avanzados de Git, GitHub y Markdown



## Crear una rama v0.2

```code
git branch v0.2
```
 <details>
 <summary><strong>Explicación</strong></summary>

- git branch v0.2

    ```code
    Crea una rama llamada v0.2 
    ```

</details>

<details>
<summary><strong>Salida</strong></summary>

- git branch v0.2

    ```code

    ```


</details>

---


## Añadir fichero 2.txt

```code
touch 2.txt
```
 <details>
 <summary><strong>Explicación</strong></summary>

- touch 2.txt

    ```code
    Crea un archivo llamado 2.txt
    ```

</details>

<details>
<summary><strong>Salida</strong></summary>

- touch 2.txt

    ```code

    ```


</details>

---



## Crear rama remota v0.2

```code
git add .
git commit -m "Creacion de la rama remota v0.2"
git push origin v0.2
```
 <details>
 <summary><strong>Explicación</strong></summary>

- git add .

    ```code
    Añade todos los ficheros a la siguiente subida
    ```

- git commit -m "Creacion de la rama remota v0.2"

    ```code
    Creamos un puntero llamado "Creación de la rama remota v0.2"
    ```

- git push origin v0.2

    ```code
    Crea una rama remota llamada v0.2 y la envia a la nube
    ```

</details>

<details>
<summary><strong>Salida</strong></summary>

- git commit -m "Creacion de la rama remota v0.2"

    ```code
    git commit -m "Creacion de la rama remota v0.2"
    ```

- git push origin v0.2

    ```code

    ```


</details>

---



## Merge directo

```code
git checkout main
git merge v0.2 -m "Merge directo"
```
 <details>
 <summary><strong>Explicación</strong></summary>

- git checkout main

    ```code
    Nos mueve a la rama main
    ```

- git merge v0.2 -m "Merge directo"

    ```code
    Une la rama v0.2 a la main
    ```


</details>

<details>
<summary><strong>Salida</strong></summary>

- git checkout main

    ```code
        Cambiado a rama 'main'
    Tu rama está adelantada a 'origin/main' por 1 commit.
    (usa "git push" para publicar tus commits locales)
    ```

- git merge v0.2 -m "Merge directo"

    ```code
    Une la rama v0.2 a la main
    ```



</details>

---

</div>