# 📈 Croissance & Éducation – Projet Collectif 2

## 👨‍🏫 Sujet

Projet réalisé en L3 dans le cadre d’un travail collectif portant sur la question suivante :  
**"Croissance et éducation sont-elles liées, et comment ?"**

L’objectif était d’étudier cette problématique en deux étapes :
1. Recherche documentaire via la lecture d’articles scientifiques et de rapports.
2. Analyse économétrique à l’aide de données extraites de la base **World Development Indicators (WDI)** et de fichiers fournis par l’enseignant.

---

## 👥 Auteurs

- Marc  
- Hugo  
- Ludovic  
- Maxime  
- Jean-Baptiste  
- Mathias  

---

## 🧠 Contexte

La relation entre croissance économique et éducation est complexe.  
Bien que l'éducation soit souvent considérée comme un moteur du développement, elle ne suffit pas à elle seule à expliquer la dynamique de croissance. De nombreux facteurs tels que le chômage, le contexte géopolitique ou encore la qualité institutionnelle peuvent interférer.  

Ce projet visait à illustrer cette complexité à travers des modèles de régression linéaire simples et des instruments économétriques.

---

## 📂 Données

- **Sources** :
  - World Bank – World Development Indicators (WDI)
  - Fichiers Excel et CSV fournis par l’enseignant

- **Pays analysés** :  
  13 pays d’Afrique subsaharienne, dont le Burkina Faso, le Ghana, le Mali, le Nigeria, etc.

- **Période** :  
  1985 à 2015

---

## 📦 Packages R utilisés

```r
library(foreign)
library(psych)
library(data.table)
library(lmtest)
library(sandwich)
library(margins)
library(haven)
library(readxl)
library(AER)
```

## 🔧 Traitement & Construction des modèles
Nettoyage des fichiers et remplacement des valeurs manquantes (..) par NA

Agrégation des données par année pour créer un panel simplifié

Fusion des différentes sources

Construction de trois régressions :

## 🔹 Régression 1
Relation entre le taux d’alphabétisation et le PIB.
→ Coefficient significatif, R² ajusté de 0.69
⚠️ Présence probable de biais d’omission de variables

## 🔹 Régression 2
Lien entre dépenses publiques en éducation (en % du PIB) et croissance.
→ Peu de données disponibles, modèle peu fiable.

## 🔹 Régression 3 – Régression instrumentale (IV)
Utilisation de variables instrumentales :

Conditions socio-économiques

Qualité de la bureaucratie
→ Coefficients non significatifs, R² ajusté négatif, modèle non concluant.

## 📉 Interprétation
Les résultats économétriques confirment que la relation croissance ↔ éducation n’est pas directe.

Le taux d’alphabétisation semble jouer un rôle, mais il est difficile d’en isoler l’effet causal.

Les dépenses gouvernementales ne montrent pas d'effet direct significatif.

Une analyse plus robuste nécessiterait des données plus complètes et un meilleur contrôle des variables confondantes.

## 📌 Conclusion
L’éducation est un facteur parmi d'autres de la croissance économique.
Bien qu’elle constitue un levier important du développement, son impact réel dépend de nombreux paramètres externes.

Ce projet a permis de :

Manipuler des données économiques réelles

Construire des modèles économétriques

Mieux comprendre la complexité des politiques publiques de développement


