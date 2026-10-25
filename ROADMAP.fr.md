# Feuille de route Station
[English](ROADMAP.md) · [Français](ROADMAP.fr.md) · [Commencer](START_HERE.fr.md)

Orientation convenue le 25 octobre 2026. Cette page décrit des chantiers, pas des capacités livrées ni des dates de livraison.

| Priorité | Chantier | Preuve d'achèvement |
|---|---|---|
| 1 | Organiser GitHub autour de Station | Profil d'organisation bilingue, parcours documentaires publics, liens cohérents depuis les dépôts d'intégration et de preuves. |
| 2 | Aligner la documentation sur l'architecture réelle | Cartographie versionnée des charges utiles réelles, destinations, stockages internes et exports par mode pris en charge. |
| 3 | Consolider le MCP : REST et SSE | Deux modes d'interaction de mesure testés ; outils, versions des routes, authentification, erreurs, interruptions et résultats terminaux documentés. Le transport client MCP est documenté séparément du transport vers la mesure. |
| 3 | Consolider le SDK Python : REST et SSE | Interfaces requête-réponse et streaming testées, compatibilité versionnée, états et null préservés, délais et reprises explicites. |
| 4 | Qualifier les versions et droits d'usage | Décisions de licence, installation reproductible, matrice de compatibilité et notes de version. |
| 5 | Publier progressivement les expériences Station | Chaque résultat publié porte un protocole approuvé, son régime d'exécution, sa provenance, ses versions, sa couverture et ses limites. |
| 6 | Raccorder les programmes d'observation et les stations métiers | Exports validés, frontières des séries explicites, protocoles et critères d'acceptation propres au métier. |

## Comment vérifier que cela fonctionne
- REST et SSE préservent la même sémantique de mesure applicable ; les fragments du flux restent distincts du résultat final.
- Les mesures partielles et les valeurs null restent visibles ; une erreur de transport ne devient pas un état de mesure inventé.
- Interruptions, annulations, délais et reprises ont un comportement explicite ; une reprise ne doit pas dupliquer silencieusement une génération payante.
- Les informations sur les modèles demandés et servis et les versions applicables sont conservées lorsqu'elles sont fournies.
- L'authentification et les frontières d'accès par client sont testées avant élargissement de la diffusion.
- La minimisation des données suit l'implémentation vérifiée. Un mode limité aux métriques exige la preuve du calcul local et une provenance suffisante pour les métriques annoncées.
- La documentation distingue rejeux, tests synthétiques et exécutions réelles chez un fournisseur.

## Simplifier GitHub
Migrer le contenu unique et vérifier consommateurs, CI, Pages, citations et liens avant d'archiver un dépôt remplacé.
Conserver les études historiques et leur provenance. Cette feuille de route ne programme aucune suppression de dépôt.

## Ce qui est disponible
Les [conditions d'accès actuelles](README.fr.md#accès-à-la-station) restent applicables.
Le tableau de bord et les stations métiers prévus restent présentés comme prévus tant que leur fonctionnement n'est pas démontré.
