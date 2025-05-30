# Remise du travail pratique 1

Travail individuel.

## Identification

- Cours      : Utilisation et administration des systèmes informatiques
- Sigle      : INF1070
- Session    : Automne 2022
- Groupe     : INF1070-001 
- Enseignant : Philippe Olivier
- Auteur     : Aymen Benyahia (BENA74070105)




Mission 1 – Affichage de texte formaté
Problème
Afficher trois lignes spécifiques de texte (alpha, beta, gamma) dans un fichier en respectant les sauts de ligne.

## Solution de la mission 1 d'exemple

### État de la mission : résolue

### Démarche

J'ai utilisé la commande `echo` pour afficher les trois lignes.
J'ai utilisé l'option `-e` pour interpréter les caractères `\n` correctement.
J'ai redirigé le résultat dans le fichier `exemple.txt` :

```sh
echo -e 'alpha\nbeta\ngamma\n' > exemple.txt
```

Ensuite, en entrant

```sh
gash check
```

la mission a été validée, ce qui a conclu cette mission.



Mission 2 – Navigation dans les répertoires
Problème
Atteindre un répertoire cible (paris) en naviguant dans une structure de dossiers en suivant des contraintes spécifiques (ordre, types de transport, etc.).

## Solution de la mission 2

### État de la mission : résolue

### Démarche

J'ai utilisé la commande `tree` pour m'afficher les chemins que je pouvais utiliser.
J'ai utilisé la commande `cd montreal/toronto/avion/bruxelles/bus/paris` pour arriver a paris en suivant les contraintes.


```sh
cd montreal/toronto/avion/bruxelles/bus/paris
```

Ensuite, en entrant

```sh
gash check
```

la mission a été validée, ce qui a conclu cette mission.


Mission 3 – Déplacement de fichiers avec permissions
Problème
Déplacer un fichier (coffre) d’un emplacement à un autre et modifier ses permissions selon des règles précises.

## Solution de la mission 3

### État de la mission : résolue

### Démarche

J'ai utilisé la commande `mv ~/kinshasa/pekin/coffre ~/bruxelles/amsterdam` pour deplacer le coffre au repertoire amsterdam 
J'ai utilisé la commande `chmod 544 ~/bruxelles/amsterdam/coffre` pour modifier les permissions pour repondre aux contraintes 


```sh
mv ~/kinshasa/pekin/coffre ~/bruxelles/amsterdam
```
```sh
chmod 544 ~/bruxelles/amsterdam/coffre
```

Ensuite, en entrant

```sh
gash check
```

la mission a été validée, ce qui a conclu cette mission.


Mission 4 – Création d’un lien symbolique
Problème
Créer un tunnel (lien symbolique) entre deux répertoires spécifiques avec le bon chemin et le bon nom.

## Solution de la mission 4

### État de la mission : partiellement résolue

### Démarche

J'ai utilisé la commande `ln -s ~/berri-uqam/champ-de-mars/place-d-armes ~/berri-uqam/saint-laurent/place-des-arts` pour creer un tunnel
comme demande.

```sh
ln -s ~/berri-uqam/champ-de-mars/place-d-armes ~/berri-uqam/saint-laurent/place-des-arts
```

Ensuite, en entrant

```sh
gash check
```

La mission n'a pas ete validee 


Mission 5 – Recherche dans un fichier à une date précise
Problème
Trouver une ligne dans un fichier en fonction d’une date donnée en format Unix timestamp, convertie en format lisible (YYYY-MM-DD), et enregistrer cette ligne dans un fichier.

## Solution de la mission 5

### État de la mission : résolue

### Démarche

J'ai utilisé la commande `grep $(date -d @1593576000 '+%Y-%m-%d') pays` pour trouver la ligne qui equivaut a la date en secondes converti en format annee, mois et jour
J'ai utilisé la commande `> epochnational` pour rediriger le resultat vers le fichier epochnational

```sh
grep $(date -d @1593576000 '+%Y-%m-%d') pays > epochnational
```


Ensuite, en entrant

```sh
gash check
```

la mission a pas ete validee


Mission 6 – Fusion et tri de fichiers
Problème
Fusionner deux fichiers ligne par ligne, puis trier le résultat dans l’ordre alphabétique et sauvegarder dans un fichier.

## Solution de la mission 6

### État de la mission : résolue

### Démarche

J'ai utilisé la commande `paste -d '' datesfetes nomspays` pour coller les fichiers datesfetes et nomspays avec un espace entre eux.
J'ai utilisé le tube `| sort` pour trier par ordre croissant le resultat.
J'ai utilise la commande `> resultats` pour rediriger le resultat dans le fichier resultats :

```sh
paste -d '' datesfetes nomspays | sort > resultats
```

Ensuite, en entrant

```sh
gash check
```

la mission a été validée, ce qui a conclu cette mission.


Mission 7 – Recherche de suffixes spécifiques
Problème
Rechercher toutes les lignes d’un fichier se terminant par les lettres tz et sauvegarder ces résultats dans un fichier.

## Solution de la mission 7

### État de la mission : résolue

### Démarche

J'ai utilisé la commande `grep 'tz$'` pour rechercher les lignes qui finissent seulement par tz
J'ai utilisé la commande `~/french` pour que la recherche se fasse dans le fichier french.
J'ai utilise la commande `> suffixetz` pour rediriger le resultat dans le fichier suffixetz :

```sh
grep 'tz$' ~/french > suffixetz
```

Ensuite, en entrant

```sh
gash check
```

la mission a été validée, ce qui a conclu cette mission.


