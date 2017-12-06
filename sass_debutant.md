Pas-à-pas pour installer et mettre en place un environnement capable de compiler le sass proprement en utilisant Atom.

##Télécharger et installer NodeJS + node-sass
1. Se rendre sur cette page:
https://nodejs.org/en/

2. Télécharger/installer.

3. Lancer en ligne de commande "npm install"

##Pour pouvoir compiler en Sass
4. Lancer "npm install node-sass -g"
Note: Le -g est un "drapeau" qui ajoute node-sass en environnement global.

5. Il est possible qu'il faille ajouter le PATH pour avoir une variable d'environnement dans Windows.
La procédure est expliquée ici : http://blog.idleman.fr/nodejs-15-installation-sous-windows/
Clic droit sur l'ordinateur, aller dans variable d'environnements, et dans le champ "Path", modifier, puis ajouter après un point virgule (pour ne pas supprimer ce qui existe déjà), le chemin d'installation de nodejs (par exemple c:\Program File\nodejs\).
Taper "node" permet de vérifier s'il n'y a pas de message d'erreur. Note que ceci concerne node et non node-sass.

##Atom + Sass-autocompile
1. Dans Atom -> Packages -> Setting View -> Install Packages

2. Prendre sass-autocompile, il devrait avoir +80 000 téléchargements.



A NOTER :

On peut configurer autocompile pour qu'il parte du dossier scss et qu'il compile vers le dossier css, ce qui m'arrangerait.
Sauf que là je ne trouve plus, je regarderais ça demain, c'est une petite configuration. A l'heure actuelle il enregistre la css dans le dossier où se trouve le scss en le nommant .min.css, ce qui est bof.
---
Réferences
Installation de nodejs : Ici
Vérification de l'installation et erreurs : Ici
Sass-autocompile : Documentation
