## Rebase
## ¿Para qué sirve hacer git rebase?
Supongamos que creamos un feature con ciertos cambios, pero main recibió código de algún pull request de otra persona, entonces el diagrama del estatus actual se vería de la siguiente manera:
![image](https://github.com/rafaelortegar/starting_with_github/assets/51694410/e94a5e4e-ec6f-477c-bfa0-0bc24658e3ae)

Podría ser que quieras integrar los cambios que se encuentran en main a tu feature, para asegurarte de que tus cambios no afectarán a los que ya se encuentran en main:
![image](https://github.com/rafaelortegar/starting_with_github/assets/51694410/507398d8-b368-4d80-98eb-42ec92493178)

Al momento de realizar un rebase, todos tus cambios estarán "como si hubiesen iniciado después del estado actual de la rama main"
![image](https://github.com/rafaelortegar/starting_with_github/assets/51694410/bec1274f-0761-4893-99f7-8426570303d0)

Esto sirve para mantener una historia lineal de un proyecto, evitando tener ramas que salen de otras ramas.

## Diferencias entre git merge y git rebase:
Git merge, a diferencia de git rebase, crea dos commits distintos, uno de cada rama.
Git rebase ejecuta los cambios de una rama sobre otra y los aplica como si los cambios fueron realizados directamente en esa rama.

## ¿Cómo hacer rebase de una rama a tu rama local?
```bash
# moverte a la rama main (o a la rama desde la cual quieres realizar el rebase)
git checkout origin/main

# Jalar los cambios remotos a tu repositorio local
git pull

# regresar a tu rama
git checkout <nombre de tu rama>

# Iniciar un rebase interactivo
git rebase -i

# realizar las modificaciones
# utilizar git add para agregar los archivos modificados
git rebase --continue
# o, para saltarse los cambios:
git rebase -skip

# al final del rebase, deberás hacer push a tu rama remota.
```

