# Creación y carga de un commit

¿Qúe es un commit?
Podríamos pensar en un commit como una captura instantánea de los cambios realizados sobre el repositorio de forma local.

Estas capturas instantáneas pueden ser consideradas como versiones "seguras" o listas para subir de un proyecto.

Para poder subir tus cambios locales a la rama remota, tienes que correr los siguientes comandos:

```bash
# revisar los archivos modificados
git status

# añadir los archivos que quieres agregar al commit
git add <ruta y nombre del archivo>

# Para que se abra el editor de textos y crees el mensaje de commit ahi: (si quieres que se abra en visual studio code y no en vim, deberás correr el siguiente comando: git config --global core.editor "code --wait")
git commit

# Para agregar el mensaje de commit desde la línea de comandos:
git commit -m "mensaje del commit"

# hacer push de tus cambios locales a la rama remota
git push
```

En el caso de que quieras modificar el mensaje del último commit o el ultimo commit, deberás correr el siguiente comando:
```bash
git commit --amend
```

Si quieres modificar el commit sin modificar el mensaje:
```bash
git commit --amend --no-edit
```



