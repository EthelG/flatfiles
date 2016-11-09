# flatfiles
#### Cours sur le Git :  
* récuperer un file dans GitHub -> git clone ...(URL)  
* synchroniser des fichiers :
    * git init (flatfiles)
    * git add ... (nom du fichier à ajouter)
    * git commit - "message" (correspond au changements apportés)
    * git status
    * git push (-u origin master)

#### Cours sur Jekyll :  
* layout: squelette de la page sans contenu
* includes: diviser la pages en plusieurs parties et les inclure dans la page
* index.md: seulement le contenu de la page  
* config.yml: base de donnée  


* _nomdufichier n'est pas génerer par Jekyll

http://jekyllrb.com/

#### Cours sur les boucles Jekyll :  
Faire une boucle sur une nav :  
* ajouter un titre à toutes les pages à ajouter
* ajouter "navigation_weight: (la place numérique de la page dans la nav)" ou ajouter 01.(nomdufichier), etc
* ajouter dans le header :  
    * dans le ul :   
        {% assign navigation_pages = site.html_pages | sort: 'navigation_weight' %}  
        {% for p in navigation_pages %}  
        {% if p.navigation_weight %}  
    * dans le a de li :  
        href="{{ p.url }}" {% if p.url == page.url %}class="active"{% endif %}>  
        {{ p.title }}  
    * après le li :  
        {% endif %}  
        {% endfor %}  
        
Faire une boucle pour appeler des articles :
* avant le li : {% for post in site.posts %}
* dans le a href : "{{ post.url }}">{{ post.title }}
* après le li : {% endfor %}