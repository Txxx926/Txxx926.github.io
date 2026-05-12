<h2 id="publications" style="margin: 2px 0px -15px;">Publications</h2>

<style>
  .publications{
    max-width: 1200px;
    width: 100%;
    margin-left: auto;
    margin-right: auto;
  }

  .publications .col-sm-12{
    padding-left: 10px !important;
    padding-right: 10px !important;
  }
  
  .publications ol.bibliography > li {
    margin-bottom: 8px;
  }

.publications h3.pub-section{
  font-size: 1.35rem;
  font-weight: 600;
  color: #222;

  display: inline-block;
  line-height: 1.1;

  padding-bottom: 1px;
  border-bottom: 1.5px solid #bdbdbd;  

  margin-bottom: 0.9em;
}
  
</style>

<div class="publications">

  <!-- ===================== Preprints ===================== -->
  {% assign preprints = site.data.publications.main | where: "preprint", true %}
  {% if preprints.size > 0 %}
  <h3 id="preprints" class="pub-section">Preprints</h3>
  <ol class="bibliography">
    {% for link in preprints %}
      <li>
        <div class="pub-row">
          <div class="col-sm-12" style="position: relative;padding-right: 10px;padding-left: 20px;">
            <div class="title"><a href="{{ link.pdf }}">{{ link.title }}</a></div>
            <div class="author">{{ link.authors }}</div>
            <div class="periodical"><em>{{ link.conference }}</em></div>

            <div class="links">
              {% if link.pdf %}<a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>{% endif %}
              {% if link.arxiv %}<a href="{{ link.arxiv }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Arxiv</a>{% endif %}
              {% if link.code %}<a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>{% endif %}
              {% if link.page %}<a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>{% endif %}
              {% if link.bibtex %}<a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>{% endif %}
              {% if link.notes %}<strong><i style="color:#e74d3c">{{ link.notes }}</i></strong>{% endif %}
              {% if link.others %}{{ link.others }}{% endif %}

              {% if link.reproduced %}
                <div style="margin-top:8px; display:flex; align-items:center;">
                  {% if link.available %}
                    <img src="./assets/img/artifacts_available.png" alt="Artifact Available" title="Artifact Available"
                         style="height:22px; margin-right:1px;">
                  {% endif %}
                  {% if link.functional %}
                    <img src="./assets/img/artifacts_evaluated_functional_v1_1.png" alt="Artifact Functional" title="Functional"
                         style="height:22px; margin-right:1px;">
                  {% endif %}
                  <img src="./assets/img/results_reproduced_v1_1.png" alt="Artifact Reproduced" title="Reproduced"
                       style="height:22px;">
                  <span style="color:#27ae60; font-size:16px; font-weight:bold; margin-left:4px;">
                    (Artifact Available, Functional, Reproduced)
                  </span>
                </div>
              {% endif %}
            </div>
          </div>
        </div>
      </li>
    {% endfor %}
  </ol>
  {% endif %}

  <!-- ============ Conference and Workshops ============ -->
  {% assign confpapers = site.data.publications.main | where_exp: "item", "item.preprint != true" %}
  {% if confpapers.size > 0 %}
  <h3 id="conf-workshops" class="pub-section">Conference and Workshops</h3>
  <ol class="bibliography">
    {% for link in confpapers %}
      <li>
        <div class="pub-row">
          <div class="col-sm-12" style="position: relative;padding-right: 10px;padding-left: 20px;">
            <div class="title"><a href="{{ link.pdf }}">{{ link.title }}</a></div>
            <div class="author">{{ link.authors }}</div>
            <div class="periodical"><em>{{ link.conference }}</em></div>

            <div class="links">
              {% if link.pdf %}<a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>{% endif %}
              {% if link.arxiv %}<a href="{{ link.arxiv }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Arxiv</a>{% endif %}
              {% if link.code %}<a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>{% endif %}
              {% if link.page %}<a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>{% endif %}
              {% if link.bibtex %}<a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>{% endif %}
              {% if link.notes %}<strong><i style="color:#e74d3c">{{ link.notes }}</i></strong>{% endif %}
              {% if link.others %}{{ link.others }}{% endif %}

              {% if link.reproduced %}
                <div style="margin-top:8px; display:flex; align-items:center;">
                  {% if link.available %}
                    <img src="./assets/img/artifacts_available.png" alt="Artifact Available" title="Artifact Available"
                         style="height:22px; margin-right:1px;">
                  {% endif %}
                  {% if link.functional %}
                    <img src="./assets/img/artifacts_evaluated_functional_v1_1.png" alt="Artifact Functional" title="Functional"
                         style="height:22px; margin-right:1px;">
                  {% endif %}
                  <img src="./assets/img/results_reproduced_v1_1.png" alt="Artifact Reproduced" title="Reproduced"
                       style="height:22px;">
                  <span style="color:#27ae60; font-size:16px; font-weight:bold; margin-left:4px;">
                    (Artifact Available, Functional, Reproduced)
                  </span>
                </div>
              {% endif %}
            </div>
          </div>
        </div>
      </li>
    {% endfor %}
  </ol>
  {% endif %}

</div>
