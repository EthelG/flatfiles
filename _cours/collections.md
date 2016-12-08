---
---
#### Les collections

* Dans config :  

        collections:
          cours:
            output: true
            
        defaults: //pour rajouter les layout
  
            scope:
              layout: page
        
* Dans footer :  
        {% for cour in site.cours %}
        <li>
            <img src="{{ cour.thumbnail-path }}" alt="{{ cour.title }}"/>
            <a href="{{ cour.url }}">{{ cour.title }}</a>
            <p>{{ cour.short-description }}</p>
        </li>
        {% endfor %}
        
* Et dans les fichiers .md :  

        ---
        ---

Pour appeler un style css sur toutes les pages, posts, etc :  

        href="{{ site.baseurl }}/assets/css/style.css"