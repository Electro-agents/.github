# Agents IA sur Claude

Des agents IA spécialisés, construits avec une méthode commune : **un noyau stable, des métiers interchangeables**. Chaque dépôt contient un agent ; la méthode et le modèle de départ sont dans [methode-agents](https://github.com/__ORG__/methode-agents).

```mermaid
flowchart TD
  M[methode-agents<br>10 prompts + modèle] --> N[noyau-coach v1]
  N --> G[greenfit-coach<br>coaching-sportif-greenfit v1]
  N -. prochain métier .-> X[nouvel agent<br>= nouvelle skill]
```

| Dépôt | Rôle | État |
| --- | --- | --- |
| [methode-agents](https://github.com/__ORG__/methode-agents) | Suite de 10 prompts, architecture mutable, modèle de nouvel agent | Stable |
| [greenfit-coach](https://github.com/__ORG__/greenfit-coach) | GREENFIT AI, coach sportif | Conception terminée (prompts 0 à 3) |

**Principes** : le système le plus simple qui atteint les critères · stable au début, variable à la fin (cache) · le calcul reste en code · aucun changement sans évals · jamais la triade létale.

**Ajouter un agent** : copier `methode-agents/modele-agent` dans un nouveau dépôt, puis lancer le prompt 0 avec le métier visé.
