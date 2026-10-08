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
- Gmail connecté MAIS **NE JAMAIS ENVOYER DE MAIL** (demande utilisateur 08/10) : donner seulement le texte prêt à copier (destinataire, objet, corps). C'est l'utilisateur qui envoie.
- Netlify : publish directory = `site`. Domaine : https://prototype-web-site.netlify.app (prototypes : https://prototype-web-site.netlify.app/prototype/<slug>/).

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
- **Marque** : Louis Maillet, développeur web (Olivet, 45). Site : https://louismaillet.fr — bandeau : "Maquette proposée par Louis Maillet" + lien louismaillet.fr. LinkedIn : https://www.linkedin.com/in/louis-maillet-06064a32b/. Pas d'email/tél publics sur son site → lien vers le site. Tél perso à mettre dans les mails de prospection : 07 82 52 45 37 (pas sur les maquettes).
- Références à citer dans la vitrine : Gîtes La Grande Boeufferie, European CLIL Academy, refonte Oumami (restaurant asiatique).
- **Hébergement** : Netlify (sites statiques, pas de back-end).
- **index.html racine** : page vitrine très simple — qui il est, ce qu'il fait (sites pour restaurants), lien vers louismaillet.fr. **Changement (08/10)** : barre « Maquettes : » tout en haut avec un bouton par prototype (demande utilisateur) → ajouter un bouton à chaque nouveau prototype.
- **Images** : par défaut, placeholder à plat (bloc coloré) avec le texte "Illustration". Version « complète » sur demande : photos libres Unsplash en hotlink (images.unsplash.com, crédits en pied de page, mention « photos d'illustration »). Jamais les photos du restaurant prises sur Google/TripAdvisor.
- **Identité visuelle** : chaque prototype doit avoir sa PROPRE charte (structure de mise en page, polices, couleurs) — ne pas recycler le même gabarit (demande utilisateur 08/10). Frazé et L'Argoat partagent encore le même gabarit.
- **Style des prototypes** : SIMPLES et LÉGERS, peu de contenu. Sections limitées : hero, courte présentation, quelques plats/carte, horaires + adresse, contact. Pas de galerie lourde, pas de JS inutile.

## Restaurants

### Le Pré de Frazé — slug `le-pre-de-fraze` — FAIT (2026-10-08)
- URL : `/prototype/le-pre-de-fraze/`. Ex-« L'Étape des Saveurs » de Frazé (même adresse, repris/renommé ; le nom L'Étape des Saveurs survit à Brou → aucomptoirbrou.com, qui a déjà un site).
- 6 rue du 8 Mai 1945, 28160 Frazé. Tél 02 37 37 01 92, lepredefraze@yahoo.com, Instagram @le.pre.de.fraze. Pas de site propre.
- Cuisine française, formules plancha, menus originaux, salon de thé/bar ; épicerie de terroir (style brocante) ; chambres d'hôtes pour cyclistes Véloscénie (recharge VAE). Terrasse, parking, animaux OK, emporter, traiteur.
- Prototype version COMPLÈTE : hero photo plein écran, 3 univers avec photos (restaurant, épicerie, chambres), carte 4 blocs (plancha, entrées, desserts/enfant, salon de thé/bar) sans prix, section Véloscénie, galerie 5 photos Unsplash, horaires « À compléter » (non trouvés), services, Google Maps intégrée, contact tél/email/Instagram.
- Mail ENVOYÉ par l'utilisateur le 08/10 à lepredefraze@yahoo.com.
- Alternative non faite : Au Comptoir by L'Étape des Saveurs, 3 place des Halles, Brou (02 37 96 05 69).