Mission 8 – Compter les caractères d’une ligne spécifique
Problème
Afficher uniquement la 7e ligne d’un fichier texte et compter le nombre de caractères qu’elle contient.

## Solution de la mission 8

### État de la mission : résolue
### Démarche

J'ai utilisé la commande `sed` pour filtrer et transfomer le texte.
J'ai utilisé l'option `-n` pour desactive l'impression automatique.
J'ai utilise le commande `7p lorem.txts` pour qu'on affiche seulement la ligne 7 du fichier lorem.txt 
J'ai utilise le commande `| wc -m` pour que le resultat soit le nombre de caracteres :

```sh
sed -n 7p lorem.txt | wc -m
```

Ensuite, en entrant

```sh
gash check
```

la mission a été validée, ce qui a conclu cette mission.


Mission 9 – Afficher une ligne spécifique
Problème
Afficher uniquement la ligne 9999 d’un fichier.

## Solution de la mission 9

### État de la mission : résolue

### Démarche

J'ai utilisé la commande `sed` pour filtrer et transformer du texte
J'ai utilisé l'option `-n` pour desactive l'impression automatique
J'ai utilise la commande `9999p french` pour qu'on m'affiche uniquement la ligne 9999 du fichier french:

```sh
sed -n 9999p french
```

Ensuite, en entrant

```sh
gash check
```

la mission a été validée, ce qui a conclu cette mission.


Mission 10 – Compter les mots après avoir ignoré les 9 premiers caractères
Problème
Supprimer les 9 premiers caractères de chaque ligne d’un fichier, puis compter combien de mots il reste.

## Solution de la mission 10

### État de la mission : résolue

### Démarche

J'ai utilisé la commande `cut` pour couper des caracteres
J'ai utilise l'option `-c 10- french` pour couper des mots de moins de 10 caracteres
J'ai utilise `| wc -w` pour qu'on m'affiche en resultat le nombre de mots de moins de 10 caracteres
```sh
cut -c 10- french | wc -w 
```

Ensuite, en entrant

```sh
gash check
```

la mission a ete validee.


Mission 11 – Création d’une arborescence complexe
Problème
Créer une structure de répertoires imbriqués représentant plusieurs pays et villes, d’un seul coup avec la bonne syntaxe.

## Solution de la mission 11

### État de la mission : résolue

### Démarche

J'ai utilisé la commande `mkdir` pour creer un dossier.
J'ai utilisé l'option `-p`pour pouvoir creer des repertoires parents.
J'ai utilise la commande `asie/{chine/{beijing,gansu/lanzhou,guizhou/guiyang},japon/{osaka,tokyo,yokohama},vietnam/hanoi}` pour creer l'arborescence demandee
```sh
mkdir -p asie/{chine/{beijing,gansu/lanzhou,guizhou/guiyang},japon/{osaka,tokyo,yokohama},vietnam/hanoi}
```

Ensuite, en entrant

```sh
gash check
```

la mission a été validée, ce qui a conclu cette mission.


Mission 12 – Recherche et redirection conditionnelle de fichiers
Problème
Trouver tous les fichiers se terminant par .out et .err et rediriger leur chemin vers des fichiers log/out.log et log/err.log respectivement.

## Solution de la mission 12

### État de la mission : partiellement résolue

### Démarche

J'ai utilisé la commande `find . -type f` pour faire une recherche dans tous les repertoires pour trouver les fichiers demandes. 
J'ai utilisé la commande `\(-name "*.out" > log/out.log -o -name "*.err" > log/err.log\)` pour que la recherche trouve les fichiers
qui terminent par .out et les redirigent vers le fichier log/out.log, meme chose pour les fichiers qui terminent par .err qui seront rediriges vers le fichier 
log.err.log


```sh
find . -type f \(-name "*.out" > log/out.log -o -name "*.err" > log/err.log\)
```

Ensuite, en entrant

```sh
gash check
```

la mission n'a pas ete validee.



Mission 13 – Modification de permissions
Problème
Modifier les permissions de certains fichiers pour empêcher les autres utilisateurs (other) d’avoir accès en lecture, écriture et exécution.
## Solution de la mission 13

### État de la mission : résolue

### Démarche

J'ai utilisé la commande `chmod o-wrx permissions/fichier_10 permissions/fichier_13 permissions/fichier_20 permissions/fichier_27 permissions/fichier_30 permissions/fichier_35 permissions/fichier_4 permissions/fichier_47 permissions/fichier_47 permissions/fichier_49` pour changer les permissions des fichiers qui n'etaient comme ceux demandes 

```sh
chmod o-wrx permissions/fichier_10 permissions/fichier_13 permissions/fichier_20 permissions/fichier_27 permissions/fichier_30 permissions/fichier_35 permissions/fichier_4 permissions/fichier_47 permissions/fichier_47 permissions/fichier_49
```

Ensuite, en entrant

```sh
gash check
```

La mission a ete validee


Mission 14 – Détection de palindromes
Problème
Trouver les mots qui sont des palindromes dans un fichier, c’est-à-dire qui restent les mêmes lus à l’endroit et à l’envers.
## Solution de la mission 14

### État de la mission :  résolue

### Démarche

J'ai utilisé la commande `comm` pour inverser les chaines de caracteres du fichier mot.
J'ai utilisé le tube `| sort` pour mettre le resultat en ordre croissant.
J'ai redirigé le résultat dans le fichier `palindromes` :

```sh
comm -1 -2 <(sort mots) <(rev mots | sort) > palindromes
```

Ensuite, en entrant

```sh
gash check
```
La mission a ete validee

