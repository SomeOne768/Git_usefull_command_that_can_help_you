Commande récurrente:

git init .
git config --list [permet de vérifier qu'on est sur le bon dépot avec les bons identifiants]
git config user.email mon@mail
git config user.name username
git status
git add [* | file]
git rm [file]
git commit -m "Mon message"
git push 
git pull
git config -[h | a]
git config credential.


Eviter de retaper ses identifiants:

Dans les projets qui le necessite (comme par exemple celui avec le raspberry) je genererai un token public qui permettra de clone/pull automatiquement de manière automatisé

Setting -> developper setting -> generate token with the good options (be carefull)

script pour automatiser:

script.sh (faire un chmod +x)
#!/bin/bash
cd repo && git [clone | pull] "https://<token>@github.com/SomeOne768/repo"

ajouter le ./script.sh au crountab (linux)