---
permalink: /
title: "Sitong Zhou"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a PhD candidate in the [Electrical & Computer Engineering department](https://www.ece.uw.edu/) at the University of Washington, advised by [Prof. Mari Ostendorf](https://people.ece.uw.edu/ostendorf/) and [Prof. Meliha Yetisgen](https://faculty.washington.edu/melihay/). My research focuses on natural language processing (NLP) applied to clinical text, including information extraction from electronic health records, clinical timeline summarization, and disease prediction.

## Education

- **PhD, Electrical & Computer Engineering** — University of Washington, Seattle (2019–2026)
- **MS, Data Science** — Columbia University, New York City (2016–2017)
- **BS, Mathematics & Economics** — Hong Kong University of Science and Technology (2012–2016)
  - Exchange at École Polytechnique Fédérale de Lausanne (EPFL)

## Research Interests

Clinical NLP, information extraction from unstructured EHRs, disease prediction, longitudinal patient modeling, and large language models applied to healthcare.

## News

- **2026**: Dissertation defense — *Extracting Clinical Information From Unstructured EHRs Using Language Models, and Its Role in Disease Prediction*
- **2026**: Paper accepted at LREC 2026 — *RadTimeline: Timeline Summarization for Longitudinal Radiological Lung Findings*
- **2025**: Paper at NeurIPS 2025 GenAI4Health Workshop — *Traj-CoA: Patient Trajectory Modeling via Chain of Agents for Lung Cancer Risk Prediction*

---

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
