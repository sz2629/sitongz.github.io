---
permalink: /
title: "Sitong Zhou"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I recently completed my PhD in [Electrical & Computer Engineering department](https://www.ece.uw.edu/) at the University of Washington, honored to be advised by [Prof. Mari Ostendorf](https://people.ece.uw.edu/ostendorf/) and [Prof. Meliha Yetisgen](https://faculty.washington.edu/melihay/). 
I build language model applications for understanding and using clinical texts. My thesis focuses on building **robust** and **trustworthy** tools to **extract clinical information** and on using signals from unstructured EHRs for **disease prediction**. 
I'm particularly fascinated by the longitudinal nature of EHRs, and have worked on **longitudinal EHR summarization** and using patients' longitudinal history to  future **predict clinical outcomes**.

## Publications



{% include base_path %}

{% assign sorted_pubs = site.publications | sort: 'date' | reverse %} {% for post in sorted_pubs %}

**{% if post.paperurl and post.paperurl != '' %}[{{ post.title }}]({{ post.paperurl }}){% else %}{{ post.title }}{% endif %}**  
{% if post.authors %}{{ post.authors | markdownify | remove: '

' | remove: '

' | strip }}{% endif %}  
{{ post.venue }}.



 {% endfor %}