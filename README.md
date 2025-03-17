# Github repositorios

Creación de un repositorio donde el código es el corazón de los repositorios donde además de incluir codigo en diferentes lenguajes de programación también se incluye todo tipo de archivos en la sección de código. 

Instrucciones Generales

Cuando te unas a un proyecto existente, primero clona el repositorio remoto. Luego, cree una rama desde el repositorio principal y trabaje en ella. Agrega los archivos actualizados al área de preparación y haz commit en la rama. Envía los commits al repositorio remoto. Crea una solicitud de extracción para fusionar la rama en la rama principal, la cual será revisada y aprobada por el mantenedor de IA. Cuando inicias un nuevo proyecto, inicializa un repositorio Git local. Luego, selecciona los archivos que quieres que Git rastree, muévelos a un área de preparación, y realiza un commit inicial. Cree un repositorio remoto en blanco y establezca un vínculo con su repositorio local. Envía los cambios para que otros desarrolladores puedan clonar este repositorio remoto y seguir el flujo de trabajo regular para actualizar los archivos del proyecto.

Comandos básicos en Git 

git add

Descripción: Agrega cambios al área de preparación. Este comando prepara los cambios realizados en los archivos y los prepara para el próximo commit.

Sintaxis:

git add <nombre-de-archivo.txt> (para agregar un archivo específico)
git add . (para agregar todos los archivos que son nuevos o han cambiado en el directorio actual)
git add -A (para agregar todos los cambios en todo el árbol de trabajo, desde la raíz del repositorio, sin importar dónde te encuentres en la estructura de directorios)

git reset

Descripción: Restablece los cambios en el directorio de trabajo. Cuando se usa con –hard HEAD, este comando descarta todos los cambios realizados en el directorio de trabajo y el área de preparación y restablece el repositorio al último commit (HEAD).

Sintaxis:

git reset
git reset –hard HEAD

git branch

Descripción: Lista, crea o elimina ramas en un repositorio. Para eliminar la rama, primero cambia a la rama usando git checkout y luego ejecuta el comando para eliminar la rama localmente.

Sintaxis:

git branch (para listar ramas)
git branch <nueva-rama> (para crear una nueva rama)
git branch -d <nombre-de-rama> (para eliminar una rama)

git checkout main

Descripción: Cambia a la rama “main”. Esto cambiará tu rama actual a “main”.

Sintaxis: git checkout main

git clone

Descripción: Copia un repositorio de una fuente remota a tu máquina local. Esto creará una copia del repositorio en tu directorio de trabajo actual.

Sintaxis: git clone "URL del repositorio"

git pull

Descripción: Obtiene cambios de un repositorio remoto y los fusiona en tu rama local. Primero, cambia a la rama en la que deseas fusionar los cambios ejecutando el comando git checkout. Luego, ejecuta el comando git pull, que obtendrá los cambios de la rama principal del repositorio remoto de origen y los fusionará en tu rama actual.

Sintaxis: git pull origin main

git push

Descripción: Sube el contenido del repositorio local a un repositorio remoto. Asegúrate de estar en la rama que deseas enviar ejecutando primero el comando git checkout, luego empuja la rama al repositorio remoto.

Sintaxis: git push origin "nombre-de-rama"

git version

Descripción: Muestra la versión actual de Git instalada en tu sistema.

Sintaxis: git version

git diff

Descripción: Muestra cambios entre commits, entre un commit y el árbol de trabajo, etc. También compara las ramas.

Sintaxis:

git diff (muestra la diferencia entre el directorio de trabajo y el último commit)
git diff HEAD~1 HEAD (muestra la diferencia entre el último y el penúltimo commit)
git diff "rama-1" "rama-2" (compara las ramas especificadas)

git revert

Descripción: Revierte un commit aplicando un nuevo commit. Esto creará un nuevo commit que deshace los cambios realizados por el último commit.

Sintaxis: git revert HEAD

git config –global user.email "Tu Email de GitHub"

Descripción: Establece una configuración de correo electrónico global para Git. Esto debe ejecutarse antes de hacer un commit para autenticar el ID de correo electrónico del usuario.

Sintaxis: git config –global user.email "Tu Email de GitHub"

git config –global user.name "Tu Nombre de Usuario de GitHub"

Descripción: Establece una configuración de nombre de usuario global para Git. Esto debe ejecutarse antes de hacer un commit para autenticar el nombre de usuario del usuario.

Sintaxis: git config –global user.name "Tu Nombre de Usuario de GitHub"

git remote

Descripción: Lista los nombres de todos los repositorios remotos asociados con tu repositorio local.

Sintaxis: git remote

git remote -v

Descripción: Lista todos los repositorios remotos a los que está conectado tu repositorio local de Git, junto con las URL asociadas a esos repositorios remotos.

Sintaxis: git remote -v

git remote add origin <URL>

Descripción: Agrega un repositorio remoto llamado “origin” con la URL especificada.

Sintaxis: git remote add origin "URL"

git remote rename

Descripción: El comando git remote rename se sigue del nombre del repositorio remoto (origin) que deseas renombrar y el nuevo nombre (upstream) que deseas darle. Esto renombrará el repositorio remoto “origin” a “upstream”.

Sintaxis: git remote rename origin upstream

git remote rm <nombre>

Descripción: Elimina un repositorio remoto con el nombre especificado.

Sintaxis: git remote rm origin

git format-patch

Descripción: Genera parches para envío por correo electrónico. Estos parches se pueden utilizar para enviar cambios por correo electrónico o para compartirlos con otros.

Sintaxis: git format-patch HEAD~3 (crea parches para los últimos tres commits)

git request-pull

Descripción: Genera un resumen de cambios pendientes para una solicitud por correo electrónico. Ayuda a comunicar los cambios realizados en una rama o bifurcación al mantenedor del repositorio upstream.

Sintaxis: git request-pull origin/main <mi bifurcación o nombre_de_rama>

git send-email

Descripción: Envía una colección de parches como correos electrónicos. Te permite enviar múltiples archivos de parches a los destinatarios por correo electrónico. Asegúrate de configurar la dirección de correo electrónico y el nombre utilizando el comando git config para que el cliente de correo conozca la información del remitente al enviar los correos electrónicos.

Sintaxis: git send-email *.patch

git am

Descripción: Aplica parches al repositorio. Toma un archivo de parche como entrada y aplica los cambios especificados en el archivo de parche al repositorio.

Sintaxis: git am <archivo-de-parche.patch>

git daemon

Descripción: Expone repositorios a través del protocolo Git://. El protocolo Git es un protocolo ligero diseñado para una comunicación eficiente entre clientes y servidores de Git.

Sintaxis: git daemon –base-path=/ruta/a/repositorios

git instaweb

Descripción: Lanza instantáneamente un servidor web para navegar por los repositorios. Proporciona una forma simplificada de ver el contenido del repositorio a través de una interfaz web sin necesidad de configurar un servidor web completo.

Sintaxis: git instaweb –httpd=webrick

git rerere

Descripción: Reutiliza la resolución registrada de conflictos de fusión resueltos anteriormente. Ten en cuenta que la opción de configuración rerere.enabled debe estar configurada en “true” (git config –global rerere.enabled true) para que git rerere funcione. Además, ten en cuenta que git rerere solo se aplica a conflictos que han sido resueltos utilizando la misma rama y commit.

Sintaxis: git rerere
