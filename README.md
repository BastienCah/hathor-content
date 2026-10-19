# Hathor · contenu

Ce que l'app Hathor télécharge au lancement (publié sur
https://bastiencah.github.io/hathor-content/content.json).

Modifier `content.json` sur github.com (crayon ✏️ → « Commit changes ») :
les apps le récupèrent à leur prochaine ouverture (quelques minutes de cache).

- `palmares` : palmarès du Pass, un par mois (`month` = `AAAA-MM`, sortie le 1er).
  Un palmarès déjà dans l'app : seulement `id` et `month`. Un nouveau : ajouter
  `title` (« Grammy · Meilleur album jazz »), `shortTitle` (sur les cartes,
  « Grammy · Jazz »), `category`, `blurb` (une phrase), `org` (Billboard, Grammy,
  Oscar…), `color` (`#RRGGBB`, couleur des cartes), `kind` (`albums` ou `tracks`)
  et `items` (`[{ "t": titre, "a": artiste, "y": année }]`).
- `news` : actus d'Explore. `draft: true` = visible seulement dans les builds perso.
- `message` : `{ "text": "…", "until": "AAAA-MM-JJ" }` affiché sous le billet des
  Découvertes, ou `null`.

Le fichier doit rester du JSON valide (guillemets droits, virgules) : en cas
d'erreur l'app garde la dernière version reçue.
