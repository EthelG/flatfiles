---
---
#### Le fichier data et .yml

* création d'un fichier "members.yml" avec :  

        - nom: Ethel GAUDIN  
          hobbies: Jeux vidéos  
          cursus: Graphisme  
          motivation: Devenir un chat  
          avatar: ../assets/img/favicon/favicon.icon  

* boucles dans le fichier "equipe.md" avec :  

        {% for member in site.data.members %}  
          Nom : {{ member.nom }}  
          Hobbies : {{ member.hobbies }}  
          Cursus : {{ member.cursus }}  
          Motivation : {{ member.motivation }}  
          Avatar :  
          ![avatar]({{ member.avatar }})
        {% endfor %}
        
* avec un fichier JSON :

        {% for club in site.data.club %}
        {% for clubs in club[1] %}
          {{ clubs.name }}
        {% endfor %}
        {% endfor %}