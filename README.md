# ECDSA_lab — Travaux pratiques et challenges ECDSA

Résumé
-------
Ce dépôt contient une série d'exercices et challenges autour d'ECDSA (Elliptic Curve Digital Signature Algorithm) réalisés dans le cadre du cours ICR — Laboratoire 2. Les scripts fournissent des exemples pratiques, des défis exploitant des faiblesses ou variantes d'implémentation, ainsi qu'un fichier utilitaire `ecdsa.sage` pour les opérations communes.

Prérequis
---------
- SageMath (version recommandée : 9.2 ou supérieure). Installer depuis https://www.sagemath.org/
- Python 3 (utilisé seulement pour manipulation externe si nécessaire).

Structure du dépôt
-------------------
Contenu principal :
- `challenge1.sage`, `challenge2.sage`, `challenge3.sage`, `challenge4.sage` : scripts d'exercices/challenges (chaque fichier est autonome et documenté en en-tête).
- `ecdsa.sage` : bibliothèque/utilitaires partagés pour ECDSA (courbes, signatures, vérifications, helpers pour les challenges).
- `parameters.txt` : paramètres de configuration ou données utilisées par certains challenges.
- `ICR_Labo2_Pellandini-2.pdf` : énoncé du laboratoire et consignes (ressource pédagogique).

Usage — exécution des scripts
-----------------------------
Méthodes recommandées pour exécuter un script Sage :

1) Lancer Sage puis charger le script :

   sage
   sage: load('challenge1.sage')

2) Exécuter directement depuis le shell (zsh) :

   sage -c "load('challenge1.sage')"

Remarques :
- Les scripts sont écrits pour s'exécuter dans l'environnement Sage. Si vous utilisez une installation où `sage` n'est pas dans le PATH, adaptez la commande avec le chemin complet.
- Certains scripts génèrent des sorties (clé, signature, messages chiffrés) ou sauvent des fichiers ; vérifiez l'en-tête du script pour les détails.

Description succincte des scripts
---------------------------------
- `ecdsa.sage` : fonctions utilitaires — génération de clés, signature/verif, conversion formats, outils pour manipuler k non aléatoires ou réutilisés.
- `challenge1.sage` : (exemple) démonstration d'une réutilisation de nonce k entre signatures et récupération de la clé privée.
- `challenge2.sage` : (exemple) attaque par nonce biaisé (faible entropie) — variantes pédagogiques.
- `challenge3.sage` : (exemple) mise en œuvre d'une attaque de side-channel simulée / démonstration théorique.
- `challenge4.sage` : (exemple) exercice d'analyse de signatures et reconstruction par combinatoire / masquage.

Bonnes pratiques et sécurité
----------------------------
- N'exécutez ces scripts que dans un environnement de laboratoire contrôlé. Les attaques implémentées sont à but pédagogique.
- Ne réutilisez jamais de code d'attaque en production. Ce dépôt sert d'outil d'apprentissage.
- Pour expérimenter, travaillez sur des courbes de test ou des clés non sensibles.

Tests et validation
-------------------
Chaque challenge contient des assertions ou étapes de vérification — lisez les commentaires en en-tête pour connaître les sorties attendues. Pour valider rapidement :

1) Exécutez le script dans Sage ;
2) Vérifiez que la clé privée récupérée (lorsqu'une attaque le permet) correspond à la clé de référence donnée dans le fichier ou le commentaire ;
3) Consultez les prints/commentaires du script pour interpréter les résultats.

Contribuer
----------
- Forkez le dépôt et proposez des pull requests avec des ajouts ou corrections.
- Documentez toute modification — ajoutez un exemple d'exécution qui montre le comportement attendu.

Crédits et contact
------------------
Auteur : Pellandini Leo 

