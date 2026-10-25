# Glossaire
[English](GLOSSARY.md) · [Français](GLOSSARY.fr.md) · [Commencer](START_HERE.fr.md)

Un guide de lecture. Les noms de champs et les valeurs admises restent définis par les schémas et contrats versionnés.

| Terme | Sens dans cette documentation |
|---|---|
| Observation | Enregistrement d'une exécution d'IA dans des conditions déclarées. |
| Mesure | Résultat associé à une méthode, une version et un contexte d'exécution. |
| Évaluation de référence | Évaluation face à une référence déclarée ; distincte des signaux de mesure. |
| Interprétation | Sens donné au résultat par une personne ou un système consommateur. |
| Couverture | Composants de mesure attendus effectivement disponibles, selon le contrat applicable. |
| Complete / partial | États définis par le contrat applicable ; un succès HTTP ne prouve pas à lui seul la complétude. |
| Refus | Résultat qui ne peut pas être qualifié, consigné avec son motif selon le contrat de Station. Ce n'est pas un zéro. |
| Null | Absence de valeur selon la définition du champ ; distincte d'un zéro mesuré. |
| Provenance | Origine, versions et conditions de production d'un enregistrement. |
| Comparabilité | Conditions permettant de comparer des résultats ; des libellés identiques ne suffisent pas. |
| Modèle demandé / servi | Modèle demandé et modèle attesté comme ayant réellement répondu. |
| Registre / ledger | Structure d'enregistrement de Station en ajout seul ; une correction est une nouvelle entrée qui désigne la précédente. |
| Intégrité | Élément permettant de vérifier qu'un artefact n'a pas changé par rapport à sa référence de vérification ; ne prouve pas la vérité du contenu. |
| Contrat d'interopérabilité | Format d'échange versionné pour les consommateurs, distinct des schémas internes du registre. |
| REST / SSE | Interaction requête-réponse et flux d'événements envoyé par le serveur. Aucun de ces transports n'établit la validité d'une mesure. |
| Station métier | Protocoles et configuration métier prévus sur un socle commun ; ne signifie pas qu'ils sont déjà disponibles. |

Sources : [schémas de Station](schemas/) · [Metric Contract](https://github.com/neomundi-io/neomundi-metric-contract) · [contrat d'échange](https://github.com/neomundi-io/neomundi-measurement-interoperability)
