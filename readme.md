# Overzicht verschillende HGI plots

## Uitleg
Hier een voorbeeld van hoe je de plots zou kunnen maken. De procedure is vrij eenvoudig, al zou je het in een productie omgeving waarschijnlijk wel iets anders willen doen. Wat hier gebeurt is het volgende: 

1. Eerst wordt er een AJAX call gedaan naar een statische JSON file in deze repository (zie `index.html`, regel 96). Dat houdt in dat er op de achtergrond een bestandje (`data/example_data.json`)wordt geladen met daarin de data die geplot moet worden. Voor deze plots is het dan ook heel belangrijk dat hetzelfde format gebruikt wordt. Zou je liever andere variabele namen willen gebruiken, dan zou je even in de code moeten duiken. De bestandjes waarin de plots gemaakt worden zijn `d3hgi.js` en `d3hgi_render.js`.

2. Na het laden van de data wordt de data omgezet naar een formaat dat elk van de plots begrijpt. Dit gebeurt op regel 102 van `index.html`. Dit is een stap die je moet doen, maar die verder niet heel interessant is. 

3. Na het omzetten van de data worden elk van de plaatjes geplot. Elke JavaScript functie die vanaf regel 103 wordt aangeroepen vult een van de divs (die in regel 20 - 91 worden gedefinieerd) met een plaatje.  

Dat was het eigenlijk al. Ik heb geprobeerd het zo eenvoudig mogelijk te houden, maar laat het vooral weten als je vragen hebt.


## De website bekijken
Als je nu naar de website gaat (het bestand `index.html` opent) dan zou je de gerenderde plots moeten zien. Let wel dat het op deze manier laden van data in een website standaard in Chrome geblokkeerd wordt. Dit geldt alleen voor dit voorbeeldje, en dus niet als je het daadwerkelijk ergens voor wilt gaan gebruiken.  Als je het wel in Chrome wilt testen moet je even een webserver starten. In Firefox zou het wel goed moeten gaan. Ik zelf test het wel in Chrome en gebruik hiervoor de volgende regel om een simpel HTTP server te starten in de root folder van deze repository:

``` bash
python -m SimpleHTTPServer
```

Als je dan naar localhost:8080 gaat zou je de website ook moeten kunnen zien, ongeacht de browser.  Verder heb ik GitHub pages aangezet voor deze repository, en is deze website is ook toegankelijk online: https://compsy.github.io/demo-wkz-example-plots/.
