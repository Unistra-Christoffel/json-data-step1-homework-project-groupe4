# Activité : Création et Utilisation de Données JSON pour une To-Do List

Ce document détaille les étapes pour structurer les données d'une application de type "To-Do List" en utilisant le format JSON, puis de les intégrer dans une page HTML.

-----

## Étape 1A : Structure JSON d'une tâche

### Quelles sont les données pour renseigner une tâche ?

Pour commencer, nous devons définir les informations essentielles pour une seule tâche. Proposez une structure contenant au minimum :

* Un **libellé** pour la tâche.
* Un **identifiant** unique qui s'incrémentera pour chaque nouvelle tâche (1, 2, 3, etc.).
* Optionnellement, une **description** plus détaillée ou une **date de création/finalisation**.

**Attention** : Pour l'instant, n'incluez pas de paramètres variables comme la priorité (important, non important, etc.).

### Action à réaliser

1.  Créez la structure JSON d'un seul objet de tâche, délimité par `{ }`, contenant des paires **clé/valeur**.
2.  Utilisez un éditeur en ligne comme [JSON Editor Online](https://jsoneditoronline.org/) pour vérifier que votre structure est valide.
3.  **Exemple** pour un catalogue de CD (notez l'identifiant) :
    ```json
    {"idCD":"1","title":"Empire Burlesque","artist":"Bob Dylan","country":"USA","company":"Columbia","price":"10.9","year":"1985"}
    ```
4.  **Dépôt** : Déposez sur GitHub Enseignement votre structure **compactée** (sur une seule ligne). Nom du dépôt : `Activité JSON 1A`. *Une structure non compactée entraînera la note de 0.*

-----

## Étape 1B : Données relatives aux paramètres d'une tâche

### Création du paramètre "Priorité"

Nous allons maintenant inclure des paramètres pour caractériser une tâche.

1.  Créez la structure JSON pour un paramètre : la **priorité**.
2.  Cette structure, pour chaque niveau de priorité, doit comporter au moins deux clés : un **identifiant** et une **propriété** décrivant le niveau.
    * *Exemple pour des catégories de films* : `{"idCategorie":"1","categorie":"Comédie"}`
3.  Les différents niveaux de priorité doivent être des éléments d'un tableau (une **Array** JSON, définie avec `[ ]`).
    * *Exemple pour plusieurs catégories* :
      ```json
      [{"idCategorie":"1","categorie":"Comédie"},{"idCategorie":"2","categorie":"Thriller"}]
      ```

### Action à réaliser

1.  Proposez une structure JSON pour le paramètre "priorité" contenant un tableau (`Array`) d'objets (`{ }`).
2.  Définissez au moins 4 ou 5 niveaux de priorité (ex: Urgent, Important, Normal, Faible...).
3.  Assurez-vous que chaque niveau a un identifiant unique et incrémenté (1, 2, 3...).
4.  **Dépôt** : Déposez sur GitHub Enseignement votre structure **compactée**. Nom du dépôt : `Activité JSON 1B`.

-----

## Étape 1C : Autres paramètres pour une tâche

### Action à réaliser

1.  Proposez **2 à 3 autres paramètres** originaux pour caractériser une tâche (par exemple : état d'avancement, catégorie, contexte, etc.).
2.  Pour chaque paramètre, créez une structure JSON similaire à celle de l'étape 1B (un tableau d'objets avec identifiant et valeur). L'originalité sera prise en compte.
3.  **Dépôt** : Déposez sur GitHub Enseignement chaque structure **compactée**. Nom du dépôt : `Activité JSON 1C`.

-----

## Étape 1D : Intégration des paramètres dans la structure de la tâche

### Action à réaliser

1.  Reprenez la structure initiale de la tâche (de l'étape 1A) et complétez-la en y ajoutant les paramètres créés en 1B et 1C.
2.  **Important** : Vous devez inclure uniquement l'**identifiant** du paramètre, et non sa valeur textuelle.
3.  Créez un tableau (`Array`) contenant au moins 2 ou 3 tâches complètes.

<!-- end list -->

* **Exemple correct** (avec l'identifiant `idCategorie`) :
  ```json
  [{"idFilm":"1","titreFilm":"Le dîner de con","idCategorie":"1"},{"idFilm":"2","titreFilm":"Les bronzés font du ski","idCategorie":"1"},{"idFilm":"3","titreFilm":"Taxi driver","idCategorie":"2"}]
  ```
* **Exemple incorrect** (n'utilisez pas cette méthode) :
  ```json
  [{"idFilm":"1","titreFilm":"Le dîner de con","categorie":"comédie"},{"idFilm":"2","titreFilm":"Les bronzés font du ski","categorie":"Comédie"}]
  ```

<!-- end list -->

4.  **Dépôt** : Déposez sur GitHub Enseignement votre structure de tâches finale, **compactée**. Nom du dépôt : `Activité JSON 1D`.

-----

## Étape 1E : Création d'une page HTML avec les données JSON

### Action à réaliser

1.  Créez une page HTML de base avec un élément `<script>` dans la balise `<head>`.
2.  Dans le script, affectez vos données JSON à des variables JavaScript : une variable pour le tableau des tâches, puis une variable pour chaque tableau de paramètres.
3.  Utilisez `console.log()` pour afficher le contenu de chaque variable dans la console du navigateur.

<!-- end list -->

* **Exemple de code JavaScript** :
  ```javascript
  let listeFilms = [ 
      {"idFilm":"1","titreFilm":"Le dîner de con","idCategorie":"1"},
      {"idFilm":"2","titreFilm":"Les bronzés font du ski","idCategorie":"1"},
      {"idFilm":"3","titreFilm":"Taxi driver","idCategorie":"2"} 
  ];

  let listeCategories = [ 
      {"idCategorie":"1","categorie":"Comédie"},
      {"idCategorie":"2","categorie":"Thriller"} 
  ];

  console.log(listeFilms);
  console.log(listeCategories);
  ```

<!-- end list -->

4.  **Dépôt** : Hébergez votre page HTML sur Alwaysdata ou Planet Hoster, puis indiquez l'URL de la page dans l'activité de dépôt nommée : `Dépot Activité JSON 1E`.