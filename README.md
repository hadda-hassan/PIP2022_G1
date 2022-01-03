# PIP2022_G1
N.B :  Attention ICI on partage que le code!!!

_________________________________________________
Sujet de groupe:   Détection d’anomalie supervisée

ici c'est pauline.

__________________________________________________
data:
Jeu de données n°1

---------------------------
Comment utiliser Git
---------------------------

Une démonstration de l'utilisation de Git avec Github. Ce projet vous permet de prendre en main rapidement Git en association avec Github. Les commandes sont directement saisies dans une console. J'utilise terminal sur MAC OS X.

Je liste les commandes de base.

Mémento des principales commandes Git

git init : initialisation d'un projet (si le projet est créé depuis github, ne pas utiliser cette commande) ou réinitialisation d'un projet existant

git status : vérifier le statut, l'état (si modification de fichier) du répertoire de travail (le repository)

git add nom_du_fichier : ajoute un nouveau fichier (du répertoire de travail) à l'index

git add . : ajoute tous les fichiers à l'index

git commit -m "Phrase_explication_détaillée_du_commit" : Ajouter les fichiers de l'index dans un commit

git commit -am "Phrase_explication" : ajouter les fichiers au repositery, directement sans le add si le fichier est déjà ajouté - update de fichiers

git log : Voir l'historique des modifications du commit sous forme de liste

git checkout [sha_du_commit] : se positionner sur un ancien commit - attention le retour à un commit efface les commits les plus récents - si push après retour

git checkout master : retour au commit principal - le dernier

git clone [https_ssh_adresse_du_repositery_github] : rapatrier / clôner les sources d'un remote github vers un ordinateur local

git push origin master : envoyer les modifications des fichiers (le commit) vers github (le remote)

git pull origin master : récupérer les modifications effectuées par d'autres développeurs sur un remote

git pull [url_du_repositery] : récupérer les fichiers d'initialisation en local après la création d'un repositery distant

git branch [nom_de_la_branche] : créer une branche

git checkout [nom_de_la_branche_créée] : se positionner sur la branche créée (raccourci de création)

git checkout -b [nom_de_la_branche] : créer une branche et se positionner sur la branche créée

git push --set-upstream origin [branche-test-01] : envoyer la branche créée sur le remote Github

git push : envoyer les commit dans la branche créée sur le remote (possibilité d'ommettre origin et nom_de_la_branche)

git merge [nom_de_la_branche_à_fusionner] : fusionner les modifications de 2 branches, ici positionné sur master, la branche "nom_de_la_branche_à_fusionner" va fusionner avec la branche master. Attention, rien n'empêche de fusionner master avec une branche secondaire en se positionnant sur une branche secondaire et en codant -> git merge master. Merge ne supprime la branche

git merge [nom_de_la_branche_à_fusionner] --no-ff ou - git merge --no-ff [nom_de_la_branche_à_fusionner] : Merger 2 branches - methode récursive - méthode conseillée pour forcer la création d'un commit et conserver une trace dans l'historique de développement

git branch -d [nom_de_la_branche_à_supprimer] : supprimer une branche en local

git push origin :[nom_de_la_branche_à_supprimer] : supprimer une branche sur le remote github (distante)

git blame [nom_du_fichier_à_vérifier] : savoir qui a modifié une ligne de code précise, la commande affiche une liste avec les modifications effectuées sur le fichier ainsi que le nom de la personne qui a fait la modification

git show [identifiant_du_sha] : afficher le détail précis des modifications sur un fichier et dans un commit précis. L'identifiant du sha est récupéré lors de l'utilisation de la commande blame. Cet identifiant est placé en début de ligne

git stash : mettre de côté des modifications sur un fichier en cours d'écriture (temporairement) - sans faire de commit - travailler sur d'autres modifications - permet alors de faire un commit des modifications sans faire de commit sur les modifications mises de côté

git stash pop : reprendre le développement en cours sur les modifications mises de côté - pop supprime les données dans stash

git remote set-url origin [new_url] : modifier l'url du repositery distant - origin ici (si le nom du repositery n'est pas modifié)

git commit --amend -m "nouveau_message" : modifier le dernier message de commit en local

git push [nom_du_remote nom_de_branche] --force ou -f : envoyer la modification du dernier message sur le repositery à distance

git remote add [nomcourt] [url] : Ajoute un dépôt distant au repositery local

git reset [nom_du_fichier] : Efface le fichier de l'index

git reset HEAD [nom_du_fichier] : Efface le fichier de l'index

git push --set-upstream origin master : permet d'utiliser la commande simple git push (sans origin master)

git rebase -i [numero_commit] : "naviguer" dans les commit - "retour en arrière" - permet de modifier la description d'un commit par exemple - le mode interactif (i pour interactive) ouvre l'editeur - attention ne jamais modifier un ancien commit public sur lequel travaille plusieurs personnes

git reset --hard HEAD^ : permet d'annuler un merge branch en local - si le push sur le repository n'est pas fait

git checkout -f: 'annuler' une suppression - si non commitée

----------------------------
Actions classiques de base
----------------------------
Coder 
Commit 
Push
Pull

-------------------------------------------------
Mémento pour travailler avec des dépôts distants
-------------------------------------------------

git remote : affiche les dépôts distants

git remote add [remote_name] [url: -> git://github.com/to/project.git : ajoute un dépôt distant

git fetch [nom-distant -> ex : origin] : récupère et tire toutes les données sous sa propre branche sans merge (fusion) ajoutées au dépôt distant - recommandé

git pull : récupère et fusionne une branche distante - si clone récupère origin - plus confortable si certain des modifications

git push [remote -> origin] [branche -> master] : pousse les modifications sur un dépôt distant (origin) et daans la branche spécifiée (ici master)

git remote show [nom_distant_repository -> origin] : inspecte le dépôt distant (origin)

---------------
Configurer Git
---------------
git config --list : lister la config

git config --global color.ui false : desactive les couleurs

git config --global color.ui false : desactive les couleurs

-------------------
Commandes terminal
-------------------
mkdir : créer un répertoire

rm -rf : effacer un dossier et ses fichiers (tous même les protégés sans alerte)

cd [nom_dossier_créé] : se placer dans le dossier créée

cat [nom_du_fichier] : lire le contenu d'un fichier par l'intermédiaire d'un terminal
