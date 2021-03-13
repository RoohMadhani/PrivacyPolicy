---
layout: default
---

{% for s in site.data.content %}
  <section>
    <div class="container">
        {% if s.h1 == 'yes' %}
            <h1>{{ s.section }}</h1>
        {% else %}    
            <h2>{{ s.section }}</h2>
        {% endif %}   
        {{ s.text | markdownify }}
    </div>
  </section>
{% endfor %}