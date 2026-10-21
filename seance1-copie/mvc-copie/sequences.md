
# TP 1 — Étapes 1 et 2

## Étape 1 : Exécution des tests

Les tests des trois exemples MVC, MVP et MVVM ont été exécutés.

- MVC : tests du TodoModel.
- MVP : tests du LoginPresenter.
- MVVM : tests du CartViewModel.

Les tests exécutés sont réussis, sans échec.

## Étape 2 : Diagrammes de séquence

### Diagramme MVC — Ajouter une tâche

```mermaid
sequenceDiagram
    actor U as Utilisateur
    participant V as TodoView
    participant C as TodoController
    participant M as TodoModel

    U->>V: Saisit le titre et valide
    V->>C: Transmet le titre
    C->>M: add(title)
    M->>M: Vérifie le titre
    M->>M: Ajoute la tâche
    M-->>V: Notifie les abonnés
    V->>V: render(todos)
    V-->>U: Affiche la nouvelle tâche
```

### Diagramme MVVM — Ajouter une tâche

```mermaid
sequenceDiagram
    actor U as Utilisateur
    participant V as View
    participant VM as ViewModel
    participant M as Model

    U->>V: Saisit le titre et valide
    V->>VM: Demande l'ajout de la tâche
    VM->>M: Ajoute la tâche
    M->>M: Met à jour les données
    M-->>VM: Retourne le résultat
    VM-->>V: Met à jour l'état affiché
    V-->>U: Affiche la nouvelle tâche
```
