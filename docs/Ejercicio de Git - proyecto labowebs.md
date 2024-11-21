# Ejercicio de Git - proyecto labowebs 

[TOC]

> Módulo: Despliegue de Aplicaciones
>
> Alumno: Iker Pérez Cortina



## Trabajo en local

### Cuestiones

1. Inicializa un nuevo repositorio Git en una carpeta llamada `"labowebs"` y agrega los archivos proporcionados en el aula virtual. Renombra la rama master a `main` , si es necesario. Realiza el primer `commit`. Muestra el log del repositorio.

   

   ```bash
   $ git init
   ```

   ![image-20241114090238940](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241114090238940.png)

   ```bash
   $ git branch -m main
   ```

   ![image-20241114090832350](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241114090832350.png)

   ![image-20241114090944828](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241114090944828.png)

   ```bash
   $ git add .
   ```

   ![image-20241114091009332](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241114091009332.png)

   ```bash
   $ git commit -m "Primer commit"
   ```

   ![image-20241114091127636](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241114091127636.png)

   

2. Incluye un fichero `.gitignore` para que los ficheros `README.md` , `LICENCE.txt` y `passwords.txt` sean ignorados por el control de versiones. Realiza el `commit` y muestra los logs del repositorio en una línea.

   

   Haremos un .txt con el nombre .gitignore y añadiremos los nombres de los archivos que queremos ignorar:

   ![image-20241114091536772](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241114091536772.png)

   ```bash
   $ git status
   ```

   ![image-20241114091710339](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241114091710339.png)

   ```bash
   $ git add .gitignore
   ```

   ![image-20241114092140413](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241114092140413.png)

   ```bash
   $ git commit -m "Agregar .gitignore"
   ```

   ![image-20241114092234836](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241114092234836.png)

   ```bash
   $ git log --oneline
   ```

   ![image-20241114092315908](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241114092315908.png)

   

3. En el repositorio, crea los archivos `README.md` , `LICENCE.txt` y `passwords.txt` con algún contenido. Muestra el estado del repositorio. Muestra el listado de archivos ignorados.

   

   ![image-20241114092822325](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241114092822325.png)

   ```bash
   $ git status
   $git status --ignored
   ```

   ![image-20241114092905845](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241114092905845.png)

   

4. Crea una rama `feature-estilos` . Cámbiate a ella. 

   

   ```bash
   $ git branch feature-estilos
   $ git checkout feature-estilos
   ```

   ![image-20241114093930782](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241114093930782.png)

   

   - Modifica el archivo `estilos.css` : 

     - propiedad color del `body` y de `h2` : `#2a2a2a` 

       ![image-20241114094320093](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241114094320093.png)

       ![image-20241114094343797](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241114094343797.png)

     

     - propiedad `background-color` de `header` y `footer`: `#2a75ff`

       ![image-20241114094546292](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241114094546292.png)

       ​		![image-20241114094637053](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241114094637053.png)	

     - Comprueba el estado del repositorio. Añade los cambios, realiza un `commit` con el mensaje "actualizados estilos a azules"

       ```bash
       $ git status
       $ git add .
       $ git commit -m "Actualizados estilos a azules"
       ```

       ![image-20241114095042535](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241114095042535.png)

       

5. Vuelve a la rama `main` . En el archivo `index.html` añade un comentario donde se indique tu nombre como autor de la página. Comprueba el estado del repositorio. Añade los cambios, realiza un commit con el mensaje ' añadido autor en index'. Muestra los logs del repositorio en una línea, gráficamente y con 'decoración'.

   

   ```bash
   $ git checkout main
   ```

   ![image-20241114095341998](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241114095341998.png)

   ![image-20241114095453596](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241114095453596.png)

   ```bash
   $ git status
   $ git add .
   $ git commit -m "Añadido autor en index"
   ```

   ![image-20241114095703551](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241114095703551.png)

   ```bash
   $ git log --oneline --graph --decorate
   ```

   ![image-20241114095749774](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241114095749774.png)

   

6. Fusiona la rama `feature-estilos` en la rama `main` . Muestra los logs del repositorio en una línea, gráficamente y con 'decoración'.

   

   ```bash
   $ git merge feature-estilos
   $ git log --oneline --graph --decorate
   ```

   ![image-20241114100304199](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241114100304199.png)

   

## Trabajo en remoto

### Cuestiones

1. Continúa con el repositorio labowebs . Añade el repositorio a Sourcetree. 

   

   ![image-20241114101522312](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241114101522312.png)

   

2. Crea un repositorio remoto y sube al remoto los ficheros de tu repositorio local. Debes subir todas las ramas. 

   ![image-20241115084007631](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241115084007631.png)

   ```bash
   $ git remote add origin https://github.com/Ikerpc123/labowebs.git
   ```

   ![image-20241115084139849](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241115084139849.png)

   ```bash
   $ git push -u origin --all
   ```

   ![image-20241115084322144](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241115084322144.png)

   ![image-20241115084343898](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241115084343898.png)

   

3. Crea una rama `feature-index` . Añade el siguiente código dentro de la `<section class="about">`. Añade los cambios y crea un commit. Sube los cambios al remoto.

   

   ```bash
   $ git branch feature-index
   $ git checkout feature-index
   ```

   ![image-20241115084733265](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241115084733265.png)

   Hacemos los cambios:

   ![image-20241115085350599](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241115085350599.png)

   ```bash
   $ git status
   $ git add .
   $ git commit -m "Cambios en index"
   ```

   ![image-20241115085603538](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241115085603538.png)

   ```bash
   $ git push -u origin feature-index
   ```

   ![image-20241115085906817](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241115085906817.png)

   ![image-20241115085846337](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241115085846337.png)

   

