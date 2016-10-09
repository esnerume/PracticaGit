#Solución a la práctica

##¿Qué comando utilizaste en el paso 11? ¿Por qué?
Comando:

    git reset --hard HEAD~1

Con el comando ***git reset*** podemos desplazarnos entre los commits que se ha ido haciendo. En nuestro caso, cuando usamos ***'HEAD~1'*** retrocedemos al commit anterior. Además usando el parámetro ***'--hard'*** descartamos/eliminamos todo los posibles cambios que haya en la working copy.

##¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?
Comandos:

  git reflog
  git reset --hard 2e8d7c8

Primeramete utilizo el comando ***git reflog*** que me saca el histórico de todas las operaciones que hemos ido haciendo. Una vez que git me lista las operaciones, busco el hash del commit anterior (el deshecho). En mi caso, el hash era 2e8d7c8. Volví hacer un ***git reset --hard*** añadiendo el hash del commit al que quería regresar. Aunque en este caso no había modificado nada, me siento más agusto utilizando parámetro --hard para tener el working copy con una foto exacta de ese commit.


##El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?

No, este merge no causó ningún conflicto porque la rama ***styled*** contiene todos los  ***commits*** incluidos en la rama ***master***.

##El merge del paso 19, ¿Cuasó algún conflicto? ¿Por qué?

Sí, en este caso el merge **sí crea un conflicto** ya que trata de unir dos ramas en las que se modifican las mismas líneas del fichero ***git-nuestro.md***. En nuestro caso, hemos resulto los conflictos quedándonos con la versión del fichero de la rama style y descartando los cambios relativos a html. Una vez resueltos los conflictos a nivel de fichero volvemos a hacer un add para indicarle a Git que ya hemos resuelto los conflictos. Después ha hacer commit ya se finaliza el merge.

##El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?

No, no hay ningún conflicto en este caso, porque el puntero de la rama que absorbe ***master*** se quiere mergear con otro situado por encima. Git resuelve esta situación con un ***fast-forward*** en el que avanza el puntero de la rama ***master*** al mismo punto donde está el puntero de la rama con la que se hace el merge. (***styled***). El fichero ***git-nuestro.md*** contiene todas los cambios de ambas ramas, así que no existe conflicto posible.

##¿Qué comando o comandos utilizaste en el paso 25?
Comando:

  git log --graph --decorate --pretty=oneline


##El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?

Sí, podría ser fast forward porque la rama ***title*** se creó a partir de la rama ***master*** y la rama ***master*** no hay sido modificada, por tanto podría ser fast forwads ya que bastaría simplemente con mover el puntero de la rama ***master*** al commit (en el que hemos añadido el título) que habíamos realizado en la rama ***title***.

##¿Qué comando o comandos utilizaste en el paso 27?
Comando:

  git reset HEAD~1

Movemos el puntero al commit inmediatamente anterior. Al contrario que en la pregunta del paso 12, en este caso no usamos el modificador ***--hard*** ya que queremos mantener los cambios en la ***working copy***).

##¿Qué comando o comandos utilizaste en paso 28?
Comando:

  git checkout -- git-nuestro.md

##¿Qué comando o comandos utilizaste en el paso 29?
Comando:

  git branch -D title

##¿Qué comando o comandos utilizaste en el paso 30?
Comandos:

  git reflog

  git reset --hard 741aa70

##¿Qué comando o comandos utilizaste en el paso 32
Comandos:

  git reflog

  git reset --hard 59dd2aa


##¿Qué comando o comandos utilizaste en el paso 33?
Comandos:

  git reflog

  git reset --hard 741aa70
