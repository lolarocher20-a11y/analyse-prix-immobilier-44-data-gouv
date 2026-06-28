# Analyse prix immobilier Loire Atlantique 44 Data Gouv
Analyse de l'évolution du prix de l'immobilier de 2021 à 2025 dans le département de la Loire Atlantique 44. Données issues du site data.gouv.fr.
(Données de Demande de Valeurs Foncières DVF)

## Nettoyage

**- Conservation des types Maison/ Appartement seulement**
*Concentration de l'analyse sur l'achat d'appartement et de maisons*
**- Supression des colonnes inutiles**
*Supression des colonnes inutiles telles que les anciens noms de communes, ou les lots par exemple.Nous ne nous en préocuperont pas pour l'analyse, seule la colonne surface réelle du bien nous intéressera. Les colonnes avec des pourcentages trop élevés en valeurs nulles sont aussi supprimées.*
**- Supression des valeurs nulles**
*Pour les colonnes telle que "valeur_foncière" par exemple qui sera très utile dans notre analyse"*
**- Supression des doublons**
*Garder uniquement les id_mutation qui apparaissent 1 seule fois.  Si on ne filtre pas sur cet identifiant, on risque de compter plusieurs fois le même prix de vente (le valeur_fonciere étant répété sur chaque ligne d'une même mutation), ce qui aurait faussé les statistiques de prix. C'est pour ça qu'on a gardé uniquement les id_mutation apparaissant une seule fois (ventes simples, un seul bien par transaction) pour simplifier l'analyse résidentielle. En excluant les mutations multi-lignes nous avons perdu ~11% de l'ensemble du dataset au départ (les ventes complexes:appartement + cave + parking en même temps) *
**- Analyse des outliers**
*Filtrage des aberrations de prix au m² élimination des lignes avec des prix au m2 <500 et >20000€.*
**- Vérification des formats**
Date au format datetime.



- Liste à puce 1
- Liste à puce 2

## Analyse 
### 

**Texte en gras**
*Texte en italique*

- Liste à puce 1
- Liste à puce 2

1. Liste numérotée
2. Deuxième élément

[Texte cliquable](https://lien-vers-le-site.com)

![Description de l'image](chemin-vers-image.png)
