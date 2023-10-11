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
 - [Merge directo]()
 - [Merge con conflicto]()
 - [Listado de ramas]()
 - [Arreglar conflicto]()
 - [Borrar rama]()
 - [Listado de cambios]()

## README.md

```code
touch README.md
```

 <details>
 <summary><strong>Explicación</strong></summary>

```code
No es necesario la creación del READM.md ya que seleccione la opción de crearlo por defecto
```
</details>
<details>
<summary><strong>Salida</strong></summary>

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



## Añadir fichero 2.txt

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