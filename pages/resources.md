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
      <div class="shinyapp" style="width: 300px;height:460px;text-align: center; overflow: hidden;">
        <a class="applink" href="{{ resource.url }}" target="_blank" style="display: block; text-decoration: none; color: inherit;">
          <img class="appimg" src="{{ site.url }}/assets/img/resource-screenshots/{{ resource.img }}" 
              alt="" 
              style="width: 100%; height: 300px; object-fit: contain;" />
          <div class="apptitle" 
              style="font-weight: bold; font-size: 16px; white-space: nowrap; overflow: hidden; text-overflow: ellipsis; max-width: 100%;">
            {{ resource.title }}
          </div>
          <div class="appdesc" 
              style="font-size: 14px; max-height: 6em; overflow: hidden; text-overflow: ellipsis; display: -webkit-box; -webkit-line-clamp: 4; -webkit-box-orient: vertical;">
            {{ resource.description }}
          </div>
        </a>
      </div>
	  {% endfor %}
    </div>
  </div>
</div>
