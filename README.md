# TP Initiation GIT

Bienvenu·e sur Github !

Je vous fais vite fait un petit récap de ce qu'est **Git** :
> Git est un outil pour versionner vos projets. Vous envoyez votre projet dans un **repository** (similaire à des dossiers) sur des platformes tel que Github, Gitlab ou *Gitea* dans le cas d'YNOV. Ainsi vous pouvez partager ou encore travailler à plusieurs sur vos projets.

Dans ce TP, vous appliquerez les notions vues précédemment. Ainsi vous comprendrez un peu mieux le fonctionnement des commandes.

Le TP se fera en 2 parties. Dans la première, vous manipulerez sur un repository seul pour que vous vous familiarisez avec l'outil. Dans la seconde partie, vous serez en groupe sur un seul repository.

---
## Sommaire

- [TP Initiation GIT](#tp-initiation-git)
	- [Sommaire](#sommaire)
- [Installation](#installation)
	- [Windows](#windows)
	- [Mac](#mac)
	- [Linux](#linux)
- [Partie 1 - Familiarisation](#partie-1---familiarisation)
	- [Objectif](#objectif)
	- [Création de votre repository](#création-de-votre-repository)
	- [Manipulation](#manipulation)
- [Partie 2 - Travailler en groupe](#partie-2---travailler-en-groupe)
	- [Objectif](#objectif-1)
	- [Repository du groupe](#repository-du-groupe)
	- [Manipulation](#manipulation-1)
		- [Problème pour push](#problème-pour-push)
		- [Aucun souci](#aucun-souci)

# Installation

Avant de commencer, il faut s'assurer que vous avez l'outil sur votre machine.

Pour cela, ouvrez un terminal.
> Sous **Windows**, cherchez `cmd` dans la recherche de la barre des tâches.\
> Sous **Mac**, faites le raccourci `Command + Barre d'espace` et tappez `Terminal`.\
> Sous **Linux**, cherchez dans vos applications `Terminal`.

Pour vérifier que vous avez Git, faites la commande suivante :
```shell
> git --version
```
Si vous avez une erreur, alors il faudra l'installer.
## Windows
Pour windows, téléchargez l'installeur via [cette page](https://git-scm.com/download/win).

Pas besoin de modifier les paramètres d'installation, laissez par défaut.

## Mac
Toutes les informations se situent sur [cette page](https://git-scm.com/download/mac).

## Linux
Les informations sont sur [cette page](https://git-scm.com/download/linux). Prenez bien la commande en fonction de votre distribution.

# Partie 1 - Familiarisation
## Objectif
L'objectif de cette partie est de vous familiariser avec l'outil **Git** afin de comprendre son fonctionnement et de pouvoir l'utiliser dans des projets de groupe.

## Création de votre repository

> On utilisera le mot `repo` pour dire `repository`.

Sur [Gitea](https://git.ytrack.learn.ynov.com/), vous pouvez créer un nouveau repository avec le bouton suivant :

![](./images/create_repo.png)

Appelez votre repo **tp-git-initiation**
> Pas besoin de modifier les autres options, donnez lui juste un nom.

Une fois créé, nous pouvons commencer le TP.

## Manipulation
> En cas de souci, une doc récapitulative se situe [ici](./doc/).\
> À chaque étape, vérifiez votre repo sur Gitea pour confirmer les modifications.
1. Clonez votre repository.
	- Sur votre terminal, entrez la commande `git clone url`.
		- Pour ouvrir le terminal, regardez la partie [Installation](#installation). Une explication rapide s'y trouve.
		- Vous trouverez les explications de la commande dans la [documentation](./doc/).
		- Vous trouverez l'url ici :

		![](./images/link_repo.png)
    - Un dossier a dû être créé à l'endroit où vous avez cloné votre repo.
		- Ouvrez ce dossier avec **Visual Studio Code** (Plus couramment `VScode`).
		- Vous pouvez télécharger VScode ici : [<img src="https://img.shields.io/badge/Visual%20Studio%20Code-0078d7.svg?style=for-the-badge&logo=visual-studio-code&logoColor=white" width="20%">](https://code.visualstudio.com/download)
	- Toutes les étapes qui vont suivre se feront sur **VScode**.
		- Vous pouvez ouvrir un terminal dans le menu en haut de VScode :

		![](./images/open_terminal.png)

	> ⚠ Si vous êtes sur **Mac**, vous devez créer un fichier `.gitignore` et écrire dans ce fichier : `.DS_Store`. N'oubliez pas de l'enregistrer.\
	> Une fois cela effectuer, il faudra l'ajouter à votre repo pendant l'étape 3.
2. Créez un fichier au nom de `hello.txt` dans le dossier du repository sur votre pc.
	- Sur **VScode**,  vous pouvez créer un fichier ici :

	![](./images/new_file.png)
	- Dans ce fichier écrivez `Hello World!` et enregistrez le.
	- Effectuez un `git status` pour voir les changements qui ont été effectués en local.
		- Un joli texte rouge écrit `hello.txt` devrait s'afficher.
3. Ajoutez ce fichier à votre repo (il doit apparaître sur le repo Gitea 👀).
	- Vous devez vous servir de la [doc](./doc/).
		- Il s'agit des commandes de bases (`git add`, `git commit`, `git push`)
			- Ces commandes doivent être utilisées pour envoyer des nouveaux fichiers ou des modifications des fichiers déjà existants.
			- Pour la commande `git commit`, le message doit contenir les modifications effectuées. Dans notre cas, le message sera `Adding hello.txt`.
		- En exécutant `git commit`, vous aurez certainement une erreur. Allez dans [cette partie](./doc/README.md#erreur-de-commit) pour régler ce problème.
	- Pour s'assurer que tout est bon, faites un `git status`.
4. Recréez un autre fichier que vous appelerez `world.txt` et ajoutez le à votre repo.
5. Maintenant, il faut **revert** votre commit.
    - L'objectif est de revenir un pas en arrière, donc l'étape 4 sera annulée.
	- Si vous avez regardez la doc, la commande adapté demande un `hash`
		- Vous trouverez ce hash sur la page **Gitea du repo** à cet endroit :

		![](./images/where_hash.png)
		- Sinon, vous pouvez cliquer sur `Commits` pour lister vos commits avec les hash de chacun.
		- Quand vous allez exécuté la commande, vous aurez ceci :

		![](./images/revert_commit.png)
		- Pas de panique ! Vous pouvez juste fermez cette page et le commit se fera tout seul.
		- Il ne vous restera plus qu'à push !
    - Vous devez avoir à ce point, seulement le fichier `hello.txt` de l'étape 3 dans votre repo.
6. Créez un fichier qui aura pour nom `rouge.exe`
> ⚠ Le nom est important !
7. Ajoutez le à votre repo.
	- Les commandes classiques (`git add`, `git commit`, `git push`).
	- Normalement, vous ne pourrez pas push, vous aurez un joli texte rouge écrit :
	```
	 ! [remote rejected] master -> master (pre-receive hook declined)
	error: failed to push some refs to 'https://git.ytrack.learn.ynov.com/NOMUTILISATEUR/tp-git-initiation.git'
	```
	- Cette erreur est due au fait que la plateforme n'accepte pas les fichiers `.exe` (les fichiers exécutables)
8. Corrigeons cette erreur ! Utilisons le **reset**.
	- Comme nous n'avons pas pu effectuer l'envoi de notre fichier au repo, nous devons annuler notre commit en cours.
		- Vous pouvez voir que le commit est en attente de push avec un `git status`.
	- Servez vous de la [documentation](./doc/).
		- Nous voulons **revenir seulement d'un commit en arrière** et **retirer les modifications en local**.
	- Une fois la commande effectuée, vous ne devriez plus avoir le fichier `rouge.exe` et la commande `git status` devrez vous dire que vous êtes à jour.
9. Créez une branche `tomate` et sélectionnez la.
	- Aidez vous de la [documentation](./doc/) pour ça.
	- Pour vous assurez que vous avez bien sélectionné la branche, effectuez la commande `git status`. Vous devrez avoir ce résultat :

	![](./images/select_branch.png)
10. Modifiez le fichier `hello.txt`.
	- Changez le texte par `Good bye World!` et enregistrez le fichier.
11. Créez un nouveau fichier qui aura pour nom `feuille.txt`.
12. Faites un commit avec ces modifications.
	- Pour allez plus vite, vous pouvez faire un `git add .`
		- Cette commande ajoutera toutes les modifications qui ont été effectuées en local.
		- Le `git add` ne sert pas uniquement à envoyer un nouveau fichier, mais aussi à envoyer les modifications des fichiers déjà existants.
	- Comme pour l'ajout de `hello.txt`, 
	- Vous pouvez avoir l'erreur suivante :

	![](./images/push_branch_error.png)
	- Pour corriger cette erreur, faites la commande suivante :
	```shell
	> git push --set-upstream origin tomate
	```
13. Sélectionnez sur la branche **master**.
14. Faites une modification sur le fichier `hello.txt`.
	- Remplacez le texte par `Say Hello World!` et enregistrez le fichier.
15. Faites un commit avec vos modifications.
16. Effectuez un merge avec la branche `tomate`.
	- À cette étape, vous êtes normalement sur la branche **master**.
		- Faites une vérification avec la commande `git status`.
	- Pour fusionner la branche **tomate** avec la branche **master**, faites la commande de merge trouvable dans la [documentation](./doc/).
17. Oups ! Vous avez un conflit ( ͡° ͜ʖ ͡°) . On va régler ça !
	- Dans votre fichier `hello.txt` vous devriez avoir ce texte :
	```
	<<<<<<< HEAD
	Say Hello World!
	=======
	Good bye World!
	>>>>>>> tomate
	```
	- L'erreur qu'il y a eue est un **conflit**. **Git** a donc remplacé la ligne contenant le conflit par ce texte.
	- Le conflit est représenté en 2 parties séparées par des "=".
		- Sur la partie supérieure représentée par `<<<<<<< HEAD`, il s'agit de la modification qu'il y a sur la branche actuelle, soit la branche **master**.
		- Sur la partie inférieure représentée par `>>>>>>> tomate`, il s'agit de la modification qu'il y a sur la branche avec laquelle vous voulez effectuer votre merge.
	- Pour corriger ce conflit, il vous suffit de retirer les parties non désirées.
		- Dans notre cas, on va garder notre `Good bye World!`
			- Modifiez à la main le fichier pour garder uniquement ce texte. Pensez à enregistrer le fichier.
	- Une fois cela effectué, vous pouvez faire un commit (`git add`, `git commit`, `git push`).
		- Pensez à expliquer dans le message de votre commit, les modifications effectuées d'une manière très condensée.

Bien, maintenant que vous avez fait cette première partie en étant seul, vous allez vous mettre un peu plus dans la plus grande utilisation de Git : un travail de groupe.

# Partie 2 - Travailler en groupe
## Objectif
Dans cette deuxième partie, vous allez devoir utiliser Git en groupe. Ainsi, vous verrez l'utilisation au sein d'une équipe.
> Il s'agira d'un petit projet, mais imaginez son utilisation à plus grande échelle.

Mettez vous en groupe de **4 à 6 personnes**.

## Repository du groupe
Toujours sur **Gitea**, un membre du groupe doit créer un repo (et uniquement un seul membre). Vous pouvez returner à la partie [Création de votre repository](#création-de-votre-repository) si besoin.

Le repo aura pour nom **tp-git-initiation-groupe**
> Pour ceux qui ne font pas le repo, suivez quand même cette partie.

Une fois le repo de créé, vous aurez un bouton qui permettra d'accéder aux paramètres du repo en haut à droite :

![](./images/settings_repo.png)

Dans les paramètres, un onglet **Collaborators** permet de gérer les collaborateurs de votre repo :

![](./images/collaborators.png)

Ajoutez les autres membres du groupe et mettez-les en **Write**.
> `Read` : Peut seulement voir le repo, ne peut pas agir dessus.\
> `Write` : Peut lire et modifier le repo.\
> `Administrator` : Peut lire, modifier et changer la configuration du repo.

Vous devriez avoir quelque chose de similaire à ceci :

![](./images/write_collab.png)

## Manipulation
> Chaque membre du groupe doit effectuer les étapes de leur côté.

1. Clonez le repo qui vient d'être créé.
2. Créez un fichier avec pour nom `NOM Prénom.txt`.
    > Ne mettez pas `NOM Prénom.txt` mais votre nom suivi de votre prénom 👀\
    > Vous perdrez des points si je remarque ceci dans vos commits.
3. Ajoutez ce fichier à ce repo.

<details>
<summary style="cursor: pointer; font-weight: bold;">La suite une fois que vous aurez fini les étapes du dessus.</summary>
<br>

Bien, avez vous eu des difficultés ? Par exemple avec le `push` ?\
Si vous n'avez pas eu de problèmes je vous conseille d'aller directement à l'étape [Aucun souci](#aucun-souci).

---
### Problème pour push
C'est tout à fait normal d'avoir des problèmes sur ça. Vous apprendrez à l'utiliser.

La solution basique est qu'à chaque fois qu'une personne effectue un commit, tout le groupe fait un pull avant de faire à nouveau un commit sur la branche main.

Cependant, il existe une autre solution pour éviter ces problèmes :
1. Créez une nouvelle branche et la sélectionner.
2. Recréez un nouveau fichier avec cette fois `Prénom NOM.txt`.
3. Ajoutez le fichier au repo sur la branche.
4. Effectuez un merge depuis la branche **master**.

---
### Aucun souci
Si vous avez eu aucun souci en effectuant des `git pull` puis des `git push`, veuillez quand même voir la partie [Problème pour push](#problème-pour-push). Une solution plus adaptée est proposée.

Sinon, voici la suite du TP :

À partir de maintenant, dés que vous verrez une étoile (⭐), seulement un membre du groupe doit s'occuper de faire cette étape. Dans le cas contraire, vous verrez des notes de musiques (🎶).

4. ⭐ Créez un fichier `.gitignore` (le nom est important).
	- Dans ce fichier, écrivez `renard.txt`. (N'oubliez pas d'enregistrer)
	- Effectuez un commit.
5. 🎶 Récupérez le fichier en local.
	- Les autres membres doivent effectuer la commande `git pull`.
6. ⭐ Créez deux fichiers, l'un qui sera `renard.txt` et l'autre `belette.txt`.
	- Faites un commit après qu'ils soient créés.
		- Faites le commit avec un `git add .`
7. 🎶 Récupérez les fichiers en local (même chose que l'étape 5).
	- Une fois que vous aurez fait la commande, vous devriez avoir récupérer seulement le fichier `belette.txt`.
	- Le fichier `.gitignore` a empéché l'envoie de `renard.txt`

Bravo à vous ! Vous avez fini le TP !

<details>
<summary style="cursor: pointer; font-weight: bold;">Vous avez votre récompense.</summary>

<img src="https://c.tenor.com/P-8ZvqnS4AwAAAAC/dancing-cat-dancing-kitten.gif" width="200" height="200">

> Et d'ailleurs, ce n'est pas noté ;)
</details>
</details>