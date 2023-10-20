# muell-melder-cramerstr
Ein paar Helfer um einfacher Probleme mit dem Müll der Häuser in der Wiesenstraße zu melden


## Beschwerde melden

Die Beschwerde sollte über die Seite der Stadt Göttingen eingereicht werden. Unter 'Bookmarklet' gibt es ein Script das man sich als Bookmark (Lesezeichen) im Browser speichern kann. Wenn man dieses Lesezeichen dann aufruft während man auf der Webseite ist, werden die notwendigen Daten vor-ausgefüllt und man muß nur noch wenige Felder ausfüllen bis man die Meldung komplett hat.

Link: https://www.goettingen.de/rathaus/buergerservice/maengelmelder/neuen-hinweis-melden/

## Bookmarklet

<a href="javascript: (() => {// Webseite: https://www.goettingen.de/rathaus/buergerservice/maengelmelder/neuen-hinweis-melden/ // Angaben meldende Person document.getElementById('kdstrasse').value = 'Cramerstraße'; document.getElementById('kdplz').value = '37073'; document.getElementById('kdort').value = 'Göttingen'; // Angaben Ort document.getElementById('strasse').value = 'Cramerstraße'; document.getElementById('hnr').value = '4'; document.getElementById('plz').value = '37073'; document.getElementById('ort').value = 'Göttingen'; document.getElementById('zusatz_ortsangabe').value = `Müllcontainer Abstellplatz beim Tiefgaragen-Treppenhaus an der Einfahrt zum Parkplatz`; // Beschreibung document.getElementById('bemerkung').value = `Sehr geehrte Damen und Herren, an der genannten Stelle finden Sie m.E. in Ihrem Zuständigkeitsgebiet unzumutbare Müllablagerungen: Aufgerissene Müllsäcke, Unrat achtlos neben den Tonnen und Containern. Reguläre Abholung oft nicht möglich. Müll quillt auch oft auf den Gehweg. Lockt Ratten an. Zu verursachenden Personen kann ich folgende Angaben machen: Mitarbeitende der Firmen sowie Bewohner der angrenzenden Häuser an der Wiesenstr. `; // Haken setzen document.getElementById('id_rubrik0_4').click(); document.getElementById('cb_datenschutz').click(); // Karte ausblenden jQuery('#inlinemap_ref').toggle(); // markieren was noch ausgefüllt werden sollte const markWithCss = `border: 2px solid magenta;`; document.getElementById('kdname').style = markWithCss; document.getElementById('kdhnr').style = markWithCss; document.getElementById('kdmail').style = markWithCss; document.getElementById('upload_available_bild').style = markWithCss; // Hinweis wie man den Rest vervollständigt alert(`Bitte mindestens die Magenta gefärbten Felder ausfüllen. Am besten ein Foto unter Anlagen hinzufügen und Absenden.`); })();">
  Automatisch Vorausfüllen
</a>

## Code des Scriptes zum nachlesen:

```JavaScript
javascript: (() => {
	// Webseite: https://www.goettingen.de/rathaus/buergerservice/maengelmelder/neuen-hinweis-melden/
	// Angaben meldende Person
	document.getElementById('kdstrasse').value = 'Cramerstraße';
	document.getElementById('kdplz').value = '37073';
	document.getElementById('kdort').value = 'Göttingen';
	// Angaben Ort
	document.getElementById('strasse').value = 'Cramerstraße';
	document.getElementById('hnr').value = '4';
	document.getElementById('plz').value = '37073';
	document.getElementById('ort').value = 'Göttingen';
	document.getElementById('zusatz_ortsangabe').value = `Müllcontainer Abstellplatz beim Tiefgaragen-Treppenhaus an 
	der Einfahrt zum Parkplatz`;
	// Beschreibung
	document.getElementById('bemerkung').value = `Sehr geehrte Damen und Herren,

	an der genannten Stelle finden Sie m.E. in Ihrem Zuständigkeitsgebiet unzumutbare Müllablagerungen:
	Aufgerissene Müllsäcke, Unrat achtlos neben den Tonnen und Containern. Reguläre Abholung oft nicht möglich. 
	Müll quillt auch oft auf den Gehweg. Lockt Ratten an.

	Zu verursachenden Personen kann ich folgende Angaben machen:
	Mitarbeitende der Firmen sowie Bewohner der angrenzenden Häuser an der Wiesenstr.
	`;
	// Haken setzen
	document.getElementById('id_rubrik0_4').click();
	document.getElementById('cb_datenschutz').click();
	// Karte ausblenden
	jQuery('#inlinemap_ref').toggle();
	// markieren was noch ausgefüllt werden sollte
	const markWithCss = `border: 2px solid magenta;`;
	document.getElementById('kdname').style = markWithCss;
	document.getElementById('kdhnr').style = markWithCss;
	document.getElementById('kdmail').style = markWithCss;
	document.getElementById('upload_available_bild').style = markWithCss;
	// Hinweis wie man den Rest vervollständigt
	alert(`Bitte mindestens die Magenta gefärbten Felder ausfüllen.
	 Am besten ein Foto unter Anlagen hinzufügen und Absenden.`);
})();
```