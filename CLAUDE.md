# Projet : Prototypes de sites pour restaurants (prospection)

## Objectif
Démarcher des restaurants en leur montrant un prototype de site déjà fait à leur nom.

## Workflow (pour chaque restaurant donné par l'utilisateur)
1. Rechercher le restaurant : adresse, horaires, type de cuisine, menu/carte, ambiance, avis, réseaux sociaux, images.
2. Noter les infos clés dans la section "Restaurants" ci-dessous (court, pour économiser les tokens).
3. **Attendre le "top" de l'utilisateur avant de coder.**
4. Générer la page dans `site/prototype/<slug-du-restaurant>/index.html` → URL : `<domaine-netlify>/prototype/<slug>/`.
5. Ajouter un bouton vers le prototype dans la barre « Maquettes » en haut de `site/index.html`.
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
- **index.html racine** : page vitrine très simple — qui il est, ce qu'il fait (sites pour restaurants), lien vers louismaillet.fr. **Changement (08/10)** : barre « Maquettes : » tout en haut avec un bouton par prototype (demande utilisateur) → ajouter un bouton à chaque nouveau prototype.
- **Images** : par défaut, placeholder à plat (bloc coloré) avec le texte "Illustration". Version « complète » sur demande : photos libres Unsplash en hotlink (images.unsplash.com, crédits en pied de page, mention « photos d'illustration »). Jamais les photos du restaurant prises sur Google/TripAdvisor.
- **Style des prototypes** : SIMPLES et LÉGERS, peu de contenu. Sections limitées : hero, courte présentation, quelques plats/carte, horaires + adresse, contact. Pas de galerie lourde, pas de JS inutile.

## Restaurants

### Le Pré de Frazé — slug `le-pre-de-fraze` — FAIT (2026-10-08)
- URL : `/prototype/le-pre-de-fraze/`. Ex-« L'Étape des Saveurs » de Frazé (même adresse, repris/renommé ; le nom L'Étape des Saveurs survit à Brou → aucomptoirbrou.com, qui a déjà un site).
- 6 rue du 8 Mai 1945, 28160 Frazé. Tél 02 37 37 01 92, lepredefraze@yahoo.com, Instagram @le.pre.de.fraze. Pas de site propre.
- Cuisine française, formules plancha, menus originaux, salon de thé/bar ; épicerie de terroir (style brocante) ; chambres d'hôtes pour cyclistes Véloscénie (recharge VAE). Terrasse, parking, animaux OK, emporter, traiteur.
- Prototype version COMPLÈTE : hero photo plein écran, 3 univers avec photos (restaurant, épicerie, chambres), carte 4 blocs (plancha, entrées, desserts/enfant, salon de thé/bar) sans prix, section Véloscénie, galerie 5 photos Unsplash, horaires « À compléter » (non trouvés), services, Google Maps intégrée, contact tél/email/Instagram.
- Alternative non faite : Au Comptoir by L'Étape des Saveurs, 3 place des Halles, Brou (02 37 96 05 69).

### Crêperie L'Argoat — slug `creperie-largoat` — FAIT (2026-10-08)
- URL : `/prototype/creperie-largoat/`. Version COMPLÈTE (demande utilisateur) : hero photo plein écran, section maison + services, carte 4 blocs (galettes, crêpes, salades, boissons/enfant) sans prix, avis (notes Google/TA + 3 thèmes, pas de faux témoignages), galerie 5 photos Unsplash, horaires confirmés par l'utilisateur (mer–dim 12h–22h ; fermé lun + mar), carte Google Maps intégrée, paiements, footer mentions légales. Pas d'email (suspect) → téléphone seul.
- Mail de prospection rédigé (constat détaillé de la page eatbu : pas de carte/photos/avis, mentions légales « FR1234 A COMPLETER », lien données vide, sous-domaine eatbu). Pas encore envoyé.
- 9 place d'Armes, 28160 Brou. Tél 02 37 47 00 65. Email (fiche eatbu) michelverrier@range.fr (domaine suspect, à vérifier).
- Site actuel : creperie-l-argoat.eatbu.com (mini-page DISH, pas de carte, mentions légales « A COMPLETER ») → argument de prospection.
- Crêperie familiale : galettes de blé noir, crêpes, tartes, plats régionaux, sur place ou à emporter. Terrasse, salles climatisées, parking gratuit. CB/sans contact.
- Horaires CONFIRMÉS (utilisateur, 08/10) : mercredi–dimanche 12h–22h, fermé lundi et mardi (la page eatbu est fausse).
- Avis : Google 4,2/5 (325), TripAdvisor 4,0/5 (143). Portions généreuses, prix doux, accueil familial, bonbons d'enfance offerts en fin de repas (roudoudous, violettes). Pas de carte avec prix en ligne.

### Les Tontons Fines Gueules — slug `les-tontons-fines-gueules` — recherche faite, en attente du "top"
- 51 rue Jean Moulin, 28290 Chapelle-Royale (Perche, Eure-et-Loir). Tél 02 18 00 63 44. Facebook : facebook.com/LesTontonsFinesGueules (seule présence en ligne, pas de site).
- Restaurant traditionnel / bar, ambiance décontractée, petit-déj dès 7h, sur place, à emporter, livraison. Prix moyen ~25 €. Parking gratuit, accès PMR. Desserts.
- Horaires (kazfeed) : mar–jeu 7h–16h30 ; ven–sam 7h–21h30 ; fermé dim + lun → à confirmer.
- Avis : Google 4,7/5 (≈37 avis) ; Facebook 4,8 (selon utilisateur). Établissement récent (fiches 2025).
- Pas de carte en ligne. Nom = clin d'œil aux « Tontons flingueurs » → ton humoristique possible, sans reprendre visuels/répliques du film.
