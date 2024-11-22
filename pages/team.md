---
layout: page
title: Team
---
<style>
  .team-sections {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    gap: 20px; /* Space between columns */
}

.team-section {
    flex: 1; /* Flexibly take up available space */
    min-width: 300px; /* Minimum width to prevent items from getting too small */
    box-sizing: border-box;
    padding: 10px;
}

@media (max-width: 768px) {
    .team-sections {
        flex-direction: column;
        align-items: center;
    }
}

</style>
<hr>
<div style="padding-top: 10px; padding-bottom: 30px; text-align:center;">
    <div class="team-section">
        <h3 style="text-align:center; margin:40px">Core Team</h3>
        {% for member in site.data.team %}
            <div class="team-member-container" align= "center" style="padding-bottom: 10px; padding-top:20px;">
                <img alt="Image" height = "230px" src="{{site.url}}{{member.image}}"/>
                <div class="team-member team-member-name">{{member.name}}</div>
                <div class="team-member team-member-role">{{member.role}}</div>
                <div class="team-member team-member-affiliation">{{member.affiliation}}</div>
            </div>
        {% endfor %}   
        </div>
        <div class="team-section">
                <hr>
        <h3 style="text-align:center; margin:40px">Participating Researchers</h3>
        {% for member in site.data.team_members %}
            <div class="team-member-container" align= "center" style="padding-bottom: 10px; padding-top:20px;">
                <img alt="Image" height = "230px" src="{{site.url}}{{member.image}}"/>
                <div class="team-member team-member-name">{{member.name}}</div>
                <!-- <div class="team-member team-member-role">{{member.role}}</div> -->
                <div class="team-member team-member-affiliation">{{member.affiliation}}</div>
            </div>
        {% endfor %}   
        </div>
</div>

    


<!-- <h3 style="text-align:center;">Executive Board</h3>
      {% for member in site.data.board_members %}
        <div class="team-member-container" style="padding-top: 30px;" align= "center">
            <div class="team-member team-member-role">{{member.role}}</div>
            <img alt="Image" height = "200px" src="{{site.url}}{{member.image}}"/>
            <div class="team-member team-member-name">{{member.name}}</div>
            <div class="team-member team-member-affiliation">{{member.affiliation}}</div>
        </div>
	  {% endfor %} -->
<!-- <div class="team-sections">
    <div class="team-section">
        <h4 style="text-align:center;">Scientific Coordination</h4>
        {% for member in site.data.team_scientific_coord %}
        <div class="team-member-container" align="center" style="padding-bottom: 20px; padding-top:20px;">
            <img alt="Image" height="200px" src="{{site.url}}{{member.image}}" />
            <div class="team-member team-member-name">{{member.name}}</div>
            <div class="team-member team-member-affiliation">{{member.affiliation}}</div>
        </div>
        {% endfor %}
    </div>
    <div class="team-section">
        <h4 style="text-align:center;">Outreach and Valorisation</h4>
        {% for member in site.data.team_outreach %}
        <div class="team-member-container" align="center" style="padding-bottom: 30px; padding-top:20px;">
            <img alt="Image" height="200px" src="{{site.url}}{{member.image}}" />
            <div class="team-member team-member-name">{{member.name}}</div>
            <div class="team-member team-member-affiliation">{{member.affiliation}}</div>
        </div>
        {% endfor %}
    </div>
</div>
<hr>
 <h3 style="text-align:center; padding-top:30px; padding-bottom:30px">Participating researchers</h3>
      -->


