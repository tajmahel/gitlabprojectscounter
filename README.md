# GitLab Projects Counter

Ce projet permet de compter le nombre de projets d'un utilisateur GitLab. Il propose deux modes d'utilisation : une version en ligne de commande et une interface graphique utilisant PyQt6.

## Prérequis

- Python 3.6+
- pip (gestionnaire de paquets Python)
- Librairies :
  - requests
  - PyQt6


## Installation

1. Clonez ce dépôt :
   ```
   git clone https://gitlab.com/maelmemain1/gitlabprojectscounter.git
   cd gitlabprojectscounter
   ```

2. Installez les dépendances :
   ```
   pip install requests PyQt6
   ```

## Utilisation
- Deux versions : 
  1. Version en ligne de commande.
  2. Version avec une interface qt.
- Les deux versions peuvent utiliser un token permettant de compter les projets privés en plus des projets publiques.
- Sans token, **seuls les projets publiques** du compte seront comptés.

### Version en ligne de commande

1. Pour lancer la version classique **sans token** en ligne de commande :

```
bash classicLaunch.sh <votre_nom_utilisateur>
```
- Remplacer '<votre_nom_utilisateur>' par votre nom GitLab.
#

2. Pour lancer la version classique **avec token** en ligne de commande :
- Trouver votre token GitLab : 
  1. Connectez-vous à votre compte GitLab.
  2. Cliquez sur votre avatar en haut à droite, puis sélectionnez "Edit profile".
  3. Dans le menu de gauche, cliquez sur "Access Tokens" puis sur Add new token.
  4. Donnez un nom à votre token (par exemple, "ProjectCounter").
  5. Sélectionnez la portée "read_api" pour ce script.
  6. Cliquez sur "Create personal access token".
  7. Copiez immédiatement le token généré. Vous ne pourrez plus le voir après avoir quitté cette page.
-  N'oubliez pas de garder ce token secret, car il donne accès à votre compte GitLab.

```
bash classicLaunch.sh <votre_nom_utilisateur> -t <votre_token>
```

- Remplacer '<votre_nom_utilisateur>' par votre nom GitLab et '<votre_token>' par votre token GitLab.

#
### Version avec interface graphique (Qt)

Pour lancer la version avec interface graphique :

```
bash qtLaunch.sh
```

Dans l'interface qui s'ouvre :
1. Entrez le nom d'utilisateur GitLab
2. Entrez le token si vous en avez un (optionnel)
3. Cliquez sur "Compter les projets"

Le résultat s'affichera dans l'interface.

## Sécurité

- Ne partagez jamais votre token d'accès personnel GitLab.
- Le token est optionnel mais permet d'accéder à plus d'informations et d'augmenter les limites de taux d'API.

## Contribution

- Les contributions à ce projet sont les bienvenues. N'hésitez pas à ouvrir une issue ou à soumettre une pull request.

## Crédits 
- MEMAIN Maël - 10/2024