### Crêperie L'Argoat — slug `creperie-largoat` — FAIT (2026-10-08)
- URL : `/prototype/creperie-largoat/`. Version COMPLÈTE (demande utilisateur) : hero photo plein écran, section maison + services, carte 4 blocs (galettes, crêpes, salades, boissons/enfant) sans prix, avis (notes Google/TA + 3 thèmes, pas de faux témoignages), galerie 5 photos Unsplash, horaires confirmés par l'utilisateur (mer–dim 12h–22h ; fermé lun + mar), carte Google Maps intégrée, paiements, footer mentions légales. Pas d'email (suspect) → téléphone seul.
- Mail ENVOYÉ par l'utilisateur le 08/10 à michelverrier@orange.fr (adresse corrigée).
- 9 place d'Armes, 28160 Brou. Tél 02 37 47 00 65. Email (fiche eatbu) michelverrier@range.fr (domaine suspect, à vérifier).
- Site actuel : creperie-l-argoat.eatbu.com (mini-page DISH, pas de carte, mentions légales « A COMPLETER ») → argument de prospection.
- Crêperie familiale : galettes de blé noir, crêpes, tartes, plats régionaux, sur place ou à emporter. Terrasse, salles climatisées, parking gratuit. CB/sans contact.
- Horaires CONFIRMÉS (utilisateur, 08/10) : mercredi–dimanche 12h–22h, fermé lundi et mardi (la page eatbu est fausse).
- Avis : Google 4,2/5 (325), TripAdvisor 4,0/5 (143). Portions généreuses, prix doux, accueil familial, bonbons d'enfance offerts en fin de repas (roudoudous, violettes). Pas de carte avec prix en ligne.

### Les Tontons Fines Gueules — slug `les-tontons-fines-gueules` — FAIT (2026-10-08)
- URL : `/prototype/les-tontons-fines-gueules/`. Version COMPLÈTE, charte UNIQUE (demande utilisateur : chaque site doit avoir sa propre identité) : style affiche/néo-brutaliste jaune moutarde + noir + bordeaux, polices Google Anton / Courier Prime / Work Sans, hero affiche typographique + tampon 4,8★, bandeau défilant CSS, journée 01-02-03, carte imprimée à pointillés, ticket de caisse pour horaires, bande photos à glisser, section maison, avis (FB 4,8 / Google 4,7), galerie Unsplash, horaires « à confirmer », Google Maps, tél + Facebook. Bouton ajouté sur l'accueil. Mail de prospection rédigé (style imaginé mais entièrement modifiable + lien + tél) ; email (trouvé par l'utilisateur sur leur Facebook) : leperegourmand@sfr.fr. Mail final prêt avec lien https://prototype-web-site.netlify.app/prototype/les-tontons-fines-gueules/ ; ENVOYÉ le 08/10/2026 depuis Gmail (connecté). En attente de réponse.
- Société J.F.B. (SAS), créée le 24/03/2025, NAF 5630Z débit de boissons. Paiement : CB, titres-restaurant, espèces.
- Horaires contradictoires : kazfeed mar–jeu 7h–16h30, ven–sam 7h–21h30 ; Mappy/PagesJaunes mar–jeu 9h30–19h, ven–sam 9h30–21h30 ; fermé dim + lun.
- 51 rue Jean Moulin, 28290 Chapelle-Royale (Perche, Eure-et-Loir). Tél 02 18 00 63 44. Facebook : facebook.com/LesTontonsFinesGueules (seule présence en ligne, pas de site).
- Restaurant traditionnel / bar, ambiance décontractée, petit-déj dès 7h, sur place, à emporter, livraison. Prix moyen ~25 €. Parking gratuit, accès PMR. Desserts.
- Horaires (kazfeed) : mar–jeu 7h–16h30 ; ven–sam 7h–21h30 ; fermé dim + lun → à confirmer.
- Avis : Google 4,7/5 (≈37 avis) ; Facebook 4,8 (selon utilisateur). Établissement récent (fiches 2025).
- Pas de carte en ligne. Nom = clin d'œil aux « Tontons flingueurs » → ton humoristique possible, sans reprendre visuels/répliques du film.

