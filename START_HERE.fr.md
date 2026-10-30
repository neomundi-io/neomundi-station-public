# Commencer
[English](START_HERE.md) · [Français](START_HERE.fr.md)

[Station — Observer et expérimenter](README.fr.md) · [Runtime Measurement — Mesurer et intégrer](https://github.com/neomundi-io/neomundi-runtime-measurement/blob/main/README_FR.md) · [Use Cases — Applications, pilotes et preuves](https://github.com/neomundi-io/neomundi-use-cases/blob/main/README_FR.md) · [Créer un compte — ControlTower](https://controltower.neomundi.io/welcome)

Station est l'entrée produit de NeoMundi : un instrument pour observer les réponses de l'IA dans des conditions déclarées et examiner les mesures et preuves associées.

[**Explorer toutes les preuves →**](EVIDENCE.fr.md)

## Choisir son parcours
| Votre objectif | À consulter |
|---|---|
| Comprendre l'instrument | [Présentation de Station](README.fr.md#ce-que-ça-fait-simplement) |
| Examiner les enregistrements | [Schémas JSON publics](schemas/) |
| Comprendre les termes | [Glossaire](GLOSSARY.fr.md) |
| Intégrer l'API de mesure | [Documentation API](https://github.com/neomundi-io/neomundi-runtime-measurement) |
| Utiliser un client ou un connecteur agent | [SDK Python](https://github.com/neomundi-io/neomundi-python-sdk) · [MCP](https://github.com/neomundi-io/neomundi-measurement-mcp) |
| Examiner les méthodes et pilotes antérieurs | [Validation](https://github.com/neomundi-io/neomundi-metrology-validation) · [Cas d'usage](https://github.com/neomundi-io/neomundi-use-cases) |
| Voir les chantiers prévus | [Feuille de route](ROADMAP.fr.md) |
| Discuter de votre pilote | [contact@neomundi.io](mailto:contact@neomundi.io) |

## Ce qui est accessible aujourd'hui
Lire les schémas et la documentation ne demande pas de compte. L'accès à Station hébergée est accordé au cas par cas ; voir les [conditions d'accès](README.fr.md#accès-à-la-station).
Ce dépôt contient les contrats et la documentation publics, pas une implémentation déployable. SDK et MCP sont expérimentaux et gardent leurs propres conditions d'installation et de licence.

## Que deviennent vos données ?
Distinguer quatre flux : exécution de l'IA ; soumission pour mesure ; enregistrements internes ; restitution ou export vers un consommateur. L'interface en lecture seule et l'export d'interopérabilité ne décrivent pas tous les flux internes.
Un champ dans une interface client ne prouve pas son envoi dans tous les modes. Un export sans texte brut ne prouve pas non plus l'absence de traitement du texte en amont.
La revue d'architecture prévue documentera les charges utiles réelles, les destinations et la conservation par mode avant toute affirmation plus générale de confidentialité. Un mode SDK limité aux métriques n'est pas annoncé comme disponible.

## Documentation publique et dossiers pilotes
Glossaire, contrats, limites et guides d'intégration relèvent de la documentation publique.
Données pilotes, identifiants et résultats propres à un destinataire circulent par des canaux contrôlés. Une documentation approfondie sélectionnée peut être partagée sous NDA selon son périmètre ; un NDA ne donne accès ni aux secrets ni aux données d'autres pilotes.

Les études antérieures conservent leur propre provenance. Elles ne prouvent pas que Station a produit leurs résultats.
