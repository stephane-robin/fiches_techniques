# CREATION D'UN MKDOC MATERIAL

Il faut avoir installé Python préalablement sur la machine.


## Construction du projet

1. Créer le dossier hébergeant le projet :
```bash
mkdir monProjet
cd monProjet
```

2. Créer un environnement de développement qu'on appela .venv, à la racine du projet :
```bash
python3 -m venv .venv
```

3. Activer l'environnement de développement :
```bash
source .venv/bin/activate
```
L'invite de commande affiche le nom de l'environnement entre parenthèses (.venv)

4. Installer MkDocs Material dans l'environnement :
```bash
pip install mkdocs-material
```

5. Construire la structure du projet :
```bash
mkdocs new .
```
Le fichier automatiquement créé ***mkdocs.yml*** est un fichier de configuration. Le dossier **docs/** contient par défaut le point d'entrée ***index.md***.

6. Configurer ***mkdocs.yml*** :
```bash
site_name: monProjet
theme:
  name: material
  language: fr
```

7. Tester le site en local :
```bash
mkdocs serve
```
puis ouvrir le navigateur à l'adresse http://127.0.0.1:8000

8. Créer le repository github.

9. Héberger le site sur github pages (déploiement sur la branche **gh-pages** du repository) :
```bash
mkdocs gh-deploy
```
Puis se rendre sur le repository github du projet, dans **Settings/pages**. Il apparaît alors l'adresse à laquelle le site est visible live.


## Fermeture du serveur

1. Arrêter le serveur :
```bash
Ctrl+c
```

2. Arrêter l'environnement de développement :
```bash
deactivate
```


## Modification du projet

1. Relancer l'environnement de développement :
```bash
source .venv/bin/activate
```

2. Tester le site en local :
```bash
mkdocs serve
```
puis ouvrir le navigateur à l'adresse http://127.0.0.1:8000

3. Procéder aux modifications sur VS Code.

4. Mettre à jour le commit sur github pour assurer le déploiement des modifications sur le site :
```bash
git add .
git commit -m "résumé des modifications"
git push
```

