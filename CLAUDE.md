# Consignes pour Claude

## Publication sur GitHub
- Ne jamais demander s'il faut pousser le code ou ouvrir une pull request.
- Après chaque modification : commit, push sur la branche de travail, puis ouvrir directement la pull request vers `main`.
- La seule étape laissée à l'utilisateur est la validation (fusion) de la pull request : lui donner le lien.

## Site
- Tout le site est dans `index.html` (même esthétique que le site BAC 2027 : variables `:root` / `body.night`).
- Navigation par adresse `#…` : l'accueil affiche les rubriques en cartes (pas de menu en haut à gauche) ; le bouton « Retour » remonte d'un niveau.
- `TEXTES` : métadonnées de chaque texte, découpage en `mouvements` (source unique du plan, de l'annonce et de l'affichage), `problematique`, `introduction`, `conclusion`.
- `texteLines` (texte ligne par ligne, `"__BREAK__"` = saut de strophe) et `analysesData` (clé `T<n°>l<ligne>`) : il faut exactement une analyse par ligne ; si on fusionne ou coupe une ligne, réaligner les analyses.
- `NOTIONS` : lexique ; les termes listés dans `formes` sont soulignés automatiquement (notions cliquables) dans les analyses et les fiches, sauf dans les citations en `<em>`. Mettre `auto:false` pour un mot trop courant.
- `AUTEURS`, `OEUVRES`, `GRAMMAIRE`, `METHODO`, `REPERES_HTML` : fiches en HTML (composants `.section`, `.def`, `.exemple`, `.piege`, `.aretenir`, `.astuce`, `.tbl`, `.idcard`, `.frise`).
- `FLASHCARDS_MAIN` : flashcards rédigées ; d'autres paquets sont générés (notions par catégorie, problématiques et mouvements des textes). Chaque question doit se comprendre seule.
- Les exemples attribués à un auteur doivent être des citations exactes des textes étudiés ; sinon, indiquer « exemple construit ».
