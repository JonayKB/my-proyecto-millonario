<div align="justify">

# Manipulación Avanzada en Git (trabajo con tags y ramas)

## Índice
 - [README.md](#readmemd)
 - [Commit inicial](#commit-inicial)
 - [Push inicial]()
 - [Ignorar archivos]()
 - [Añadir fichero 1.txt]()
 - [Crear el tag v0.1]()
 - [Subir el tag v0.1]()
 - [Crear una rama v0.2]()
 - [Añadir fichero 2.txt]()
 - [Crear una rama remota v0.2]()
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
<details>


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

<summary><strong>Pregunta</strong></summary>

- 
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



## Ignorar archivos

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

    ```




</details>

<details>
<summary><strong>Pregunta</strong></summary>

- Respuesta:
```code

```


</details>

---

</div>
