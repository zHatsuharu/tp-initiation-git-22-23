# TP Initiation GIT

Bienvenu(e) sur Github !

Je vous fais vite fait un petit récap de ce qu'est **Git** :
> Git est un outil pour versionner vos projets. Vous envoyez votre projet dans des **repository** (similaire à des dossiers) sur des platforms tel que Github, Gitlab ou Gitea dans le cas d'YNOV. Ainsi vous pouvez partager ou encore travailler à plusieurs sur vos projets.

Dans ce TP, vous appliquerez les notions vu précédemment. Ainsi vous comprendrez un peu mieux le fonctionnement des commandes.

Le TP se fera en 2 parties. Dans la première, vous manipulerez sur un repository seul pour que vous vous familiarisez avec l'outil. Dans la seconde, vous serez en groupe sur un seul repository.

---
## Sommaire

- [Haut de page](#tp-initiation-git)
- [Sommaire](#sommaire)
- [TP Partie 1](#partie-1---familiarisation)
    - [Objectif](#objectif)
    - [Création du repository](#création-de-votre-repository)
    - [Manipulation](#manipulation)
- [TP Partie 2](#partie-2---travailler-en-groupe)
    - [Objectif](#objectif-1)
    - [Repository du groupe](#repository-du-groupe)
    - [Manipulation](#manipulation-1)

# Partie 1 - Familiarisation
## Objectif
L'objectif de cette partie est de vous familiarisez avec l'outil **Git** afin de comprendre son fonctionnement et de pouvoir l'utiliser dans des projets de groupe.

## Création de votre repository
Sur **Gitea**, vous pouvez créer un nouveau repository avec le bouton suivant :\
![](./images/create_repo.png)
> Il se situe en haut à droite de la page.

Appeler votre repo **tp-git-initiation**
> Pas besoin de modifier les autres options, donnez lui juste un nom.

Une fois créer, nous pouvons commencer le TP.

## Manipulation
> En cas de soucie, une doc récapitulative se situe [ici](./doc/).\
> À chaque étape, vérifiez votre repo via Gitea pour confirmer les modifications.
1. Cloner votre repository.
2. Créer un fichier quelconque dans le dossier du repository sur votre pc.
    - Un dossier a du être créer à l'endroit où vous avez cloné votre repo.
3. Ajouter ce fichier à votre repo (il doit apparaître sur le repo Gitea 👀).
4. Recréer un autre fichier que vous allez ajouter aussi à votre repo.
5. Maintenant, il faut **revert** votre commit.
    - L'objectif et de revenir un pas en arrière, donc l'étape 4 sera annulé.
    - Vous devez avoir à ce point, seulement le fichier de l'étape 3 dans votre repo.
6. Créer une branche et sélectionner la.
7. Effectuer un commit (création d'un fichier).
8. Faites un merge vers la branche **main** .

Bien, maintenant que vous avez fait cette première partie en étant seul, vous allez vous mettre un peu plus dans la plus grande utilisation de Git : un travail de groupe.

# Partie 2 - Travailler en groupe
## Objectif
Dans cette deuxième partie, vous allez devoir utiliser Git dans un groupe. Ainsi, vous verrez l'utilisation au sein d'une équipe.
> Il s'agira d'un petit projet, mais imaginez son utilisation à plus grande échelle.

Mettez vous en groupe de **4 à 6 personnes**.

## Repository du groupe
Toujours sur **Gitea**, un membre du groupe doit créer un repo (et uniquement un seul membre).
> Pour ceux qui ne font pas le repo, suivez quand même cette partie.

Une fois le repo de créer, tu auras un bouton qui permettra l'accès aux paramètres du repo en haut à droite :\
![](./images/settings_repo.png)\
Dans les paramètres, un onglet **Collaborators** permet de gérer les collaborateurs de ton repo. Ajoutez les autres membres du groupe et mettez les en **Write**.
> `Read` : Peut seulement voir le repo, ne peut pas agir dessus.\
> `Write` : Peut lire et modifier le repo.\
> `Administrator` : Peut lire, modifier et changer la configuration du repo.
## Manipulation
> Chaque membre du groupe doit effectuer les étapes de leur côté.

1. Cloner le repository.
2. Créer un fichier avec pour nom `NOM Prénom`.
    > Mettez pas `NOM Prénom` mais votre nom suivi de votre prénom 👀\
    > Vous perdrez des points si je remarque ceci dans vos commits.
3. Ajoutez ce fichier au repo.


<details>
<summary style="cursor: pointer;">La suite une fois que vous aurez fini les étapes du dessus.</summary>
<br>

Bien, avez vous eu des difficultés ? Par exemple avec le `push` ?\
Si vous avez pas eu de problème je vous conseille d'aller directement [ici](#aucun-soucie).

---
### Problème pour push
C'est tout à fait normal d'avoir des problème sur ça. Vous apprenez à l'utiliser.

La solution basique est qu'à chaque fois qu'une personne effectue un commit, tout le groupe fait un pull avant de faire à nouveau un commit sur la branche main.

Cependant, il existe une autre solution pour éviter ces problèmes :
1. Recréer un nouveau fichier avec cette fois `Prénom NOM`.
2. Créer une nouvelle branche et sélectionner là.
3. Ajouter le fichier au repo sur la branche.
4. Effectuer un merge.

---
### Aucun soucie
Si vous avez eu aucun soucie en effectuant des `git pull` puis des `git push`, veuillez quand même voir [la partie au dessus](#problème-pour-push). Une solution plus conseillée à utiliser est proposée.

Sinon, bravo ! Vous avez fini le TP !
<details>
<summary style="cursor: pointer;">Vous avez votre récompense.</summary>

<img src="https://c.tenor.com/P-8ZvqnS4AwAAAAC/dancing-cat-dancing-kitten.gif" width="200" height="200">

> Et d'ailleurs, ce n'est pas noté ;)
</details>
</details>