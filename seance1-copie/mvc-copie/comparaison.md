
# TP 1 — Étape 4 : Comparaison des architectures

| Critère | MVC | MVP | MVVM |
|---|---|---|---|
| Signification | Model-View-Controller | Model-View-Presenter | Model-View-ViewModel |
| Composant principal de coordination | Controller | Presenter | ViewModel |
| Rôle | Transmet les actions au modèle | Coordonne la vue et le modèle | Prépare les données et l'état de présentation |
| Communication avec la vue | La vue transmet les actions au contrôleur | La vue transmet les actions au Presenter | La vue est liée à l'état du ViewModel |
| Avantage | Architecture simple | Logique de présentation bien séparée | Mise à jour de l'interface facilitée |
| Limite | Le contrôleur peut devenir trop chargé | Le Presenter peut devenir volumineux | Les liaisons peuvent être complexes |
| Exemple en Data | Affichage de données | Préparation d'indicateurs | Tableau de bord interactif |

## Application à la spécialité Data

| Besoin | Architecture adaptée | Justification |
|---|---|---|
| Afficher des données | MVC | Sépare les données, les actions et l'affichage |
| Préparer des indicateurs | MVP | Centralise la logique de présentation |
| Créer un tableau de bord interactif | MVVM | Facilite la synchronisation entre l'état et l'affichage |

## Conclusion

Pour un tableau de bord interactif en Data, je choisirais MVVM, car il facilite la mise à jour de l'interface lorsque les données ou les filtres changent. Le choix dépend néanmoins des besoins du projet.
