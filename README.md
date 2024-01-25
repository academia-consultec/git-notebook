# git-notebook

## Introducción de GIT

Este documento contiene información sobre la herramienta de GIT

## github
GitHub es una plataforma de desarrollo colaborativo de software para alojar proyectos utilizando el sistema de control de versiones Git.

## Contenido
- [Sistemas de Control de versiones](#sistemas-de-control-de-versiones-)
- [Que es GIT](#qué-es-git)
- [Archivos de Texto y Binarios](#archivos-de-texto-y-binarios-)
- [Crear un repositorio y un commit](#crear-un-repositorio-y-un-commit-)
- [Verificar cambios entre archivos DIFF](#verificar-cambios-entre-archivos-diff-)
- [¿Que es el Staging y los Branch?](#qué-es-el-staging-y-los-branch-)
- [¿Que es un Merge?](#qué-es-un-merge-)
- [¿Como volver en el tiempo?](#cómo-volver-en-el-tiempo-)
- [¿Como revertir cambios?](#cómo-revertir-cambios-)
- [Repositorios remotos](#repositorios-remotos-)
- [Peticiones de cambios](#peticiones-de-cambios-)
- [Merge entre ramas y resolución de conflictos](#merge-entre-ramas-y-resolucion-de-conflictos-)
- [Gestión de ramas](#gestión-de-ramas)
- [Forks en control de versiones](#forks-en-control-de-versiones-)
- [¿Qué son tags?](#que-son-tags-)
- [GIT fetch, pull y push](#git-fetch-pull-y-push-)
- [Diferencias de GIT fetch y pull](#diferencias-de-git-fetch-y-pull)
- [.gitignore](#gitignore)
- [README.md](#readmemd-)
- [Convenciones para comentar commits](#convenciones-para-comentar-commits-)
- [Cómo documentar una solicitud de cambio](#como-documentar-una-solicitud-de-cambio-)
- [¿Qué es el CODE REVIEW?](#que-es-el-code-review-)
- [GIT clean y rebase](#git-clean-y-rebase-)
- [GIT stash](#git-stash-)
- [GIT cherry-pick](#git-cherry-pick-)
- [GIT reset y reflog](#git-reset-y-reflog-)
- [Uso avanzado del commit (amend)](#uso-avanzado-del-commit-amend)
- [Uso avanzado de checkout](#uso-avanzado-de-checkout)
- [GIT blame](#git-blame-)
- [GIT grep y log](#git-grep-y-log-)
- [Repositorios dentro de otros repositorios (Submódulos)](#repositorios-dentro-de-otros-repositorios-submódulos)
- [¿Que son los tags?](#que-son-los-tags)
- [Comandos para la creacion de un tag](#comandos-para-la-creacion-de-un-tag)
- [Comandos para GIT fetch, pull y push](#comandos-para-git-fetch-pull-y-push)
- [Comando Basicos de GIT](#comandos-basicos-de-git)
- [Video Informativo sobre git (explicacion completa)](#video-informativo-sobre-git-explicacion-completa-)
- [GIT Reset y Reflog](#git-reset-y-reflog)
- [Uso Avanzado del commit (amend)](#uso-avanzado-del-commint-amend)
- [Comandos Checkout y Blame](#comandos-checkout-y-blame)
- [GIT Grep y Log](#git-grep-y-log)
- [Submodulos](#submodulos)

### Sistemas de Control de versiones 📝

Un sistema de control de versiones es una herramienta fundamental para el desarrollo de cualquier proyecto.
Permite los siguientes puntos :bookmark_tabs: :
- Mantener un historial de cambios en los archivos
- Evita la pérdida de datos
- Facilita la colaboración en equipo
- Mejora la gestión de cambios en el proyecto
- Ingración con plataformas de Colaboración

### ¿Qué es GIT?

Git es un sistema de control de versiones distribuido que se utiliza principalmente para el desarrollo de software.  

En lugar de tener un único espacio para todo el historial de versiones del software, como sucede de manera habitual en los sistemas de control de versiones antaño populares, en Git, la copia de trabajo del código de cada desarrollador es también un repositorio que puede albegar el historial completo de todos los cambios.
Permite controlar las diferentes versiones de un proyecto, trabajar en equipo de manera más eficiente y es muy flexible y personalizable.
Nos ayuda a llevar un control y asi poder gestionar de mejor manera las diferentes versiones que pueden surgir durante un proyecto en nuestro repositorio local y asi posteriormente cargarlo a un repositorio remoto.


### Archivos de Texto y Binarios 📄

En Git se pueden manejar dos tipos de archivos: archivos de texto y archivos binarios. Ambos son manejados de la misma manera,
creando una copia completa de cada archivo en cada commit, pero los archivos binarios son más grandes y consumen más espacio en disco que los archivos de texto.
Ademas de que los archivos binarios son más pesados, tambien debemos de tomar en cuenta de que al subir nuevamente este archivo va a volver a cargar todo el programa,
por esto es recomendable no subier estos tipos de archivos.  

### Crear un repositorio y un commit 📦
Pasos:

-Para crear un repositorio y un commit en Git, se debe inicializar el repositorio con el comando **`git init`**
-Agregar los archivos al repositorio con **`git add`**
-Paso siguiente es crear un nuevo commit con **`git commit`**
>[!INOTE]
>Es importante utilizar un mensaje significativo para describir los cambios realizados en el commit y actualizar la rama principal del repositorio con frecuencia.

### Verificar cambios entre archivos ‘DIFF’ 🔎


Para verificar los cambios entre dos versiones de un archivo en Git, se debe utilizar el comando **`git diff`**. \
Este comando mostrará las diferencias entre el archivo actual y su última versión guardada o entre una versión específica del archivo y su versión actual.
- Se puede agregar la bandera hash para comparar el archivo actual con una versión en especifico.


NOTA: Utiliza el comando **`git log`** para ver el historial del commit junto al id de cada commit

## ¿Qué es el Staging y los Branch? 🌲

El Staging y las Branches son dos conceptos importantes en Git. El Staging permite preparar los cambios antes de realizar un commit,  
mientras que las Branches permiten organizar el trabajo en diferentes funcionalidades del proyecto sin afectar el trabajo de otros desarrolladores.
Tambien podemos agregar el concepto de Stage area que vendria siendo el area donde nuestro documento pasa luego de ejecutar el comando git add y luego de eso tendriamos 
que hacerle commit. Y las branches seria una manera de trabajar colaborativamente de forma mas ordenada.
### ¿Qué es un Merge? 🤝

El Merge en Git es el proceso de combinar dos o más ramas en una sola rama. Se utiliza comúnmente para integrar cambios realizados en Branches separadas en la rama principal del proyecto.  
El proceso de Merge implica cambiar a la rama de destino, ejecutar el comando de Merge, resolver conflictos (si es necesario) y crear un nuevo commit.
El Merge es la accion de fusionar dos ramas con el comando (git merge "nombre de la rama"), o sea comparar archivo por archivo buscando cambios que se hayan realizado en cualquiera de las dos ramas esto, actualizando con los ultimos cambios la rama a la cual esta dirigido el merge.
Es recomendable actualizar las ramas remotas a las cuales se les esta haciendo merge utilizando comandos como pull o fetch en dicha rama.

## ¿Cómo volver en el tiempo? 🕧

En Git hay varias formas de volver en el tiempo para acceder a versiones anteriores de un proyecto, como revertir un commit, cambiar al estado de un commit anterior, crear una nueva rama desde un commit anterior o utilizar el comando reset.  
Es importante recordar que al retroceder en el tiempo, los cambios realizados posteriormente se perderán, a menos que se hayan guardado en una rama o commit diferente, por lo que se recomienda crear ramas y commits nuevos regularmente para evitar perder trabajo importante.

### ¿Cómo revertir cambios? ⏳

En Git hay varias formas de revertir cambios. Puedes revertir un commit específico utilizando el comando **`git revert`**, o revertir un archivo a su versión anterior utilizando **`git checkout`**.  
Si deseas revertir varios commits, puedes utilizar **`git revert -n`**. 
Además, existe la opción de utilizar el comando **`git reset`**, aunque es una operación peligrosa. Al revertir cambios, se crean nuevos commits que deshacen los cambios realizados, 
y es importante recordar que siempre se puede volver a los cambios originales si es necesario. Se recomienda crear una nueva rama antes de realizar cambios importantes para poder revertirlos de manera segura si es necesario.

En Git hay varias formas de revertir cambios. Puedes revertir un commit específico utilizando el comando **`git revert`**, o revertir un archivo a su versión anterior utilizando **`git checkout`**
. Si deseas revertir varios commits, puedes utilizar **`git revert -n`**

. En el comando **`git reset`** podemos indicarle dos opciones: **`--hard`** y **`--soft`**, siendo la primera para eliminar todos los commits posteriores y la segunda para que el sistema que se eliminaron, pero en realidad sigue ahí.
. Además, existe la opción de utilizar el comando **`git reset`**, aunque es una operación peligrosa. Al revertir cambios, se crean nuevos commits que deshacen los cambios realizados, y es importante recordar que siempre se puede volver a los cambios originales si es necesario. Se recomienda crear una nueva rama antes de realizar cambios importantes para poder revertirlos de manera segura si es necesario. Algunos tipos de git reset son los siguientes: `git reset --hard` vuelve a un punto en la historia y elimina todo lo que sigue, permitiendo eliminar permanentemente los cambios, `git reset --soft` regresa a un punto de la historia pero sin eliminar los cambios siguientes.  


### Flags para git 🏳️

- **`git reset --soft`**: Permite volver hacia un commit anterior suponiendo que lo de más adelante "no existe".

- **`git reset --hard`**: ⚠️ ¡¡¡PELIGROSO!!! ⚠️ Directamente dice que todo lo que le sigue al commit al que regresaste no existe, se pierde esa sección de la historia del branch.


### Repositorios remotos 🌐

Un repositorio remoto en Git es una versión de tu proyecto alojada en un servidor remoto. Te permite colaborar con otros desarrolladores y mantener una copia segura de tu código en caso de pérdida o daño en tu computadora local. Para trabajar con repositorios remotos en Git, debes vincular tu repositorio local con el repositorio remoto mediante el comando **`git remote add`**
. Puedes enviar tus cambios locales al repositorio remoto utilizando **`git push`**, y descargar los cambios realizados en el repositorio remoto utilizando **`git fetch`**
. Los repositorios remotos son esenciales para el trabajo colaborativo con Git.
**git clone --mirror <repositorio-a-duplicar> <repositorio-donde-alojar-nuevo-repo>**
- todas las refs estaran disponibles en el repositorio nuevo como una copia del original
- obtendras todas las tags
- obtendras todas las ramas
- todas las ramas remotas estaran disponibles en el repositorio destiono.
paso:
- git clone --mirror <repositorio-fuente>
- git remote set-url --push origin <repositori-destino>
- git push --mirror

### Peticiones de cambios ✋

Una petición de cambios es una forma de solicitar que otro colaborador revise y apruebe tus cambios antes de fusionarlos con la rama principal del proyecto. Es una práctica común en proyectos colaborativos y ayuda a mantener la calidad del código y evitar errores.

### Merge entre ramas y resolución de conflictos ✔️

El merge es el proceso de fusionar dos ramas en Git, normalmente la rama principal y una rama secundaria. Si no hay conflictos, Git realizará el merge de forma automática. Pero si hay conflictos, Git pedirá al usuario que resuelva los conflictos manualmente antes de completar el merge. La resolución de conflictos es una parte importante del proceso de merge y puede ser un poco complicada en algunos casos. Por lo tanto, es recomendable asegurarse de tener una buena comprensión de las herramientas de Git y de las buenas prácticas para evitar conflictos innecesarios.

### Gestión de ramas

La gestión de ramas en Git permite trabajar en diferentes características de forma aislada sin interferir entre ellas. Esto se logra a través de la creación, eliminación, combinación y comparación de ramas. Además, la funcionalidad de etiquetado permite identificar y etiquetar versiones específicas del software. Para conocer las ramas existentes y la rama de trabajo local se puede utilizar el comando **`git branch`** el cual lo imprime en línea de comando.

## Eliminar una rama local

el comando para borrar ramas locales en git es **`git branch --delete <rama>`** o **`git branch -d <rama>`**.
Podriamos eliminar una rama remota utilizando **`git push <remoto> delete <rama>`**

## Forks en control de versiones 🍴

Un fork en control de versiones es una copia independiente de un repositorio que se crea en una cuenta diferente de la original. Los forks son especialmente útiles para proyectos de código abierto, ya que permiten a los desarrolladores contribuir al proyecto sin necesidad de tener permisos de escritura en el repositorio original.

### ¿Qué son tags? 🏷️

Los tags en Git son identificadores asociados a versiones específicas de un repositorio. Se utilizan para marcar versiones importantes y hitos en el desarrollo de un proyecto, y se crean con el comando `git tag`. Los tags se pueden compartir con otros usuarios a través de repositorios remotos y se pueden ver con los comandos `git tag` y `git show`. Para firmar la tag con las credenciales del usuario se utiliza el comando `git tag -s`.


### GIT fetch, pull y push 🔴🔵⚪ 

**`git fetch`** se utiliza para descargar los cambios del repositorio remoto, **`git pull`**
 combina los cambios descargados con la rama actual en tu repositorio local y **`git push`**
 se utiliza para enviar los cambios locales al repositorio remoto.

### Diferencias de GIT fetch y pull

**`git fetch`** es el comando que le dice a tu git local que recupere la última información de los metadatos del original (aunque no hace ninguna transferencia de archivos.Es más bien como comprobar si hay algún cambio disponible). 
**`git pull`** por otro lado hace eso Y trae (copia) esos cambios del repositorio remoto. 

### .gitignore 🙅

**`.gitignore`** es un archivo que se utiliza para especificar los archivos y directorios que se deben ignorar en el control de versiones. Es útil para evitar agregar archivos generados automáticamente por tu aplicación o sistema de construcción al control de versiones, lo que puede llevar a conflictos innecesarios al fusionar ramas. Los patrones pueden incluir comodines y caracteres especiales para hacer coincidir nombres de archivo específicos o patrones de nombres de archivo. El archivo **`.gitignore`**se coloca en la raíz del directorio de tu repositorio Git.

### README.md 👀

**`README.md`** es un archivo importante que se utiliza para proporcionar información básica y contexto sobre un proyecto en un repositorio Git. Proporciona detalles útiles sobre el proyecto, como la descripción, los requisitos previos, las instrucciones de instalación y los ejemplos de uso. También se puede usar la función de edición en línea de GitHub para modificar el archivo **`README.md`** directamente en el navegador, lo que hace que la actualización sea fácil y rápida. En general, tener un buen archivo **`README.md`** puede ser muy útil para que los usuarios puedan entender rápidamente tu proyecto y comenzar a usarlo de manera efectiva.

### Convenciones para comentar commits 👍

Las convenciones para comentar commits son una práctica recomendada para que el historial de cambios en un repositorio sea más legible, comprensible y coherente. Se trata de establecer un formato y una estructura para los mensajes de los commits, de manera que se especifiquen de manera clara y concisa los cambios realizados y la razón de los mismos. Esto facilita la revisión de los cambios por parte de los miembros del equipo y ayuda a mantener un registro histórico completo de todas las modificaciones en el código. Algunas convenciones comunes incluyen el uso de un encabezado descriptivo, seguido de una descripción detallada de los cambios, el uso de palabras clave para identificar el tipo de cambio realizado (por ejemplo, "feat" para nuevas características, "fix" para correcciones de errores, etc.), y el uso de un límite de caracteres en el mensaje para evitar mensajes demasiado largos y desorganizados.

### Convenciones para el nombramiento de branchs 👍

Las convenciones para nombrar ramas en Git son una forma de estandarizar el nombre de las ramas de un proyecto, lo que facilita su comprensión y su uso por parte de los desarrolladores. Algunas de las convenciones más comunes son:

- Usar nombres cortos, pero descriptivos, para las ramas.
- Emplear una sintaxis que indique la función o el tipo de rama (por ejemplo, "feature/", "bugfix/", "hotfix/", etc.).
- Evitar el uso de espacios y caracteres especiales en los nombres de las ramas.
- Usar letras minúsculas y separar las palabras con guiones (-) en lugar de espacios.

Al seguir estas convenciones, los desarrolladores pueden entender rápidamente el propósito de cada rama en el proyecto y encontrar fácilmente la rama que necesitan trabajar o fusionar.

### Cómo documentar una solicitud de cambio✏️

1. Título: Debe ser breve y descriptivo del cambio que se propone.
2. Descripción: Proporcione una descripción detallada de los cambios propuestos, lo que se espera que resuelva y los motivos detrás del cambio.
3. Pasos para probar: Proporcione pasos detallados para probar los cambios propuestos para que los revisores puedan verificarlos.
4. Capturas de pantalla: Proporcione capturas de pantalla o vídeos, si es posible, para ilustrar los cambios propuestos.
5. Problemas relacionados: Si la solicitud de cambio se relaciona con un problema específico, proporcione un enlace al problema.
6. Etiquetas: Asegúrese de etiquetar adecuadamente la solicitud de cambio para facilitar la organización y la búsqueda.

### ¿Qué es el CODE REVIEW? 🤓

El Code Review es un proceso de revisión de código en el que otros miembros del equipo revisan el código escrito por un desarrollador. El objetivo es encontrar errores, mejorar la calidad del código y asegurarse de que se cumplan los estándares del equipo. Además, también se busca fomentar la colaboración y el aprendizaje en el equipo. El proceso de Code Review suele ser una práctica común en proyectos de software y ayuda a garantizar la calidad y la estabilidad del código.

### git clean y rebase 🧹

git clean es un comando que se utiliza para eliminar archivos no rastreados que se encuentran en el directorio de trabajo. Es útil para limpiar el repositorio de archivos innecesarios.

Por otro lado, el comando GIT rebase se utiliza para integrar cambios de una rama en otra. Reescribe el historial de la rama en la que se está trabajando para incluir los cambios realizados en la rama que se va a fusionar. Esto puede ayudar a mantener un historial de cambios más limpio y fácil de entender.

### git stash 📚

git stash es un comando que permite guardar temporalmente los cambios realizados en un directorio de trabajo sin necesidad de hacer commit. Los cambios se guardan en una pila de cambios temporales (stash) y pueden recuperarse en un momento posterior. Esto es útil cuando se necesita hacer cambios en una rama sin comprometer el estado actual del repositorio.

### git cherry-pick 🍒

git cherry-pick es una herramienta que permite aplicar un commit específico de una rama a otra rama diferente, sin tener que realizar un merge completo entre ambas ramas. Esto es útil cuando se necesita incluir cambios específicos en una rama sin afectar el resto de la rama de destino. Para utilizar cherry-pick, se debe especificar el hash del commit que se desea aplicar y luego confirmar la operación.

# Comandos de emergencia

### git reset y reflog 🔄

En git, **`reset`** es un comando que permite mover la rama actual y la cabeza del repositorio a un commit anterior. Por otro lado, **`reflog`** muestra un historial detallado de todos los movimientos de la cabeza del repositorio, incluidos los movimientos realizados mediante reset o rebase. Ambos comandos son útiles para deshacer cambios no deseados o volver a versiones anteriores del código.

### Uso avanzado del commit (amend) 

En git, el comando **`git commit --amend`** permite agregar cambios adicionales a un commit previo en lugar de crear un nuevo commit separado. Esto es útil para hacer pequeñas correcciones o agregar archivos que se hayan olvidado en un commit anterior. Al usar **`--amend`**, los cambios se agregan al commit anterior y se reemplaza el mensaje del commit original con el nuevo mensaje que se proporciona. Sin embargo, este comando solo se debe usar en commits que no se hayan compartido con otros usuarios, ya que reescribe el historial del repositorio y puede causar problemas si otros han trabajado en el mismo commit.

### Uso avanzado de checkout

**`git checkout`** es una herramienta poderosa y versátil en Git que nos permite hacer mucho más que simplemente cambiar de rama.

Al usar `git checkout -- <file>`, podemos descartar los cambios en un archivo y volver a la última versión guardada. 
También podemos usar `git checkout <branch> -- <file>` para restaurar un archivo de una rama específica en nuestra rama actual.

### git blame 🕵️

**`git blame`** es un comando de GIT que se utiliza para determinar qué usuario realizó cambios en qué parte del archivo y cuándo se realizaron esos cambios. Con este comando, se puede ver el historial de revisiones línea por línea y ver quién fue responsable de introducir cada cambio. Es especialmente útil para encontrar errores o problemas en un archivo específico y para determinar quién debe ser responsable de corregirlos. También se puede utilizar para entender el proceso de desarrollo de un archivo y cómo ha evolucionado con el tiempo.

### git grep y log 🎣

**`git grep`** es un comando que se utiliza para buscar cadenas de texto dentro de los archivos de un repositorio. Puede buscar en el contenido de los archivos, en los nombres de los archivos o en los mensajes de confirmación.

**`git log`** es un comando que se utiliza para mostrar el historial de confirmaciones en un repositorio. Muestra información detallada sobre cada confirmación, como el autor, la fecha y hora, y el mensaje de confirmación. También se pueden utilizar opciones para filtrar y ordenar las confirmaciones.

Ambos comandos son útiles para realizar búsquedas y obtener información sobre el historial de un repositorio, lo que puede ayudar en la resolución de problemas y en la toma de decisiones sobre el desarrollo futuro. el git log se puede tunear

### **Repositorios dentro de otros repositorios (Submódulos)**

Los submódulos en Git permiten mantener en un solo repositorio, múltiples subproyectos alojados en otros repositorios. Esto es útil cuando se quiere incluir un proyecto dentro de otro proyecto más grande, sin tener que copiar todo el código y mantener ambas copias separadas. Al usar submódulos, se puede mantener una referencia al repositorio original y permitir la actualización y la colaboración en ambos proyectos de manera más eficiente.


## GIT HELP

**`git help --all`** lista todos los posibles comandos.
**`git <comando> -help`** permite ver una lista de todas las opciones de un comando.

## ¿Que son los tags? ��

- Los tags o etiquetas se parecen al mensaje del commit.
- Son identificadores asociados a versiones especificas de un repositorio.
- Debemos usarlas para versionamiento productivo.
- Estos versionamientos pueden ser lanzamiento de software o marcar hitos importantes.

###Versiones

> version Alpha: Es el punto mas bajo del sistema.

> version Beta: Es el punto intermedio del producto (version semiestable).

> version release: de ellas se espera que esten mas cerca a produccion.

> version 1.0: es la mas estable que se logra conseguir.

> con **git tag** tenemos un identificador estatico.

> podemos usar **git checkout tag** para llegar a un identificador del punto de la historia.

### Comandos para la creación de un tag

- son identificadores asociados a versiones específicas de un repositorio
- son utilizadas para marcar versiones importantes como el lanzamiento de un software
- `git tag v1.0`
- `git tag -s v1.0` (firma la creación de un tag)
- `git push -tags`
- `git show v1.0`

## Comandos para la creacion de un tag

- **git tag v1.0** para asignar el tag.
- **git tag -s v1.0** envia un parametro al comando para firmar los tags.
- **git push -tags** para publicar los tags
- **git show v1.0** para mostrar informacion de un tag como si fuera un git log.


### Comandos para git fetch, pull y push

- usamos **git fetch** descarga los cambios de un repositorio remoto a local.
- usamos **git pull** combina automaticamente los cambios del repositorio remoto con la rama actual en tu repositorio actual.
- usamos **git push** se usa para enviar cambios en la rama actual de tu repositorio local al repositorio remoto.


### Comando Basicos de git

- `git init`
- `git add <Archivo>`
- `git add .`
- `git commit -m "Mensaje"`
- `git diff <Archivo>`
- `git diff <hash><Archivo>`
- `git branch <CurNombre><NuevoNombre>`
- `git checkout <NombreDelBranch>`
- `git checkout -b <NuevoNombre>`
- `git status`


### Vídeo Informativo sobre git (explicacion completa) 🎥
Si te intera saber mas sobre git y [¿Como Funciona git?](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwjawdTC9oP-AhWuEVkFHSwPB4sQtwJ6BAgLEAI&url=https%3A%2F%2Fwww.youtube.com%2Fwatch%3Fv%3DjGehuhFhtnE&usg=AOvVaw3EzVfE049RTxvTijwZ3C9z)
aqui te muestro un video util y completo.

## Forks en control de versiones 🍴

`git tag -s v1.0` (firma la creación de un tag)

fork permite experimentar con el código sin el temor de dañar el respositorio original

## Guia de como clonar un repositorio
Partamos del punto en donde el dueño del repositorio remoto nos agregor como colaborador de ese repositorio y nos asignos los permisos necesarios.

Pimer paso: Clonar

	git clone https://github.com/academia-consultec/git-notebook.git

Segundo paso: Creacion de una rama, se recomienda no trabajar en el main.

	git branch documentacion/rm

Tercer paso: Sincronizar el repositorio global con el remoto

	git pull

Cuarto paso: Editar el archivo README.md

	nano README.md

Quinto paso: Hacer commit

	git add README.md
	git commit -m "Edicion del README.md"
	git status

Sexto paso: Realizar el push

	git push origin documentacion/rm

### Flujos de trabajo avanzados
> Archivo **.gitignore**
- Esto es especialmente util cuando tienes archivos que son generados automaticamente por tu aplicacion, como archivos de registro o archivos cache.
- Agregar estos archivos al control de versiones no es util y puede llevar a conflictos innecesarios al fusionar ramas.

> Archivo **README.md**
- Se utiliza para proporcionar informacion basica y contexto sobre un proyecto en un repositorio GIT.
- se muestra en la pagina principal del proyecto, es la primera cosa que alguien vera al visitar el repositorio.

### Convenciones para comentar commit
1. la oracion sea imperativa, resolver forma clara y precisa diga lo que deseamos alcanzar con el commit.
3. limitar longitud del mensaje del commit.
3. Agregar detalles de ser necesarios. Historias de usuarios
4. incluir numero de tareas en el mensaje.
5. usar verbos precisos como **fix**, **add**, **delete**, **feat** o muchos mas. La primera la palabra del commit debe dar a entender lo que se esta haciendo con el commit.

### Convenciones para el nombramiento de branchs
- Utilizar nombres cortos y descriptivos.
- Utilizar nombres minusculas separados por **guiones** o **barras diagonales**.
- Utilizar prefijos para indicar el tipo de branch. se puede usar un **ID** como **master**, **release**, entre otros.
- Evitar nombres genericos como **dev**, **feature**, **feature**, **nuevo**.

### ¿Cómo documentar una solicitud de cambio?
- **El titulo** Debe ser breve y descriptivo del cambio que se propone.
    - Colocar el identificador de la historia, titulo de la historia, lenguaje usado.
- **Descripcion** Se proporciona una descripcion detallada de lo que se espera que resuelva y los motive detras del cambio.
- **Capturas de pantalla** Proporcione capturas para ilustrar los cambios propuestos.

### CODE REVIEW
- Parte importante del proceso de desarrollo de software.
- verificamos punto de mejora, estandares y calidad.
- se revisa funcionalidades.
- permite compartir conocimientos y experiencias.
- **Donde todos nos hacemos responsables del proyecto de un compañero**
- Se recomienda que se haga de forma apares, el dueño del codigo y el que revisa.

### git clean y git rebase
> **Clean** Comando que se utiliza para eliminar el archivo no rastreado en un directorio de trabajo local. aproximadamente lo que hace el **rm** en Shell Script.

> **Rebase** Se usa para integrar cambios de una rama a otra de una manera mas ordenada y lineal.

> **statsh** Este guarda tempralmente los cambios en un estado intermedio para que puedas trabajar en otra cosa sin tener que hacer commits de los cambios actuales. **pop** pone el ultimo **apply** los pone todos.

### Comandos de emergencias
- **reset** Es un comando que permite mover la rama actual y la cabeza del repositorio a un commit anterior.
- **reflog** Muestra un historial detallado de todos los movimientos de la cabeza del repositorio.

### Uso avanzado del commit (amend)
- el comando **git commit --amend** se usa para modificar el commit anterior en caso de que se haya olvidado alguin archivo o mensaje de confirmacion o para fusionar multiples confirmaciones en una sola.

### Uso avanzado del checkout
- al usar **git checkout -- archivo**, podemos descartar los cambios de un archivo y volver a la ultima version guardada.
- Tambien podemos usar **git checkout branch -- file** para restaurar un archivo de una rama especifica en nuestra rama actual.
- la bandera **--** es un checkout de emergencia.

### git blame
- Muestra quien y cuando realizo cambiios en cada linea de un archivo determinado.

### git grep
- Es un comando que se utiliza para buscar cadenas de texto dentro de los archivos de un repositorio.
- Buscar en funcion de la salida de un comando de salida. como el resultado de un git log, todos los commit de una persona por ejemplo.

### git log
- Es un comando que se utiliza para mostrar el historial de confirmacion en un repositorio.

### Repositorio dentro de otro repositorio
- Son **submodulos**
- Estos permiten incluir un repositorio git dentro de otro repositorio, como una subcarpeta
- Si tenemos un **mono repositorio** quiero trabajar con la version de master.
- **git submodule add https://github.com/chaconinc/DbConnector** una forma de añadir submodulos.

### git reset y reflog

- `git reset`
	- Es un comando que permite mover la rama actual y la cabeza del repositorio a un commit anterior

- `git reflog` 
    	- muestra un historial detallado de todos los movimientos de la cabeza del repositorio, incluidos los movimientos realizados mediante reset o rebase

### Uso Avanzado del commint (amend)

   	- El comando git commit --amend se utuliza para modificar el commit anterior en case de que se haya olvidaado algún archivo o mensaje de confirmación, o para fusionar múltiples confirmaciones en una sola.

    	- Esto permite mantener la historia del proyecto más limpia y fácil de seguir.

### Comandos Checkout y Blame

- git checkout 

    `git checkout -- <file>`
    `git checkout <branch> -- <file>`

- git blame

    - Muestra quien y cuando realizo los cambios en cada linea de un archivo determinado

### git grep y log

    `git grep`
       	- es un comando que se utiliza para buscar cadenas de terxto dentro de los archivos de un repositorio

    `git log`
       	- es un comando que se utiliza para mostrar el historial de confirmaciones en un repositorio

### Submódulos 

- Los submodulos en git permiten incluir un repositorio de git dentro de otro repositorio git, como una subcarpeta

- Es una forma de mantener y utilizar proyectos relacionados o independientes

## git rm --cached <archivo>
 dejar de seguir los cambios en un archivo que git estaba versionando, pero sin eliminarlo del sistema operativo.

# Git Reset y Reflog: úsese en caso de emergencia
![](https://johngodlee.github.io/geotaster_git_workshop/img/geotaster_git_banner.png)

## Git nunca olvida, git reflog
Git guarda todos los cambios aunque decidas borrarlos, al borrar un cambio lo que estás haciendo sólo es actualizar la punta del branch, para gestionar éstas puntas existe un mecanismo llamado registros de referencia o reflogs.
.
La gestión de estos cambios es mediante los hash’es de referencia (o ref) que son apuntadores a los commits.
.
Los recoges registran cuándo se actualizaron las referencias de Git en el repositorio local (sólo en el local), por lo que si deseas ver cómo has modificado la historia puedes utilizar el comando:

```
git reflog
```

Muchos comandos de Git aceptan un parámetro para especificar una referencia o “ref”, que es un puntero a una confirmación sobre todo los comandos:

- git checkout Puedes moverte sin realizar ningún cambio al commit exacto de la ref

```
git checkout eff544f
```
- git reset: Hará que el último commit sea el pasado por la ref, usar este comando sólo si sabes exactamente qué estás haciendo

```
git reset --hard eff544f # Perderá todo lo que se encuentra en staging y en el Working directory y se moverá el head al commit eff544f
git reset --soft eff544f # Te recuperará todos los cambios que tengas diferentes al commit eff544f, los agregará al staging area y moverá el head al commit eff544f
```

- git merge: Puedes hacer merge de un commit en específico, funciona igual que con una branch, pero te hace el merge del estado específico del commit mandado

```
git checkout master
git merge eff544f # Fusionará en un nuevo commit la historia de master con el momento específico en el que vive eff544f
```

## Convenciones para el nombramiento de branchs

	• Utilizar nombres cortos y descriptivos
	• Utilizar nombres en minuscula separados por guiones o barra diagonal
	• Utilizar prefijos, Evitar nombres genericos
