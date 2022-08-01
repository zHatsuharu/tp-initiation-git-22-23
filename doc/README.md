Légende :
- `<argument>` : L'argument est requis pour le bon fonctionnement de la commande.
- `[argument]` : L'argument est optionnel.

| Commande | Argument | Description |
| -------- | --------- | ----------- |
| `git clone <url>` | `url` : l'url du repository à cloner | Clone un repository distant sur votre pc en local. |
| `git add <file> [files...]` | `file` : le fichier à ajouter au commit. Peut être remplacer par `*` pour tout ajouter ou `.` pour ajouter uniquement les fichiers modifiés<br />`files` : les fichiers supplémentaires à ajouter au commit. | Ajoute un ou plusieurs fichier pour le prochain commit. |
| `git commit -m <text>` | `text` : Le message de votre commit. | Effectue un commit à votre repo sur la branche actuelle. |
| `git push` | | Mets à jour votre repo avec le commit effectuer. |
