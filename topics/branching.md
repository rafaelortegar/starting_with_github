Manejo de ramas:
* ver la lista de ramas locales y conocer la rama actual:
```bash
git branch
```

* cambiar de rama:
```bash
git checkout <nombre_de_rama>

# Nueva version:
git switch <nombre_de_rama>
```

* Crear una nueva rama localmente:
```bash
git checkout -b <nombre_de_rama>

# Nueva version:
git switch -c <nombre_de_rama>
```

* Crear una rama desde un commit específico:
```bash
git log
git branch <branch name> <identifier>
```

* Crear una rama desde otra rama:
```bash
git checkout -b <nombre de tu nueva rama> <nombre de la rama existente>

# Nueva version:
git switch -c <nombre de tu nueva rama> <nombre de la rama existente>
```

* Descargar a tu local una rama remota:
```bash
git pull origin <branch name>
git branch
git checkout <branch name>
git branch

# Nueva version:
git pull origin <branch name>
git branch
git switch <branch name>
git branch
```


