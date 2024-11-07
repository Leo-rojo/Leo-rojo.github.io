<h2 id="publications" style="margin: 2px 0px -15px;">Projects</h2>

<div class="publications">
<ol class="bibliography">

{% for link in site.data.projects.main %}

<li>
<div class="pub-row">
  <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
    {% if link.image %} 
    <img src="{{ link.image }}" style="border-radius: 8px; box-shadow: 3px 3px 6px #888; height: 123px; width: 270px; margin-top: 5px; margin-left: 5px; margin-bottom: 5px; object-fit: cover;">
    {% endif %}
  </div>
  <div class="col-sm-9" style="position: relative;padding-right: 20px;padding-left: 20px;">
      <div class="title"><a href="{{ link.link }}">{{ link.title }}</a></div>
      <div class="author" style="font-size: 14px;" >{{ link.description }}</div>
      {% if link.reference_1_link %}
      <a href="{{ link.reference_1_link }}"><sup>1</sup>Reference 1</a>
      {% endif %}
      &nbsp;&nbsp; <!-- Adds two non-breaking spaces between the links -->
      {% if link.reference_2_link %}
      <a href="{{ link.reference_2_link }}"><sup>2</sup>Reference 2</a>
      {% endif %}

  </div>
</div>
</li>
<br>

{% endfor %}

</ol>
</div>
