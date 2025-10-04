# Correction - Exercice 3 : Arborescence Hiérarchisée (mkdir -p, cd ../..)

| Tâche | Commandes Exécutées | Résultat / Vérification | Remarques |
| :--- | :--- | :--- | :--- |
| Créer actualites/politique | `mkdir -p actualites/politique` | `ls actualites` -> politique | **Clé :** L'option **`-p`** crée les répertoires parents (`actualites`) si nécessaire. |
| Entrer dans politique | `cd actualites/politique` | `pwd` -> ~/actualites/politique | Navigation. |
| Créer elections et candidats.txt | `mkdir elections`<br>`echo -e "Issoufou\nHama\nSeini" > candidats.txt` | `ls` -> candidats.txt  elections | Utilisation de `echo -e` et `\n` pour forcer les retours à la ligne. |
| Vérifier candidats.txt | `cat candidats.txt` | Issoufou<br>Hama<br>Seini | Affichage du contenu. |
| Remonter deux niveaux | `cd ../..` | `pwd` -> ~/actualites | **Clé :** `../..` remonte de deux niveaux dans l'arborescence. |
| Créer buzz | `mkdir buzz` | `ls` -> buzz  politique | Extension de l'arborescence. |
| Retour | `cd ..` | `pwd` -> ~ | Retour au répertoire personnel. |
# mkdir -p actualites/politique/elections && touch actualites/politique/elections/candidats.txt && echo -e "Issoufou\nHama\nSeini" > actualites/politique/elections/candidats.txt && cd actualites/politique/elections/.. && cd .. && mkdir buzz 

Explication détaillée de la commande
Voici le décryptage de chaque partie de la commande :



mkdir -p actualites/politique/elections && touch actualites/politique/elections/candidats.txt && echo -e "Issoufou\nHama\nSeini" > actualites/politique/elections/candidats.txt && cd actualites/politique/elections/.. && cd .. && mkdir buzz
Explication détaillée de la commande
Voici le décryptage de chaque partie de la commande :

mkdir -p actualites/politique/elections :

mkdir crée des répertoires (dossiers).

L'option -p permet de créer le répertoire final (elections) ainsi que tous les répertoires parents nécessaires (actualites et politique) s'ils n'existent pas encore.

&& :

Cet opérateur logique permet d'enchaîner les commandes : la commande suivante ne s'exécute que si la précédente a réussi.

touch actualites/politique/elections/candidats.txt :

touch crée le fichier vide candidats.txt à l'intérieur du dossier elections.

&& echo -e "Issoufou\nHama\nSeini" > actualites/politique/elections/candidats.txt :

echo -e "Issoufou\nHama\nSeini" affiche les noms avec des sauts de ligne (\n grâce à l'option -e).

Le symbole > redirige cette sortie et écrase le contenu du fichier candidats.txt pour y mettre les noms.

&& cd actualites/politique/elections/.. && cd .. :

cd change de répertoire.

Chaque .. représente le répertoire parent. Pour remonter de deux niveaux (de elections à actualites), on utilise deux commandes cd .. successives (techniquement, on pourrait utiliser cd actualites, mais l'énoncé demandait de remonter deux niveaux).

&& mkdir buzz :

Une fois revenu dans le dossier actualites, cette commande crée le nouveau dossier buzz.

Vérification (Optionnel)
Pour vérifier si tout s'est bien passé, vous pouvez utiliser :

Bash

tree actualites
cat actualites/politique/elections/candidats.txt
Si l'outil tree est installé, la première commande affichera l'arborescence :

actualites
├── buzz
└── politique
    └── elections
        └── candidats.txt
Et la deuxième affichera le contenu du fichier

Quelque Diffilcultés est que la maitrise des different commande vraiment il faut bien les maitriser  pour bien appliquer 

**Difficulté Rencontrée :** L'utilisation de `cd ../..` est essentielle pour une navigation rapide vers un dossier parent éloigné.

![](exo3.png)
