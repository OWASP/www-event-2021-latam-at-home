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

function registrationNotYetAvailable(event) {
  event.preventDefault()
  let url = window.location.pathname
  if (url.includes("-en.html")) {
    alert("Registration is not available yet. Stay tuned to our social networks");
  } else if (url.includes("-pt.html")) {
    alert("O registro ainda não está disponível. Fique atento às nossas redes sociais");
  } else {
    alert("La inscripción aún no está disponible. Mantente atento a nuestras redes sociales");
  }
}

let registerButtons = document.getElementsByClassName("cta-button blue")
var i
for (i = 0; i < registerButtons.length; i++) {
  registerButtons[i].addEventListener("click", registrationNotYetAvailable);
}
</script>

<style>
.left-70 {
  width: auto!important;  
}
.info-h4 {
  margin-top: 8px!important;
}
footer {
  margin: auto!important;
  width: 80%!important;
}
.footer-wrapper {
  max-width: 100%!important;
}
</style>