### Brocéliande — slug `broceliande` — FAIT (2026-10-08)
- URL : https://prototype-web-site.netlify.app/prototype/broceliande/. Charte UNIQUE « légende arthurienne » : fond vert forêt sombre + or + parchemin, polices Cinzel / Cormorant Garamond, en-tête centré sans barre, hero plein écran centré (forêt moussue), chapitres I–IV, carte « Les chevaliers de la carte » en chiffres romains, triptyque photos, bouton « Réserver » flottant.
- Crêperie, 28 rue de Sully, 28400 Nogent-le-Rotrou. Tél 02 37 81 83 76. Email (fiche Perche tourisme) : sas.broceliande@laposte.net. Facebook seulement, aucun site (Mapstr pointe à tort vers jardinsdebroceliande.fr, un jardin près de Rennes).
- Avis : Google 4,8 (514 selon utilisateur) ; TripAdvisor 4,8 (371), n°1/30 à Nogent. Points forts : galettes aux noms arthuriens (Lancelot, Merlin, Guenièvre…), galette Saint-Jacques « Juniper » (carotte, poireau, Noilly Prat), dessert « Excalibur » (pêches rôties, glace, caramel), poutres + cheminée, clim, accueil souriant, patron (Thomas) plein d'humour, amuse-bouches offerts, crêpes « tournées à la main », produits frais/de saison, cidre local.
- Horaires (TripAdvisor) : fermé lun–mer ; jeu–sam 12h–13h30 / 19h–20h30 ; dim 12h–13h30 / 19h–20h15 → à confirmer. Réservation conseillée. CB, NFC, titres-resto/Pluxee, à emporter, PMR, anglais parlé.
- Mail de prospection : texte donné à l'utilisateur, pas envoyé.

