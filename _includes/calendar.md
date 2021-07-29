<style>
  .event-wrapper .left-70 {
    float:none;
  }
</style>
<div id="calendar" style="overflow: auto; width: 90vw; max-width: 1000px; margin: auto; text-align: center;"/>

<script>
  const tzid = Intl.DateTimeFormat().resolvedOptions().timeZone;
  
  let iframe = document.createElement("iframe");
  iframe.src = "https://calendar.google.com/calendar/embed?width=1000px&height=600&wkst=1&bgcolor=%23ffffff&ctz=" + encodeURIComponent(tzid) + "&src=Y19yMTFyYjRlbjVsaXJxc2R1dHRscmphY2JiZ0Bncm91cC5jYWxlbmRhci5nb29nbGUuY29t&color=%23F6BF26&showNav=0&showDate=0&mode=AGENDA&showTitle=0&showPrint=0&showTabs=0&showCalendars=0&showTz=1&hl=" + document.lang;
  iframe.style.width = "1000px";
  iframe.style.height = "600px";
  
  document.getElementById("calendar").appendChild(iframe);
    
</script>
