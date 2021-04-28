<img alt="Latam at home logo" src="assets/images/LatamAtHome.png">

{% assign pages=site.pages | where:"ref", page.ref | sort: 'lang' %}
<ul style="text-align: right;">
{% for page in pages %}
  <li style="display:inline;">
    <a href="{{ page.url }}" class="{{ page.lang }}">{{ page.lang }}</a>
  </li>
{% endfor %}
</ul>

{% assign pages=site.pages | where:"lang", page.lang | sort: 'order' %}
<ul style="margin-top: -45px;">
{% for page in pages %}
  <li style="display:inline; margin-right: 5px;" class="tab-link">
    <a href="{{ page.url }}">{{ page.tabtext }}</a>
  </li>
{% endfor %}
</ul>
