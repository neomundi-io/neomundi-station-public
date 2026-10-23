# NeoMundi Station

## Quand l'IA répond, NeoMundi mesure.

Posez une question à une IA. NeoMundi Station enregistre la réponse, mesure ce
qu'elle vaut, et en garde la preuve — pour que ce qu'un système d'IA a dit
puisse être **montré à quelqu'un d'autre** au lieu d'être seulement retenu.

🇬🇧 [Read this document in English](README.md)

---

## Ce que ça fait, simplement

Une IA répond. Cette réponse est vue une fois, dans une fenêtre de
conversation, puis elle disparaît — personne ne peut y revenir, et personne ne
peut la montrer à un tiers.

Station comble ce manque. Elle pose la question dans des **conditions
déclarées**, **enregistre** la réponse telle qu'elle est arrivée, demande à
l'API de mesure **ce que cette réponse vaut**, et écrit les trois dans un
**registre où l'on ne peut qu'ajouter** — chaque entrée scellée à la
précédente. Rien n'est modifié ensuite : une correction est une **nouvelle**
entrée qui désigne l'ancienne.

**Station ne décide rien.** Elle n'approuve pas, ne bloque pas, ne filtre pas,
ne classe pas. Elle établit ce qui s'est passé et ce que cela valait, puis le
remet à ceux dont le métier est de décider.

Et elle dit quand elle ne peut pas mesurer. Un résultat qu'elle ne peut pas
qualifier est enregistré comme un **refus**, et non deviné — parce qu'un refus
est un résultat honnête, et qu'un chiffre plausible ne l'est pas.

---

## Ce que ça vous apporte

