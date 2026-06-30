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

<div class="publications-list">
{% assign sorted_pubs = site.publications | sort: 'date' | reverse %}
{% for post in sorted_pubs %}
  <p class="pub-entry">
    <strong>{% if post.paperurl and post.paperurl != '' %}<a href="{{ post.paperurl }}">{{ post.title }}</a>{% else %}{{ post.title }}{% endif %}</strong><br>
    {% if post.authors %}{{ post.authors | markdownify | remove: '<p>' | remove: '</p>' | strip }}{% endif %}<br>
    {{ post.venue }}.
  </p>
{% endfor %}
</div>
