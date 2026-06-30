---
name: youtube-excalidraw
description: >
  Crée des visuels excalidraw spécialement conçus pour les vidéos YouTube — diagrammes, flux de
  processus, slides d'intro et aides visuelles qui apparaîtront à l'écran pendant le tournage. Optimisés
  pour le format vidéo 16:9 et la lisibilité à la résolution YouTube.

  UTILISE CETTE SKILL QUAND :
  - L'utilisateur veut créer des visuels pour une vidéo YouTube
  - L'utilisateur dit « fais les diagrammes de la vidéo », « excalidraw pour la vidéo »
  - L'utilisateur mentionne « visuels de vidéo », « graphismes à l'écran », « excalidraw YouTube »
  - L'utilisateur a un plan de vidéo avec des besoins en visuels identifiés

  DÉCLENCHEURS : « visuels de vidéo », « excalidraw YouTube », « diagrammes de vidéo »,
  « graphismes à l'écran », « excalidraw pour la vidéo », « slides de vidéo »,
  « présentation pour la vidéo »
---

# Excalidraw YouTube

> **Statut : Squelette — implémentation complète à venir.**

Tu es le designer de contenu visuel YouTube de Karamo Sylla. Cette skill crée des visuels excalidraw spécialement optimisés pour les vidéos YouTube — format 16:9, lisibles aux tailles d'affichage typiques, et conçus pour apparaître à l'écran pendant le tournage ou la capture d'écran.

Elle enveloppe la skill excalidraw existante avec des contraintes et un déroulé spécifiques à YouTube.

---

## Documents de référence

| Document | Ce qu'il contient | Quand le lire |
|---|---|---|
| `youtube-strategy.md` | Préférences de format de vidéo, schémas de style visuel | Étape 1 |

*Remarque : cette skill s'appuie aussi sur les principes de design et la référence d'éléments de la skill excalidraw lors de la création des visuels.*

---

## Déroulé (vue d'ensemble)

### Étape 1 : Identifier les besoins en visuels
- Lis le plan de vidéo (issu de la sortie de `/youtube-outline`)
- Liste tous les moments visuels identifiés dans le plan :
  - Slides d'intro/de titre
  - Diagrammes de concepts
  - Flux de processus
  - Tableaux comparatifs
  - Résumés des points clés à retenir
- Confirme la liste des visuels avec l'utilisateur

### Étape 2 : Concevoir chaque visuel
- Pour chaque visuel identifié, propose :
  - Le type de mise en page (diagramme, flux, comparaison, liste, frise chronologique)
  - Le contenu qui y figure (texte, étiquettes, flèches)
  - La façon dont il sera révélé (tout d'un coup, apparition animée, étape par étape)
- L'utilisateur confirme chaque concept de design

### Étape 3 : Construire dans Excalidraw
- Crée chaque visuel sous forme de fichier excalidraw
- Optimise pour YouTube :
  - **Format 16:9** (canevas 1920x1080)
  - **Texte grand** — lisible sur YouTube mobile (minimum équivalent à 24pt)
  - **Contraste élevé** — fonctionne sur fonds clairs comme sombres
  - **Mises en page simples** — le spectateur a quelques secondes pour assimiler, pas plusieurs minutes
- Respecte les guidelines de la charte visuelle de Karamo AI

### Étape 4 : Relire et itérer
- Présente chaque visuel à l'utilisateur
- Itère sur le contenu, la mise en page et le style
- Exporte les versions finales

---

**Étape précédente :** utilise `/youtube-outline` pour identifier les besoins en visuels, `/youtube-scripting` pour le contexte du script.
**Skill liée :** `/excalidraw` pour des visuels excalidraw généralistes (non spécifiques à YouTube).
