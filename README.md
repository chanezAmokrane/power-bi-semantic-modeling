<!-- ========================= -->
<!--        README.md          -->
<!-- ========================= -->

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rect&height=120&text=Modélisation%20des%20données%20dans%20Power%20BI&fontSize=36&animation=blinking&fontAlignY=50" />
</p>

<p align="center">
  <i>Pas un cours.</i><br/>
  <i>De « stocker la donnée » à « modéliser pour l’analyse ».</i>
</p>

---

## 🧠 De stocker des données → répondre à des questions

### ✅ Vision base de données classique
- Réduire la redondance  
- Garantir la cohérence  
- Protéger l’intégrité  
- Utiliser des clés et des relations  
- Reconstruire l’information via des jointures SQL  

### ✅ Vision Power BI
Power BI change la question :

> « Comment la donnée est stockée ? » ❌  
> « Que s’est-il passé ? Combien ? Quand ? Pour qui ? » ✅

Le modèle doit être :
- orienté analyse  
- lisible pour l’humain  
- pensé pour la performance  

---

## 🧩 Comment Power BI perçoit la base de données

Dans Power BI, une base de données n’est pas seulement  
un ensemble de tables reliées entre elles.

Elle devient un **modèle analytique**, conçu pour :
- 🔎 l’exploration  
- 📊 le reporting  
- ⚡ le filtrage et l’agrégation rapides  
- 🧭 une navigation intuitive pour les utilisateurs métiers  

C’est pour cela que l’on raisonne en :

### 📌 Table de faits
Les événements mesurables (ventes, transactions, montants, quantités).

### 📌 Tables de dimensions
Le contexte (clients, produits, dates, localisations).

> Faits = ce qui s’est passé  
> Dimensions = comment on le décrit  

---

## ⭐ Schéma en étoile vs ❄️ schéma en flocon

### ⭐ Schéma en étoile (souvent privilégié dans Power BI)
- Plus lisible  
- Relations plus simples  
- Meilleures performances analytiques  

### ❄️ Schéma en flocon
- Moins de redondance  
- Plus normalisé  
- Modèle plus complexe  

📍 Il ne s’agit pas de « bon » ou « mauvais » modèle.  
C’est un choix qui dépend :
- du volume de données  
- des besoins métiers  
- des performances attendues  
- de la clarté pour l’utilisateur final  

---

## 🔗 Jointures et relations dans Power BI (le point clé)

Dans une base de données classique, les relations sont exprimées via des jointures SQL :
- INNER JOIN  
- LEFT JOIN  
- RIGHT JOIN  
- etc.

Dans Power BI, l’approche est différente.

### 🛠️ Les jointures sont créées en amont dans Power Query
Grâce à **Merge Queries**, on peut :
- créer de nouvelles jointures  
- choisir le type de jointure (left, right, inner…)  
- les modifier facilement  