4. En el repositorio local, fusiona la rama `feature-index` en la rama `main` .

   

   ```bash
   $ git checkout main
   $ git merge feature-index
   ```

   ![image-20241115090154118](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241115090154118.png)

   ![image-20241115090539740](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241115090539740.png)

   

5.  Edita el fichero `contacto.html` . Borra unas líneas. Muestra los ficheros con cambios pendientes y las diferencias. Añade los cambios y haz un commit.

   

   Borraemos esta parte del .html:

   ![image-20241115090721057](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241115090721057.png)

   ```bash
   $ git status
   $ git diff
   ```

   ![image-20241115091123561](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241115091123561.png)

   ```bash
   $ git add contacto.html
   $ git commit "cambio en contacto.html"
   ```

   ![image-20241115091335056](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241115091335056.png)

   

6. Te das cuenta del error. Deshaz el commit anterior. Captura el estado actual del repositorio.

   

   ```bash
   $ git log
   ```

   ![image-20241115091615096](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241115091615096.png)

   ```bash
   $ git reset --soft HEAD~1
   ```

   ![image-20241115092424047](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241115092424047.png)

   ```bash
   $ git reset HEAD~1
   $ git status
   ```

   ![image-20241115092512418](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241115092512418.png)

   

7. Crea una rama `feature-mapa` . Incluye este código en el archivo `contacto.html` . Añade los cambios. Realiza un commit. Sube los cambios al remoto. Muestra en el remoto los cambios del archivo `contacto.html` en la rama `feature-mapa`.

   

   ```bash
   $ git branch feature-mapa
   $ git checkout feature-mapa
   ```

   ![image-20241120125053557](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241120125053557.png)

​	![image-20241120125217393](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241120125217393.png)



```bash
$ git status
$ git add contacto.html
$ git commit -m "Mapa en contacto.html"
$ git push
```

![image-20241120125400175](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241120125400175.png)



```bash
$ git push -u origin feature-mapa
```

![image-20241120130122588](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241120130122588.png)

![image-20241120130313249](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241120130313249.png)



8. En GitHub, en la rama `main` , fusiona la rama `feature-mapa` . Baja los cambios del remoto a local. Deja los dos repositorios sincronizados.

   ![image-20241120130544130](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241120130544130.png)

   

![image-20241120130723744](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241120130723744.png)



![image-20241120130831271](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241120130831271.png)

![image-20241120130851063](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241120130851063.png)

```bash
$ git checkout main
$ git pull origin main
```

![image-20241120131024472](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241120131024472.png)



```bash
$ git log --oneline --graph --decorate
```

![image-20241120131218104](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241120131218104.png)



​	Solo nos faltaría sincronizar los repositorios: 

```bash
$ git fetch --all
```



## Conflictos

### Cuestiones

1. Crea una rama `hotfix-js` . Cámbiate a ella. Añade este código en el fichero `script.js` . Confirma el cambio y haz un commit. (Fíjate en los números de línea...)

   

   ```bash
   $ git branch hotfix-js
   $ git checkout hotfix-js
   ```

   ![image-20241120131906991](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241120131906991.png)

   ![image-20241120131956519](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241120131956519.png)

   

   ```bash
   $ git status
   $ git add .
   $ git commit -m "Cambio hotfix-js"
   ```

   ![image-20241120132329944](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241120132329944.png)

   

2. Vuelve a la rama `main` . En el fichero `script.js` en las mismas líneas que en la cuestión anterior, añade el código siguiente. Confirma el cambio y haz un commit.

   ```bash
   $ git checkout main
   ```

   ![image-20241120132743678](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241120132743678.png)

   ![image-20241120133023646](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241120133023646.png)

   

   ```bash
   $ git status
   $ git add .
   $ git commit -m "Cambio main-js"
   ```

   ![image-20241120133237590](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241120133237590.png)



3. Fusiona la rama `hotfix-js` en `main` . Debe producirse un conflicto. Resuélvelo. Cuando termines la resolución del conflicto sube los cambios al remoto - Deja los repositorios sincronizados -

   ```bash
   $ git merge hotfix.js
   ```

   ![image-20241121094831501](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241121094831501.png)

![image-20241121094938576](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241121094938576.png)

​	Lo cambiamos a:

​				![image-20241121101109638](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241121101109638.png)

​	

```bash
$ git add .
$ git status
$ git commit -m "Resolver conflicto"
$ git push
```

![image-20241121124033339](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241121124033339.png)

![image-20241121124216642](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241121124216642.png)

![image-20241121124247457](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241121124247457.png)

![image-20241121124437235](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241121124437235.png)



## Subida de documentación 

En la carpeta del proyecto `labowebs` añade una carpeta `docs` . Copia en esa carpeta el fichero markdown y la carpeta con las imágenes. Incluye también el `pdf` . Añade todo al repositorio. Súbelo al remoto.

![image-20241121130120548](./Ejercicio%20de%20Git%20-%20proyecto%20labowebs.assets/image-20241121130120548.png)

![image-20241121130211651](C:/Users/alumno/AppData/Roaming/Typora/typora-user-images/image-20241121130211651.png)



​	

```
$ git status
$ git add .
$ git push
```

![image-20241121130352147](C:/Users/alumno/AppData/Roaming/Typora/typora-user-images/image-20241121130352147.png)

![image-20241121130401706](C:/Users/alumno/AppData/Roaming/Typora/typora-user-images/image-20241121130401706.png)

![image-20241121130639025](C:/Users/alumno/AppData/Roaming/Typora/typora-user-images/image-20241121130639025.png)
