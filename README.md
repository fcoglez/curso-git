GIT


1. Instalamos git en nuestro ordenador https://git-scm.com/downloads

1. Comprobamos que se ha instalado con el comando git --version

1. Configuramos nuestro nombre y email con git config --global user.name "nombre usuario" y git config --global user.email "nombre correo electronico"

1. Para poder hacer un control de versiones en un directorio, en la consola ponemos git init. Ahora ya podemos usar los comandos de git.

COMANDOS BASICOS

git status -> muestra el estado actual del repositorio. Proporciona información sobre los archivos modificados, los archivos que están en el área de preparación (staging area) y los archivos que no están bajo seguimiento.

git commit -m nombreCommit ->  guarda los cambios realizados en el área de preparación en el historial del repositorio, junto con un mensaje que describe los cambios. Esto los hace permanentes y recuperables en el futuro. Siempre debemos de poner un comentario al commit, para ello se usa el -m "message".

git log ->  se utiliza para ver el historial de commits en un repositorio Git. Proporciona detalles sobre quién realizó cada commit, cuándo se realizó y los mensajes asociados a cada cambio. Es una herramienta útil para entender la evolución del proyecto y rastrear cambios específicos.

git checkout nombreFichero -> Si en un fichero hacemos cambios pero no tiene un commit echo, con este comando, volvemos a la version que estaba el ultimo commit de dicho fichero.

git log --graph -> Muestra el historial de commits en forma de grafo, lo que facilita la visualización de las ramificaciones y fusiones en el desarrollo del proyecto.

git checkout numeroHash -> Con este comando, nos movemos a la fotografia de como estaba el proyecto en ese momento.

git reset --hard numeroHash -> Podemos volver al commit con dicho hash aunq haya 20 commit por detras. Y desaparece todo los commit que habia por delante.

git reflog -> Historial completo de todas los commit echos en el proyecto.

git tag -> Se usa para poner etiquetas importantes a un commit cualquiera.



RAMAS

git branch nombreRama -> Se usa para crear nuevas ramas.

git switch nombreRama -> Se usa para cambiar de una rama a otra.

git branch -m nombreRama -> El significado de -m en este comando es simplemente abreviatura de "move" (mover). Indica que deseas mover o renombrar la rama especificada por nombreRama a un nuevo nombre.

git branch -d nombreRama -> Se usa para borrar ramas.


MERGE

git merge nombreRama -> Se usa para unir lo que hay en un rama en otro. Por ejemplo si estoy trabajando en mi rama personal de un proyecto creada para trabajar solamente yo, y en la rama main del proyecto hay cambios, desde mi rama personal, lanzo el git merge y esos cambios se vienen a mi rama tambien.







GIT HUB


Para poder trabajar con nuestro equipo en local y poder subir los cambios al servidor de git hub, debemos de configurar la configuracion de ssh.

1. comprobamos que tengamos claves ssh generadas. Si no la tenemos ver video https://www.youtube.com/watch?v=rVvNn0ZEy7s
1. comprobamos la conexion ssh de nuestro equipo con git hub mediante el comando ssh -T git@github.com



Cuando tengamos conexion con nuetro equipo local y queremos subir los cambios a un repositorio de git hub, usamos el comando git remote add origin <URL\_del\_repositorio\_remoto> y justo despues git push -u origin main




























