---
title: Papers
title_key: papers_title
nav:
  order: 3
redirect_from: 
  - publications
  - research
  - research_highlights
  - publication_types/
  - publication-type/1/
  - publication-type/2/
  - publication-type/3/
  - publication-type/4/
  - publication-type/5/
  - publication-type/6/

---

# {% include icon.html icon="fa-solid fa-file-lines" %}<span data-i18n="papers_title">Publications</span>

<span data-i18n="papers_1">We primarily publish our research in the relevant IEEE Transactions titles.</span>

<span data-i18n="papers_2">Most of our recent work should be accessible on an Open Access basis. However, if you cannot locate a specific manuscript online, please feel free to contact us.</span>



{% include section.html %}

{% include search-box.html %}

{% include search-info.html %}

<div class="publication-filters" data-publication-filters>
  <label class="publication-filter">
    <span>Year</span>
    <select id="publication-year-filter" aria-label="Filter publications by year">
      <option value="">Select Year</option>
    </select>
  </label>

  <label class="publication-filter">
    <span>Venue</span>
    <select id="publication-venue-filter" aria-label="Filter publications by venue">
      <option value="">Select Venue</option>
    </select>
  </label>

  <label class="publication-filter">
    <span>Topic</span>
    <select id="publication-topic-filter" aria-label="Filter publications by topic">
      <option value="">Select Topic</option>
    </select>
  </label>

  <button type="button" class="publication-clear-button" id="publication-clear-filters">
    Clear
  </button>
</div>

{% include list.html data="citations" component="citation" style="publication-list" %}

{% capture content %}
<span data-i18n="papers_3">For a list of our research initiatives, visit our [projects page](/projects/).</span>
{% endcapture %}

{% include more-info.html 
  content=content 
  icon="fa-solid fa-flask" 
  color="#0A66C2" 
%}
