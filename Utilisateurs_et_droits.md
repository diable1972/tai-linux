* Les utilisateurs et les droits


## Sommaire

* Gestion des utilisateurs et des groupes
* Gestion des droits UGO
* Gestion des ACL

## Gestion des utilisateurs et des groupes

### Gestion des utilisateurs

Un utilisateur est identifié par :
* un login
* un identifiant numérique (UId)
* un groupe principal
* une liste de groupes secondaires

L'administrateur s'appelle root et a l'UId 0.

Pour créer un utilisateur :
* `useradd thierry`
* commande complète : `useradd -m -d /home/thierry -s /bin/bash thierry`

Pour créer le groupe apprenants :
* `groupadd apprenants`

Pour ajouter thierry au groupe apprenants :
* `usermod -aG apprenants thierry`

Pour afficher la liste des groupes de l'utilisateur thierry :
* `groups thierry`

Mise en pratique :
* créer un utilisateur "webapp" groupe principal www-data groupe secondaire applis dossier principal /home/system/webapp shell /bin/false

```bash
sudo mkdir /home/system
sudo groupadd www-data
sudo groupadd applis
sudo useradd -m -d /home/system/webapp -g www-data -G applis -N -s /bin/false webapp
```

# changer le mot de passe `passwd`

1. installer la machine 
   * mettre un mot de passe root simple et qui marche en azerty et en qwerty
   * decocher "intreface de bureau" et "gnome" et **cocher "serveur ssh*""*

2. Se connecter sur la machine , et devenir root  avec `su -`

3. changer le mot de passe root , avec un mot de passe sécurisé, en utilisant `passwd`

4.Installer sudo avec `apt install sudo`

5.Donner les droits sudo à l'utilisateur de base (ici hb) : `usermod -aG sudo hb`

6.Vérifier que le user a bien récupéré le groupe : `groups hb`

7.couper complètement la session root + la session hb (fermer la connexion ssh ) puis se re connecter.

8.Rechercher puis appliquer les mise à jour :
```bash
sudo apt update
# pour mettre à jour un seul paquet, par exemple apache2: sudo apt install apache2
# pour metre à jour tous les paquets :
sudo apt upgrade

# pour désinstaller mais garder les fichiers de config, par exemple apache2
sudo apt remove apache2
# pour désinstaller complètement :
sudo apt purge apache2
```














      




