---
layout: post-alternate
title: Locator
---

<img id="together" src='assets/images/logo.png' onerror='imgError(this)' />

<div class="centered">
    <button id="spanish" onclick="changeTextEnglish()">Español</button>
    <button id="english" onclick="changeTextSpanish()">English</button>
</div>

<h2 id="heading">Su viaje comienza aquí.</h2>

<p id="text"><strong>Todo el mundo sabe que cambiar puede ser difícil.</strong> Sin embargo, muchas personas sí cambian. ¿Cómo lo hicieron? La investigación sobre el cambio de comportamiento ha descubierto algunas cosas que pueden resultarle útiles.<br><br><strong>Las personas que intentan dejar de consumir sustancias se enfrentan a los mismos problemas que las personas que intentan cambiar otros hábitos.</strong> Ya sea una dieta poco saludable, no hacer ejercicio o consumir, surgen las mismas dificultades. Reconocemos un mal hábito. Intentamos cambiar. Podemos empezar y cambiar un poco, por un tiempo. Entonces volvemos a los viejos hábitos. Nos frustramos y tenemos ganas de rendirnos. El punto es que la gente a menudo piensa que las adicciones son diferentes de alguna manera.<br><br><strong>No son. El proceso es el mismo.</strong><br><br><strong>El cambio no es un evento de todo o nada.</strong> No es un interruptor que se activa. Para la mayoría, es gradual. Hay días de progreso y días de retroceso. Se necesita tiempo, pensamiento y determinación para cambiar, especialmente cuando se cambian hábitos de larga data como el uso intensivo.<br><br><strong>Pero buscar tratamiento es un gran primer paso.</strong><br><br>Su ser querido ha completado cierta información en su nombre: <strong>se preocupan por usted y quieren que sea lo más fácil posible para usted comenzar su viaje hacia adelante.</strong> Agregue su código postal o dirección actual en el cuadro a continuación; se lo dirigirá a una lista personalizada de proveedores relevantes para su situación actual.<br><br>Ni nosotros ni SAMHSA (el mantenedor de la lista de proveedores) almacenamos su información; <strong>simplemente esperamos facilitarle el comienzo.</strong><br><br><strong>Ingrese su código postal o dirección actual en el cuadro a continuación para comenzar.</strong></p>
<br><br>
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
        document.getElementById("text").innerHTML = "<strong>Todo el mundo sabe que cambiar puede ser difícil.</strong> Sin embargo, muchas personas sí cambian. ¿Cómo lo hicieron? La investigación sobre el cambio de comportamiento ha descubierto algunas cosas que pueden resultarle útiles.<br><br><strong>Las personas que intentan dejar de consumir sustancias se enfrentan a los mismos problemas que las personas que intentan cambiar otros hábitos.</strong> Ya sea una dieta poco saludable, no hacer ejercicio o consumir, surgen las mismas dificultades. Reconocemos un mal hábito. Intentamos cambiar. Podemos empezar y cambiar un poco, por un tiempo. Entonces volvemos a los viejos hábitos. Nos frustramos y tenemos ganas de rendirnos. El punto es que la gente a menudo piensa que las adicciones son diferentes de alguna manera.<br><br><strong>No son. El proceso es el mismo.</strong><br><br><strong>El cambio no es un evento de todo o nada.</strong> No es un interruptor que se activa. Para la mayoría, es gradual. Hay días de progreso y días de retroceso. Se necesita tiempo, pensamiento y determinación para cambiar, especialmente cuando se cambian hábitos de larga data como el uso intensivo.<br><br><strong>Pero buscar tratamiento es un gran primer paso.</strong><br><br>Su ser querido ha completado cierta información en su nombre: <strong>se preocupan por usted y quieren que sea lo más fácil posible para usted comenzar su viaje hacia adelante.</strong> Agregue su código postal o dirección actual en el cuadro a continuación; se lo dirigirá a una lista personalizada de proveedores relevantes para su situación actual.<br><br>Ni nosotros ni SAMHSA (el mantenedor de la lista de proveedores) almacenamos su información; <strong>simplemente esperamos facilitarle el comienzo.</strong><br><br><strong>Ingrese su código postal o dirección actual en el cuadro a continuación para comenzar.</strong>";
        document.getElementById("heading").innerHTML = "Su viaje comienza aquí.";
    }
    function changeTextSpanish(){
        document.getElementById("text").innerHTML = "<strong>Everybody knows that changing can be difficult.</strong> Yet, many people do change. How do they do it? Research in behavior change has discovered some things that you may find helpful.<br><br><strong>People trying to stop using substances face the same issues as people trying to change other habits.</strong> Whether it's an unhealthy diet, not exercising, or using, the same difficulties come up. We recognize a bad habit. We try to change. We may get started and change a bit, for a while. Then we slip back into old habits. We get frustrated and feel like giving up. The point is, people often think that addictions are different somehow.<br><br><strong>They're not. The process is the same.</strong><br><br><strong>Change is not an all-or-nothing event.</strong> It is not a switch that gets flipped. For most, it is gradual. There are days of progress and days of setbacks. It takes time, thought, and determination to change, especially when changing long-standing habits like heavy use.<br><br><strong>But seeking treatment is a great first step.</strong><br><br>Your loved one has filled out some information on your behalf -- <strong>they care about you and want to make it as easy as possible for you to begin your journey forward.</strong> Please add your current zip code or address to the box below -- you will be directed to a customized list of providers relevant to your current situation.<br><br>Neither we nor SAMHSA (the maintainer of the list of providers) store any of your information --  <strong>we simply hope to make it easy for you to get started.</strong><br><br><strong>Put your current zip code or address in the box below to get started.</strong>";
        document.getElementById("heading").innerHTML = "Your journey begins here.";
    }

</script>