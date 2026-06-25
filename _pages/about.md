---
permalink: /
title: "Sitong Zhou"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a PhD candidate in the [Electrical & Computer Engineering department](https://www.ece.uw.edu/) at the University of Washington, advised by [Prof. Mari Ostendorf](https://people.ece.uw.edu/ostendorf/) and [Prof. Meliha Yetisgen](https://faculty.washington.edu/melihay/). My research focuses on natural language processing (NLP) applied to clinical text, including information extraction from electronic health records, clinical timeline summarization, and disease prediction.

**Research Interests:** Clinical NLP, information extraction from unstructured EHRs, disease prediction, longitudinal patient modeling, and large language models applied to healthcare.


## Publications 

{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}

{% include base_path %}

{% if site.publication_category %}
  {% for category in site.publication_category %}
    {% assign title_shown = false %}
    {% for post in site.publications reversed %}
      {% if post.category != category[0] %}
        {% continue %}
      {% endif %}
      {% unless title_shown %}
        <h3>{{ category[1].title }}</h3><hr />
        {% assign title_shown = true %}
      {% endunless %}
      {% include archive-single.html %}
    {% endfor %}
  {% endfor %}
{% else %}
  {% for post in site.publications reversed %}
    {% include archive-single.html %}
  {% endfor %}
{% endif %}
