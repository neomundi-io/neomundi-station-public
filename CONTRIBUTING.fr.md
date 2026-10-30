[English](CONTRIBUTING.md) · **Français**

# Contribuer — ce qui est possible ici, et ce qui ne l'est pas

Merci de l'intérêt. **Lisez ce fichier avant d'ouvrir quoi que ce soit** : ce
dépôt n'accepte pas le genre de contribution auquel un dépôt public fait
normalement penser.

> **Avertissement juridique.** Aucune licence n'est déclarée sur ce dépôt :
> **tous droits réservés**. Une contribution n'est donc **pas** encadrée par une
> licence open source, et aucun accord de contribution n'existe à ce jour.
> **Avant d'investir du temps, ouvrez une issue** — nous ne voulons pas accepter
> un travail dont le statut serait ambigu.

## Ce que ce dépôt est

**La surface publique d'un instrument de mesure.** Pas une bibliothèque, pas un
produit à installer, pas une démonstration.

🔴 **Il ne contient pas l'implémentation.** Celle-ci est privée. Il n'y a donc
**ni code à corriger, ni test à écrire, ni dépendance à mettre à jour** ici, et
une *pull request* qui en proposerait serait refusée — non par principe, mais
parce qu'elle n'aurait rien à modifier.

## Ce qui est utile, et par ordre de valeur

| | Ce que vous pouvez signaler | Pourquoi c'est précieux |
|---|---|---|
**1** | 🔴 **Un schéma qui décrit mal ce que le registre consigne** — un champ obligatoire qui ne l'est pas, une contrainte absente, une description ambiguë | Un tiers qui vérifie une preuve s'appuie sur ces contrats. **S'ils mentent, sa vérification ne vaut rien** |
**2** | **Un défaut scientifique** — une mesure qui ne mesure pas ce qu'elle dit, une série qui mêlerait deux clés de comparabilité, un zéro pris pour une mesure | Ce sont les signalements que nous cherchons le plus |
**3** | **Une affirmation non étayée dans la documentation** — une capacité annoncée que rien n'établit, un chiffre sans provenance | Ce dépôt a pour règle qu'un chiffre porte sa provenance. Prenez-nous en défaut |
**4** | **Une incohérence entre ce dépôt et la Station** — ce qui est écrit ici et ce que l'instance fait | Les deux doivent dire la même chose |
**5** | **Une faute de langue ou un lien mort** | Utile, et bienvenu, mais c'est le poste le moins critique |

**Une faille de sécurité ne passe JAMAIS par une issue :**
[`SECURITY.md`](SECURITY.md).

## Comment signaler

Ouvrez une **issue**, et dites trois choses :

1. **ce que vous avez lu ou appelé** — le fichier, ou la route ;
2. **ce que vous en attendiez** ;
3. **ce que vous avez observé**, avec de quoi le reproduire.

Si vous écrivez *« vérifié »*, **montrez la sortie.** C'est une règle que nous
nous appliquons, et nous vous l'appliquons aussi.

## Ce qui sera refusé

- **une modification des schémas sans démonstration.** Un schéma décrit un
  registre réel : le changer sans montrer ce que le registre écrit vraiment
  casserait le contrat au lieu de le corriger ;
- **une proposition de licence open source.** Le régime juridique est une
  décision ouverte, et elle ne se tranche pas dans une *pull request* ;
- **un score composite, un classement de modèles, une agrégation par-dessus une
  clé de comparabilité.** L'instrument refuse les trois, par construction ;
- **un secret, une clé, un jeton** — même factice s'il est plausible ;
- **un contenu de jeu de données tiers.** Seuls les manifestes circulent, avec
  leurs empreintes et leur licence déclarée ;
- **une valeur par défaut qui masque une absence.** `null` n'est pas zéro ;
- **une affirmation de capacité non étayée par une exécution.**

## Ce que nous ne vous demanderons pas

De la vitesse. Ce dépôt avance en montrant ses preuves, et un signalement qui
prend un jour de plus pour établir un fait par exécution plutôt que par lecture
est un meilleur signalement.
