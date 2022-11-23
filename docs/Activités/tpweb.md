# TP Web

Consigne : Travail en **binôme**, ou en **trinôme** s'il y a un nombre impair d'élèves. Rédigez un document texte avec le logiciel LibreOffice Writer que vous sauvegarderez sous la forme `SNT_TPWeb_nom1_nom2.odt` dans votre dossier SNT. Il doit contenir les réponses aux différentes questions et des captures d'écrans (si 📸) des différentes pages Web que vous allez créer :)


## 1. Le langage HTML

Pour rappel, le langage HTML (*HyperText Markup Language*) définit la structure et le contenu des pages web. Il permet de créer tous les paragraphes, les titres, les listes, les images et les liens qui composent une page Web typique.

## 2. Elements et balises

Un **élément** d'une page HTML sont entourés de **balises** **ouvrantes** et **fermantes** (sauf exception). On distingue des **balises ouvrantes**, qui indiquent le début de la portion de page web à délimiter, et des **balises fermantes**, qui en indiquent la fin. Les balises ouvrantes sont toujours de la forme `#!html <exemple>` et les balises fermantes de la forme `#!html </exemple>` où `exemple` indique le nom de la balise.

Par exemple, un paragraphe s'écrit en HTML avec la balise prédéfinie `p` :

```html
<p>Un peu de texte</p>
```

Le navigateur Web peut ensuite utiliser ces informations pour déterminer comment il doit interpréter et formater visuellement le contenu.

## 3. Votre première page Web

Vous en savez suffisamenent pour créer votre premier site Web !

1. Dans votre espace personnel, dans le dossier SNT, créez un nouveau dossier `TP Web` qui contiendra par la suite tous les fichiers du TP.

2. Ouvrez le bloc-notes (ou votre éditeur de code préféré) et coller le code HTML suivant :

    ```html
    <!DOCTYPE html>
    <html lang="fr">
    </html>
    ```

3. Enregistrez le document au format `.html`. Pour cela, allez dans *Fichier > Enregistrer sous...* et dans la nouvelle fenêtre, définissez le *nom du fichier* comme `page.html` et son *type* comme `Tous les fichiers (*.*)`, car sinon il sera enregistré au format texte `.txt`.

4. Vous pouvez maintenant ouvrir le fichier avec votre Navigateur Web ! Rien ne s'affiche ? C'est parfait.

!!! info "Euh... ça signifie quoi ce bout de code HTML ?"
    * Chaque page HTML commence avec un
    déclaration *doctype* dont le but est de dire
    au navigateur Web quelle version du langage
    HTML il doit utiliser pour afficher le
    document. 
    * Après avoir déclarer le doctype, on doit
    fournir l'élement `#!html <html>` . C'est ce
    que l'on appelle l'*élément racine* du
    document, ce qui signifie que **tous** les
    autres éléments du document en seront des
    descendants (c'est-à-dire contenu entre la
    balise ouvrante `#!html <html>` et fermant
    `#!html </html>`)
    * `lang` est ce qu'on appelle un
    **attribut**. Les éléments HTML peuvent
    recevoir des attributs, c'est-à-dire des
    informations supplémentaires. Ici, on indique
    que la langue utilisée sera le français.

## 4. Donnons un titre à notre page !

Commençons par modifier le titre de votre page Web. Pour cela on va créer l'élement `#!html <head>` qui contiendra des méta-informations sur notre page Web. On utilisera alors l'élément `title` pour spécifier le titre de la page Web.

```html hl_lines="3 4 5"
<!DOCTYPE html>
<html lang="fr">
    <head>
        <title>Mon premier site Web</title>
    </head>
</html>
```
!!! Example "Questions"
    1. Enregistrez ce document et affichez-le dans un navigateur (réactualisez la page avec F5). Où s'affiche le titre de la page ?

## 5. Une page bien vide

L'élement final pour compléter la structure principale de notre page est l'élement `#!html <body>`. C'est entre ces balises que l'on définit le contenu de la page Web à proprement parler.

```html hl_lines="6 7"
<!DOCTYPE html>
<html lang="fr">
    <head>
        <title>Mon premier site Web</title>
    </head>
    <body>
    </body>
</html>
```

Par exemple, si l'on veut écrire un paragraphe :

```html hl_lines="7"
<!DOCTYPE html>
<html lang="fr">
    <head>
        <title>Mon premier site Web</title>
    </head>
    <body>
        <p>Bonjour tout le monde !</p>
    </body>
</html>
```

!!! Example "Questions"
    1. 📸 Copier ce code HTML. Qu'affiche le nagivateur Web ?


