# livraison-repas

## Description
Ce projet, réalisé dans le cadre du cours d'Architecture et Génie Logiciel (AGL), vise à modéliser une application à l'aide de diagrammes UML. Il permet d’identifier les cas d'utilisation clés et de documenter l'architecture du système.                                                                                                                       

## Objectifs de projets
Définir et documenter les cas d'utilisation essentiels.
Concevoir des diagrammes UML pour illustrer le fonctionnement de l'application.
Gérer le projet via Git et GitHub.

## Cas d'utilisation prioritaires
### Cas d'utilisation 1 : Se connecter Client
- Acteurs : client,système
- Description : Ce cas d'utilisation permet à un client de se connecter à son compte en utilisant son email et son mot de passe. Le système valide les informations fournies et autorise l'accès si elles sont correctes.
- Scénario : 
1. L'utilisateur entre son email et son mot de passe dans les champs appropriés.
2. Le système vérifie les identifiants.
3. Si les identifiants sont corrects, l'accès est autorisé et l'utilisateur est redirigé vers la page d'accueil de son compte.
4. Si les identifiants sont incorrects, un message d'erreur s'affiche, indiquant que l'email ou le mot de passe est incorrect, et l'utilisateur peut réessayer.

### Cas d'utilisation 2 : Passer commande
- Acteurs : client,système
- Description : Ce cas d'utilisation permet à un client de sélectionner des plats à partir d'un menu, de les ajouter à son panier, de valider sa commande et de procéder au paiement pour recevoir une confirmation de la commande.
- Scénario : 
1. Le client consulte le menu.
2. Le client ajoute les plats souhaités au panier.
3. Le client valide la commande en vérifiant les articles dans son panier.
4. Paiement et confirmation.
## Tests de validation - Tables de décision

### Table de décision pour "Se connecter Client"

#### Précondition

| Condition                               | T   | T   | T   | T   |
| --------------------------------------- | --- | --- | --- | --- |
| Email valide (respecte le format email) | F   | T   | T   | T   |
| Mot de passe non null et non vide       | F   | F   | T   | T   |
| Compte existant avec cet email          | F   | F   | F   | T   |

#### Postcondition

| Condition                            | T   | T   | T   | T   |
| ------------------------------------ | --- | --- | --- | --- |
| Connexion réussie                    | F   | F   | F   | T   |
| Nombre de tests dans le jeu de tests | 1   | 2   | 3   | 4   |

---

### Table de décision pour "Passer commande"

#### Précondition

| Condition                  | T   | T   | T   | T   |
| -------------------------- | --- | --- | --- | --- |
| Client connecté            | F   | T   | T   | T   |
| Plats ajoutés au panier    | F   | F   | T   | T   |
| Stock des plats disponible | F   | F   | F   | T   |

#### Postcondition

| Condition                            | T   | T   | T   | T   |
| ------------------------------------ | --- | --- | --- | --- |
| Commande validée                     | F   | F   | F   | T   |
| Nombre de tests dans le jeu de tests | 1   | 2   | 3   | 4   |
