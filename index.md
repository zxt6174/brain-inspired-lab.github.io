---
redirect_from:
  - home/
  - cive60008_21/
  - cive60008_21/week01/seminar1/
  - cive60008_22/
  - cive60008_22/assignments/1/
  - cive60008_22/assignments/2/
  - cive60008_22/week01/notebooks/
  - cive60008_22/week02/notebooks/
  - cive60008_22/week03/notebooks/
  - cive60008_22/week04/notebooks/
  - cive60008_22/week05/notebooks/
  - cive60008_22/week06/notebooks/
  - cive60008_22/week07/notebooks/
  - cive60008_22/week08/notebooks/
  - cive60008_22/week09/notebooks/
  - cive97129_23/assignments/1/
  - cive97129_23/assignments/2/
  - demo-pathfinding/
  - project/shift-project/
  - research/autonomy/
  - research/logistics/
  - tags/
  - tag/autonomy
  - teaching/
  - tf/
  - tf/60008_21/
  - wsds/
---


<span data-i18n="home_1">The **Brain-Inspired Laboratory** at **Peking University** focuses on brain-inspired computing,spiking neural networks ,computational neuroscience and ai4science.</span>
<span data-i18n="home_2">Our group is led by [**Zhaofei Yu**](/members/zhaofei-yu), and is affiliated with the **College of Artificial Intelligence**.</span>

{% include section.html %}

#### <span data-i18n="home_5">Research Areas</span>

{% include theme-carousel.html %}


{% include section.html %}

#### <span data-i18n="recent_work_title">Recent work</span>
{% include project-carousel.html data="recent_works" %}

{% include section.html %}


#### <span data-i18n="home_6">Our publications</span>

{% assign home_featured_papers = site.data.citations | data_filter: "group: featured" | sort: "date" | reverse %}
{% if home_featured_papers.size == 0 %}
{% assign home_featured_papers = site.data.citations | sort: "date" | reverse %}
{% endif %}
{% for paper in home_featured_papers limit:2 %}
{% include citation.html lookup=paper.id %}
{% endfor %}

{%
  include button.html
  link="papers"
  text='<span data-i18n="home_button_2">"All publications"</span>'
  icon="fa-solid fa-arrow-right"
  flip=true
  style="bare"
%}


{% capture text_team %}

<span data-i18n="home_7">Our laboratory is an academic community rooted in **freedom and inclusivity**, driven by **unity and innovation**. From the spark of inspiration to scientific breakthroughs, we always stand side by side.</span>

<span data-i18n="home_8">Backed by first-class research capabilities, we delve into cutting-edge fields, equipped with top-tier experimental facilities and academic resources to provide a solid foundation for exploring the unknown. Leveraging extensive social connections and international cooperation networks, we break down geographical and disciplinary boundaries, enabling students to deeply participate in transnational research projects, engage with world-leading scholars, and grasp the pulse of academic frontiers from a global perspective.</span>

<!-- Regardless of your background or academic aspirations, we welcome you with an equal and open attitude. Here, your **potential will be unlocked**, and your **talents will be cherished**—let us jointly write our own chapter of innovation in the vast ocean of scientific research. -->

<span data-i18n="home_9">If you are interested, please feel free to contact us and join this academic journey!</span>

{%
  include button.html
  link="team"
  text='<span data-i18n="home_button_3">"Meet our team"</span>'
  icon="fa-solid fa-arrow-right"
  flip=true
  style="bare"
%}

{%
  include button.html
  link="apply"
  text='<span data-i18n="home_button_4">"Join us"</span>'
  icon="fa-solid fa-arrow-right"
  flip=true
  style="bare"
%}

{% endcapture %}

{% include section.html %}

{%
  include feature.html
  image="images/team/team.jpg"
  link="team"
  title='<span data-i18n="home_team_title">Our team</span>'
  style="bare"
  text=text_team
%}




{% include section.html %}

#### <span data-i18n="home_10">Our funders</span>


{% capture col1 %}
<img src="images/funders/NERC.jpg">
{% endcapture %}

{% capture col2 %}
<img src="images/funders/pku_cs.png">
{% endcapture %}

{% capture col3 %}
<img src="images/funders/pku_ai.png">
{% endcapture %}


{% include cols.html col1=col1 col2=col2 col3=col3%}
