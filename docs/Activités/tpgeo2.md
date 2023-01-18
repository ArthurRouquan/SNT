# TP Les systèmes de positionnement

Pour se repérer lors d’une randonnée, pour trouver son chemin avec les transports en commun, pour repérer un bateau en mer, pour calculer un itinéraire en voiture etc. on utilise souvent une application couplée au **système GPS** (et bientôt à Galiléo). Ce système de géolocalisation par satellites permet de repérer un objet appelé « récepteur » et d’indiquer sa position sur une carte.


## Repérer un point en 2D


<figure markdown>
![](images/treasure.png){ width="200px" }
</figure>


Pour comprendre	le principe	de géolocalisation	d’un point sur Terre par un ensemble de satellites, commençons par une petite énigme.

On cherche à localiser un trésor en France. Pour cela, nous avons 4 informations, nous savons qu'il se situe à :

* 260 km de Nantes

* 340 km de Paris

* 328 km de Dijon

* 178 km de Bordeaux

!!! Example "Questions"
    
    Q1. Compléter la phrase suivante : "Si le trésor se situe à 260 km de Nantes, alors il se situe sur un ... de centre ... et de rayon ... ".

    Q2. Sur [cette carte de France](https://www.geogebra.org/calculator/yx4tdepn), ajoutez les 4 cercles correspondant aux informations. Pour créer un cercle, on se rend dans l'onglet **Algèbre**, puis dans le champ **Saisie** on écrit par exemple `Cercle(Nantes, 260)`. Pouf, le cercle apparaît !

    Q3. Dans quelle ville se situe le trésor ?

    Q4. Combien **au minimum** faut-il d'informations pour situer avec certitude le trésor ?


La géolocalisation par satellite fonctionne à l’aide d’un principe similaire appelé la **trilatération**. C'est un principe proche de la triangulation en cherchant à connaître la distance d’un récepteur par rapport à 3 satellites (ou plutôt 4 satellites, voir la suite) dont on connaît la position.


## Les systèmes de positionnement

<figure markdown>
  ![](images/tri.png){ width="300px" }
</figure>


Le *Global Positioning System* (GPS) est un système de positionnement par satellites appartenant aux États-Unis, achevé en 1995 avec un total de 24 satellites. L'Europe s'est dotée d'une technologie similaire, **Galileo**, qui sera pleinement opérationnelle d'ici 2024.


A l'aide de [cette vidéo](https://youtu.be/e79tSIpLiDk), répondre aux questions suivantes.

!!! Example "Questions"
    
    Q5. Quel est l'intérêt de diposer d'une grande quantité de satellites pour un système de positionnement ?

    Q6. Qui détermine la position de Lucas ? Le satellite ou son téléphone ?

    Q7. Quelle information envoie un satellite ? Est-ce une information disponible que pour Lucas ?

    Q8. Pourquoi un quatrième satellite ?

    Q9. Un signal émis à 18 h 35 min 24.525800 s est capté par un récepteur Galileo à 18 h 35 min 24.593650 s. A quelle distance du satellite se trouve le récepteur ? La vitesse du signal est celui de la lumière, environ 300 000 km/s.

    Q10. Aïe ! Un des satellites de Galileo a un retard de 0.001 ms ! De combien est l'erreur de distance calculée par un récepteur ?

Regardez ensuite [cette vidéo](https://www.youtube.com/watch?v=V51dGqHw_24) qui rentre un peu plus dans les détails !

!!! note "Et Einstein dans tout ça ?"

    Comme vous l'avez constaté par le calcul, le GPS (ou Galileo) nécessite une précision effroyable sur les durées. Or cette précision est soumise à des phénomènes relativistes (expliqués par les théories d'Einstein). Il y en a deux principaux :

    * Le premier est dû à la **vitesse de déplacement très grande des satellites** (14 000 km/h) : leurs référentiels de temps et d’espace sont différents du nôtre (sur Terre). Leurs horloges sont ainsi retardées de 7 µs par jour.

    * Le second provient la différence dans **le champ gravitationnel terrestre** auquel les satellites sont soumis, du fait de leur altitude élevée (20 200 km). La relativité implique que l’écoulement du temps est accéléré si le champ gravitationnel diminue. On parle ici de 45 µs.

    Ces deux effets cumulés produisent donc un décalage de 38 µs quotidiennement. Ça semble peu, mais ça suffit à induire une erreur sur la position du satellite supérieure à 11 km.

!!! Example "Questions"
    Q11. Citer 5 systèmes de positionnement.

    Q12. Le GPS a-t-il besoin d'une connexion internet ?

    Q13. En conclusion, expliquer le fonctionnement du GPS en quelques lignes. Comme si vous l'expliquiez à votre grand-mère, pourquoi pas.

## Attention, vous êtes suivis.

<figure markdown>
![](images/maps.webp){ width="350px" }
</figure>

Connectez-vous à votre compte Google du quotidien et accèder à [l'adresse suivante pour accéder à votre historique des positions]( https://www.google.com/maps/timeline).


!!! Example "Questions"
    Q14. Que fait Google de vos données GPS ? 

    Q15. A votre avis pourquoi Google conserve de telles données ?

    Il est possible de désactiver l'historique des positions sur ce même site. 


## Les données EXIF d'une photo

EXIF signifie "Exchangeable Image File Format". C'est un type de fichier utilisé pour enregistrer des informations sur une photo numérique, comme la date de prise de vue, la résolution, la marque et le modèle de l'appareil photo, et d'autres détails. **Cette information est enregistrée dans le fichier image lui-même**, ce qui signifie qu'elle est disponible chaque fois que l'image est ouverte, même si elle est transférée à d'autres personnes ou utilisée sur un autre appareil.

On souhaite justement localiser cette photo que j'ai prise en Décembre :

<figure markdown>
  ![](images/photo.jpg){ width="350px" }
</figure>

Pour cela, on utilisera [ce site web](https://jimpl.com/) pour extraire ces métadonnées.

!!! warning "Faites attention à ce que vous téléversez"
    Le site utilisé pour déterminer les données EXIF conserve les images téléversées pendant 24 heures, c'est une promesse hélas invérifiable. Pour plus de sécurité, il faudrait utiliser un logiciel open-source qui fonctionne sans Internet.


!!! Example "Questions"
    Q16. Quelles sont les coordonnées géographiques de cette photo (au format degrés, minutes, secondes) ?

    Q17. Quel est le bâtiment sur cette photo ?

    Q18. Un petit malin en 2011 a eu la brillante idée de faire fuiter le sujet de maths du bac de 2011. Voici la photo qu'il a partagée en ligne :

    <figure markdown>
    ![](images/bac.jpg){ width="350px" }
    </figure>

    Aidez les forces de police à retrouver ce chenapan !


On retient que lorsque vous partagez directement votre photo .jpg à quelqu'un, sans supprimer les métadonnées, il peut alors s'en servir à des fins malveillantes. La plupart des messageries en ligne les retirent automatiquement par mesure de sécurité, il ne faut pas hésiter à explorer les paramètres de l'application pour bien spécifier ce comportement.