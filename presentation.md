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

.footnote[.red[*] ainsi que les librairies [`reshape`](https://github.com/hadley/reshape) 
et [`scales`](https://github.com/hadley/scales)]

---

# Réalisation

a faire


---

# Utilisation

a faire

---

class: middle, center, inverse

Une démonstration ?

--

# [Lien vers l'application](http://193.51.82.116:3838/explore-data/) .red[*]

.footnote[.red[*] Serveur hébergé dans les locaux de l'Université Paris Descartes]

---

# Et après ?

a faire


