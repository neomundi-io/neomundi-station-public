# Politique de sécurité

## Ce que ce dépôt contient, et ce que cela change pour vous

**Ce dépôt ne contient aucun code.** Il porte la surface publique de la
Station : sa présentation, et les **schémas JSON** des enregistrements du
registre.

**Il reste donc deux surfaces qui valent un signalement**, et elles ne sont pas
dans ce dépôt :

1. **l'instance** — <https://station.neomundi.org> ;
2. **l'API de mesure NeoMundi**, que l'instance interroge.

Et une troisième, propre à ce dépôt : **un schéma qui décrirait mal ce que le
registre consigne réellement.** Un contrat faux est un défaut, même sans code.

## Signaler une vulnérabilité

**N'ouvrez pas d'issue publique.** Utilisez le signalement privé de GitHub —
onglet *Security* → *Report a vulnerability* — ou écrivez à
**admin@neomundi.io**.

Donnez de quoi reproduire : ce que vous avez appelé, quand *(en UTC)*, et ce que
vous avez observé. Ne joignez **aucune clé réelle**, même la vôtre.

Nous accusons réception et nous vous disons ce que nous faisons. Nous ne
promettons pas de délai : ce projet n'a pas d'astreinte.

## Ce que nous considérons comme une vulnérabilité

- une **fuite de secret** : une clé, un jeton ou un en-tête d'autorisation qui
  apparaîtrait dans un journal, une réponse d'API ou un message d'erreur ;
- une **écriture dans le registre** par un chemin qui ne devrait pas l'avoir.
  L'API de consultation est en lecture seule, et monte le registre en lecture
  seule ;
- un **contournement de l'authentification** de l'API de consultation ;
- une **exposition** d'une surface qui doit rester fermée — le schéma OpenAPI,
  la documentation interactive, le port de l'API ;
- une **destruction de preuves** : tout chemin par lequel un enregistrement du
  registre pourrait être modifié ou supprimé ;
- 🆕 **un schéma de ce dépôt qui ne décrirait pas ce que le registre écrit
  vraiment.** Un tiers qui vérifie une preuve s'appuie sur ces contrats : s'ils
  mentent, sa vérification ne vaut rien.

## Ce qui n'en est pas, et pourquoi

- **le registre ne chiffre pas son contenu.** Il est conçu pour être
  vérifiable par un tiers, pas confidentiel. Ce qui ne doit pas être lu n'y
  entre pas ;
- **un seul jeton de consultation, sans isolation par client.** C'est une
  limite **connue et écrite**, pas un défaut : un jeton valide donne accès à
  tout le registre servi. Les conditions qui en découlent — un porteur à la
  fois, un registre par usage, changement du jeton après toute démonstration —
  sont des obligations, et l'ouverture multi-client est **interdite** tant que
  la politique d'autorisation n'est pas écrite et testée ;
- **l'API de consultation ne rend ni les invites ni les réponses.** Leur
  contenu est retenu — empreinte et longueur suffisent à vérifier un texte déjà
  détenu — faute d'une politique permettant de décider qui a le droit de le
  lire ;
- **l'absence de licence.** C'est un choix, et il est écrit dans le README.

## Ce que ce dépôt ne contient pas

Vérifié avant transfert, et vérifiable :

- **aucune clé, aucun jeton, aucun secret**, dans l'arbre comme dans
  l'historique — ce dépôt est **créé pour l'occasion**, et son historique
  commence à sa première publication ;
- **aucun code, aucun test, aucun fichier de déploiement** ;
- **aucune adresse d'hôte, aucune adresse IP, aucun chemin de système de
  fichiers** ;
- **aucun contenu de jeu de données tiers.** Seuls les *manifestes* ont un
  schéma ici ; aucun item, aucune réponse de référence ;
- **aucune donnée de pilote.** Aucun nom de client, aucun registre de pilote.

Si vous trouvez le contraire, c'est exactement ce que nous voulons savoir.
