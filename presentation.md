class: middle, center, inverse, title

# `explore-data`

## Un outil d'enseignement de la statistique descriptive

François-Xavier Jollois

.footnote[lien vers le [projet Github](http://github.com/fxjollois/explore-data)]

---

# Présentation

--

### En quelques mots

- Application **web** dédiée à l'enseignement

- Développée en **interne**, pour correspondre aux besoins

- Utilisée pour les TPs en **1ère année** de DUT Statistique et Informatique Décisionnelle (**STID**)

--

### Que permet-elle de faire ?

- Choix de données (déjà présentes ou chargement de fichiers textes)

- Sélection d'un sous-ensemble basée sur des critères

- Réalisation des calculs statistiques simples

- Création des graphiques usuels

---

# Besoins

--

### Pourquoi ne pas utiliser un logiciel statistique ?

- Informations souvent **trop** complètes

- Terminologie différente du cours

- Installation nécessaire pour un travail à la maison

--

### Pourquoi ne pas utiliser un langage statistique ?

- Etudiants de **1ère année** post-bac, sans réelle connaissance informatique

- Complexité (relative) de la programmation

- Etudiants concentrés sur la partie code et pas sur les aspects **analyse**

- Installation nécessaire pour un travail à la maison

---

class: middle, center, inverse

La solution ?

--

# Une application **web** et **dédiée**

---

# Et dans le détail

- Utilisation du langage [`R`](https://www.r-project.org/) et de la librairie 
[`shiny`](https://shiny.rstudio.com/)
	- Simplicité de programmation
	- Utilisation de la librairie [`ggplot2`](http://ggplot2.org/) pour les 
	graphiques .red[*]

- Projet [github](http://github.com/) pour une réutilisation possible par tous
	- sous licence [GNU GPLv3](https://www.gnu.org/licenses/gpl-3.0.fr.html)

- Hébergement sur un serveur dédié dans les locaux de l'Université Paris Descartes
	- plateforme de serveurs virtuels basé sur *OpenNebula*
	- serveur : 8go RAM, 8 coeurs

.footnote[.red[*] ainsi que d'autres librairies telles que [`reshape`](https://github.com/hadley/reshape) 
et [`scales`](https://github.com/hadley/scales)]

---

# Réalisation

- Développement durant le premier semestre 2016
	- Programmation par FX Jollois
	- Test et validation par l'équipe statistique du département STID

- Application en deux fichiers
	- `ui.R` : mise en forme et déclaration des *inputs*  et *outputs*
	- `server.R` : définition des *outputs* (en fonction des *inputs*) et de fonctions et variables globales utiles

- Utilisation de plusieurs interfaces dynamiques (avec `uiOutput()`) pour la gestion des options 
	- lors de l'importation d'un fichier texte
	- des représentations numériques
	- des graphiques


---

# Utilisation

- Tout en *clic* 

- Interface épurée et simple pour ne pas perturber les étudiants

- 5 onglets
	- **Données** : soit déjà présentes, soit importées (fichier texte délimité)
	- **Variables** : équivalent à la commande `str()`
	- **Sous-population** : restriction sur critères (à écrire comme dans un `subset()`)
	- **Univarié** : description d'une variable 
	- **Bivariée** : description du lien entre deux variables

- Plus 
	- *Informations* sur l'application 
	- *Aide* sur le jeu de données si celui-ci est déjà présent

---

# Quelles possibilités ?

- Informations de base (nombre de valeurs, nombre de valeurs manquantes, % de valeurs manquantes)

--

### Quantitative

- *Numérique* : moyenne, écart-type, variance, minimum, Q1, médiane, Q3, maximum
- *Histogramme* : par nombre d'*intervalles*, par largeur, discrétisation personnalisée
- *Boîte à moustaches*
- *QQ plot*
- *Fréquences cumulées*
- *Courbe cumulée* : même choix que pour l'histogramme

--

### Qualitative

- *Numérique* : modalités, effectifs, proportions (avec cumulées si demandé)
- *Diagramme en barres* : en effectifs ou en proportions
- *Diagramme circulaire*

---

### 2 Quantitatives

- *Numérique* : covariance et corrélation
- *Nuage de points*
- *Heatmap*

--

### 2 Qualitatives

- *Numérique* : table de contingence, de proportions, des profils lignes ou des profils colonnes
- *Diagramme en barres* : empilées ou séparées, en effectifs ou en fréquences
- *Heatmap*

--

### Quantitative vs qualitative

- *Numérique* : même informations que pour une variable quantitative, mais pour chaque modalité
- *Histogramme*
- *Boîtes à moustaches*
- *Fréquences cumulées*

---

class: middle, center, inverse

Une démonstration ?

--

# [Lien vers l'application](http://193.51.82.104:2223/explore-data/) .red[*]

.footnote[.red[*] serveur hébergé dans les locaux de l'Université Paris Descartes]

---

# Et après ?

### Améliorations prévues dans le cadre des cours :

- Ajout de quelques calculs statistiques
- Création d'une variable ordinale sur la base d'un découpage d'une variable quantitative

--

### Programmation par modules 

- Meilleure lisibilité du code
- Personnalisation des sorties plus cohérentes

--

### Autres améliorations éventuelles 

- Description des variables à améliorer
- Choix d'un thème générique et/ou des couleurs pour chaque graphique
- Extension vers des statistiques plus complexes ?
- Intégration possible d'autres types de données ?
- Réflexion sur le *design* à mener éventuellement

---

class: middle, center, inverse

# Merci

## N'hésitez pas à utiliser et à participer éventuellement

### [Projet Github](http://github.com/fxjollois/explore-data)