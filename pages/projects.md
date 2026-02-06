---
layout: projects
title: Projects
subtitle: Research Projects that engage with different aspects of digital sustainability

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
    <h3 style="text-align:left; margin:40px">Ongoing Projects</h3>
       {% for project in site.data.projects %}
        {% if project.status == "current"%}
        <div class="shinyapp">
            <a class="applink" href="{{ project.url }}" target="_blank">
              <img class="appimg" src="{{ site.url }}/assets/img/project-screenshots/{{ project.img }}" alt="" />
              <div class="apptitle">{{ project.title }}</div>
              <div class="appdesc">{{ project.description }}</div>
            </a>
          </div>
          {% endif %}
	  {% endfor %}
    </div>
    <div id="shinyapps-big">
    <hr>
      <h3 style="text-align:left; margin:40px">Past Projects</h3>
      <ul>
        {% for project in site.data.projects %}
          {% if project.status == "past"%}
          <div style="text-align:left; margin-left:40px">
                  <li><a href="{{ project.url }}" target="_blank">
                <div class="apptitle">{{ project.title }}</div>
              </a></li>
            </div>
          {% endif %}
        {% endfor %}
      </ul>
    </div>
  </div>
</div>
