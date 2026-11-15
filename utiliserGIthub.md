# UTILISER GITHUB

## Création d'un repository github

1. Créer le projet sur l'ordinateur. Par exemple le dossier local contenant le projet pourra s'appeler monProjet.

2. Créer le repository vide sur Github. Ne pas l'initialiser avec un README.md et un .gitignore. Cela compliquerait le workflow inutilement. Copier l'URL créée pour le projet. Elle ressemble à https://github.com/nom-compte-github/monProjet.git.

3. Lier le dossier local au repository distant avec les commandes suivantes :
```bash
git init
git add .
git commit -m "commit initial, configuration"
git branch -M main
git remote add origin https://github.com/nom-compte-github/monProjet.git
git push -u origin main
```

4. Il faut ensuite donner l'identifiant de connexion github puis valider le token comme un mot de passe.


## Lorsque le repository est en avance sur le dossier local

Il arrive parfois que des modifications soient effectuées directement dans le repository github. Dans ce cas, le repository a pris de l'avance sur le dossier local et toute nouvelle modification de ce dernier entraînera un conflit lors du commit. Durant ce conflit il faudra choisir les versions à conserver.

Pour éviter cela, il est possible de mettre à jour le dossier local facilement si aucune modication n'a été faite sur celui-ci.

1. Vérifier que le dossier local est propre :
```bash
git status
```

2. Si aucune modification n'a été effectuée dans le dossier local, récupérer et fusionner les modifications du repository :
```bash
git pull origin main
```

3. Puis commiter pour synchroniser :
```bash
git add .
git commit -m "mise à jour du dossier local en retard"
```