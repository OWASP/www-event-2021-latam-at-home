<!--<img alt="Latam at home logo" src="assets/images/LatamAtHome.png">-->

{% assign pages=site.pages | where:"ref", page.ref | sort: 'lang' %}
<ul style="text-align: right;">
{% for page in pages %}
  <li style="display:inline;">
    <a id="{{ page.lang }}-site" href="{{ page.url | relative_url }}" class="{{ page.lang }}">{{ page.lang }}</a>
  </li>
{% endfor %}
</ul>

{% assign pages=site.pages | where:"lang", page.lang | sort: 'order' %}
<ul style="margin-top: -45px;">
{% for page in pages %}
  <li style="display:inline; margin-right: 5px;" class="tab-link">
    <a href="{{ page.url | relative_url }}">{{ page.tabtext }}</a>
  </li>
{% endfor %}
</ul>

<script>
let alreadyTranslated = localStorage.getItem("translation")
if (!alreadyTranslated) {
  let lang = navigator.userLanguage || navigator.language || navigator.browserLanguage || navigator.systemLanguage
  if (lang && lang.length > 2) {
    lang = lang.substring(0, 2)
  }

  localStorage.setItem("translation", lang)

  if (lang.includes("es")) {
    document.getElementById("ES-site").click()
  } else if (lang.includes("pt")) {
    document.getElementById("PT-site").click()
  } else {
    document.getElementById("EN-site").click()
  }
}
</script>
