# Crear repositorio desde cero
Crear repositorio por primera vez
## Crear un repositorio remoto
1. Crear un repositorio nuevo, agrega nombre
2. Seleccione Public o Private
3. Selecciona Agrega Readme.md
4. Selecciona License
Segun lo que se requiera

## En repositorio local
```
git init
git add .
git commit -m "Confirmación inicial"
```
## Fusionar remoto con local
```
git remote add origin https://github.com/jhonn/repositorio.git
git pull origin main --allow-unrelated-histories --no-rebase
```
origin (alias de la repo remota)
git remote (El comando remote por sí solo muestra la lista de controles remotos que conoce su repositorio local)
git pull <alias> <rama>
--allow-unrelated-histories (necesaria la primera vez que fusionamos porque los directorios remoto y local se generaron por separado, no comparten historial)

## Subir la rama local a remoto
```
git add .
git commit -m "Actualizacion de la rama"
git push -u origin main
```

## configuraciones globales en github opcional
-----
```
git config --global init.defaultBranch <nombre>  #Los nombres comúnmente elegidos en lugar de 'master' son 'main', 'trunk'

git config --global pull.rebase false  # Esto hará que Git realice una fusión (merge) de los cambios del repositorio remoto con tu repositorio local de forma predeterminada
```

## Vim
salir (Esc) luego :wq

# Crear rama y subir a rama remota
```
git checkout -b nombre_de_rama
git branch       # Ver las ramas
git add .
git commit -m "Commit de la rama"
git push -u origin nombre_de_rama
```

# Fusionar rama en local
```
git checkout [rama_estable]
git merge [rama_desarrollo]
git pull origin [rama_estable]
```
