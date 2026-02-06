---
layout: labs
title: Labs
subtitle: Our long-term collaborations
description: Labs are funded by external companies. They provide structure for their strategic collaboration with DiSC researchers and young talents, for PhD research and Master-level research.
css:
- /assets/css/index.css
ext-css:
- //fonts.googleapis.com/css?family=Roboto:400,700
ext-js:
- //cdn.jsdelivr.net/npm/particles.js@2.0.0/particles.min.js
---

<div id="portfolio-out">
  <div id="portfolio" style="text-align:left; padding:40px;">
    <div id="shinyapps-big"> 
      {% for lab in site.data.labs %}
       {% if lab.status == "current"%}
	    <div class="shinyapp" style="background-color:#e6ffe7; margin-top:10px; ">
          <a class="applink" href="{{ lab.url }}" target="_blank">
            <img src="{{ site.url }}/assets/img/lab-screenshots/{{ lab.img }}" alt="" />
            <div class="apptitle">{{ lab.title }}</div>
            <div class="appdesc">{{ lab.description }}</div>
            <!-- <div class="appdesc">{{ lab.details }}</div> -->
            <div class="appdesc">{{ lab.contact }}</div>
          </a>
        </div>
        {% endif %}
	  {% endfor %}
    </div>
    <div style="text-align:left; margin-bottom:40px;">
    <h3 style="text-align:left; margin-left:40px; padding-top:10px; padding-bottom:10px;">Past Labs</h3>
      {% for lab in site.data.labs %}
        {% if lab.status == "past"%}
            <div class="shinyapp" style="text-align:left; margin-left:40px; margin-top:10px;margin-bottom:10px;">
                <a href="{{ lab.url }}" target="_blank">
                  <div class="apptitle">{{ lab.title }}</div>
                </a>
          </div>
        {% endif %}
	  {% endfor %}
    </div>
  </div>
</div>
