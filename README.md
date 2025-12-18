# 📕 CRÉATOPIOS

Document de Conception Global
*(Game Design Document + Spécifications Fonctionnelles)*

---

## 0. UNIVERS & CONTEXTE NARRATIF

### 0.1 Le Monde de Créatopios

Créatopios est un monde vivant, composé de territoires élémentaires où coexistent des créatures appelées **Créatopiens**.
Chaque Créatopien est lié à une forme d’énergie naturelle : écorce, foudre, ombre, eau, vent, harmonie, etc.

Ces créatures ne sont ni bonnes ni mauvaises : elles incarnent des forces brutes de l’équilibre du monde.

### 0.2 Les Éleveurs

Les **Éleveurs** sont des êtres rares, capables de créer un **Lien** avec les Créatopiens.

* N’interviennent jamais physiquement
* Ne sont jamais visibles
* Agissent uniquement par stratégie et anticipation

Ils ne contrôlent pas directement les Créatopiens mais orchestrent leur coopération.

### 0.3 La Grande Confrontation

Depuis la disparition de l’ancien Roi des Éleveurs, l’équilibre de Créatopios s’est fragilisé.

Les Éleveurs s’affrontent lors de **Confrontations de Liens**, des épreuves stratégiques ritualisées destinées à désigner :

🏆 **Le nouvel Éleveur Gardien de l’Équilibre**

---

## 1. VISION GÉNÉRALE DU JEU

### 1.1 Concept

**Créatopios** est un jeu de stratégie tactique au tour par tour, **sans hasard**, jouable de **2 à 4 joueurs**.

Chaque joueur incarne un Éleveur dirigeant une équipe de Créatopiens sur une carte en grille.

🎯 **Objectif** :
Être le dernier Éleveur possédant au moins un Créatopien en jeu.

### 1.2 Piliers de Design

* Zéro hasard (aucun RNG)
* Information parfaite
* Décisions irréversibles
* Synergies d’équipe
* Rythme maîtrisé (max 4 joueurs)

---

## 2. RÈGLES DU JEU

### 2.1 L’Éleveur

* N’a pas de points de vie
* N’est pas une entité sur le plateau
* Ne peut ni être ciblé, ni attaqué

**Élimination** :
Un Éleveur est éliminé dès qu’il n’a plus aucun Créatopien sur le plateau.

### 2.2 Création et Gestion des Équipes

* Maximum **8 équipes** sauvegardées par Éleveur
* Une seule équipe utilisée par partie

**Budget de recrutement** :

* Budget fixe : **10 points**
* **1 à 10 Créatopiens** par équipe
* Le coût total ne peut jamais dépasser 10

### 2.3 Classes de Créatopiens

| Classe               | Coût | PV | Force | Mobilité | Portée | Pouvoir                    |
| -------------------- | ---- | -- | ----- | -------- | ------ | -------------------------- |
| Garde de l’Écorce    | 3    | 15 | 2     | 2        | 1      | Régénère 1 PV              |
| Armurion             | 3    | 13 | 3     | 1        | 1      | Ignore 1 dégât/tour        |
| Archimage Végétal    | 3    | 5  | 4     | 2        | 3      | —                          |
| Lanceur d’Éclairs    | 3    | 4  | 4     | 2        | 3      | Ignore obstacles           |
| Esprit de la Cascade | 2    | 6  | 2     | 4        | 2      | Régénère 1 PV              |
| Sylphide             | 2    | 5  | 2     | 5        | 2      | Soin + déplacement 1       |
| Ombrefeu             | 2    | 6  | 3     | 6        | 2      | +1 Force après déplacement |
| Ombrelame            | 2    | 5  | 3     | 7        | 2      | Traverse 1 ennemi          |
| Lien-Tisseur         | 1    | 5  | 0     | 4        | —      | Régénère 2 PV              |
| Harmonisatrice       | 1    | 4  | 0     | 5        | —      | Régénère 1 PV à 2 alliés   |
| Voltigeur            | 1    | 4  | 1     | 8        | 1      | Attaque + déplacement 2    |
| Aérospirale          | 1    | 3  | 2     | 9        | 1      | Ignore zones de menace     |

### 2.4 Cartes et Arènes

| Taille   | Dimensions | Joueurs |
| -------- | ---------- | ------- |
| Petite   | 10×10      | 2       |
| Standard | 14×14      | 2–3     |
| Large    | 18×18      | 3–4     |

### 2.5 Système de Tour

* 4 Points d’Action (PA) par Éleveur
* PA non utilisés perdus
* Actions (1 PA) : Déplacement / Attaque / Pouvoir

### 2.6 Combat

* Dégâts = Force
* Portée stricte
* Créatopien éliminé à 0 PV

### 2.7 Victoire

