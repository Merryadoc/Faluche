# Archive de la Faluche

Site statique d'une seule page regroupant l'histoire, la chronologie, les insignes, les villes, le folklore et le lexique de la faluche.

## Hébergement sur GitHub Pages

1. Créez un dépôt (par ex. `faluche`) et déposez-y **`index.html`**.
2. Dans **Settings → Pages**, choisissez la branche `main` et le dossier `/ (root)`, puis **Save**.
3. Le site est en ligne sous quelques minutes à l'adresse `https://<votre-compte>.github.io/faluche/`.

`index.html` est **autonome** : il contient déjà tout le contenu et toutes les feuilles de style. Aucun autre fichier n'est nécessaire (seules les polices Google Fonts sont chargées en ligne ; le site reste lisible hors-ligne avec des polices de repli).

## Modifier le contenu

Tout le contenu se trouve dans un seul bloc de données en tête de `index.html` :

```js
window.FALUCHE_DATA = { ... };
```

- Chaque **section** a un `id`, un `title` et une liste de `blocks`.
- Types de blocs : `p` (paragraphe), `h3` (sous-titre), `list`, `kv` (terme/définition), `table`, `note`, `accordion`.
- Pour ajouter une ville : ajoutez un objet `{title, sub, blocks:[…]}` dans l'`accordion` de la section « Les villes ».

Après modification, il suffit de pousser le fichier : GitHub Pages se met à jour automatiquement.

> Variante « deux fichiers » : si vous préférez séparer le contenu, le fichier **`data.js`** fourni contient exactement le même bloc de données. Remplacez alors, dans `index.html`, le grand `<script>window.FALUCHE_DATA = …</script>` par `<script src="data.js"></script>` et hébergez les deux fichiers ensemble.

## Fonctions

- **Recherche** instantanée (villes, insignes, termes…).
- **Sommaire** latéral avec suivi de lecture.
- **Fiches de villes repliables**.
- Mise en page **responsive** et adaptée à l'impression.

## Sources

Compilation documentaire d'après : Lavisse (1890), Guy Daniel (1990), Segura (1994, 2012), Fayemendy (2009-2010), Dillemann (1988), les codes nationaux (1966-2023), la présentation des Grands Archivistes, « Les Insignes Décernables », l'étude de R. Pamart sur les caducées, et les codes de ville. Les usages varient selon les communautés et les époques.
