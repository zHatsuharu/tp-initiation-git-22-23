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
Sur [Gitea](https://git.ytrack.learn.ynov.com/), vous pouvez créer un nouveau repository avec le bouton suivant :

![](./images/create_repo.png)
> Il se situe en haut à droite de la page.

Appelez votre repo **tp-git-initiation**
> Pas besoin de modifier les autres options, donnez lui juste un nom.

Une fois créé, nous pouvons commencer le TP.

## Manipulation
> En cas de souci, une doc récapitulative se situe [ici](./doc/).\
> À chaque étape, vérifiez votre repo via Gitea pour confirmer les modifications.
1. Clonez votre repository.
    - Un dossier a dû être créé à l'endroit où vous avez cloné votre repo.
2. Créez un fichier quelconque dans le dossier du repository sur votre pc.
3. Ajoutez ce fichier à votre repo (il doit apparaître sur le repo Gitea 👀).
4. Recréez un autre fichier que vous allez ajouter aussi à votre repo.
5. Maintenant, il faut **revert** votre commit.
    - L'objectif est de revenir un pas en arrière, donc l'étape 4 sera annulée.
    - Vous devez avoir à ce point, seulement le fichier de l'étape 3 dans votre repo.
6. Créez une branche et la sélectionner.
7. Effectuez un commit (création d'un fichier).
8. Faites un merge vers la branche **main**.

Bien, maintenant que vous avez fait cette première partie en étant seul, vous allez vous mettre un peu plus dans la plus grande utilisation de Git : un travail de groupe.

# Partie 2 - Travailler en groupe
## Objectif
Dans cette deuxième partie, vous allez devoir utiliser Git en groupe. Ainsi, vous verrez l'utilisation au sein d'une équipe.
> Il s'agira d'un petit projet, mais imaginez son utilisation à plus grande échelle.

Mettez vous en groupe de **4 à 6 personnes**.

## Repository du groupe
Toujours sur **Gitea**, un membre du groupe doit créer un repo (et uniquement un seul membre).
> Pour ceux qui ne font pas le repo, suivez quand même cette partie.

Une fois le repo de créé, vous aurez un bouton qui permettra d'accéder aux paramètres du repo en haut à droite :

![](./images/settings_repo.png)

Dans les paramètres, un onglet **Collaborators** permet de gérer les collaborateurs de votre repo. Ajoutez les autres membres du groupe et mettez-les en **Write**.
> `Read` : Peut seulement voir le repo, ne peut pas agir dessus.\
> `Write` : Peut lire et modifier le repo.\
> `Administrator` : Peut lire, modifier et changer la configuration du repo.

## Manipulation
> Chaque membre du groupe doit effectuer les étapes de leur côté.

1. Cloner le repository.
2. Créer un fichier avec pour nom `NOM Prénom`.
    > Ne mettez pas `NOM Prénom` mais votre nom suivi de votre prénom 👀\
    > Vous perdrez des points si je remarque ceci dans vos commits.
3. Ajouter ce fichier au repo.

<details>
<summary style="cursor: pointer;">La suite une fois que vous aurez fini les étapes du dessus.</summary>
<br>

Bien, avez vous eu des difficultés ? Par exemple avec le `push` ?\
Si vous n'avez pas eu de problèmes je vous conseille d'aller directement à l'étape [Aucun souci](#aucun-souci).

---
### Problème pour push
C'est tout à fait normal d'avoir des problèmes sur ça. Vous apprendrez à l'utiliser.

La solution basique est qu'à chaque fois qu'une personne effectue un commit, tout le groupe fait un pull avant de faire à nouveau un commit sur la branche main.

Cependant, il existe une autre solution pour éviter ces problèmes :
1. Recréez un nouveau fichier avec cette fois `Prénom NOM`.
2. Créez une nouvelle branche et la sélectionner.
3. Ajoutez le fichier au repo sur la branche.
4. Effectuez un merge.

---
### Aucun souci
Si vous avez eu aucun souci en effectuant des `git pull` puis des `git push`, veuillez quand même voir la partie **Problème pour push**. Une solution plus adaptée est proposée.

Sinon, bravo ! Vous avez fini le TP !
<details>
<summary style="cursor: pointer;">Vous avez votre récompense.</summary>

<img src="https://c.tenor.com/P-8ZvqnS4AwAAAAC/dancing-cat-dancing-kitten.gif" width="200" height="200">

> Et d'ailleurs, ce n'est pas noté ;)
</details>
</details>