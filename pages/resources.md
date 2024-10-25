---
layout: labs
title: Resources
subtitle: Some highlights of results we share
css:
- /assets/css/index.css
ext-css:
- //fonts.googleapis.com/css?family=Roboto:400,700
ext-js:
- //cdn.jsdelivr.net/npm/particles.js@2.0.0/particles.min.js
---

<div id="portfolio-out" class="page-section grey-section">
  <div id="portfolio">
    <div id="shinyapps-big">
      {% for resource in site.data.resources %}
	    <div class="shinyapp" style="width:300px">
          <a class="applink" href="{{ resource.url }}" target="_blank" >
            <img class="appimg" src="{{ site.url }}/assets/img/resource-screenshots/{{ resource.img }}" style="width: 100%" alt="" />
            <div class="apptitle">{{ resource.title }}</div>
            <div class="appdesc">{{ resource.description}}</div>
          </a>
        </div>
	  {% endfor %}
    </div>
  </div>
</div>
