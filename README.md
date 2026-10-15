# Space Mining Tycoon V5 — Galaxies & Ascensions

Version de développement construite à partir du projet fourni.

- 3 galaxies de 32 planètes (96 au total).
- Bâtiments spécialisés par galaxie.
- Sélecteur de galaxies sur la carte.
- Ascension avec seuil d'argent, déblocage des 32 planètes, 10 exemplaires de chaque bâtiment sur chaque planète et confirmation.
- Points d'ascension et conservation des succès, du compte et des galaxies débloquées.
- Clé de sauvegarde locale et intégration Supabase existantes conservées.

## Installation
Tester d'abord cette version dans un dépôt GitHub séparé. Ne remplace pas la version actuellement jouée avant d'avoir vérifié les sauvegardes et le comportement cloud.

## Notes
Le projet conserve le client Supabase existant. Aucune migration SQL n'est incluse dans cette version.


Version V5.6 : accordéons repliables pour les branches technologiques et catégories de missions, indicateurs rouges sur les catégories et récompenses prêtes, cinq technologies avancées supplémentaires.


## Halloween 2026 (temporaire)
- Événement disponible jusqu'au 1er novembre 2026 inclus (fin à minuit, heure française).
- Nouvelle galaxie événementielle avec 10 planètes et 4 bâtiments spécifiques par planète.
- Les bâtiments génèrent des bonbons, monnaie temporaire indépendante des crédits principaux.
- Boutique de boosts achetés en bonbons : multiplicateurs de production et de clic à durée limitée.
- Thème saisonnier orange/violet, carte événementielle, effets de toile d'araignée dans les coins.
- Les bonbons et bâtiments événementiels sont stockés dans `state.halloween`; les données de progression existantes sont conservées.
- Les boosts déjà achetés continuent jusqu'à leur expiration même si l'événement se termine.

### Mise à jour prudente
Teste d'abord cette archive sur une branche GitHub distincte ou un déploiement de prévisualisation. Vérifie les sauvegardes locales et Supabase avant de remplacer le jeu public. Le changement de thème et les ajouts d'événement ne nécessitent pas de migration SQL.


## Halloween V2 (15 octobre 2026)
- La carte de la galaxie Halloween ouvre maintenant l’onglet **Colonie**.
- Bouton de clic 🍬 dans le Centre lorsque la galaxie Halloween est sélectionnée.
- Les planètes Halloween se débloquent dans l’ordre : les 4 bâtiments de la planète précédente doivent avoir au moins un niveau. La planète 1 est ouverte dès le départ.
- Boutique des maléfices avec 20 boosts à prix progressifs, dans un menu déroulant.
- Missions d’Halloween avec récompenses en bonbons, dans un menu déroulant dans Colonie et dans Missions.
- Thème orange/violet renforcé dans le Centre, y compris l’arrière-plan et le bouton de forage.
- Une réserve de départ de 250 bonbons est attribuée une seule fois pour permettre de démarrer l’événement.

Tester sur une branche séparée avant de remplacer la version publique. Cette archive a été vérifiée par contrôle de syntaxe JavaScript, mais pas par un test navigateur complet.


## V4 — Correctif accordéons
- Les groupes Tech, Missions et la Boutique des maléfices sont fermés par défaut au chargement.
- L’ouverture/fermeture est stockée en mémoire, indépendamment du DOM, pour résister au rendu automatique toutes les 250 ms.
- Les clics sur les résumés sont gérés explicitement afin d’éviter que le rendu ne referme immédiatement les panneaux.
- Cache du service worker et versions des ressources mis à jour.