## 6. Les paragraphes

Pour comprendre l'interêt de l'élément `#!html <p>`, affichez ces deux pages Web :

    ```html
    <html>
        <body>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.

            Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
        </body>
    </html>
    ```

    ```html
    <html>
        <body>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>

            <p>Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
        </body>
    </html>
    ```

    !!! info "Et le doctype et l'élément head !?"
        Ils ne sont pas strictement obligatoires, on peut donc les omettre pour tester rapidement du code. Vous pouvez tout à fait les conserver !

1. Quelle est la différence notable ?

!!! Example "Questions"
    1. Quelle est la différence notable ?

## 7. Les titres

Les titres diffèrent des autres élements HTML textuels : ils sont généralement affichés en plus grand et en plus épais. Il y a 6 niveaux hiérarchiques de titres, de `#!html <h1>` à `#!html <h6>`. De la même manière que pour les paragraphes, pour créer un titre h1, on entoure le texte du titre entre des balises `#!html <h1>` et `#!html </h1>`.

```html hl_lines="3 4"
<html>
    <body>
        <h1>Ceci est un titre</h1>
        <h2>Ceci est un sous-titre ? Sûrement.</h2>

        <p>Et ceci est un paragraphe, juste en-dessous.</p>
    </body>
</html>
```

!!! info "Pourquoi h ?"
    Titre se dit *header* en anglais, d'où la lettre **h** comme nom de balise.

!!! Example "Questions"
    1. 📸 Créer une page HTML qui affiche des titres des 6 niveaux différents.
   
    2. Dans quel ordre d'importance sont classés les niveaux de titres ?

## 8. Un peu de formatage de texte

```html
<html>
    <body>
        <p>Le livre <em>Les Misérables</em> à été écrit par <strong>Victor Hugo</strong> en 1862.</p>
    </body>
</html>
```

!!! Example "Questions"
    1. Affichez cette page Web. Que permet de faire l'élement `#!html <em>` ?
   
    2. Idem pour l'élement `#!html <strong>` ?

## 9. Les listes

On va identifier deux types de listes `#!html <ul>` et `#!html <ol>` :

```html
<html>
    <body>
        Ma liste de course :
        <ul>
            <li>Pâtes</li>
            <li>Beurre</li>
            <li>Pomme</li>
        </ul>
    </body>
</html>
```

```html
<html>
    <body>
        Mon top 3 de plats d'hiver :
        <ol>
            <li>La tartiflette</li>
            <li>La raclette</li>
            <li>La carbonade flamande</li>
        </ol>
    </body>
</html>
```



!!! info "Je suis perdu avec les noms de balises  👉👈"
    Ce n'est pas à apprendre par coeur évidemment, une petite recherche Google permet de rapidement retrouver la syntaxe.

    * `#!html <ul>` est l'acronyme de *unordered list* ou liste non-ordonnée.

    * `#!html <ol>` est l'acronyme de *ordered list* ou liste ordonnée.

    * `#!html <li>`est l'acronyme de *list item* ou élément de liste.

!!! Example "Questions"

    1. Affichez ces pages HTML. Quel est la différence notable entre une liste `#!html <ul>` et `#!html <ol>` ?

    2. 📸 Dans une même page Web, créez les listes suivantes :
       
        * Une liste non-ordonnée des 5 lieux que vous voulez vister un jour.

        * Une liste ordonnée de vos 5 films préférés.

## 10. Les ancres

Pour créer un lien en HTML, on utilise un élément d'ancrage `#!html <a>` (ou *anchor* en anglais). On peut soit entourer du texte avec, soit d'autres éléments HTML.

```html hl_lines="3"
<html>
    <body>
        <a>Cliquez-moi !</a>
    </body>
</html>
```

Si vous affichez ce code, vous remarquerez que cliquer sur le lien ne fait absolument rien. C'est parce que l'élément d'ancrage ne sait pas où aller ! On doit alors spécifier la destination de ce lien par un **attribut** HTML :

```html hl_lines="3"
<html>
    <body>
        <a href="http://arthurrouquan.github.io/SNT/">Cliquez-moi !</a>
    </body>
</html>
```

Il convient de noter que vous pouvez utiliser des balises d'ancrage pour créer des liens vers n'importe quel type de ressource sur Internet, et pas seulement vers d'autres documents HTML. Vous pouvez créer des liens vers des vidéos, des fichiers PDF, des images, etc.

## 11. Les liens

En général, il y a deux types de liens que nous allons créer :

* Les liens vers des pages situées sur d'autres sites Web sur l'Internet

