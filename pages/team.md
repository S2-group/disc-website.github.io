---
layout: page
title: Team
---

### Executive Board
<div style="padding-top: 10px; padding-bottom: 30px;">

      {% for member in site.data.board_members %}
        <div class="team-member-container" align= "center">
            <div class="team-member team-member-role">{{member.role}}</div>
            <img alt="Image" height = "200px" src="{{site.url}}{{member.image}}"/>
            <div class="team-member team-member-name">{{member.name}}</div>
            <div class="team-member team-member-affiliation">{{member.affiliation}}</div>
        </div>
	  {% endfor %}
</div>


### Outreach and Valorisation

<div style="padding-top: 10px; padding-bottom: 30px;">

      {% for member in site.data.team_outreach %}
        <div class="team-member-container" align= "center" style="padding-bottom: 20px">
            <img alt="Image" height = "200px" src="{{site.url}}{{member.image}}"/>
            <div class="team-member team-member-name">{{member.name}}</div>
            <div class="team-member team-member-affiliation">{{member.affiliation}}</div>
        </div>
	  {% endfor %}
</div>

### Participating researchers

<div style="padding-top: 10px; padding-bottom: 30px;">

      {% for member in site.data.team_members %}
        <div class="team-member-container" align= "center" style="padding-bottom: 20px">
            <img alt="Image" height = "200px" src="{{site.url}}{{member.image}}"/>
            <div class="team-member team-member-name">{{member.name}}</div>
            <div class="team-member team-member-affiliation">{{member.affiliation}}</div>
        </div>
	  {% endfor %}
</div>
