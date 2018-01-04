# Attributs de formulaire

## 1. Définition



Les attributs d'un formulaire peuvent être créés, édités et supprimés
dans le studio. Certains attributs exploitent des valeurs issues de base
de données ou de services web, d'autres sont des composants de mise en
page destinés à personnaliser l'interface du formulaire, et d'autres
sont des attributs classiques directement configurables dans vMap.

Il existe plus d'un vingtaine de types d'attributs paramétrables dans la
fenêtre de définition en bas à gauche du studio.

## 2. Édition des attributs

### 2.1. Bouton radio

![](../../images/bouton_radio1.png)

Nommer l'attribut et son libellé tel qu'il sera affiché dans le
formulaire. Définir la valeur par défaut et déterminer si le bouton
radio doit être désactivé ou pas. Définir ensuite les options possibles
en entrant le libellé du bouton et la valeur envoyée en base. Le bouton
"Option" permet l'ajout d'une option supplémentaire.

![](../../images/bouton_radio.png)

### 2.2. Boîte à cocher

![](../../images/boite_a_cocher1.png)

Nommer l'attribut et son libellé tel qu'il sera affiché dans le
formulaire. Définir si la boîte doit être cochée par défaut ou pas.

![](../../images/boite_a_cocher.png)

### 2.3. Paramètres de type Carte Bing, OSM, vMap
 vMap permet d'exploiter les services
web OSM, Bing Maps ou Vitis vMap pour personnaliser un formulaire en
exploitant leurs ressources cartographiques.

#### 2.3.1. Carte OSM

![Carte OSM](../../images/carte_osm.png)

Nommer le paramètre et définir le libellé qui sera affiché dans le
formulaire de demande. Définir la hauteur et la largeur de la carte et
indiquer si ce paramètre est obligatoire ou pas en cochant la case
Requis.

Paramétrer ensuite les options spécifiques aux éléments de type carte :

-   La projection de la carte : WGS84 ou Lambert 93. En Lambert 93,
    l’étendue par défaut correspond à l'ensemble de la
    France métropolitaine.
-   Méthode de centrage de la carte : l'auteur choisit si le centre de
    la carte est défini par un point défini via des coordonnées X/Y et
    une échelle d'affichage, ou si le centre de la carte est
    paramétrée par son étendue définie par les coordonnées X et Y Min
    et Max.

Choisir ensuite les éléments de dessin et de navigation qui seront
affichés sur la carte du formulaire de demande :

-   Position de la souris : affichage dynamique des coordonnées de la
    souris selon la projection définie.
-   Boutons de zoom : affichage des boutons de navigation classique
    zoom avant, zoom arrière et retour à l'étendue par défaut.
-   Echelle : affichage de l'échelle.
-   Projection de la carte : affichage de la projection Lambert 93 ou
    WGS 84.
-   Multiples géométries : possibilité ou pas de saisir des géométries
    de type différent (point, ligne et polygone).
-   Plein écran : permet d'afficher la carte en mode plein écran.
-   Suppression générale : Suppression de toutes les géométries
    saisies sur la carte.
-   Edition : modification de la géométrie sélectionnée.
-   Dessiner un point.
-   Dessiner une ligne.
-   Dessiner un polygone.
-   Le champ Valeur permet à l'auteur de définir une géométrie qui
    sera affichée par défaut dans le formulaire. Cette géométrie est
    décrite via une chaîne WKT :

![](../../images/carte_valeur_par_dafaut.png)

![](../../images/c_formulaire_carteOSM.png)

#### 2.3.2. Carte Bing

![image](../../images/c_formulaire_carte_bing.png)

Tous les paramètres de personnalisation d'une carte Bing Maps sont
identiques à ceux des cartes OSM. Il faut fournir en plus, une clé
d'accès pour pouvoir exploiter ce service web cartographique.

Générer une clé Bing Maps sur le site .. :
<https://www.bingmapsportal.com/>

Une fois obtenue, entrer la clé dans le champs Clé et sélectionner la
carte à afficher dans le formulaire de demande :

-   Aerial
-   Aerial WithLabels
-   Road

#### 2.3.3. carte vMap

![Carte vMap](../../images/carte_vmap.png)

Pour pouvoir exploiter une carte vMap, il faut au préalable, dans vMap,
exporter la définition de la carte.

L'export d'une carte vMap génère un fichier map.json que l'auteur du
formulaire doit télécharger (champ Fichier local) pour pouvoir
l'intégrer dans un formulaire.

Procéder ensuite de la même façon qu'avec les autres ressources de type
carte, en nommant le paramètre et son libellé, puis en paramétrant
l'affichage des outils propres aux cartes.

### 2.6. Champ caché

Un attribut de type Champ caché permet de masquer un attribut. Il est
exploité dans le formulaire mais n'est pas apparent. Nommer le paramètre
et définir la valeur à exploiter. 

### 2.7. Couleur

![Attribut de type sélecteur de couleur](../../images/selecteur_couleur.png)

Un attribut de tye Choix de la couleur insère un sélecteur de couleurs.
Nommer le paramètre et le libellé à afficher dans le formulaire, et
définir la couleur par défaut.

### 2.8. Curseur

Un attribut de tye curseur insère un curseur dans le formulaire. Nommer
le paramètre et le libellé à afficher et définir les valeurs minimales
et maximales de la plage de données ainsi que la valeur par défaut.

![Attribut de type curseur](../../images/curseur.png)

