---
---
#### Cours sur les boucles Jekyll :  
Faire une boucle sur une nav :  
* ajouter un titre à toutes les pages à ajouter
* ajouter "navigation_weight: (la place numérique de la page dans la nav)" ou ajouter 01.(nomdufichier), etc
* ajouter dans le header :  
        {% assign navigation_pages = site.html_pages | sort: 'navigation_weight' %}
        {% for p in navigation_pages %}
          {% if p.navigation_weight %}
            <li>
              <a href="{{ p.url }}" {% if p.url == page.url %}class="active"{% endif %}>
                {{ p.title }}
              </a>
            </li>
          {% endif %}
        {% endfor %} <!--boucle-->
        
Faire une boucle pour appeler des articles :  

        {% for post in site.posts %}
          <li>
            <a href="{{ post.url }}">{{ post.title }}</a>
          </li>
        {% endfor %}