| Vous êtes | Ce que Station vous donne |
|---|---|
| **Développeur ou ingénieur IA** | **Les contrats d'enregistrement, lisibles tout de suite** — [`schemas/`](schemas/), 15 schémas JSON, aucun compte, aucune clé, rien à installer. Ils énoncent exactement ce qui est consigné pour chaque réponse d'une IA : le modèle qui l'a réellement servie, les paramètres qui ont pris effet, ce qui a été mesuré, et ce qui n'a pas pu l'être. Si vous avez déjà essayé de reconstituer après coup **ce que votre système a répondu, exactement, mardi dernier**, c'est ce manque que ces contrats comblent. |
| **Ingénieur IA qui fait de l'évaluation** | Une forme pour un problème que vous avez déjà : questions gelées, conditions déclarées, mesures tenues **séparées** des verdicts de référence, et les deux tenues séparées de vos propres conclusions. Une mesure qui échoue reste visible comme un **refus** au lieu de devenir un zéro en silence — c'est la façon ordinaire dont une chaîne d'évaluation commence à vous mentir. |
| **Chercheur** | Des questions versionnées et gelées ; des conditions d'exécution déclarées ; le modèle qui a **réellement** répondu enregistré à côté de celui qui était demandé ; un refus enregistré comme un résultat plutôt que deviné ; et une clé de comparabilité qui rend impossible de moyenner en silence deux dispositifs différents dans une même série. |
| **Entreprise qui déploie de l'IA** | De quoi montrer à un client, à un auditeur ou à un comité : voici ce que le système a répondu, dans **ces** conditions, et voici ce que la réponse valait — une preuve qui se vérifie, plutôt qu'une affirmation qu'il faut croire. |
| **Équipe pilote** | Un registre qui vous est propre. [Écrivez-nous](https://neomundi.io). |

---

## Comment ça fonctionne

| RÉPONSE IA | OBSERVATION | MESURE | PREUVE | DÉCISION HUMAINE |
|---|---|---|---|---|
| L'IA répond | Consigner ce qui s'est passé | Évaluer les signaux disponibles | Conserver une preuve vérifiable | L'humain interprète |

| Étape | Ce qui se passe |
|---|---|
| **1 — IA** | Une question versionnée et gelée est posée à un vrai modèle, dans des conditions écrites à l'avance. |
| **2 — Observation** | La réponse est enregistrée telle qu'elle est arrivée, avec son empreinte, ses temps, et le modèle qui l'a **réellement** servie — pas seulement celui qui était demandé. |
| **3 — Mesure** | L'API de mesure est interrogée sur ce texte. Les signaux qu'elle rend, la couverture qu'elle avait, et les signaux qu'elle **n'a pas pu** mesurer sont tous enregistrés. |
| **4 — Preuve** | Chaque étape écrit sa propre entrée dans un registre en ajout seul, scellée à la précédente. Toute altération brise le sceau et se détecte. |
| **5 — Décision humaine** | Ce que le résultat **signifie** est un jugement, et il reste aux personnes. Station fournit la preuve ; elle ne fournit jamais le verdict. |

### Quatre choses tenues séparées, toujours

**Ce que le modèle a répondu** · **ce que la mesure en dit** · **si c'était
juste face à une référence** · **ce qu'un humain en conclut.**

Les confondre, c'est ainsi qu'on obtient des chiffres d'apparence propre qui ne
veulent rien dire. Station les garde dans des enregistrements distincts, par
construction.

---

## Explorer

| | |
|---|---|
| 🛰 **Live Station** | **<https://station.neomundi.org>** — l'instance unique. Voir [Accès](#accès-à-la-station). |
| 🧪 **Expériences** | [Ce qu'une expérience portera](#expériences), et pourquoi aucune n'est encore publiée. |
| 🔒 **Preuves** | [Ce qui est consigné, et ce qui est retenu](#preuves). |
| 📘 **Documentation** | [Les contrats d'enregistrement](#documentation) — 15 schémas JSON, lisibles dès maintenant. |
| 🐍 **SDK** | [neomundi-python-sdk](https://github.com/neomundi-io/neomundi-python-sdk) — appeler la mesure directement. Expérimental ; voir [Intégrations](#intégrations). |
| 🔌 **MCP** | [neomundi-measurement-mcp](https://github.com/neomundi-io/neomundi-measurement-mcp) — un seul outil, pour un agent. Expérimental ; voir [Intégrations](#intégrations). |
| 🤝 **Pilotes** | [neomundi.io](https://neomundi.io) — écrivez-nous. |

---

## Expériences

Une **expérience**, c'est une question posée de façon répétée dans des
conditions fixées, pour qu'une chose soit **établie** plutôt qu'affirmée.

Station est **en préparation de lancement public**, et les expériences seront
**ajoutées ici progressivement, chacune seulement après avoir été validée.**

**Rien n'y est encore publié, et c'est délibéré.** Quand une entrée
apparaîtra, elle portera, au même endroit :

- son **protocole** — la question, les conditions, les répétitions ;
- son **statut** — préparée, en cours, ou close ;
- son **régime d'exécution** — appel réel à un fournisseur, rejeu d'un corpus
  gelé, ou exécution synthétique ;
- sa **version de mesure** et sa **clé de comparabilité** ;
- et **ce qu'elle ne montre pas** — dit clairement, dans la même entrée.

**Aucun résultat, aucun taux et aucune série n'est publié dans ce dépôt
aujourd'hui.** Un chiffre sans sa provenance n'est pas une mesure : il attend.

---

## Preuves

Le registre est **en ajout seul et scellé d'entrée en entrée** : chaque
enregistrement porte l'empreinte du précédent. Rien n'est modifié ni supprimé ;
une correction est un **nouvel** enregistrement qui désigne l'ancien.

**Ce qui est consigné :** l'empreinte de la question, la réponse et son
empreinte, le modèle réellement servi et la façon dont il a été attesté, les
paramètres envoyés et ceux qui ont réellement pris effet, les temps, les
signaux mesurés et leurs valeurs, la couverture, les signaux qui **n'ont pas
pu** être mesurés et pourquoi, et — là où une référence existe — le verdict de
référence avec la version de l'évaluateur qui l'a produit.

**Ce que l'API en lecture seule retient :** les questions et les réponses
elles-mêmes ne sont **jamais** restituées. Vous obtenez leurs empreintes et
leurs longueurs. Vous pouvez **vérifier** un texte que vous détenez déjà ; vous
ne pouvez pas en **découvrir** un que vous ne détenez pas. Aucune politique ne
dit qui a le droit de lire le contenu brut — et l'absence de politique n'est
pas une permission.

**Un signal non mesuré reste vide.** Il n'est jamais transformé en zéro. Un
zéro déclaré est une vraie mesure, et prendre une panne pour un score parfait
est exactement la défaillance que cette règle empêche.

**Ce que Station ne produira jamais :** un score composite unique, un classement
de modèles, ou une dérive déclarée avant la clôture de la baseline qu'elle
s'est elle-même fixée. Ce sont des règles de l'instrument, pas une prudence de
style.

---

## Documentation

**Disponible dès maintenant — les contrats d'enregistrement.**
[`schemas/`](schemas/) porte les **15 documents JSON Schema** qui définissent
chaque entrée que le registre accepte : observation, mesure, divulgation de
mesure, enregistrement de preuve, évaluation de référence, provenance de rejeu,
exécution, campagne, panel, protocole, version d'invite, profil de fournisseur,
manifeste de jeu de données, référence d'item, exclusion d'item.

Ce sont des **contrats, pas des résultats.** Ils énoncent ce que l'instrument
est **tenu** de consigner — c'est-à-dire la partie que n'importe qui doit
pouvoir contrôler avant d'accorder sa confiance au moindre chiffre qui en sort.
Les lire montre, entre autres, que le modèle réellement servi est enregistré à
côté de celui qui était demandé, qu'un signal non mesuré reste vide, et qu'une
mesure qui ne peut pas être qualifiée est écrite comme un refus, avec son motif.

**Une documentation sélectionnée suivra** — le contrat de mesure, ce que l'API
refuse de restituer, et la méthode — relue pièce par pièce avant d'être publiée
ici.

---

## Pour commencer

**Il n'y a rien à cloner et rien à installer ici** : l'implémentation est
privée, et ce dépôt est la surface publique d'un instrument unique, hébergé.

**Commencez par les contrats.** [`schemas/`](schemas/) — 15 schémas JSON,
aucun compte, aucune clé, rien à installer. C'est le moyen le plus rapide de
juger si cet instrument consigne ce que vous auriez besoin qu'il consigne, et
c'est la seule chose ici que vous pouvez contrôler vous-même, aujourd'hui, en
entier.

Ensuite : **la Station elle-même**, à **<https://station.neomundi.org>** — voir
[Accès](#accès-à-la-station). Et pour un travail sur vos propres données,
[écrivez-nous](https://neomundi.io).

### Intégrations

**Il en existe deux, toutes deux expérimentales. Ce qui suit est ce qu'elles
font aujourd'hui — pas une feuille de route.**

| | |
|---|---|
| [**neomundi-python-sdk**](https://github.com/neomundi-io/neomundi-python-sdk) | Appelle l'API de mesure directement, sans Station. **Non publié sur un index de paquets** : l'installation se fait depuis les sources. |
| [**neomundi-measurement-mcp**](https://github.com/neomundi-io/neomundi-measurement-mcp) | Expose un unique outil `measure_execution`, pour qu'un agent puisse mesurer ce qu'il a produit. **Transport validé ; son contrat de mesure ne l'est pas encore en production.** |

**Une mise en garde compte plus que les autres, et elle est pratique avant
d'être juridique.** Le SDK cible une version de mesure **antérieure** à celle
que cet instrument audite : mêler les résultats des deux dans une même série
briserait la règle de comparabilité **sans vous avertir**. Gardez-les dans des
séries distinctes.

**Ni l'un ni l'autre ne vous accorde de licence.** Le connecteur MCP n'a
aucun fichier de licence ; le SDK porte une mention disant que le choix n'est
pas arbitré. Voir [Licence](#licence).

---

## Accès à la Station

**<https://station.neomundi.org>** est l'instance unique. Il y a **une**
Station, **une** adresse, et ce dépôt n'en est pas une seconde.

**Elle est en préparation de lancement public, et l'accès est aujourd'hui
accordé au cas par cas.** La raison est écrite plutôt que cachée : l'instance
porte **un seul identifiant de consultation, sans séparation par client** —
qui le détient peut donc lire tout le registre servi. Le distribuer largement
reviendrait à tout distribuer d'un coup. Tant qu'une autorisation par client
n'est pas conçue et éprouvée, l'accès reste **délibérément étroit** : un
porteur à la fois, un registre par usage, et un identifiant renouvelé après
toute démonstration.

**Il n'y a donc pas de données de démonstration ouvertes aujourd'hui.** Les
contrats de [`schemas/`](schemas/) sont ce que vous pouvez examiner sans
demander la permission à personne. Pour un travail sur vos propres données,
[écrivez-nous](https://neomundi.io).

---

## Licence

**Aucune licence n'est déclarée sur ce dépôt, et c'est une décision plutôt
qu'un oubli.**

Un dépôt public sans fichier de licence est **tous droits réservés** par
défaut : vous pouvez le lire et en discuter, et aucun droit de copie, de
modification ou de redistribution n'est accordé. Concrètement, aujourd'hui :
lire et discuter — oui ; réutiliser dans un autre projet, redistribuer, ou en
dériver un travail — non.

Choisir une licence est une décision encore à prendre, et elle n'appartient pas
à ce fichier. Il en va de même du SDK et du connecteur MCP : ni l'un ni l'autre
n'en accorde.

**Les jeux de données gardent leurs propres licences**, déclarées à l'import et
portées par leurs manifestes — et **aucun contenu de jeu de données tiers n'est
publié ici.**

---

## Sécurité

Signalez en privé : l'avis privé de GitHub sur ce dépôt, ou l'adresse nommée
dans [`SECURITY.md`](SECURITY.md). **Jamais une issue publique pour une
vulnérabilité.**

`SECURITY.md` dit aussi ce qui en est une — y compris un schéma, ici, qui
décrirait mal le registre. Celui qui vérifie une preuve s'appuie sur ces
contrats : s'ils décrivent de travers, la vérification ne vaut rien.

---

## Ce qu'est ce dépôt — et ce qu'il n'est pas

**Il est** la surface publique d'un instrument hébergé : ses contrats, ses
règles, et la porte d'entrée.

**Il n'est pas** l'implémentation — aucune source, aucun test, aucun
déploiement, rien qui s'installe ou s'exécute. **Il n'est pas** une seconde
Station. **Il n'est pas** une publication de résultats : rien de mesuré n'y est
publié aujourd'hui, et quand ce le sera, chaque chiffre portera sa provenance
ou il n'apparaîtra pas. **Il n'est pas** open source. Et **ce n'est ni un
*benchmark*, ni un classement, ni un détecteur de dérive** — l'instrument est
construit pour refuser les trois.

### Contribuer

Il n'y a aucun code à corriger ici. Ce qui est utile, c'est **un schéma qui
décrit mal ce que le registre consigne**, une mesure qui ne mesure pas ce
qu'elle prétend, ou une affirmation de ce dépôt que rien n'établit. Voir
[`CONTRIBUTING.md`](CONTRIBUTING.md) — et noter qu'aucune licence ne couvre une
contribution aujourd'hui : ouvrez une issue avant d'investir du temps.

---

*Station observe, mesure et garde. Elle ne classe aucun modèle, ne publie aucun
score unique, et ne déclare aucune dérive avant la clôture de la baseline
qu'elle s'est fixée. Ce sont des règles, pas une prudence de style.*