### 2.9. Paramètres de type Date

#### 2.9.1. Date

Un attribut de type Date insère une date sous la forme jj/mm/aaaa. Un
calendrier s'affiche dans le formulaire pour faciliter la date à entrer.

Nommer le paramètre et le libellé à afficher et définir la valeur par
défaut.

![Attribut de type curseur](../../images/date.png)

#### 2.9.2. Date/heure

Un attribut de type Date et heure insère une date sous la forme
jj/mm/aaaa hh:mm. Un calendrier et une montre facilite la saisie la date
et de l'heure dans le formulaire.

Nommer le paramètre et le libellé à afficher et définir la valeur par
défaut.

### 2.10. Document - objet métier
Un attribut de type Document - objet métier est un champ de chargement de documents. 

![](../../images/document.png)

Nommer le paramètre et le libellé à afficher. 

![](../../images/formulaire_document.png)

Définir le format des documents téléchargeables en indiquant leurs extensions possibles séparées par un |. 

La boîte à cocher "Uniquement en consultation" indique si le document est uniquement consultable ou si il doit être téléchargé. 

 Un unique fichier peut être associé à un attribut. Il faut donc compresser les documents en un unique fichier zip pour pouvoir les associer à un même attribut. 

Obtenir un [exemple d'insertion d'attribut de type Document](cas_utilisation.md#5-personnalisation-dun-formulaire-insertion-dun-champ-de-chargement-de-documentimage)

### 2.11. Image Objet métier

Un attribut de type Image - objet métier est un champ de chargement d'images.

![](../../images/image.png)

Nommer le paramètre et le libellé à afficher. 

La boîte à cocher "Uniquement en consultation" indique si l'image est uniquement consultable ou si elle doit être téléchargée. 

Un unique fichier peut être associé à un attribut. Il faut donc compresser les images en un unique fichier zip pour pouvoir les associer à un même attribut. 

Obtenir un [exemple d'insertion d'attribut de type Document/image](cas_utilisation.md#5-personnalisation-dun-formulaire--insertion-dun-champ-de-chargement-de-documentimage)

### 2.12. Décimal
Nommer l'attribut et le libellé qui seront affichés dans le formulaire et définir la valeur par défaut. Définir si ce paramètre est obligatoire ou pas en cochant la case Requis. 

### 2.13. Entier
Nommer l'attribut et le libellé qui seront affichés dans le formulaire et définir la valeur par défaut. Définir si ce paramètre est obligatoire ou pas en cochant la case Requis. 


### 2.14. Editeur de code CodeMirror



### 2.15. Grille objet métier

Un attribut de type Grille objet métier permet d'associer à un élément un sous élément. La grille objet métier permet l'insertion d'objet enfant associé à un objet parent. 

Nommer le paramètre et le libellé à afficher, puis sélectionner l'objet métier enfant et définir l' attributs parent et enfant surlesquels reposent l'ascendance. 

![](../../images/exemple_studio_grille_2.png)

Obtenir un  [exemple d'insertion d'attribut de type grille objet métier](cas_utilisation.md#6-personnalisation-dun-formulaire--insertion-dune-grille-de-sous-objets)


### 2.16. Grille section vitis



### 2.18. Image URL

Un attribut de type image URL permet d'afficher dans un formulaire l'url d'un image. Indiquer le libellé, l'attribut et l'url dans le champs valeur. 



### 2.19. Interface bouton

### 2.20. Interface ligne de séparation

### 2.21. Label

### 2.22. Lien

![Attribut de type curseur](../../images/lien.png)

Un attribut de type Lien permet d'insérer des liens vers d'autres
plateformes. Nommer le paramètre et le libellé à afficher.

Définir ensuite les paramètres du lien :

-   Texte : texte à afficher
-   Cible : si laissé vide, la page s'ouvre dans un nouvel onglet.
-   Valeur : adresse du lien

Obtenir un [exemple d'insertion d'attribut de type lien](cas_utilisation.md#2-personnalisation-dun-formulaire--insertion-dun-attribut-de-type-lien)


### 2.23. Liste

3 types de listes sont paramétrables dans vMap. Le [gestionnaire de source de données](gestionnaire_source_donnees.md) permet une configuration fine des listes, de leurs sources et de leurs modalités d'affichage. 



#### 2.23.1. Liste simple

On entend par liste simple, une liste de choix dans laquelle l'utilisateur sélectionne un élément directement en cliquant parmi une des ocurrences de la liste : 

![Attribut de type curseur](../../images/liste_simple.png)

Après avoir indiqué le libellé de l'objet et l'attribut à partir duquel il est défini, sélectionner la source de données dans la liste ou cliquer sur le bouton Sources de données pour en ajouter. 

#### 2.23.2. Liste double

Une liste double permet d'afficher dans un formulaire les éléments d'une liste répartis en deux blocs : les éléments disponibles en sélection et les éléments sélectionnés. 

#### 2.23.3. Liste déroulante

Un attribut de type liste déroulante permet d'afficher la liste de choix sous forme de liste déroulante. 

Obtenir un [exemple d'insertion d'attribut de type liste](cas_utilisation.md#utilisation-du-gestionnaire-de-source-de-donnees-insertion-d-une-liste-deroulante)


### 2.24. Texte
 
 
Nommer l'attribut et son libellé tel qu'il sera affiché dans le formulaire. Une expression régulière peut être définie pour containdre la saisie de ce champ, et une valeur pas défaut peut également être définie. 
