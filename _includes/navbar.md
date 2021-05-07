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

<style>
.left-70 {
  width: auto!important;  
}
.event-banner {
    height: 10em!important;
    background-color: darkgray!important;
}
.info-h4 {
  margin-top: 8px!important;
  margin-bottom: 15px!important;
}
footer {
  margin: auto!important;
  width: 80%!important;
}
.footer-wrapper {
  max-width: 100%!important;
}
</style>
