# Projet : Prototypes de sites pour restaurants (prospection)

## Objectif
Démarcher des restaurants en leur montrant un prototype de site déjà fait à leur nom.

## Workflow (pour chaque restaurant donné par l'utilisateur)
1. Rechercher le restaurant : adresse, horaires, type de cuisine, menu/carte, ambiance, avis, réseaux sociaux, images.
2. Noter les infos clés dans la section "Restaurants" ci-dessous (court, pour économiser les tokens).
3. **Attendre le "top" de l'utilisateur avant de coder.**
4. Générer la page dans `site/prototype/<slug-du-restaurant>/index.html` → URL : `<domaine-netlify>/prototype/<slug>/`.
5. Ne PAS l'ajouter à la vitrine (liens envoyés directement aux prospects).
6. Mettre à jour ce fichier, commit + push sur GitHub (Netlify redéploie automatiquement une fois relié).

## Dépôt
- GitHub : https://github.com/louismaillet/prototypes-restaurants (branche `main`, push OK depuis Claude).
- Netlify : publish directory = `site`.

## Règles des prototypes
- Balise `<meta name="robots" content="noindex, nofollow">` sur chaque page.
- Bandeau discret "Maquette proposée par [nom à définir]".
- Design moderne, responsive (mobile d'abord), un seul fichier HTML par restaurant.
- Sections : voir "Style des prototypes" ci-dessous (version légère).
- Partir d'un template commun pour aller vite, puis personnaliser (couleurs, ton, photos).

## Structure du dossier
```
prototypes-restaurants/
├── CLAUDE.md
└── site/                       ← dossier à déposer sur Netlify
    ├── index.html              (vitrine Louis Maillet — FAIT)
    ├── _headers                (noindex sur /prototype/*)
    └── prototype/
        ├── index.html          (redirige vers l'accueil)
        └── <slug>/index.html   (un dossier par restaurant)
```

## Décisions (confirmées par l'utilisateur)
- **Marque** : Louis Maillet, développeur web (Olivet, 45). Site : https://louismaillet.fr — bandeau : "Maquette proposée par Louis Maillet" + lien louismaillet.fr. LinkedIn : https://www.linkedin.com/in/louis-maillet-06064a32b/. Pas d'email/tél publics sur son site → lien vers le site.
- Références à citer dans la vitrine : Gîtes La Grande Boeufferie, European CLIL Academy, refonte Oumami (restaurant asiatique).
- **Hébergement** : Netlify (sites statiques, pas de back-end).
- **index.html racine** : page vitrine très simple — qui il est, ce qu'il fait (sites pour restaurants), lien vers louismaillet.fr. NE PAS lister les prototypes.
- **Images** : pas de vraies photos. Placeholder à plat (bloc coloré) avec le texte "Illustration".
- **Style des prototypes** : SIMPLES et LÉGERS, peu de contenu. Sections limitées : hero, courte présentation, quelques plats/carte, horaires + adresse, contact. Pas de galerie lourde, pas de JS inutile.

## Restaurants
(aucun pour l'instant)
