# Site de RG - Rezix's Games Company

Site public du studio, hébergé gratuitement par GitHub Pages.

| Fichier | Rôle |
|---|---|
| `index.html` | Page d'accueil : studio, jeux, contact |
| `confidentialite.html` / `privacy.html` | Politique de confidentialité (FR / EN), liée dans chaque fiche Play Store et dans les jeux |
| `app-ads.txt` | Exigé par AdMob (lutte contre la fraude) ; doit rester à la racine du site |
| `crosspromo.json` | Liste des jeux pour la pub croisée, lue par le socle (format : voir `PromoParser` dans le socle) |
| `crosspromo.json.sig` | Signature de la liste : les jeux refusent une liste dont la signature ne correspond pas à la clé du studio |
| `.gitattributes` | Empêche Git de modifier les fins de ligne des fichiers signés |
| `.nojekyll` | Demande à GitHub de publier les fichiers tels quels |

## Règles

- **Dépôt public** : tout ce qui est ici, historique compris, est visible par tout le monde.
  Jamais de secret, de mot de passe, de clé ni de donnée personnelle.
- Les enregistrements Git utilisent l'adresse anonyme GitHub (`...@users.noreply.github.com`),
  jamais l'adresse e-mail personnelle.
- `crosspromo.json` : seulement des noms de package Play Store, des noms et des accroches
  courtes. Le socle ignore toute entrée invalide.
- **Après toute modification de `crosspromo.json`, la re-signer** avec l'outil du socle
  (`Socle/outils/signer_crosspromo.py`), puis envoyer les deux fichiers ensemble. Une liste
  non signée ou mal signée est ignorée par les jeux (ils gardent la dernière liste valide).
- La clé **privée** de signature n'est JAMAIS dans ce dépôt (seule la signature l'est).
- Toute modification de la politique de confidentialité : mettre à jour la date en haut des
  deux versions.
