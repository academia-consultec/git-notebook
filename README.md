# git-notebook

# Introducción de GIT

## Sistemas de Control de versiones

Un sistema de control de versiones es una herramienta fundamental para el desarrollo de cualquier proyecto. Permite mantener un historial de cambios en los archivos, evitar la pérdida de datos, facilitar la colaboración en equipo y mejorar la gestión de cambios en el proyecto.

## ¿Qué es GIT?

Git es un sistema de control de versiones distribuido que se utiliza principalmente para el desarrollo de software. Permite controlar las diferentes versiones de un proyecto, trabajar en equipo de manera más eficiente y es muy flexible y personalizable.

## Archivos de Texto y Binarios

En Git se pueden manejar dos tipos de archivos: archivos de texto y archivos binarios. Ambos son manejados de la misma manera, creando una copia completa de cada archivo en cada commit, pero los archivos binarios son más grandes y consumen más espacio en disco que los archivos de texto.

## Crear un repositorio y un commit

Para crear un repositorio y un commit en Git, se debe inicializar el repositorio con el comando **`git init`**
, agregar los archivos al repositorio con **`git add`**
, y crear un nuevo commit con **`git commit`**
. Es importante utilizar un mensaje significativo para describir los cambios realizados en el commit y actualizar la rama principal del repositorio con frecuencia.

## Verificar cambios entre archivos ‘DIFF’

Para verificar los cambios entre dos versiones de un archivo en Git, se debe utilizar el comando **`git diff`**
. Este comando mostrará las diferencias entre el archivo actual y su última versión guardada o entre una versión específica del archivo y su versión actual.

## ¿Qué es el Staging y los Branch?

El Staging y las Branches son dos conceptos importantes en Git. El Staging permite preparar los cambios antes de realizar un commit, mientras que las Branches permiten organizar el trabajo en diferentes funcionalidades del proyecto sin afectar el trabajo de otros desarrolladores.

## ¿Qué es un Merge?

El Merge en Git es el proceso de combinar dos o más ramas en una sola rama. Se utiliza comúnmente para integrar cambios realizados en Branches separadas en la rama principal del proyecto. El proceso de Merge implica cambiar a la rama de destino, ejecutar el comando de Merge, resolver conflictos (si es necesario) y crear un nuevo commit.

## ¿Cómo volver en el tiempo?

En Git hay varias formas de volver en el tiempo para acceder a versiones anteriores de un proyecto, como revertir un commit, cambiar al estado de un commit anterior, crear una nueva rama desde un commit anterior o utilizar el comando reset. Es importante recordar que al retroceder en el tiempo, los cambios realizados posteriormente se perderán, a menos que se hayan guardado en una rama o commit diferente, por lo que se recomienda crear ramas y commits nuevos regularmente para evitar perder trabajo importante.

## ¿Cómo revertir cambios?

En Git hay varias formas de revertir cambios. Puedes revertir un commit específico utilizando el comando **`git revert`**, o revertir un archivo a su versión anterior utilizando **`git checkout`**
. Si deseas revertir varios commits, puedes utilizar **`git revert -n`**
. Además, existe la opción de utilizar el comando **`git reset`**, aunque es una operación peligrosa. Al revertir cambios, se crean nuevos commits que deshacen los cambios realizados, y es importante recordar que siempre se puede volver a los cambios originales si es necesario. Se recomienda crear una nueva rama antes de realizar cambios importantes para poder revertirlos de manera segura si es necesario.

## Repositorios remotos

Un repositorio remoto en Git es una versión de tu proyecto alojada en un servidor remoto. Te permite colaborar con otros desarrolladores y mantener una copia segura de tu código en caso de pérdida o daño en tu computadora local. Para trabajar con repositorios remotos en Git, debes vincular tu repositorio local con el repositorio remoto mediante el comando **`git remote add`**
. Puedes enviar tus cambios locales al repositorio remoto utilizando **`git push`**, y descargar los cambios realizados en el repositorio remoto utilizando **`git fetch`**
. Los repositorios remotos son esenciales para el trabajo colaborativo con Git.

## Peticiones de cambios

Una petición de cambios es una forma de solicitar que otro colaborador revise y apruebe tus cambios antes de fusionarlos con la rama principal del proyecto. Es una práctica común en proyectos colaborativos y ayuda a mantener la calidad del código y evitar errores.

## Merge entre ramas y resolución de conflictos

El merge es el proceso de fusionar dos ramas en Git, normalmente la rama principal y una rama secundaria. Si no hay conflictos, Git realizará el merge de forma automática. Pero si hay conflictos, Git pedirá al usuario que resuelva los conflictos manualmente antes de completar el merge. La resolución de conflictos es una parte importante del proceso de merge y puede ser un poco complicada en algunos casos. Por lo tanto, es recomendable asegurarse de tener una buena comprensión de las herramientas de Git y de las buenas prácticas para evitar conflictos innecesarios.

