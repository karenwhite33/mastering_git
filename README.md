- ¿Qué comando utilizaste en el paso 11? ¿Por qué?
$ git reset-hard HEAD~1
por que este comando me permite deshacer el ultimo commit y lo que hay en el working copy.

- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?
para rehacer el ultimo commit debo hacer un reflog, buscar el commit que necesito, en este caso el commit antes de deshacer y copiar su hash.
Luego aplico $ git reset --hard <hash ultimo commit> y el ultimo commit o el especificado con el hash se rehace y lo verifico con gitlog o reflog y ahi vuelve a aparecer.

- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
no causo conflictos pues estoy en la rama "styled" en donde hice las modificaciones que eran solo de formato, no de contenido y la rama main sigue estando igual o sin ningun cambio desde que se creo 'styled'. No se crearon mas lineas o agrego o quito texto por lo que no se presenta conflicto.

- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?
si por que el archivo .md en la rama htmlify tuvo modificaciones de formato HTML y el archivo .md de la rama styled solo tiene modificaciones en markdown, en texto plano y git detecta esto como cambio en las mismas lineas.

- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
- no ninguno pues al resolver los conflictos anteriores, quedarnos con el contenido de la rama styled, hacer el add y luego el commit y pasa a la rama main para que asorba styled, el main y styled tienen la misma info, styled solo tienen ** en unas palabras pero no ha cambiado el contenido original.

- ¿Qué comando o comandos utilizaste en el paso 25?
$ git log --graph --decorate --pretty=oneline

- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?
si por que la rama main no ha tenido commits pendientes o nuevos desde que se creo la rama title, entonces tambien se podia haber hecho el ff, la unica diferencia es que en no-ff puedo dejar el rastro de ese commit con un msj de por que lo hice o alguna aclaracion necesaria para el equipo.

- ¿Qué comando o comandos utilizaste en el paso 27?
$ git reset --soft HEAD~1 asi continuo con los cambio en el working copy.

- ¿Qué comando o comandos utilizaste en el paso 28?
$ git reset --hard HEAD, asi descarto los cambios que tengo en el working copy.

- ¿Qué comando o comandos utilizaste en el paso 29?
$ git branch -D title

- ¿Qué comando o comandos utilizaste en el paso 30?
$ git reset --soft 65fe73e
ahi quedan archivos en el stating apra hacer commit
$ git commit -m "rehacer el merge del title en main"

- ¿Qué comando o comandos usaste en el paso 32?
$ git checkout af868ea

- ¿Qué comando o comandos usaste en el punto 33?
$ git checkout 58df1b7
