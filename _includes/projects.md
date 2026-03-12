<h2 id="projects" style="margin: 2px 0px -15px;">Projects</h2>

<div class="publications">
<ol class="bibliography">

{% for link in site.data.projects.main %}

<li>
<div class="pub-row">
  <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
    {% if link.video %} 
    <video src="{{ link.video }}" class="teaser img-fluid z-depth-1" style="width: 100%; height: auto;" autoplay loop muted playsinline></video>
    {% elsif link.image %} 
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width: 100%; height: auto;">
    {% endif %}
    {% if link.conference_short %} 
    <abbr class="badge">{{ link.conference_short }}</abbr>
    {% endif %}
  </div>
  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
      <div class="title">
        {% if link.page %}
        <a href="{{ link.page }}">{{ link.title }}</a>
        {% else %}
        {{ link.title }}
        {% endif %}
      </div>
      {% if link.subtitle %}
      <div class="author">{{ link.subtitle }}</div>
      {% endif %}
      {% if link.period %}
      <div class="periodical"><em>{{ link.period }}</em></div>
      {% endif %}
      <div style="font-size: 0.95rem; margin-top: 5px;">{{ link.description }}</div>
    <div class="links">
      {% if link.pdf %} 
      <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
      {% endif %}
      {% if link.code %} 
      <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
      {% endif %}
      {% if link.page %} 
      <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
      {% endif %}
    </div>
  </div>
</div>
</li>
<br>

{% endfor %}

</ol>
</div>
