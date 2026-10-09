# REPRISE — Prototypes de sites pour restaurants (état au 09/10/2026)

> Fichier à donner à Claude en début de nouvelle conversation. Il résume le projet, les règles et où on en est.
> Le détail complet de chaque restaurant (sources, avis, chartes) se trouve dans `CLAUDE.md` du dépôt.

## Qui / quoi
- **Louis Maillet**, développeur web près d'Orléans (Olivet, 45). Site : https://louismaillet.fr. Il est aussi étudiant en développement d'applications.
- **Méthode** : il démarche des restaurants (surtout Eure-et-Loir / Perche) en leur montrant une **maquette de site déjà faite à leur nom**, puis il les contacte par mail, par téléphone ou en visite.
- **Dépôt** : https://github.com/louismaillet/prototypes-restaurants (branche `main`). Claude peut push.
- **Hébergement** : Netlify, publish directory = `site`. Netlify redéploie automatiquement à chaque push.
- **URL de chaque maquette** : `https://prototype-web-site.netlify.app/prototype/<slug>/`
- **Accueil** : `site/index.html` est la vitrine de Louis. Elle a une barre « Maquettes » en haut, avec **un bouton par prototype**.

## Règles IMPORTANTES
1. **Ne JAMAIS envoyer de mail.** Gmail est connecté, mais Claude donne seulement le texte prêt à copier (destinataire, objet, corps). C'est Louis qui envoie.
2. **Commit et push après CHAQUE site**, pour sauvegarder au fur et à mesure.
3. **Chaque maquette a sa propre charte graphique** : mise en page, polices et couleurs différentes. Ne jamais recycler un gabarit.
4. **Avant de coder, vérifier si le restaurant a déjà un vrai site.**
   - Les pages auto-générées (OnaTaste, res-menu, menu-world…) ne comptent pas comme un site.
   - Les mini-pages eatbu/DISH sont un argument de prospection (« votre page est incomplète »).
5. **Bien se documenter** (adresse, téléphone, horaires, carte, avis, réseaux) et **chercher sérieusement les emails** (fiches office de tourisme, annuaires).
6. **Mails de prospection.**
   - Style de Louis : « étudiant en développement d'application et à côté développeur web près d'Orléans », « je crée des sites pour les restaurants/entreprises ».
   - Le mail dit qu'il a imaginé un style mais qu'il peut **entièrement le modifier**.
   - Le mail contient le lien direct vers la maquette et son numéro : **07 82 52 45 37**. Ce numéro ne va jamais sur les maquettes.

## Règles techniques d'une maquette
- **Fichier** : un seul fichier `site/prototype/<slug>/index.html`, en HTML et CSS, sans JS.
- **Responsive** : mobile d'abord. Le vérifier à 360, 390, 768 et 1280 px avec Playwright (python). Ajouter `overflow-x:clip` si ça déborde.
- **Balises et bandeau** :
  - `<meta name="robots" content="noindex, nofollow">`
  - Bandeau en haut : « Maquette proposée par Louis Maillet — louismaillet.fr »
- **Sections**, à garder simples et légères :
  - hero
  - présentation
  - quelques plats ou la carte
  - avis : vraies notes seulement, **jamais de faux témoignages**
  - horaires et adresse
  - carte Google Maps en iframe (`https://www.google.com/maps?q=ADRESSE&output=embed`)
  - contact (`tel:`, Facebook…)
  - footer : mentions légales, confidentialité, lien maquette, crédits photos