### La Casa Line's — slug `casa-lines` — FAIT (2026-10-08)
- URL : https://prototype-web-site.netlify.app/prototype/casa-lines/. Charte UNIQUE « casa » moderne et solaire : crème + rouge tomate + bleu canard, polices DM Serif Display / DM Sans, nav en pilule flottante, hero texte + photo en arche + pastille « Fait maison », bande moments (midi/soir/pub/emporter), spécialités en cartes arrondies, carte en accordéon (details/summary, sans JS), section terrasse photo pleine largeur + carte blanche, bloc note 4,1, contact sur fond tomate arrondi.
- Restaurant-pub, 31-33 place Saint-Pol, 28400 Nogent-le-Rotrou. Tél 02 37 52 29 13. Email (fiche Perche tourisme) : contact@lacasalines.fr (domaine lacasalines.fr introuvable → l'email peut ne plus marcher). Instagram @la_casa_lines, Facebook facebook.com/casalines28. Aucun site.
- Cuisine française + italienne, décor moderne et chaleureux, pub, terrasse sur la place. Spécialités (Perche tourisme / annuaires) : foie gras de canard, ris de veau aux morilles, camembert rôti, pizzas, tarte tatin, andouillette moutarde, escargots, bruschetta, pâtes fraîches saumon, burger chèvre-miel, tartes citron meringuée / coco.
- Avis : Google 4,1 (503 selon utilisateur) ; TripAdvisor 3,5 (134). Positif : fait maison, copieux, pizzas, terrasse, rapport qualité-prix. Négatif : attente, accueil inégal.
- Horaires contradictoires : TA lun–ven 11h–14h / 18h–minuit, sam 10h–14h / 18h–minuit ; autre annuaire 9h30–1h (ven–sam 2h) ; fermé dimanche → page « midi & soir, à confirmer ». CB, NFC, titres-resto/Pluxee, emporter, PMR, chaises hautes, parking gratuit.
- Mail de prospection : texte donné à l'utilisateur, pas envoyé.

### Le Punjab Grill — slug `le-punjab-grill` — FAIT (2026-10-08)
- URL : https://prototype-web-site.netlify.app/prototype/le-punjab-grill/. Charte UNIQUE : barre latérale fixe à gauche (desktop) / barre haute (mobile), prune + safran + rose, motif jali en CSS, polices Rozha One / Mukta, hero photo plein écran dégradé prune, 4 signatures avec niveau d'épices 🌶️, carte 4 blocs (badges HALAL/VEGAN), 3 façons de commander (sur place / emporter / livraison), bandeau 4 photos, avis 4,7 sur fond jali.
- A DÉJÀ un site (lepunjabgrill28.fr, illisible pour Claude ; sa page Menus est titrée « Resto indien à Vendôme (41) » dans Google) → mail = proposition de refonte.
- 75 bis rue de la République, 28200 Châteaudun, 02 37 66 04 69. Pas d'email trouvé. 4,7 Google (588). 7j/7 11h30–14h30 / 18h30–22h30 (à confirmer). Halal, vegan, emporter, livraison gratuite dès 25 € à Châteaudun. Plats populaires : poulet tandoori, biryani, curry, cheese naan, samoussas. Salle bois + tons chauds.
- Mail : texte donné, pas envoyé.

### Le Commerce — slug `le-commerce` — FAIT (2026-10-08)
- URL : https://prototype-web-site.netlify.app/prototype/le-commerce/. Charte UNIQUE « gazette » : page de journal (manchette gothique UnifrakturCook, Oswald, Libre Baskerville), papier crème + encre + vert bouteille + laiton, « À la une » en 2 colonnes avec lettrine, encarts latéraux (spécialité, en bref), rubriques (cuisine en 3 colonnes, reportage terrasse, en images, infos pratiques), contact en « petite annonce ». Note NON affichée (3,6).
- Brasserie, 7 place du 18 Octobre, 28200 Châteaudun, 02 37 66 10 02 (TA : 07 69 25 34 88), email termeaus@wanadoo.fr (Châteaudun tourisme). Aucun site (Mapstr cite jaimelecommerce.com, introuvable). Cuisine traditionnelle simple et rapide, tous les jours 12h–14h (bar l'après-midi), terrasse l'été face à la place près du château, salle rétro. Spécialités : pommes de terre farcies au four, tartines maison ; avis : onglet sauces, tartine chèvre, salades, burger du jour. Google 3,6 (494) / TA 3,2.
- Mail : texte donné, pas envoyé.

## Suivi des mails (08/10)
- ENVOYÉS : Le Pré de Frazé, Crêperie L'Argoat, Les Tontons Fines Gueules.
- À ENVOYER (textes prêts) : Brocéliande (sas.broceliande@laposte.net), La Casa Line's (contact@lacasalines.fr, peut-être mort), Le Punjab Grill (pas d'email → tél / formulaire du site), Le Commerce (termeaus@wanadoo.fr).
- Style de l'utilisateur dans ses mails : se présente comme « étudiant en développement d'application et à côté développeur web près d'Orléans », « sites pour les restaurants/entreprises ».

## Lot n°15–24 (liste utilisateur, 08/10 soir) — vérif sites + prototypes
- Écarté : **n°16 L'Étape des Saveurs (Brou)** = a un vrai site (aucomptoirbrou.com, « Au Comptoir by L'Étape des Saveurs »).
- Délice Châteaudun et Sushi'Lys n'ont qu'une page OnaTaste « gérée par la communauté » → traités comme SANS site.
- 9 prototypes FAITS, chacun avec sa charte (URL : https://prototype-web-site.netlify.app/prototype/<slug>/), boutons ajoutés sur l'accueil, responsive vérifié (360/390/768/1280).
- Emails (recherche approfondie 08/10) : SEUL Deux Places a un email public. Sinon réseaux : Auberge du Bastard facebook.com/Aubergedubastard ; Délice facebook.com/p/Délice-Chateaudun-100071162947891 ; Pamukkale facebook.com/kebabmouss ; Sushi'Lys instagram.com/sushi_lys + FB ; Au Bon Coin facebook.com/AuBonCoinRestaurant (fiche dit aussi nouveau nom « CACHIN FREDERIC ») ; Wok 28, DIX 8, Au Point du Jour : rien → téléphone / visite.
- `restaurant-des-deux-places` — 10 place Charles de Gaulle, **Courtalain** (28290 Vald'Yerre — pas Arrou), 02 37 45 07 81, **restaurantdes2places@orange.fr**. A une mini-page eatbu (restaurantdes2places.eatbu.com : texte « Bienvenue » seul, pas de carte, liens Facebook/TripAdvisor cassés, lien d'appel mal formé) → même argument que L'Argoat. Restaurant-bar familial, cuisine traditionnelle produits frais ; pizzas & burgers à emporter ven soir 18–22h ; buffets, traiteur, mariages, coin enfants. Horaires eatbu : lun–jeu 8–16 ; ven 8–16/18–22 ; sam 9h30–15/18–22 ; dim 9h30–15. Charte : nappe vichy rouge, carte postale + timbre, ardoise verte, Fraunces/Nunito.
- `auberge-du-bastard` — 2 rue des Fouleries, Châteaudun, 02 37 45 80 41. Crêperie dans une auberge style XVe (rénovée 2025 par Studio Minuit Trois), bord du Loir, face au château, terrasse ; galette truite + fondue de poireaux, crêpe sucre-amande, cidre bio, casques de chevalier pour enfants. Horaires : mai–sept tous les jours 11h–23h ; oct–avr lun + mer–dim 12–14/19–21 (fermé mar). TA 4,9 (42), n°1. Charte : héraldique claire (gueules/azur/or), fanions, écus, parchemin déroulé, IM Fell English.
- `wok-28` — 22 av. du Président Kennedy, Nogent-le-Rotrou, 09 70 98 14 88. Buffet asiatique à volonté (sushis, wok, grill, fruits de mer, desserts), ~26,90–28,90 € selon avis. Récent. Horaires inconnus. TA 2,9 → seule la note Google 4,0 affichée. Charte : noir charbon + rouge lanterne + or, Bebas Neue, mosaïque, « stations » numérotées.
- `delice-chateaudun` — 32 place du 18 Octobre, Châteaudun, 02 36 68 11 82. Traiteur chinois à emporter/livraison, lun–sam 10–14 / 15–21, menu étudiant 6,50 € ; samoussas, nouilles sautées, crevettes, porc caramel. Charte : vert jade + rouge, Baloo 2, bulles, 3 étapes de commande, barre d'appel fixe en bas.
- `au-point-du-jour` — 2 rue Saint-Pierre, Illiers-Combray, 02 37 24 01 19. Bar-tabac-resto + PMU + relais Colissimo ; dès 6h30 ; menu du jour ~16 €. Horaires TA : lun 6h30–14h ; mar–mer 6h30–19h30 ; jeu–ven 6h30–14h / 16h30–19h30 ; sam fermé ; dim 8h–13h. Charte : dégradé lever de soleil, Archivo Black, frise horaire de la journée.
- `dix-8` — 3 place du Marché aux Grains, Bonneval, 02 59 16 15 59. Ouvert 2024, cuisine maison produits locaux, terrasse face à l'église ; brie croustillant, sauté de porc vin/échalotes, œufs cocotte, sauce poivre-cognac, tiramisu ; formule ~23,50–24,50 €. Horaires : mar 12–14 ; mer–jeu 12–14/19–21 ; ven 12–14/19–21h30 ; sam–lun fermé. Charte : minimal noir/blanc + vert acide, « DIX 8 » géant, Space Grotesk / Instrument Serif, sections numérotées.
- `pamukkale` — 45 bd Kellermann, Châteaudun, 09 87 77 12 46, Facebook facebook.com/kebabmouss. Turc/grill, halal, terrasse, emporter, menu enfant, titres-resto, ~15 € ; lun 11–15/18–23, mar–dim 11h–minuit. Charte : blanc travertin + turquoise + rouge, carreaux CSS, photos en vasques, carte en terrasses étagées, Marcellus.
- `sushi-lys` — 7 rue Gambetta, Châteaudun, 02 18 46 21 93, Instagram @sushi_lys. Sushis, california, poké, bo bun, nouilles, gyozas, tiramisu maison, 10–20 € ; mar 12–14/18h30–22 ; mer–sam 11h30–14/18h30–22 ; fermé dim–lun. Charte : japonais minimal (washi, sumi, sakura), titre vertical, bento, Shippori Mincho / Zen Kaku Gothic.
- `au-bon-coin` — 32 rue du Sous-Lieutenant Germond, Authon-du-Perche, 02 37 49 02 19, Facebook AuBonCoinRestaurant. Bistrot & bar à vin, viande française, frites, salades, desserts maison, produits locaux ; formule ~12 € (entrée, 2 plats au choix, dessert, vin). Horaires inconnus. Charte : kraft + bordeaux, étiquette de vin, ardoise, Caveat / Playfair / Karla.
