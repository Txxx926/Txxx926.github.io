<h2 id="publications" style="margin: 2px 0px -15px;">Publications</h2>

<div class="publications">
<ol class="bibliography">

{% for link in site.data.publications.main %}

<li>

<div class="pub-row">


  <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
    {% if link.image %} 
     <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width=100;height=40%">
    {% endif %}
    {% if link.conference_short %} 
    <abbr class="badge" style="background-color: #7b4bb0">{{ link.conference_short }}</abbr>
    {% endif %}
  </div>

  <div class="col-sm-9" style="position: relative;padding-right: 10px;padding-left: 20px;">
      <div class="title"><a href="{{ link.pdf }}">{{ link.title }}</a></div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.conference }}</em>
      </div>
    <div class="links">
      {% if link.pdf %} 
      <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
      {% endif %}
      {% if link.arxiv %} 
      <a href="{{ link.arxiv }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Arxiv</a>
      {% endif %}
      {% if link.code %} 
      <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
      {% endif %}
      {% if link.page %} 
      <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
      {% endif %}
      {% if link.bibtex %} 
      <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
      {% endif %}
      {% if link.notes %} 
      <strong> <i style="color:#e74d3c">{{ link.notes }}</i></strong>
      {% endif %}
      {% if link.others %} 
      {{ link.others }}
      {% endif %}

        <span style="margin-left:12px; vertical-align:middle; position:relative; top:-3px;">
  {% if link.available %}
    <img src="./assets/img/artifacts_available.png" alt="Artifact Available" title="Artifact Available" style="height:22px; margin-right:4px; vertical-align:middle;">
  {% endif %}
  {% if link.functional %}
    <img src="./assets/img/artifacts_evaluated_functional_v1_1.png" alt="Artifact Functional" title="Functional" style="height:22px; margin-right:4px; vertical-align:middle;">
  {% endif %}
  {% if link.reproduced %}
    <img src="./assets/img/results_reproduced_v1_1.png" alt="Artifact Reproduced" title="Reproduced" style="height:22px; vertical-align:middle;">
  {% endif %}
</span>
  
      
    </div>
  </div>
</div>
</li>

<br>

{% endfor %}

</ol>
</div>

