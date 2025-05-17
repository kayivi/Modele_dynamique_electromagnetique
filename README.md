# ⚡ Jumeau numérique pour le couplage électromagnétique (stage ENIT)

Ce dépôt contient mes travaux liés à mon stage de fin d'études réalisé au Laboratoire Génie de Production (LGP - ENIT) à Tarbes, dans le cadre de l’optimisation d’un système de traction ferroviaire.\
\
Sujet : Représentation énergétique des systèmes décrits par équations aux dérivées partielles (EDP) — Application aux phénomènes électromagnétiques

## 🎯 Objectif

Développer un jumeau numérique multiphysique pour le couplage électromagnétique :
- Équations de Maxwell
- Discrétisation en **volumes finis (FVM)**
- Modélisation énergétique par **Bond Graph**
- Simulation 

L’objectif final est de représenter le comportement électromagnétique du système de manière dynamique, afin d'aider à l’optimisation du compromis coût/rendement dans un système de traction ferroviaire électrique.

---

## ⚙️ Méthodologie

- **Modélisation des champs** électriques et magnétiques à partir des équations de Maxwell
- Discrétisation par FVM sur maillages cartésiens (et triangulaires via FreeFem++)
- Utilisation des Bond Graph pour représenter les échanges de puissance et la causalité
- Intégration temporelle par représentattion d'état
- Construction de la **matrice d’état dynamique** : $` \quad \dot{x} = Ax + Bu`$
- Simulation sur un cas pratique en 2D (fil infini)

---

## 📁 Organisation du dépôt

- `src/` : code source Python de la simulation FVM en 2D pour le fil infini
- `results/` : résultats numériques (champ magnétique H, densité de courant, validations 1D)
- `figures/` : images clés du projet (Domaine, Bond Graph, semi Bond Graph sur un élément dans l'air)
- `docs/` : présentation PDF, rapport de stage (en anglais)

---

## 📷 Exemples de résultats

| Champ magnétique \\( H \\) | Bond Graph |
|---------------------------|-------------------|
| ![](figures/champ_H.png)  | ![](figures/bond_graph_global.png) |
