#Création de la Version Responsive du Site
##Branche : wenjoanel-integration-1

Ce projet vise à mettre une page web statique responsive
afin qu'elle puisse s'adapter correctement aux différentes
tailles d'écrans : mobile, tablette et desktop.

---

#Choix réaliser pour adapter le site

L'approche choisie est l'adaptation au format 
mobile et tablette : la mise en page de base étant 
pensée pour les grands écrans, on utilisera alors 
le media queries afin d'ajuster le layout aux 
écrans plus petits.

Les principales décisions sont :

-Utilisation de **Flexbox** pour organiser les
éléments en ligne ou en colonne selon la taille de
l'écran.
-Utilisation d'unités flexibles, notament le **pourcentage**
(%) et le **viewport-height** (vh).
-La navigation latérale est masquée sur mobile pour 
libérer de l'espace au contenu principal.
-Les cartes de services (SERVICES 1,...), affichées côte
à côte sur desktop, se réorganisent en colonne sur mobile 
pour rester lisibles et ne pas déborder de la page.

---

#Breakpoints utilisés

-max-width : **700px** 
    Pour mobile (smartphones)

-AU delà de : **700px** 
    Tablettes et desktop


---

#Principales modifications apportées au layout

##De base
-Les éléments **html** et **body** prennent une height: 100%
afin d'occuper la totalité de la hauteur de la page
-L'élément **body** prend :
     *display: flex*
     *flex-direction: column*
     *min-height: 100vh*
Afin qu'il devienne un conteneur vertical et qu'il puisse 
s'adapter à la hauteur de l'écran.
-Le **main**, lui, prend un *flex: 1*, afin de prendre toutes
l'espace nécessaire entre le header et le footer.

##En dessous de 700px (mobile)
-La **NAV latérale** passe en *display:none* pour
ne pas empiéter sur le contenu
-Les **éléments de la section Services** passent
de **flex-direction: row** à **flex-direction: column**, s'affichant
les uns en dessous des autres
-Les conteneurs utilisent width: *100%* pour occuper toute
la largeur de l'écran
-Centrage de l'ensemble des titres de chaque sections.

##Au-delà de 700px (Tablette/Desktop)
-La **NAV** est visible et positionnée sur le côté gauche de l'écran
-Les **cards de services** s'affichent en ligne côte à côte
-Le layout global utilise **Flexbox** pour aligner le contenu 
principal et la navigation.

---

##Wen Joanel | École{241}