* Liens vers des pages situées sur notre propre site Web 

### Liens absolus

Les liens vers des pages d'autres sites Web sur l'internet sont appelés **liens absolus**. Un lien absolu typique se compose des éléments suivants : `protocole://nom_de_domaine/chemin`.

### Liens relatifs

Les liens vers d'autres pages de notre propre site sont appelés **liens relatifs**. Ils n'incluent pas le nom de domaine, puisqu'il s'agit d'une autre page du même site. C'est-à-dire que ces pages sont stockées au même endroit, on y accède grâce à un simple chemin.

!!! Example "Questions"
    1. Dans le dernier code HTML de la section 10. L'élément d'ancrage dirige-t-il vers un lien absolu ou vers un lien relatif ?

    2. Créer `page.html` :
   
    ```html hl_lines="8"
    <!DOCTYPE html>
    <html lang="fr">
        <head>
            <title>Première page</title>
        </head>

        <body>
            <a href="page2.html">Seconde page</a>
        </body>
    </html>
    ```

    3. Et une seconde page `page2.html` avec un titre et un peu de texte.

    4. Que se pass-t-il quand on clique sur le lien de `page.html` ? Est-ce un lien relatif ou absolu ?

## 12. Les images

Pour insérer une image, on utilise l'élément `#!html img` qui ne possède pas de balise fermante ! On spécifie le lien vers une image grâce à l'attribut `src` (source) :

```html
<img src="https://lwm-a1.azureedge.net/uploads/2021/11/illegally-smol-kittens-1-Copy-900x1200.jpg">
```

!!! Example "Questions"

    1. Dans cet exemple, l'attribut `src` est un lien absolu ou relatif ?

    1. Insérer ce code HTML dans un élement `#!html <body>`. Qu'affiche cette image ?

    2. Créer un dossier `images` dans le dossier contenant votre site. Y ajouter la précédente image. Réecrire alors l'attribut `src` en utilisant un lien relatif pour accèder cette image stockée sur votre machine.


## Le projet : Une recette de cuisine 

On se propose de réaliser un petit site Web de cuisine. Miam.

### Itération 1 : Structure Initiale

1. Dans un nouveau dossier `mes_recettes`, créer un fichier `index.html`.

2. Le remplir minimalement (doctype, section head, body) et y ajouter un titre `#!html h1` "Mes recettes de cuisine".

### Itération 2 : Page d'une recette

3. Créer un nouveau dossier `recettes` qui contiendra les pages HTML des différentes recettes.

4. Créer un nouveau fichier HTML dans ce nouveau dossier et nommez-le d'après une recette de cuisine. Comme par exemple, `lasagne.html`. (vous pouvez utiliser le nom de votre plat préféré !)

5. Pour l'instant, ajouter un titre `#!html h1` avec le nom de la recette comme contenu.

6. De retour au fichier `index.html`, ajouter un lien vers la page de recette que vous venez de créer. Par exemple, vous devriez avoir quelque chose comme :

```html
<h1>Mes recettes de cuisine</h1>
<a href="recettes/nom_de_la_recette.html">Titre de la recette</a>
```

### Itération 3 : Remplir la page de recette

La page de votre recette doit avoir le contenu suivant

1. Sous le titre `#!html h1`, insérer une **image** de la recette (lien absolu ou relatif).

2. Sous l'image, il doit comporter un **titre** "Description" de taille appropriée, suivie d'un **paragraphe** ou deux décrivant la recette.

3. Sous la description, ajoutez un titre "Ingrédients" suivi d'une **liste non ordonnée** des ingrédients nécessaires à la recette.

4. Enfin, sous la liste des ingrédients, ajoutez une rubrique "Étapes" suivie d'une liste ordonnée des étapes nécessaires à la réalisation du plat.


### Itération 4 : Ajouter plus de recettes

1. Ajoutez deux autres recettes avec des structures de page identiques à la page de recette que vous avez déjà créée.

2. N'oubliez pas de créer un lien vers les nouvelles recettes sur la page d'index. Pensez également à placer tous les liens dans une liste non ordonnée afin qu'ils ne soient pas tous sur une seule ligne.

```html
<ul>
    <li><a href="recettes/nom_de_la_recette1.html">Titre de la recette 1</a></li>
    <li><a href="recettes/nom_de_la_recette2.html">Titre de la recette 2</a></li>
    <li><a href="recettes/nom_de_la_recette3.html">Titre de la recette 3</a></li>
</ul>
```

### Itération 5 : M'envoyer le site

Compresser le dossier `mes_recettes` et me l'envoyer sur le Google Classroom !