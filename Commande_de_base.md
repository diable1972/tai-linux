# Commandes de base sous linux


## Sommaire

* Manipulation des fichier et des répertoires
* Gestion des users et des droits
* Gestion des logiciels
* Commande avancées

## Concepts généraux
Commande : Logiciels lancé sans interface graphique
Kiss : *keep it simple and stupid* - chaque commande ne fait q'une seule chose, on enchaine les commande pour faire des action complexes
Chainer des commandes : on utilise le `|`

Les redirections :
* \> : crée et ecrit dans un fichier : exemple : `sort /etc/passwd > /tmp/users_tries.txt`
* \>\> : ajoute à la suite du fichier : `date >> /tmp/date.txt`
aide sur une commande  : `man` + la commande , exemple : `man ls`

### Manipulation des fichiers et des répertoires

* oû suis-je ? `pwd` pour *print working directory*
* afficher le contenu d'un dossier ? `ls`
* changer de repertoire courant ? `cd` + le répertoire (pour change directory), par exemple `cd/tmp`
  * `cd` sans argument ramène dans le répertoire personnel
  * `cd -`  revient au dossier précédent
* créer un fichier vide ? `touch`
* editer un fichier ? `nano` + le non du fichier
* compresser un dossier/fichier ? `tar cvf` + nom de l'archive + nom du fichier /dossier à compressée
 * sans compression : `tar cvf achive.tar /home/barth/projets`
 * avec compression : `tar czvf achive.tar.gz /home/barth/projets`
* extraire une archive tar ? `tar xzvf glpi.tar.gz`
* afficher le contenu d'un fichier ? `cat` + chemin vers le fichier
* compter le nombre de lignes dans un fichier ? `wc -l` +chemin vers le fichier (pour *word count*)
* afficher la fin d'un fichier ? `tail` + le chemin du fichier
* afficher en temps réel la fin d'un fichier ? `tail -f`
  

