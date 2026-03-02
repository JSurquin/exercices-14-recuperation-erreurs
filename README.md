# TP – Git Reset & Git Revert 🔙↩️

## Ce qui est préconfiguré dans ce dépôt

- **`main`** contient `app.js` avec 3 commits :
  1. `feat: initial app version`
  2. `feat: add greet function`
  3. `feat: add math function`

Ce dépôt est utilisé pour deux TPs :
- **TP Reset** : tester `--soft`, `--mixed`, `--hard` et utiliser `reflog` pour récupérer
- **TP Revert** : créer des commits A/B/C et les annuler proprement avec `revert`

## TP Reset

1. Cloner et vérifier l'historique : `git log --oneline`
2. Ajouter 2-3 commits de test
3. Annuler avec `--soft` (conserve staging), `--mixed` (conserve working dir), `--hard` (tout supprime)
4. Récupérer un commit "perdu" via `git reflog`

## TP Revert

1. Cloner, créer 3 nouveaux commits (`feat: A`, `feat: B`, `feat: C`)
2. Annuler `feat: B` avec `git revert <hash>`
3. Observer que l'historique est intact + nouveau commit d'annulation créé
4. Comparer avec `reset` : `revert` est sûr sur les branches partagées
