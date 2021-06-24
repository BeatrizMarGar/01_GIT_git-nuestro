#¿Qué comando utilizaste en el paso 11? ¿Por qué?

Para eliminar el último commit y además elimiar los cambios en el working copy, el comando que se debe utilizar es *git reset --hard HEAD~1*

#¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?

Para mover el HEAD a nuestro anterior commit, el comando utilizado ha sido *git reset --hard HEAD@{1}* Esto mismo podría realizarse también mediante *reflog* y un *reset --HARD* junto con el identificador del cambio anterior.

#El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?

En este paso no hubo ningún conflicto, ya que la rama style actualmente contiene los commits de la rama master. Git nos informa de esto con el siguiente mensaje 
*$ git merge master
Already up to date.*

#El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?

Como la rama *styled* absorbe *htmlity*, para realizar el merge se emplea *$ git merge htmlify*. En este punto se genera un conflicto porque la información de git-nuestro.md es diferente en cada una de las ramas, y git nos informa con el siguiente mensaje *CONFLICT (content): Merge conflict in git-nuestro.md*. Para solucionarlo, se debe editar el archivo git-nuestro.md mediante el comando *nano git-nuestro.md* y realizar los cambios, en este caso para que el resultado sea el que teníamos en la rama *styled*. Una vez guardado este cambio, se termina el *merge* añadiendo git-nuestro.md al repositorio.

#El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?

El merge, en este caso merge fast-forward (*$ git merge --no-ff styled*)
de *master* con *styled* no causó ningún conflicto.

#¿Qué comando o comandos utilizaste en el paso 25?

Para poder dibujar el diagrama he usado el comando *$ git log --graph --pretty=oneline* con el siguiente resultado:
*   bebb1532345344d0dd9bdcdaa58bf6912ba3c579 (HEAD -> master) Merge branch 'styled'
|\
| *   8239b3e0c7cc1d04c192ee52883cc60ccf5b3dd6 (styled) P20: resolucion de conflicto con merge
| |\
| | * 200f442274ee210c36886d06d9ec5976d5dd8c20 (htmlify) P18: tercera modificacion y commit de git-nuestro
| |/
|/|
| * c5da8d661c9c7f01ceb87a7fddfa6e617c1d10f0 P10: segunda actualización de git-nuestro
|/
* c0842c2c42f2daa469802f29e5d4700d07e7d876 P4: primer commit de git-nuestro

#El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?
En este paso se ha podido realizar un merge fast forward, dado que en la rama *title* tiene la información que contenía la rama *master*, con la única modificación del título de git-nuestro.md

#¿Qué comando o comandos utilizaste en el paso 27?

Para no modificar el los cambios del working copy al deshacer el merge anterior, se ha utilizado el comando *git reset HEAD~1*. Para cambiar también los cambios del working copy, que no es el caso, se debería haber utilizado *git reset --hard HEAD~1*

#¿Qué comando o comandos utilizaste en el paso 28?



#¿Qué comando o comandos utilizaste en el paso 29?
#¿Qué comando o comandos utilizaste en el paso 30?
#¿Qué comando o comandos usaste en el paso 32?
#¿Qué comando o comandos usaste en el punto 33?
