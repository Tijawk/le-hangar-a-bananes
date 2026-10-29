# Le hangar à bananes

Le chantier de notre garage-atelier en ossature bois de 49 m², raconté étape par étape.
Site statique construit avec [Hugo](https://gohugo.io) et le thème [PaperMod](https://github.com/adityatelange/hugo-PaperMod).

## Prérequis

- Hugo **extended** 0.169 ou plus récent (traitement des images en WebP)
- Git

## Démarrer

```bash
git clone --recurse-submodules https://github.com/MaeBzh/le-hangar-a-bananes.git
cd le-hangar-a-bananes
hugo server
```

Le site est alors visible sur http://localhost:1313/le-hangar-a-bananes/.

## Écrire une étape

```bash
hugo new etapes/12-titre-de-l-etape/index.md
```

Le modèle `archetypes/etapes.md` prépare la frise, la fiche et les conseils.
Les photos se placent dans le même dossier que `index.md`. Le `weight` du billet est le numéro de sa phase.

## Shortcodes

| Shortcode | Rôle |
|---|---|
| `frise titre="…"` | Frise de progression de la série, d’après le `weight` du billet |
| `fiche titre="…"` | Encadré « en bref » contenant un tableau Markdown à deux colonnes |
| `figure src="…" alt="…" caption="…"` | Photo du dossier de l’article, servie en WebP, agrandissable |
| `duo theorie="…" vrai="…" legende="…"` | Schéma de principe et photo du chantier côte à côte |
| `conseils` | Encadré de conseils en fin d’article |

## Organisation

- `content/etapes/` : un dossier par étape, avec ses photos
- `data/chiffres.yaml` : les chiffres du bandeau d’accueil
- `assets/css/extended/hangar.css` : toute la personnalisation visuelle
- `layouts/` : shortcodes et surcharges de PaperMod (`home_info`, `list`, `entry_phase`)
- `static/img/` : personnages et icônes des étapes ([Fluent Emoji](https://github.com/microsoft/fluentui-emoji), licence MIT)
- `assets/legacy/` : images de l’ancien site VitePress, conservées mais non publiées

## Publication

Chaque envoi sur la branche par défaut reconstruit le site et le publie sur GitHub Pages
(`.github/workflows/hugo.yml`). Dans les réglages du dépôt, la source de Pages doit être « GitHub Actions ».

## Licence

Le code est sous licence MIT (voir `LICENSE`). Les textes, photos et schémas restent la propriété des auteurs.