## Gestión de ramas

La gestión de ramas en Git permite trabajar en diferentes características de forma aislada sin interferir entre ellas. Esto se logra a través de la creación, eliminación, combinación y comparación de ramas. Además, la funcionalidad de etiquetado permite identificar y etiquetar versiones específicas del software.

## Forks en control de versiones

Un fork en control de versiones es una copia independiente de un repositorio que se crea en una cuenta diferente de la original. Los forks son especialmente útiles para proyectos de código abierto, ya que permiten a los desarrolladores contribuir al proyecto sin necesidad de tener permisos de escritura en el repositorio original.

## ¿Qué son tags?

Los tags en Git son identificadores asociados a versiones específicas de un repositorio. Se utilizan para marcar versiones importantes y hitos en el desarrollo de un proyecto, y se crean con el comando `git tag`. Los tags se pueden compartir con otros usuarios a través de repositorios remotos y se pueden ver con los comandos `git tag` y `git show`.

## GIT fetch, pull y push

**`git fetch`** se utiliza para descargar los cambios del repositorio remoto, **`git pull`**
 combina los cambios descargados con la rama actual en tu repositorio local y **`git push`**
 se utiliza para enviar los cambios locales al repositorio remoto.

## .gitignore

**`.gitignore`** es un archivo que se utiliza para especificar los archivos y directorios que se deben ignorar en el control de versiones. Es útil para evitar agregar archivos generados automáticamente por tu aplicación o sistema de construcción al control de versiones, lo que puede llevar a conflictos innecesarios al fusionar ramas. Los patrones pueden incluir comodines y caracteres especiales para hacer coincidir nombres de archivo específicos o patrones de nombres de archivo. El archivo **`.gitignore`**se coloca en la raíz del directorio de tu repositorio Git.

## README.md

**`README.md`** es un archivo importante que se utiliza para proporcionar información básica y contexto sobre un proyecto en un repositorio Git. Proporciona detalles útiles sobre el proyecto, como la descripción, los requisitos previos, las instrucciones de instalación y los ejemplos de uso. También se puede usar la función de edición en línea de GitHub para modificar el archivo **`README.md`** directamente en el navegador, lo que hace que la actualización sea fácil y rápida. En general, tener un buen archivo **`README.md`** puede ser muy útil para que los usuarios puedan entender rápidamente tu proyecto y comenzar a usarlo de manera efectiva.

## Convenciones para comentar commits

Las convenciones para comentar commits son una práctica recomendada para que el historial de cambios en un repositorio sea más legible, comprensible y coherente. Se trata de establecer un formato y una estructura para los mensajes de los commits, de manera que se especifiquen de manera clara y concisa los cambios realizados y la razón de los mismos. Esto facilita la revisión de los cambios por parte de los miembros del equipo y ayuda a mantener un registro histórico completo de todas las modificaciones en el código. Algunas convenciones comunes incluyen el uso de un encabezado descriptivo, seguido de una descripción detallada de los cambios, el uso de palabras clave para identificar el tipo de cambio realizado (por ejemplo, "feat" para nuevas características, "fix" para correcciones de errores, etc.), y el uso de un límite de caracteres en el mensaje para evitar mensajes demasiado largos y desorganizados.

## Convenciones para el nombramiento de branchs

Las convenciones para nombrar ramas en Git son una forma de estandarizar el nombre de las ramas de un proyecto, lo que facilita su comprensión y su uso por parte de los desarrolladores. Algunas de las convenciones más comunes son:

- Usar nombres cortos, pero descriptivos, para las ramas.
- Emplear una sintaxis que indique la función o el tipo de rama (por ejemplo, "feature/", "bugfix/", "hotfix/", etc.).
- Evitar el uso de espacios y caracteres especiales en los nombres de las ramas.
- Usar letras minúsculas y separar las palabras con guiones (-) en lugar de espacios.

Al seguir estas convenciones, los desarrolladores pueden entender rápidamente el propósito de cada rama en el proyecto y encontrar fácilmente la rama que necesitan trabajar o fusionar.

## Cómo documentar una solicitud de cambio

1. Título: Debe ser breve y descriptivo del cambio que se propone.
2. Descripción: Proporcione una descripción detallada de los cambios propuestos, lo que se espera que resuelva y los motivos detrás del cambio.
3. Pasos para probar: Proporcione pasos detallados para probar los cambios propuestos para que los revisores puedan verificarlos.
4. Capturas de pantalla: Proporcione capturas de pantalla o vídeos, si es posible, para ilustrar los cambios propuestos.
5. Problemas relacionados: Si la solicitud de cambio se relaciona con un problema específico, proporcione un enlace al problema.
6. Etiquetas: Asegúrese de etiquetar adecuadamente la solicitud de cambio para facilitar la organización y la búsqueda.

