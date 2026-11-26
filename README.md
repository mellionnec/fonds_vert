# Observatoire du Fonds vert en Bretagne

Analyse du programme Fonds vert (Ministère de la Transition écologique), dispositifs 2023-2025.
Sources des données : https://www.data.gouv.fr/datasets/fonds-vert-liste-des-projets-subventionnes

`index.html` est un tableau de bord autonome (DSFR + Leaflet + Chart.js) couvrant les quatre départements bretons :

- **Synthèse** : KPI (montant engagé, projets, communes, ratio €/hab., montant moyen et médian par projet, bénéficiaires distincts), graphiques par thématique, par année, top 10 des bénéficiaires et répartition par tranche de montant ;
- **Carte** : cercles proportionnels par projet ou choroplèthe des EPCI (montant engagé ou ratio €/hab.), fiches projet avec photo ;
- **Projets** : liste triable et export CSV de la sélection.

Filtres : année, département, thématique, tranche de montant, recherche libre. Thème clair/sombre mémorisé.

**Rattachement des projets sans commune** : 56 projets (dont des projets intercommunaux ou départementaux) n'ont pas de commune renseignée dans le fichier source. Ils sont rattachés au siège de leur bénéficiaire principal (API Recherche d'entreprises, via le SIREN fourni par data.gouv.fr) et marqués « localisation approximative » dans leur fiche. Le champ `rattachement` du JSON indique l'origine ; `fv_no_geo.json` conserve l'archive initiale.

Ouvrir via un serveur (GitHub Pages ou serveur local, pas en `file://`). Données : `fonds_vert_bretagne.json`, `fonds_vert_bretagne_2.json` et `fonds_vert_bretagne_3.json` (1 437 projets au total, découpage en 3 fichiers pour rester sous les limites de taille des outils de dépôt), contours EPCI : `epci_simple.geojson`, projets sans rattachement géographique : `fv_no_geo.json`.

Historique : la première version (Côtes-d'Armor uniquement, onglets Analyse et Cartographie simple) est conservée dans les fichiers `projets_cotes_darmor.html`, `top12_cotes_darmor.html` et `communes_bzh.html`.
