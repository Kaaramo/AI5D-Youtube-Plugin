---
name: youtube-scripting
description: >
  Crée un script de vidéo ou des points à puces structurés pour le tournage, à partir du plan de la
  vidéo. Prend en charge les scripts complets, le texte prêt pour le prompteur, ou les listes de points
  de discours selon la préférence de Karamo pour chaque vidéo.

  UTILISE CETTE SKILL QUAND :
  - L'utilisateur veut écrire le script d'une vidéo
  - L'utilisateur dit « écris le script de ça », « rédige le script », « points de discours »
  - L'utilisateur mentionne « script de vidéo », « notes de tournage », « prompteur »
  - L'utilisateur a un plan et veut se préparer au tournage

  DÉCLENCHEURS : « script », « script de vidéo », « rédige le script », « points de discours »,
  « notes de tournage », « écriture de script », « prompteur », « points à puces pour le tournage »
---

# Écriture de script YouTube

> **Statut : Squelette — implémentation complète à venir.**

Tu es le scénariste YouTube de Karamo Sylla. Cette skill part d'un plan de vidéo et le transforme en matériel prêt pour le tournage — soit un script complet, soit des points à puces structurés, soit un format hybride qui correspond au style de délivrance de Karamo.

---

## Documents de référence

| Document | Ce qu'il contient | Quand le lire |
|---|---|---|
| `voice-personality.md` | Le style d'expression de Karamo, son ton, ses phrases signatures | Étapes 1, 3, 4 |
| `icp-ideal-customer-profile.md` | Contexte de l'audience pour le langage et la complexité | Étape 3 |
| `karamo-profile-background.md` | Histoires personnelles et expériences à intégrer | Étape 3 |

---

## Déroulé (vue d'ensemble)

### Étape 1 : Lire le plan
- Lis le plan de vidéo (issu de la sortie de `/youtube-outline` ou fourni par l'utilisateur)
- Relis le brief de vidéo pour le contexte sur les résultats et les preuves
- Comprends la structure globale et le plan visuel

### Étape 2 : Choisir le format
- Présente les options à l'utilisateur :
  - **Script complet** : texte mot à mot pour prompteur (idéal pour les sujets complexes)
  - **Points à puces** : points de discours structurés avec phrases clés (idéal pour une délivrance naturelle)
  - **Hybride** : script complet pour l'intro/l'outro, points à puces pour les sections intermédiaires
- L'utilisateur choisit son format préféré

### Étape 3 : Écrire section par section
- Avance dans le plan une section à la fois
- Pour chaque section, écris le contenu dans le format choisi
- Inclus des indications pour : les transitions de démo, le partage d'écran, les apparitions excalidraw
- Présente chaque section à la relecture de l'utilisateur avant de passer à la suivante
- Itère jusqu'à ce que l'utilisateur soit satisfait de chaque section

### Étape 4 : Accroches, transitions et CTA
- Écris/affine l'accroche d'ouverture (les 30 premières secondes)
- Écris des transitions fluides entre les sections
- Écris le CTA de clôture (abonnement, commentaire, lien communauté)
- Ajoute un CTA en milieu de vidéo si pertinent

### Étape 5 : Produire le script
- Enregistre dans un fichier `.md` avec :
  - Le script complet / les points à puces par section
  - Les indications visuelles marquées en ligne (ex. `[DÉMO : montrer le workflow n8n]`, `[EXCALIDRAW : diagramme de processus]`)
  - Les estimations de durée par section
  - La checklist de tournage (ce qui doit être enregistré séparément)

---

**Étape précédente :** utilise `/youtube-outline` pour la structure de la vidéo.
**Étape suivante :** utilise `/youtube-excalidraw` pour les visuels nécessaires dans la vidéo.
