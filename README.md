# Projet 3 : créer et interroger une base de données immobilière en SQL

Création d'une base de données relationnelle à partir des transactions immobilières françaises du 1er semestre 2020, puis analyse du marché avec des requêtes SQL.

## Contexte

Laplace Immo, un réseau d'agences immobilières, veut se démarquer de la concurrence grâce à l'analyse de données. Le projet consiste à :

- collecter les données de transactions immobilières en France ;
- les structurer dans une base de données normalisée ;
- répondre aux questions métier par des requêtes SQL, par exemple suivre le prix au m² et repérer les marchés porteurs.

## Contenu du dossier

| Élément                                   | Description               |
| ------------------------------------------- | ------------------------- |
| `SIESSE_Thomas_1_dictionnaire_03202.xlsx` | dictionnaire des données |
| `SIESSE_Thomas_2_support_032026.pptx`     | Présentation du projet   |

### Livrables

- **`SIESSE_Thomas_1_dictionnaire_032026.xlsx`** : dictionnaire des données. Pour chaque fichier source, il donne le code de chaque variable, sa signification, son type, sa longueur, sa nature (élémentaire, calculée ou concaténée), ses règles de gestion et ses règles de calcul. Exemple de variable calculée : `prix_m2 = Valeur_fonciere / Surface_carrez_du_1ER_lot`.
- **`SIESSE_Thomas_2_support_032026.pptx`** : support de présentation. Il couvre le contexte, la stratégie RGPD, les données initiales, un extrait du dictionnaire, le schéma relationnel, la vérification du chargement et les 12 requêtes SQL avec leurs résultats.

## Modèle de données

La base comporte 5 tables :

| Table                   | Contenu                                                                               |
| ----------------------- | ------------------------------------------------------------------------------------- |
| **Biens**         | Biens immobiliers : commune, surface, nombre de pièces, type (maison ou appartement) |
| **Ventes**        | Transactions : date de mutation, valeur foncière                                     |
| **Communes**      | Communes : nom, code, population totale                                               |
| **Départements** | Départements : code, nom, région de rattachement                                    |
| **Régions**      | Régions : code, nom                                                                  |

Liens entre les tables : une vente porte sur un bien, un bien se situe dans une commune, une commune appartient à un département, et un département appartient à une région.

## Conformité RGPD

La présentation décrit les mesures prévues :

- anonymisation des données ;
- minimisation des données collectées ;
- formulaire de consentement ;
- durée de conservation limitée ;
- chiffrement des données ;
- traçabilité des consultations.

## Auteur

Thomas SIESSE, mars 2026.
