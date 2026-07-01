# Analyse prix immobilier Loire Atlantique 44 Data Gouv
Analyse de l'évolution du prix de l'immobilier de 2021 à 2025 dans le département de la Loire Atlantique 44. Données issues du site data.gouv.fr.
(Données de Demande de Valeurs Foncières DVF)

## Nettoyage

- **Conservation des types Maison/ Appartement seulement***-->Concentration de l'analyse sur l'achat d'appartement et de maisons
- **Suppression des colonnes inutiles**-->Supression des colonnes inutiles telles que les anciens noms de communes, ou les lots par exemple.Nous ne nous en préocuperont pas pour l'analyse, seule la colonne surface réelle du bien nous intéressera. Les colonnes avec des pourcentages trop élevés en valeurs nulles sont aussi supprimées.
- **Suppression des valeurs nulles**-->Pour les colonnes telle que "valeur_foncière" par exemple qui sera très utile dans notre analyse"
- **Suppression des doublons**-->Garder uniquement les id_mutation qui apparaissent 1 seule fois.  Si on ne filtre pas sur cet identifiant, on risque de compter plusieurs fois le même prix de vente (le valeur_fonciere étant répété sur chaque ligne d'une même mutation), ce qui aurait faussé les statistiques de prix. C'est pour ça qu'on a gardé uniquement les id_mutation apparaissant une seule fois (ventes simples, un seul bien par transaction) pour simplifier l'analyse résidentielle. En excluant les mutations multi-lignes nous avons perdu ~11% de l'ensemble du dataset au départ (les ventes complexes:appartement + cave + parking en même temps) 
- **Analyse des outliers***-->Filtrage des aberrations de prix au m² élimination des lignes avec des prix au m2 <500 et >20000€.
- **Vérification des formats** -->Date au format datetime.

## Analyse 
### 


![Etude de la commune de Nantes](chemin-vers-image.png)

- **Vue Globale**
*Une forte densité entre 30-150m² → c'est la zone où se concentre l'immense majorité de tes ventes (logique, taille standard d'un logement)
Une dispersion qui se réduit avec la surface → plus le bien est grand, moins il y a de variabilité dans le prix au m² (les petites surfaces incluent un mélange très hétérogène de petits studios en centre-ville chers et de petites maisons rurales pas chères, alors que les grandes propriétés sont plus homogènes.)
Une légère tendance à la baisse : les surfaces au-delà de 200-300m² semblent avoir un prix au m² plus faible en moyenne ce qui est un phénomène bien connu en immobilier:  plus c'est grand, moins c'est cher au m², car la demande est plus restreinte).

- **Ralentissement des ventes**
   *Le marché nantais a connu un ralentissement de ses ventes, généralisé sur la période 2022-2024 (-30 à -35% selon les segments)
- **Baisse du prix au m2**
   *(-7% à -16% selon la taille du logement).
- **Reprise du volume des ventes en 2025**
   *sur tous les segments. 
  
Ceci pourrait s'expliquer par plusieurs facteurs:

- **La hausse du taux d'intéret**
  Quand les taux montent, pour la même mensualité, ces acheteurs peuvent emprunter beaucoup moins. Exemple simplifié :Les acheteurs, à budget mensuel égal, doivent viser des biens moins chers → ils négocient plus fort, ou achètent ailleurs/plus petit. Moins de pouvoir d'achat immobilier = pression à la baisse sur les prix de ce segment précisément.
- **L'inflation générale**
  réduisant le pouvoir d'achat des ménages( les salaires n'ont globalement pas suivi l'inflation en France et le pouvoir d'achat réel des ménages a mécaniquement diminué, réduisant leur capacité à absorber des prix immobiliers élevés.
- **Le durcissement des conditions d'octroi de crédit**.
   Les banques françaises ont dû respecter des règles plus strictes sur le taux d'endettement maximum (35% des revenus) depuis 2022 — donc même des acheteurs avec de bons revenus se sont vus refuser des prêts qu'ils auraient obtenus facilement avant. Ça réduit le nombre d'acheteurs solvables sur le marché.

Mon dataset ne permet pas d'isoler la contribution exacte de chaque facteur, mais ces éléments macroéconomiques convergent pour expliquer la tendance observée. 


Les grandes surfaces (150m²+) ont mieux résisté, suggérant que les acheteurs de biens haut de gamme sont moins sensibles à la hausse des taux d'intérêt. 
 



[Texte cliquable](https://lien-vers-le-site.com)
