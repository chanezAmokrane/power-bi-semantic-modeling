<!-- ========================= -->
<!--        README.md          -->
<!-- ========================= -->

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&height=180&text=Data%20Modeling%20in%20Power%20BI&fontAlign=50&fontAlignY=35&desc=How%20I%20think%20about%20data%20models%20(SQL%20→%20Power%20BI)&descAlign=50&descAlignY=60" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Power%20BI-Modeling-F2C811?logo=powerbi&logoColor=000" />
  <img src="https://img.shields.io/badge/SQL-Relational%20Thinking-2F80ED?logo=postgresql&logoColor=fff" />
  <img src="https://img.shields.io/badge/Power%20Query-Merge%20Queries-00A4EF?logo=microsoft&logoColor=fff" />
  <img src="https://img.shields.io/badge/Focus-Analytics%20Ready-22C55E" />
</p>

<p align="center">
  <i>Not a textbook. A mindset.</i><br/>
  <i>From “storing data” to “modeling for analysis”.</i>
</p>

---
# 🧠 Modélisation des données – Vision Power BI

Ce dépôt ne présente pas un cours théorique de bases de données.  
Il montre comment j’aborde la modélisation des données lorsqu’elles sont destinées à être exploitées dans **Power BI**.

L’objectif n’est pas uniquement de stocker des données correctement,  
mais de construire un **modèle clair, cohérent et orienté analyse**.

---

## Du modèle relationnel à l’analyse

Dans une base de données classique, la modélisation vise principalement à :
- éviter la redondance  
- garantir la cohérence  
- assurer l’intégrité des données  

On raisonne en tables, clés primaires, clés étrangères, relations et cardinalités.  
Les jointures SQL permettent de reconstruire l’information lorsque c’est nécessaire.

Ce modèle est adapté aux usages transactionnels.

---

## Comment Power BI change la perception de la base de données

Dans Power BI, la base de données n’est plus pensée uniquement pour le stockage,  
mais comme un **modèle analytique**.

On ne se demande plus seulement :
> Comment la donnée est stockée ?

Mais plutôt :
> Que s’est-il passé ?  
> Combien ?  
> Quand ?  
> Pour qui ?

La modélisation est donc guidée par l’analyse et la lecture des données.

---

## Tables de faits et tables de dimensions

Dans ce contexte :
- la **table de faits** centralise les événements mesurables  
- les **tables de dimensions** apportent le contexte nécessaire à l’analyse  

Il ne s’agit pas d’un nouveau modèle opposé au relationnel,  
mais d’une organisation des données orientée usage analytique.

---

## Schéma en étoile et schéma en flocon

Dans Power BI :
- le **schéma en étoile** est souvent privilégié pour sa lisibilité et ses performances  
- le **schéma en flocon** réduit la redondance mais introduit plus de complexité  

Le choix dépend des besoins métiers, du volume de données et de la clarté attendue pour l’utilisateur final.

---

## Jointures et relations dans Power BI

Dans un modèle classique, les relations entre les tables sont exprimées via des jointures SQL  
(INNER JOIN, LEFT JOIN, RIGHT JOIN, etc.).

Dans Power BI, les jointures sont créées et modifiées **en amont** dans **Power Query**,  
à l’aide de **Merge Queries**, où l’on définit le type de jointure à appliquer.

Le modèle Power BI exploite ensuite ces données préparées à travers des relations entre les tables.

La logique relationnelle reste la même,  
mais Power BI déplace la construction des jointures vers la phase de préparation des données.

---

## En résumé

Power BI impose de penser la base de données non seulement comme un espace de stockage,  
mais comme un **support d’analyse**.

Ce dépôt reflète cette approche :  
concevoir un modèle de données compréhensible, cohérent et réellement exploitable.


---

### 📬 Want to talk?
If you’re a recruiter or a team looking for someone who can bridge **data + clarity + modeling**, feel free to reach out.