🏆 Dernier Éleveur avec au moins un Créatopien en jeu

---

## 3. UI / UX — ÉCRANS

### 3.1 Écran de Connexion

```
+---------------------------+
|        CRÉATOPIOS         |
|                           |
|  [ Pseudo ]               |
|  [ Mot de passe ]         |
|                           |
|  ( Connexion )            |
|  ( Créer un compte )      |
+---------------------------+
```

### 3.2 Menu Principal

```
+----------------------------------+
| Joueur : Pseudo                  |
|----------------------------------|
| ▶ Jouer                          |
| ▶ Mes Équipes                    |
| ▶ Amis                           |
| ▶ Statistiques                   |
| ▶ Classement                     |
| ▶ Paramètres                     |
+----------------------------------+
```

### 3.3 Gestion & Création d’Équipe

```
+--------------------------------------------------+
| Nom de l’équipe : Équipe Rush                    |
| Budget : 7 / 10                                  |
|--------------------------------------------------|
| Créatopiens sélectionnés :                       |
| 1. Ombrelame (2)                                 |
| 2. Voltigeur (1)                                 |
|                                                  |
| Liste complète :                                 |
| [ + Garde de l'Écorce (3) ]                      |
| [ + Ombrefeu (2) ]                               |
| [ + Sylphide (2) ]                               |
|                                                  |
| [ Sauvegarder ]   [ Supprimer ]                  |
+--------------------------------------------------+
```

### 3.4 Création de Partie

```
+----------------------------------+
| Créer une Partie                 |
|----------------------------------|
| Joueurs : 2 – 4                  |
| Carte : Petite / Standard / Large|
| Mode : Amical / Classé           |
| [ Créer ]                        |
+----------------------------------+
```

### 3.5 Lobby

```
+----------------------------------+
| Lobby – Carte : Standard         |
|----------------------------------|
| Joueurs :                        |
| Pseudo1 ✔                        |
| Pseudo2 ⏳                       |
|----------------------------------|
| Chat                             |
| > Prêt ?                         |
|----------------------------------|
| [ Inviter ] [ Lancer ]           |
+----------------------------------+
```

### 3.6 Terrain de Jeu (Canvas)

Plateau central **15×15** (P) avec **zones de déploiement hors terrain** pour chaque joueur.

```
                                   +----+----+----+----+----+
                                   | J1 | J1 | J1 | J1 | J1 |
                                   +----+----+----+----+----+
                                   | J1 | J1 | J1 | J1 | J1 |
          +----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+
          |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
          +----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+
          |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
          +----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+
          |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
          +----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+
          |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
          +----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+
          |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
+----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+
| J3 | J3 |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    | J4 | J4 |
+----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+
| J3 | J3 |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    | J4 | J4 |
+----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+
| J3 | J3 |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    | J4 | J4 |
+----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+
| J3 | J3 |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    | J4 | J4 |
+----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+
| J3 | J3 |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    | J4 | J4 |
+----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+
          |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
          +----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+
          |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
          +----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+
          |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
          +----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+
          |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
          +----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+
          |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    | 
          +----+----+----+----+----+----+----+----+----+----+----+----+----+----+----+
                                   | J2 | J2 | J2 | J2 | J2 |
                                   +----+----+----+----+----+
                                   | J2 | J2 | J2 | J2 | J2 |
                                   +----+----+----+----+----+

```

---

## 4. FONCTIONNALITÉS DE L’APPLICATION

### 4.1 Comptes Joueurs

* Création / connexion
* Avatar
* Statut (en ligne / en partie)

### 4.2 Amis

* Ajouter / supprimer
* Voir statut
* Inviter en partie

### 4.3 Chat

* Lobby
* En partie
* Désactivable en classé

### 4.4 Statistiques

**Joueur** : parties, victoires, taux, temps moyen
**Équipes** : performances par créature

### 4.5 Classement

* Global
* Saisonnier
* Score ou Elo

---

## 5. MODÈLE DES ENTITÉS (DATA MODEL)

### 5.1 Joueur

```json
{ "id": "player_id", "pseudo": "string", "avatar": "string", "teams": ["team_id"], "stats": {} }
```

### 5.2 Équipe

```json
{ "id": "team_id", "name": "string", "budget": 10, "creatopiens": ["creatopien_id"], "stats": {} }
```

### 5.3 Créatopien

```json
{ "id": "creatopien_id", "type": "Ombrefeu", "pv_max": 6, "pv_current": 6, "force": 3, "mobilite": 6, "portee": 2, "capacites": [] }
```

### 5.4 Partie

```json
{ "id": "match_id", "players": ["player_id"], "map": { "width": 15, "height": 15 }, "state": "en_cours", "turn": "player_id" }
```