- **Prudence sur les infos** :
  - Mettre « à titre d'exemple » sur les cartes et les prix inventés.
  - Mettre « Horaires à confirmer » quand les sources ne sont pas sûres.
  - Ne pas afficher une note faible (en dessous d'environ 3,8).
- **Photos** :
  - Uniquement des photos libres Unsplash, en hotlink : `https://images.unsplash.com/photo-<id>?auto=format&fit=crop&w=…&q=70`. Les créditer dans le footer.
  - Vérifier que la photo n'est pas « Unsplash+ » (payante).
  - **Jamais** les photos du restaurant prises sur Google ou TripAdvisor.
  - Le shell ne peut pas charger images.unsplash.com. C'est normal : les photos fonctionnent en ligne.
- **Bouton sur l'accueil** : l'insérer dans `site/index.html`, après le dernier lien de la barre « Maquettes ».
- **Commit** :
  ```
  git add -A && git commit -m "Prototype <Nom> (<Ville>)" && git fetch origin main && git rebase origin/main && git push origin HEAD:main
  ```

## État : 25 maquettes en ligne

| Slug | Restaurant (ville) | Contact pour prospecter | Mail |
|---|---|---|---|
| le-pre-de-fraze | Le Pré de Frazé (Frazé) | lepredefraze@yahoo.com | ✅ ENVOYÉ |
| creperie-largoat | Crêperie L'Argoat (Brou) | michelverrier@orange.fr | ✅ ENVOYÉ |
| les-tontons-fines-gueules | Les Tontons Fines Gueules (Chapelle-Royale) | leperegourmand@sfr.fr | ✅ ENVOYÉ, attend réponse |
| broceliande | Brocéliande (Nogent-le-Rotrou) | sas.broceliande@laposte.net | ✉️ à envoyer |
| casa-lines | La Casa Line's (Nogent-le-Rotrou) | contact@lacasalines.fr (peut-être mort) / IG @la_casa_lines | ✉️ à envoyer |
| le-punjab-grill | Le Punjab Grill (Châteaudun) — a déjà lepunjabgrill28.fr → refonte | 02 37 66 04 69 | ✉️ tél / formulaire |
| le-commerce | Le Commerce (Châteaudun) | termeaus@wanadoo.fr | ✉️ à envoyer |
| restaurant-des-deux-places | Restaurant des Deux Places (Courtalain) | restaurantdes2places@orange.fr | ✉️ à envoyer |
| auberge-du-bastard | Auberge du Bastard (Châteaudun) | 02 37 45 80 41 / FB Aubergedubastard | 📞 |
| wok-28 | Wok 28 (Nogent-le-Rotrou) | 09 70 98 14 88 | 📞 |
| delice-chateaudun | Délice (Châteaudun) | 02 36 68 11 82 / FB | 📞 |
| au-point-du-jour | Au Point du Jour (Illiers-Combray) | 02 37 24 01 19 | 📞 |
| dix-8 | DIX 8 (Bonneval) | 02 59 16 15 59 | 📞 |
| pamukkale | Pamukkale (Châteaudun) | 09 87 77 12 46 / FB kebabmouss | 📞 |
| sushi-lys | Sushi'Lys (Châteaudun) | 02 18 46 21 93 / IG @sushi_lys | 📞 |
| au-bon-coin | Au Bon Coin (Authon-du-Perche) | 02 37 49 02 19 / FB AuBonCoinRestaurant | 📞 |
| ateria | Ateria (Châteaudun) | restaurant.ateria@gmail.com | ✉️ à envoyer |
| kebab-istanbul | Kebab Istanbul (Brou) | 02 37 66 25 76 | 📞 |
| la-croix-blanche | La Croix Blanche (Combres) | 02 37 53 00 65 | 📞 |
| le-sable-d-or | Le Sable d'Or (Châteaudun) | 02 37 45 73 68 / FB | 📞 |
| kebab-du-centre | Kebab du Centre (Châteaudun) | 09 53 93 14 11 | 📞 |
| la-madeleine-d-illiers | La Madeleine d'Illiers (Illiers-Combray) | 09 53 33 83 06 | 📞 |
| au-lion-d-or | Au Lion d'Or (Unverre) | 02 37 97 20 08 / FB | 📞 |
| la-bigoudine | La Bigoudine (Nogent-le-Rotrou) | 02 37 52 89 20 / FB | 📞 |
| restaurant-de-la-halle | Restaurant de la Halle (Beaumont-les-Autels) | 02 37 29 43 92 / FB | 📞 |

Légende : ✅ déjà envoyé · ✉️ texte de mail à préparer ou à envoyer par Louis · 📞 pas d'email public, donc téléphone, Facebook ou visite.

**Écartés (pas de maquette) :**
- **L'Étape des Saveurs (Brou)** : a déjà un vrai site, aucomptoirbrou.com.
- **Capadocce** : a un site Solocal raté (capados.site-solocal.com, faux texte « lorem ipsum », images manquantes). C'est une cible de **refonte** possible. Email : calikali1973@gmail.com.

## Prochaines étapes possibles
- Rédiger les mails restants : Ateria, Deux Places, Brocéliande, Casa Line's, Le Commerce, Capadocce (refonte).
- Préparer un petit script téléphone pour les restaurants sans email.
- Nouveaux restaurants : le workflow reste le même (recherche → vérif site → maquette avec charte unique → bouton accueil → push → mettre à jour `CLAUDE.md` et ce fichier).
