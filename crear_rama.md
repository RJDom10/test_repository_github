# Trabajar con ramas usando Git 

Para comenzar a trabajar con ramas usando comandos de Git vamos a utilizar las siguientes instrucciones 

Vamos a clonar el repositorio para tener una copia local en nuestro ordenador, para eso vamos a navegar al repositorio que vamos a neavgar. 
Cuando nos encontremos en el repositorio que vamos a navegar, nos dirigimos a la parte del repositorio, en la parte que dice code vamos a darle click y copiar la dirección url en
la sección HTTPS. 

Para crear la copia, navegamos en la taermial donde vamos a ubicar el repositorio y en la terminal ejecutamos 

git clone "URL"

Una vez con la copia podemos crear ramas para poder trabajar de manera independiente. 

Ahora que ya tenemos el repositorio clonado, vamos a navegar en el con el comando cd 

y creamos una nueva rama 

git branch rama_1

esto no hará que cambiemos de rama, para hacer este cmabio es necesario ejecutar 

git checkout rama_1 

* Como atajo, en lugar de crear una rama usando git branch y luego activarla usando git checkout, puedes usar el comando git checkout seguido de la opción -b, que crea la rama y la activa en un solo paso.

git checkout -b my1stbranch

en este punto puedes hacer tus cambios sin afectar la rama principal. 

Una vez que hayas guardado los cambios o creado nuevos archivos en la rama_1 podemos ver todos los cambios que hemos realizado con el comando 

git status 

esto refleja todos los cambios que hemos realizado, ahora para agergar los archivos a la zona de stage ejecutamos 

git add . (para todos los archivos)

esto especifica que los cambios están listos para ser confirmados. 

Y finalmente podmeos ejecutar git commit -m "" para guardar los cambios que hemos relaizado 

git commit -m "agrego archivos a la rama_1"

Para fusionar los cambios a la rama principal, vamos a cambiar a la rama main 

git checkout main 

y una vez que estamos navegando en la rama main ejecutamos 

git merge rama_1

lo que hará es agregar los cambios de la rama_1 a la rama main

ahora por lo tanto para que estos cambios sean visibles en su repositorio remoto vamos a ejecutar 

git push -u origen main 

esto agregara los cambios de la rama principal al repositorio remoto. 

y para confirmar que los cambios se han realiado usamos nuevamnete git status 

git status 

Nota: 
* A veces, es posible que no pruebes completamente tus cambios antes de comprometerlos, lo que puede tener consecuencias indeseables. Puedes deshacer tus cambios utilizando un comando git revert como el siguiente.

Puedes especificar el ID de tu commit que puedes ver en la salida del registro anterior o usar el atajo HEAD para revertir el último commit:

git revert HEAD --no-edit

Si no especificas la opción --no-edit, es posible que se te presente una pantalla de editor mostrando el mensaje con los cambios que se revertirán. En ese caso, presiona la tecla Control (o Ctrl) simultáneamente con X.

