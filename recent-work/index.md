---
title: Recent work
title_key: recent_work_title
nav:
  order: 4
permalink: /recent-work/
redirect_from:
  - /recent-work
---

# <span data-i18n="recent_work_title">Recent work</span>

<span data-i18n="recent_work_intro_1">This page highlights selected recent work from the lab, spanning brain-inspired computing, neuromorphic intelligence, and related research directions.</span>

<span data-i18n="recent_work_intro_2">It offers a concise overview of our recent research efforts and representative results.</span>

{% include project-tags.html data="recent_works" %}

{% for project in site.data.recent_works %}
    {% include project-card.html project=project %}
{% endfor %}

{% capture content %}
<span data-i18n="recent_work_more_info">For the complete publication list, visit our <a href="/papers/">publications page</a>.</span>
{% endcapture %}

{% include more-info.html
  content=content
  icon="fa-solid fa-file-lines"
  color="#0A66C2"
%}
