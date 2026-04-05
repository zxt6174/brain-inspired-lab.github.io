---
lang: en
title: Team
title_key: team_title
nav:
  order: 2
redirect_from: 
  - people
  - author
---

<div class="team-leaders-grid">
  <!-- Zhaofei Yu -->
  <div class="team-leader-card">
    <h1>
      <a class="team-leader-title-link" href="/members/zhaofei-yu.html">
        <span data-i18n="Supervisor">Principle Investigator</span>
      </a>
    </h1>
    
    <div class="leader-content">
      <div class="leader-image">
        <a class="team-leader-photo-link" href="/members/zhaofei-yu.html">
          <img src="/images/team/zhaofei-yu.jpeg"
               class="portrait-image"
               alt="Zhaofei Yu" />
        </a>
        
        <div class="team-leader-name"><span data-i18n="Zhaofei Yu name">Zhaofei Yu</span></div>
        <div class="team-leader-role"><span data-i18n="Supervisor">Assistant Professor</span></div>
      </div>
      
      <div class="leader-info">
        {% assign member = site.members | where: "slug", "zhaofei-yu" | first %}
        <ul class="team-leader-affiliations">
          {% for affiliation in member.affiliations %}
          <li>{{ affiliation }}</li>
          {% endfor %}
        </ul>
        
        <p class="team-leader-summary">
          <span data-i18n="Zhaofei Yu summary">Zhaofei Yu is the supervisor of the lab. His research interests include SNN and brain-inspired intelligence.</span>
        </p>
        <a class="team-leader-more" href="/members/zhaofei-yu.html"><span data-i18n="more">(more)</span></a>
      </div>
    </div>
  </div>
</div>


{% include section.html %}

# <span data-i18n="team_title">Team</span>

{% include list.html data="members" component="portrait" filters="role: senior" %}
{% include list.html data="members" component="portrait" filters="role: ^(?!pi$|senior$|assistant-professor|alumni$)" %}

{% include section.html %}

# <span data-i18n="alumni_title">Graduated Students</span>

{% include list.html data="members" component="portrait" filters="role: alumni" %}

{% include section.html dark="gray" %}

 <span data-i18n="alumni_1">We are looking for highly motivated students to join our group. Our group has opening positions for Ph.D. and Undergraduate Internship. If you are interested in researching on brain-like computing, please send me an email with your CV.</span>

 <span data-i18n="alumni_2">We are hiring highly motivated postdocs to join our group through the Boya Postdoctoral Fellowship at Peking University. Please send an email with your CV and Research Statement.</span>

 
 <span data-i18n="alumni_3">For more information on how to join us, you can review our [recruitment](/apply/) page. </span>

{% include section.html %}

{% capture content %}
<!-- 
{% include figure.html image="images/photos/itsc.jpg" %}
{% include figure.html image="images/photos/dinner.jpg" %}
{% include figure.html image="images/photos/trb.jpg" %} -->

{% endcapture %}

{% include grid.html style="square" content=content %}
