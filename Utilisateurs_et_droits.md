# Les utilisateurs et les droits


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









