---
layout: page
title: Equipe
navigation_weight: 2
---

{% for member in site.data.members %}  
  Nom : {{ member.nom }}  
  Hobbies : {{ member.hobbies }}  
  Cursus : {{ member.cursus }}  
  Motivation : {{ member.motivation }}  
  Avatar :  
  ![avatar]({{ member.avatar }})  
  Footballteam :  
  {% for club in site.data.club %}
    {% assign.footballteam= {{ member.footballteam }} %}
    {% assign.clubs= club[1]|where:key,footballteam %}
    {% for clubo in club[1] %}
      {{ clubo.name }}
    {% endfor %}
  {% endfor %}
{% endfor %}

    Noms des clubs :
    {% for club in site.data.club %}
    {% for clubs in club[1] %}
      {{ clubs.name }}
    {% endfor %}
    {% endfor %}