## ¿Qué es el CODE REVIEW?

El Code Review es un proceso de revisión de código en el que otros miembros del equipo revisan el código escrito por un desarrollador. El objetivo es encontrar errores, mejorar la calidad del código y asegurarse de que se cumplan los estándares del equipo. Además, también se busca fomentar la colaboración y el aprendizaje en el equipo. El proceso de Code Review suele ser una práctica común en proyectos de software y ayuda a garantizar la calidad y la estabilidad del código.

## GIT clean y rebase

GIT clean es un comando que se utiliza para eliminar archivos no rastreados que se encuentran en el directorio de trabajo. Es útil para limpiar el repositorio de archivos innecesarios.

Por otro lado, el comando GIT rebase se utiliza para integrar cambios de una rama en otra. Reescribe el historial de la rama en la que se está trabajando para incluir los cambios realizados en la rama que se va a fusionar. Esto puede ayudar a mantener un historial de cambios más limpio y fácil de entender.

## GIT stash

GIT stash es un comando que permite guardar temporalmente los cambios realizados en un directorio de trabajo sin necesidad de hacer commit. Los cambios se guardan en una pila de cambios temporales (stash) y pueden recuperarse en un momento posterior. Esto es útil cuando se necesita hacer cambios en una rama sin comprometer el estado actual del repositorio.

## GIT cherry-pick

GIT cherry-pick es una herramienta que permite aplicar un commit específico de una rama a otra rama diferente, sin tener que realizar un merge completo entre ambas ramas. Esto es útil cuando se necesita incluir cambios específicos en una rama sin afectar el resto de la rama de destino. Para utilizar cherry-pick, se debe especificar el hash del commit que se desea aplicar y luego confirmar la operación.

## GIT reset y reflog

En GIT, **`reset`** es un comando que permite mover la rama actual y la cabeza del repositorio a un commit anterior. Por otro lado, **`reflog`** muestra un historial detallado de todos los movimientos de la cabeza del repositorio, incluidos los movimientos realizados mediante reset o rebase. Ambos comandos son útiles para deshacer cambios no deseados o volver a versiones anteriores del código.

## Uso avanzado del commit (amend)

En GIT, el comando **`git commit --amend`** permite agregar cambios adicionales a un commit previo en lugar de crear un nuevo commit separado. Esto es útil para hacer pequeñas correcciones o agregar archivos que se hayan olvidado en un commit anterior. Al usar **`--amend`**, los cambios se agregan al commit anterior y se reemplaza el mensaje del commit original con el nuevo mensaje que se proporciona. Sin embargo, este comando solo se debe usar en commits que no se hayan compartido con otros usuarios, ya que reescribe el historial del repositorio y puede causar problemas si otros han trabajado en el mismo commit.

## Uso avanzado de checkout

**`git checkout`** es una herramienta poderosa y versátil en Git que nos permite hacer mucho más que simplemente cambiar de rama.

Al usar `git checkout -- <file>`, podemos descartar los cambios en un archivo y volver a la última versión guardada. 
También podemos usar `git checkout <branch> -- <file>` para restaurar un archivo de una rama específica en nuestra rama actual.

## GIT blame

**`git blame`** es un comando de GIT que se utiliza para determinar qué usuario realizó cambios en qué parte del archivo y cuándo se realizaron esos cambios. Con este comando, se puede ver el historial de revisiones línea por línea y ver quién fue responsable de introducir cada cambio. Es especialmente útil para encontrar errores o problemas en un archivo específico y para determinar quién debe ser responsable de corregirlos. También se puede utilizar para entender el proceso de desarrollo de un archivo y cómo ha evolucionado con el tiempo.

## GIT grep y log

**`git grep`** es un comando que se utiliza para buscar cadenas de texto dentro de los archivos de un repositorio. Puede buscar en el contenido de los archivos, en los nombres de los archivos o en los mensajes de confirmación.

**`git log`** es un comando que se utiliza para mostrar el historial de confirmaciones en un repositorio. Muestra información detallada sobre cada confirmación, como el autor, la fecha y hora, y el mensaje de confirmación. También se pueden utilizar opciones para filtrar y ordenar las confirmaciones.

Ambos comandos son útiles para realizar búsquedas y obtener información sobre el historial de un repositorio, lo que puede ayudar en la resolución de problemas y en la toma de decisiones sobre el desarrollo futuro.

## **Repositorios dentro de otros repositorios (Submódulos)**

Los submódulos en Git permiten mantener en un solo repositorio, múltiples subproyectos alojados en otros repositorios. Esto es útil cuando se quiere incluir un proyecto dentro de otro proyecto más grande, sin tener que copiar todo el código y mantener ambas copias separadas. Al usar submódulos, se puede mantener una referencia al repositorio original y permitir la actualización y la colaboración en ambos proyectos de manera más eficiente.
