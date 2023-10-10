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
`

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

    ```
</details>

---









</div>
