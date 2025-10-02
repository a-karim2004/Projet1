# Correction - Exercice 5 : Consolidation et Nettoyage (rmdir, {} syntax)

| Tâche | Commandes Exécutées | Résultat / Vérification | Remarques |
| :--- | :--- | :--- | :--- |
| Créer arborescence complète | `mkdir -p projet_scolaire/{maths,sciences}` | `ls projet_scolaire` -> maths  sciences | **Clé :** La syntaxe `{item1,item2}` permet la création simultanée de plusieurs sous-chemins. |
| Remplir equations.txt | `echo "x^2 + y^2 = z^2" > projet_scolaire/maths/equations.txt` | - | Ajout de contenu. |
| Remplir experiences.txt | `echo "eau + huile = séparation" > projet_scolaire/sciences/experiences.txt` | - | Ajout de contenu. |
| Renommer equations.txt | `mv projet_scolaire/maths/equations.txt projet_scolaire/maths/geometrie.txt` | `ls projet_scolaire/maths` -> geometrie.txt | Renommage avec `mv`. |
| Déplacer experiences.txt | `mv projet_scolaire/sciences/experiences.txt projet_scolaire/maths/` | `ls projet_scolaire/sciences` -> (vide) | Déplacement vers un autre dossier. |
| Supprimer sciences | `rmdir projet_scolaire/sciences` | `ls projet_scolaire` -> maths | **Clé :** `rmdir` est utilisé pour supprimer un répertoire s'il est **vide**. |

**Difficulté Rencontrée :** Bien distinguer l'utilisation de `rmdir` (dossier vide) et `rm -r` (dossier non vide). J'ai utilisé la syntaxe `{}` pour créer l'arborescence en une seule commande.

![](exo.5)
