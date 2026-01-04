---

## 🔗 Power BI : joins en Power Query, relations dans le modèle

![Power BI](https://img.shields.io/badge/Power%20BI-Modeling-yellow?style=for-the-badge)
![Power Query](https://img.shields.io/badge/Power%20Query-M%20Language-blue?style=for-the-badge)
![Join Logic](https://img.shields.io/badge/Join-Left%20%7C%20Right%20%7C%20Inner%20%7C%20Full-informational?style=for-the-badge)

> [!IMPORTANT]
> Dans Power BI, le choix du type de jointure (LEFT / RIGHT / INNER / FULL) se fait dans Power Query via <i>Merge Queries</i>.  
> Le modèle Power BI, lui, gère ensuite des <i>Relationships</i> entre tables pour la navigation analytique.

---

### 🧩 1) Créer une jointure : Merge Queries (Power Query)

Dans Power BI, si je veux “créer une jointure” au sens SQL (choisir LEFT / RIGHT / INNER / FULL), je passe par :

- Power Query Editor
- Home → Merge Queries
- choix des colonnes de matching
- choix du Join kind : Left Outer / Right Outer / Inner / Full Outer / Anti Join

> [!TIP]
> Merge Queries = jointure au moment de la préparation (ETL).  
> C’est ici que je matérialise le résultat (table fusionnée) avant d’arriver au modèle.

---

### 🧠 2) Exploiter les tables : Relationships (Model view)

Une fois les données préparées, Power BI utilise des relations dans la vue Modèle :
- cardinalité : 1:* , *:* , 1:1
- direction de filtrage : Single / Both
- clé de relation (dimension → fait dans l’idéal)

> [!NOTE]
> Le modèle Power BI ne me demande pas d’écrire une jointure SQL à chaque visuel.  
> Il s’appuie sur les <i>relationships</i> pour propager les filtres et calculer correctement les mesures.

---

### ⚙️ 3) Lecture “technique” (ce que ça veut dire concrètement)

┌─ Power Query (ETL) ──────────────────────────────┐  
│ Merge Queries = choisir le type de JOIN          │  
│ Résultat = données combinées / enrichies         │  
└──────────────────────────────────────────────────┘  
                ↓ chargement  
┌─ Model (Semantic Layer) ─────────────────────────┐  
│ Relationships = structure analytique             │  
│ Cardinality + filter direction = comportement    │  
└──────────────────────────────────────────────────┘  

> [!WARNING]
> Beaucoup d’erreurs Power BI viennent d’un mauvais choix :  
> faire une jointure (Merge) alors qu’une relation suffisait, ou l’inverse.  
> Mon réflexe : je décide selon l’objectif (préparer vs analyser).

---

### 🗺️ Mini schéma (mental model)

```mermaid
flowchart LR
  A[Source tables] --> B[Power Query: Merge Queries<br/>LEFT / RIGHT / INNER / FULL]
  B --> C[Loaded tables]
  C --> D[Model view: Relationships<br/>Cardinality + Filter direction]
  D --> E[Reports: visuals + DAX measures]
