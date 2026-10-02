<h2 id="publications" style="margin: 2px 0px -15px;">Research</h2>

<p style="color: #888; font-size: 13px; margin: 20px 0px 4px;">* indicates equal contribution</p>

<div class="publications">
<ol class="bibliography">

{% for link in site.data.publications.main %}

<li>
<div class="pub-row">
  <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
    {% if link.video %}
    <video autoplay loop muted playsinline poster="{{ link.image }}" class="teaser z-depth-1"
           style="width:197px; height:123px; object-fit:{{ link.fit | default: 'cover' }}; background:#fff; display:block;">
      <source src="{{ link.video }}" type="video/mp4">
    </video>
    {% elsif link.image %}
    <img src="{{ link.image }}" class="teaser z-depth-1"
         style="width:197px; height:123px; object-fit:{{ link.fit | default: 'cover' }}; background:#fff; display:block;">
    {% endif %}
    {% if link.conference_short %}
    <abbr class="badge">{{ link.conference_short }}</abbr>
    {% endif %}
  </div>
  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
      <div class="title"><a href="{{ link.pdf }}">{{ link.title }}</a></div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.conference }}</em>
      </div>
    <div class="links">
      {% if link.pdf %} 
      <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
      {% endif %}
      {% if link.badge %}
      {{ link.badge }}
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
      <!-- <strong> <i style="color:#e74d3c">{{ link.notes }}</i></strong> -->
      <span style="color: #888; font-size: 13px;">{{ link.notes }}</span>
      {% endif %}
      {% if link.others %} 
      {{ link.others }}
      {% endif %}
    </div>
  </div>
</div>
</li>
<br>

{% endfor %}

</ol>
</div>