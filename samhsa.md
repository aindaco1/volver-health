---
layout: post-alternate
title: Locator
---

<img id="together" src='assets/images/logo.png' onerror='imgError(this)' />

<p id="text">Spanish version</p>

<button id="spanish" onclick="changeTextSpanish()">Spanish</button>
<button id="english" onclick="changeTextEnglish()">English</button>

<div id="iframewrapper">
    <iframe allowtransparency="true" frameborder="0" height="170" id="mentalhealthtreatmentfinder" marginheight="0" marginwidth="0" name="mentalhealthtreatmentfinder" scrolling="no" src="https://findtreatment.samhsa.gov/locator/widget/170?sType=SA&sCodes=SA,DT" title="Samhsa.gov" width="170"> https://findtreatment.samhsa.gov/locator/widget/170 </iframe>
</div>

<script>

    function getUrlVars() {
        let parameters = document.location.search;
        parameters = parameters.substring(1);
        let decoded = atob(parameters);
        let qmark = '?';
        decoded = qmark.concat(decoded);
        var vars = {};
        var parts = decoded.replace(/[?&]+([^=&]+)=([^&]*)/gi, function(m,key,value) {
            vars[key] = value;
        });
        return vars;
    }

    var treatment = "sType="+getUrlVars()["treatment"];
    var code = "sCodes="+getUrlVars()["code"];
    var togetherImage = atob(getUrlVars()["image"]);

    document.getElementById("mentalhealthtreatmentfinder").src = "https://findtreatment.samhsa.gov/locator/widget/170?"+treatment+"&"+code;

    document.getElementById('together').src = togetherImage;

    function imgError(image) {
        image.onerror = "";
        image.src = "assets/images/logo.png";
        return true;
    }

    function changeTextEnglish(){
        document.getElementById("text").innerHTML = "English version";
    }
    function changeTextSpanish(){
        document.getElementById("text").innerHTML = "Spanish version";
    }

</script>