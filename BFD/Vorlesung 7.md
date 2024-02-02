# PDF(Portable Document Format): Page Objects
- 10.1.2008: PDF 1.7 wird ISO Standard •
- Dokumente enthalten Dictionaries, Page Objekte und Aktionen
- Strukturen vererben Attribute 
- meist hierarchisch
## PDF Objects
- Pfadobjekte
- Textobjekte
- Externe Objekte (XObjects)
- Inline-Images
- Shading Objekte
- Interaktive Elemente wie z.B. ein hypermediales Inhaltsverzeichnis
- Annotationen
	- Text Annotation
	- Free Text Annotation
	- Line Annotation
	- Square und Circle Annotation
- Verweise
	- Go-To-Action
	- Remote-Go-To-Action
- File-Attachment-Annotation
- Audio-Annotation
- Video-Annotation
## PDF/A
- PDF 1.4 zur Langzeitarchivierung von elektronischen Dokumenten
- geräteunabhängig
- abgeschlossen
- selbstdokumentierend
- transparent
- keine technischen Schutzmassnahmen
- offen
- eingesetzt
	- verbreiteter Einsatz dürfte der beste Schutz vor Verlust sein
- Grenzen von PDF/A
	- kann nicht allein die Langzeitarchivierung ermöglichen
	- ist noch nirgends gerichtsfest
## PDF/A-2
Vergleich mit PDF/A-1:
- basiert auf PDF 1.7 (ISO 32000-1)
- JPEG 2000 Kompression erlaubt
- Transparenz, Ebenen möglich
- OpenType-Fonts können eingebettet werden
- digitale Signaturen
- Container: PDF/A-1 Dateien können in PDF/A-2 Dateien eingebettet werden
## PDF/UA vs. WCAG
- PDF/UA definiert technische Merkmale und bietet einen technischen Rahmen
- PDF/UA enthält keine Anforderungen an die Auszeichnung des Inhalts (z.B. Akronyme)
- PDF/UA legt kein Mindestkontrastverhältnis fest
- PDF/UA beschriebt keine zeitlichen Anforderungen
- PDF/UA erweitert WCAG teilweise (Encoding, aktive Inhalte)
- PDF/UA nicht für Endanwender gedacht
- PDF/UA betrifft auch das Leseprogramm
- PDF/UA kennt (außer bei Bildern) keine alternative Darstellungen (z.B. Redetext)
# PDF und Barrierefreiheit
## Tags in PDF
Dokumente mit Tags können kompakt dargestellt werden
 - Erhöhung der Lesbarkeit für Sehbehinderte und Dyslexiker
- Die logische Leserichtung wird angewendet
- Die logische Leserichtung wird angewendet
- manuelle Aktivierung
## PDF für Scannerergebnisse
OCR Anwendungen notwendig
- Adobe Capture: ab 144 dpI, Farbe ab 200 dpI
- Omnipage, FineReader, usw.
PDF kann sowohl Bild als auch Text gemeinsam speichern
- suchen wird möglich, ebenso kann man Ausschnitte als Text extrahieren

Manuelles Anlegen des Tagstamms sowie automatische Erzeugung von Tags

Manuelle Reparatur von Fehlern durch Tagkontrolle (auch per Screenreader möglich)
## PAC 2021
Freies Werkzeug für tagged PDF, prüft u.a.
- Titel des Docs verfügbar
- Doc Spache defininiert
- Sicherheitseinstellung
- ...

WCAG Konformität
- Farbkontrast
## Rolemap/Rollen

Die Rolemap ordnet unbekannt Tags den vordefinierten Tags zu

Rollen werden (heute) auch von Screenreadern erkannt

&ltp&gtfür Paragraphen, &ltTR>, &ltTD> und &ltTH> für Tabellen, usw.
## Formulare in PDF
- Anwahlschalter
- Texteingabe und Ausklappliste
- Listenfeld
- Auswahlschalter
- Texteingabefeld
- Schalter
- Digitales Unterschriftenfeld

### Formulare in der Praxis
Bedienung per Tastatur möglich

Vorher ausfüllen nur falls Inhalte akzeptabel sind
## Verweise
Verweise werden vor den allgemeinen Tags erstellt

Automatische Erkennung aus OCR Ergebnis möglich

Verweise müssen explizit beschriftet werden

Verweise aus MS Office/OpenOffice bleiben erhalten
