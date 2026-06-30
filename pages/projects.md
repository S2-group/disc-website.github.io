---
layout: projects
title: Projects
subtitle: Research Projects that engage with different aspects of digital sustainability

css:
- /assets/css/index.css
- /assets/css/custom.css

ext-css:
- //fonts.googleapis.com/css?family=Roboto:400,700
ext-js:
- //cdn.jsdelivr.net/npm/particles.js@2.0.0/particles.min.js
---
<script>
document.addEventListener("click", function (e) {
    if (e.target.classList.contains("read-more-link")) {
        e.preventDefault();

        const link = e.target;
        const card = link.closest(".appdesc");

        const preview = card.querySelector(".preview"); // element before link
        const more = card.querySelector(".more");        // hidden content

        // remove preview + link
        if (preview) preview.remove();
        link.remove();

        // show full content
        if (more) more.style.display = "block";

        console.log("Hello world");
    }
});
</script>
<div id="portfolio-out" class="page-section grey-section">
  <div id="portfolio">
    <div id="shinyapps-big">
       {% for project in site.data.projects %}
        {% if project.status == "current"%}
        <div class="shinyapp">
            <a class="" href="{{ project.url }}" target="_blank">
              <img class="appimg" src="{{ site.url }}/assets/img/project-screenshots/{{ project.img }}" href="{{ project.url }}" />
            </a>
            <div class="appdesc">
            <p class="preview">{{ project.description | truncate: 100, "..."}}</p>
                {% if project.description.size > 100 %}
                <a href="" onclick="showMore()" class="read-more-link">Read More</a>
                <div class="more" style="display:none;"><p>{{ project.description}}</p></div>
                {% endif %}
            </div>
          </div>
          {% endif %}
	  {% endfor %}
    </div>
    {% assign past_projects = site.data.projects | where: "status", "past" %}
    {% if past_projects.size > 0 %}
    <hr>
      <h3 style="text-align:left; margin:40px">Past Projects</h3>
	  <div id="shinyapps-big">
        {% for project in past_projects %}
          {% if project.status == "past"%}
          <div class="shinyapp">
            <a class="" href="{{ project.url }}" target="_blank">
              <img class="appimg" src="{{ site.url }}/assets/img/project-screenshots/{{ project.img }}" href="{{ project.url }}" />
            </a>
            <div class="appdesc">
            <p class="preview">{{project.description | truncate: 50, "..."}}</p>
                {% if project.description.size > 100 %}
                <a href="" onclick="showMore()" class="read-more-link">Read More</a>
                <div class="more" style="display:none;"><p>{{project.description}}</p></div>
                {% endif %}
            </div>
          </div>
          {% endif %}
        {% endfor %}
		</div>
    {% endif %}
  </div>
</div>
