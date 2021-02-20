# **Universidad Galileo**
### **Instituto de Investigación de Operaciones**
### ***Postgrado en Análisis y Predicción de Datos***
### ***Ciencia de Datos en Python***


####   Catedrático Titular: Preng Biba
####   Catedrático auxiliar: Milton Godinez

##### Denis Alexis Solis Arroyo
##### Carnet: 20 000 143

<center>
<img src="https://www.galileo.edu/wp-content/uploads/2010/12/logo-ug.png" alt="Drawing" style="width: 400px;"/>
</center>

<center>
<img src=C:/Users/asoli/Downloads/logo-galileo.png  style="width: 400px;"/>
</center>
    
# <center>Ensayo-Git</center>




Git es un Version Control System, que sirve para dar seguimiento a las versiones del código relacionado a un archivo o   proyecto. Los sistemas de control de versiones facilitan el seguimiento a proyectos donde colaboran muchas personas.

Git se ha convertido en el estándar de los sistemas de control de versiones, por su parte Git hace una captura del archivo y si hubo un cambio, puede generar detalles de:

      - Quien editó el archivo
      - Cuando lo hizo
      - Que linea de código cambió
        
La herramienta genera los snapshots de las carpetas y los archivos contenidos en estas, las carpetas son llamadas "trees" y los archivos "blob", un tree puede contener a otros trees y a su vez estos contener a uno o varios blobs.

La siguiente imagen, ejemplifica los tipos de archivos y como los administra Git:

<center>
<img src="https://git-scm.com/book/en/v2/images/data-model-1.png" alt="Drawing" style="width: 400px;"/>
</center>
<center>
Fuente: https://git-scm.com/book/en/v2/images/data-model-1.png
</center>

#### ¿Como almacena Git los snapshots?
Git guarda las versiones de los trees y blobs en una línea de tiempo. Donde un nodo está relacionado al anterior. De modo que el usuario puede regresar a una versión anterior del proyecto de ser necesario. Por ejemplo, Git puede partir de un archivo y crear dos versiones distintas, donde el usuario puede agregar características a cada una de ellas y luego unirlas nuevamente.

En la siguiente imagen, se muestra un ejemplo de la forma en que Git administra las versiones en la linea temporal:

<center>
<img src="https://i.stack.imgur.com/aZmrQ.png" alt="Drawing" style="width: 500px;"/>
</center>
<center>
Fuente: https://i.stack.imgur.com/aZmrQ.png
</center>

Los cambios en Git son irreversibles, sin embargo, cada cambio que se haga a los archivos únicamente genera una nueva versión de estos, por lo que para corregir un archivo, no se reemplaza la versión anterior sino se crea una nueva versión con los cambios.

#### Los objetos en Git
Un objeto en Git puede ser un tree (carpeta), blob (archivo) o bien un commit (cambio). Si un objeto contiene a otro en Git, este ultimo se encuentra referenciado por su id.

La siguiente tabla muestra los principales objetos en Git.

| Tree | Blob | Commit |
| :- | -: | :-: |
| Carpeta. | Archivo contenido en una carpeta | Cambios realizados al proyecto
 

Los snapshots se identifican por medio de un código hexadecimal de 40 caracteres, sin embargo, para que esto sea comprensible para los usuarios, Git crea las referencias, estas no son nada más que un mapeo hacia cada uno de los cambios.

#### Repositorios
Se podría definir un repositorio como el conjunto de objetos y referencias en Git. Git guarda objetos y referencias y todo esto es considerado como un modelo de datos. 

#### El área staging
Por su parte, Git crea una área staging para que el usuario pueda decidir que cambios quiere incluir en el siguiente snapshot que tomará la herramienta. 

Git sabe de la existencia de los archivos en el área staging, sin embargo, no sabe de sus cambios finales hasta que se ejecute el comando **git commit**. Una vez el comando se ejecuta, se crea el snapshot del proyecto.

#### Algunos comandos básicos  de Git

**git help**: muestra una sección de ayuda para un comando específico. 

**git init**: crea un nuevo repositorio con la información almacenada en dicho repositorio. 

**git add**: agrega archivos al área staging.

**git add**: guarda los cambios a los archivos en el área staging.

**git diff**: muestra los cambios generados en el área staging cuando se usa con el complemento < filename >, o bien, muestra las diferencias entre un archivo de diferentes snapshots, para esto se debe usar el complemento < revision > < filename >.

**git merge**: combina los resultados dentro de archivo actual.

**git checkout -- < file >**: descarta los cambios realizados a un archivo.


#### Recursos relacionados a Git
**GitHub**: Git no es lo mismo que GitHub, por su parte GitHub tiene su propia forma de manejar el código por medio de "pull requests". 

<center>
<a href = https://github.com/ > Link a GitHub </a>
</center>

**Otros proveedores**: Aparte de GitHub existen otros sitios de almacenamiento como GitLab y BitBucket.

<center>
<a href = https://about.gitlab.com/ > Link a GitLab </a>
</center>

<center>
<a href = https://bitbucket.org/ > Link a BitBucket </a>
</center>

**ProGit**: Es un libro que muestra como usar Git de manera eficiente, los primeros cinco capítulos muestran los principales fundamentos, se puede encontrar de forma gratuita en la siguiente dirección: <a href = https://git-scm.com/book/en/v2 > ProGit eBook </a>

**Oh shit, Git!?!**: En esta página se muestran los principales errores cometidos por los usuarios y la forma de resolverlos, la página es la siguiente: <a href = https://ohshitgit.com/ > Oh shit, Git!?! </a>

**Learn Git Branching**: Esta página esta dedicada para que los principiantes puedan aprender las bases de Git, por medio de ejercicios prácticos. <a href = https://learngitbranching.js.org/?locale=es_ES > Learn Git Branching </a> 
