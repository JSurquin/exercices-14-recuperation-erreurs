# TP 3.6 – Récupération d'erreurs

Utiliser `git reflog` pour retrouver un commit « perdu » après un `reset --hard`.

## Tâches

1. Créer une branche `feature/recovery`
2. Faire **3 commits** :
   - Ajouter `work1.txt` → `feat: important work 1`
   - Ajouter `work2.txt` → `feat: important work 2`
   - Ajouter `work3.txt` → `feat: important work 3`
3. Simuler une erreur : `git reset --hard HEAD~3`
4. Constater la disparition des commits et des fichiers
5. Lancer `git reflog` et repérer l'entrée du dernier commit
6. Récupérer : `git reset --hard HEAD@{1}` (ou le hash)
7. Vérifier que tout est de retour ✨

## Points clés

```bash
git reflog           # voir tout l'historique de HEAD
git reset --hard HEAD@{n}   # revenir à un état précédent
```

> `git reflog` est votre filet de sécurité — les commits restent récupérables
> pendant ~90 jours (avant le garbage collector).
