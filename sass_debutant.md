Pas-à-pas pour installer et mettre en place un environnement capable de compiler le sass proprement en utilisant Atom.

## Télécharger et installer NodeJS
1. Se rendre sur cette page:
https://nodejs.org/en/

2. Télécharger/installer.

3. Lancer en ligne de commande "npm install"

## Pour pouvoir compiler en Sass
4. Lancer "npm install node-sass -g"
**Note:** Le -g est un "drapeau" qui ajoute node-sass en environnement global. L'oublier génèrera un message d'erreur au moment de la compilation de type "commande interne ou externe non trouvée" car le package ne sera pas installé.

5. Il est possible qu'il faille ajouter le PATH pour avoir une variable d'environnement dans Windows.
La procédure est expliquée ici : http://blog.idleman.fr/nodejs-15-installation-sous-windows/
    * Clic droit sur l'ordinateur
    * Aller dans variable d'environnements
    * Dans le champ "Path". Modifier > Ajouter un point virgule après le contenu existant si nécessaire, puis le chemin d'installation de nodejs (par exemple c:\Program File\nodejs\).
    * Taper **"node"** dans la console permet de vérifier s'il n'y a pas de message d'erreur. (Concerne node et non node-sass).

## Atom + Sass-autocompile
1. Dans Atom -> Packages -> Setting View -> Install Packages

2. Prendre sass-autocompile. Il en existe d'autres avec un nom plus ou moins similaire, prendre le plus téléchargé.

### Configuration

* Pour automatiser la prise en compte des partials (fichiers commençant par un _ importés dans le fichiers .scss principal)
    * Ajouter en première ligne des fichiers partiels :
// main: main.scss (et remplacer le nom du fichier scss si besoin).
*> Topic référent :* https://discuss.atom.io/t/sass-autocompile/40677/10

* Pour sauvegarder dans un autre dossier les fichiers compilés et ne pas avoir un fichier nommé ".min.css" à côté des ".scss"
    * Ajout en première ligne de :
    // compileCompressed: ../css/$1.css
    * Cette ligne remonte d'un dossier puis range dans le dossier **css** un fichier où le $1 sera remplacé par le nom du fichier suivi de l'extension ".css".
*> Topic référent :* https://discuss.atom.io/t/issues-questions-feedback-about-sass-autocompile/15233/9


--
### Réferences
**Installation de nodejs :** Ici
**Vérification de l'installation et erreurs :** Ici
**Sass-autocompile :** Documentation https://atom.io/packages/sass-autocompile
