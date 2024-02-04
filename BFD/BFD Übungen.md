# Übung 1
## Ziele
- Wissen aus Vorlesung
- Selbststudium zu **ARIA** und **WCAG**

## ARIA
> Accessible Rich Internet Applications Suite
- Anreicherung von Mark-up Elementen durch *zusätzliche Information*
- ohne ARIA: -> bestimmte Elemente von Webseiten nicht zugänglich, z.B. dynamische Inhalte & UIs
- Beschreiben z.B. von Regionen, Navigation, Widgets
- Umsetzung durch **Attribute** 

3 个重要的ARIA 标签, 注意结合HTML语法以及标签的位置:
***Rollen:*** `(roles)`
![[Pasted image 20240116035732.png]]

***Eigenschaften:*** `(properties)`
- Beschreibung von Elementen
- Auszeichnung von **Beziehungen**
- Wert bleibt **konstant**

> Name/Beschreibung
> - `aria-descibedby, aria-label, aria-labelledby`

![[Pasted image 20240116040248.png]]

***Zustände:*** `(states)`
- veränderliche Zustandsinformation
- Bsp.: `aria-hidden="true"`
	- deaktiviert "Sichtbarkeit" des Elements für Screenreader
	- bspw. für dekorative oder ausgeblendete Elemente wie icons.
	- ![[Pasted image 20240116040529.png]]

## WCAG: Web Content Accessibility Guidelines
-> 应该不用背吧
![[Pasted image 20240116040625.png|300]]

### 4 Prinzipien + 13 Richtlinien
#### wahrnehmbar
![[Pasted image 20240116040922.png]]
-> 大致理解就行

#### bedienbar
![[Pasted image 20240116041041.png]]

#### verständlich
![[Pasted image 20240116041142.png]]
#### robust
##### 4.1 Kompatibel
- Kompatibilität mit aktuellen und zukünftigen Benutzeragenten -> einschließlich assistiver Techniken
- Bsp.: Name, Rolle, Werte


### Erfolgskriterien
- konkrete **Handlungsanweisungen** bezüglich der 13 Richtlinien
- Grundlage zur Überprüfung der Barrierefreiheit -> ***technisch überprüfbar***

**Erweiterte Informationen beinhalten...**:
- ausreichende bzw. sichere Techniken, deren Einsatz zur Erfüllung des Erfolgskriterium führen
- Fehler-Techniken, die zur *Nicht-Erfüllung* des Erfolgskriteriums führen.
- Erläuterungen zum Zweck und Nutzen des Erfolgskriteriums
- Beispiele für die Umsetzung
- Hinweise zur ***Konformitätsprüfung***

### Konformitätsstufen
![[Pasted image 20240116041910.png]]
> An jedem **Erfolgskriterium** ist vermerkt, für welche **Konformitätsstufe** das jeweilige Kriterium erfüllt sein muss

### Technik: WAVE Browser Extension
--> für die technische Überprüfbarkeit
![[Pasted image 20240116042231.png]]

**Interpretation:**
- Ergebnis der WAVE-Toolbar gibt *Hinweise* auf Accessibility Probleme
- Zuordnung zu den Erfolgskriterien gem. Richtlinien vornehmen
- **Gutachten** verfassen

Schritte:
1. Seitenauswahl
2. WAVE-Auswertung
3. Richtlinienzuordnung
4. Gutachtenerstellung

> Aber: **keine** finale Aussage zur Barrierefreiheit basierend auf WAVE möglich!


# Übung 2
# Einleitung
## Barrierefreie Dokumente mit Word & PowerPoint

Vorteile Powerpoint:
- MS Bürostandard
- Präsentationen
- Poster
- Flyer
- auf andere Office-Programme übertragbar

## Titel, Format und Schrift

### Titel
- Der Titel ist die erste und wichtigste Information für jede **Folie**.
- Zum Anlegen des Titels muss der vordefinierte Textrahmen von PowerPoint genutzt werden.
- Alternativ können Texte durch Höherstufen der Gliederungsebene zum Titel gemacht werden.

Ansicht → Gliederungsansicht → Rechtsklick auf einen Inhalt → Höher stufen

### Format und Schrift
- Schriftart ist frei wählbar, es sollte darauf geachtet werden, dass die Schrift gut lesbar ist und sich die Buchstaben in ihrer Form gut unterscheiden.
- Das korrekte **Dokumentenformat** (bspw. A0 bei Postern) sollte in den *Dokumenteigenschaften* festgelegt werden.

## Textinhalte
Alle Textabsätze sollten mithilfe von **Absatzformatvorlagen** definiert werden. Benutzen Sie dafür die Palette „**Formatvorlagen**“. Für Textauszeichnungen innerhalb von Absätzen sollten **Zeichenformatvorlagen** erstellt werden (z. B. für einen Hyperlink).


### Überschriften
Für Überschriften verwenden Sie die Formate Überschrift 1, Überschrift 2 und Überschrift 3. 

*Zwischen* zwei Überschriften sollte immer **Fließtext** stehen. Bei Überschriften in absteigender Folge sollte keine Ebene übersprungen werden (Beispiel: auf eine Überschrift 1 darf keine Überschrift 3 folgen). 
Die Überschriftformatvorlagen können selbstverständlich Ihren Wünschen gemäß angepasst werden.


### Fließtext
Für Text sollte die **Formatvorlage** *Standard* eingesetzt werden. Diese kann selbstverständlich Ihren Wünschen gemäß angepasst werden. Es sollte darauf geachtet werden, dass die Schrift gut lesbar ist und sich die Buchstaben in ihrer Form gut unterscheiden.

### Abkürzungen
*Abkürzungen sollten vermieden werden.* 
Ist dies nicht möglich, sollten Abkürzungen ==beim ersten Vorkommen im Text erläutert werden==. 
==Sonst sollten nur Abkürzungen verwendet werden, die im Verzeichnis des **Dudens** aufgeführt werden.


### Sonderzeichen
Verwenden Sie ausschließlich typografisch korrekte Sonderzeichen, wie etwa ==**„deutsche Anführungszeichen“** – in der Regel erledigt das Microsoft Word automatisch.

### Aufzählungen und Listen
Aufzählungen werden mit der Vorlage *Listenpunkt* formatiert. Die Vorlage *Listenstrich* erlaubt Gliederungen innerhalb einer Auflistung. 

Nummerierte Listen werden mit der Vorlage *Listennr*. formatiert.

## Tabellen
-  Sollten immer als Datentabelle angelegt werden; Bitte nicht als Bild importieren!
-  Tabellen sollten einen **Alternativtext** aufweisen, der den *Zweck* der Tabelle beschreibt:
	- `Rechtsklick auf Tabelle → Form formatieren → Größe und Eigenschaften → Alternativte`
-  Um Tabellen für ==blinde Nutzer== gut wahrnehmbar umzusetzen, sollte darauf geachtet werden, dass **diese einfach strukturiert sind** und eine **Kopfzeile** besitzen. Die jeweiligen ***Spaltenüberschriften*** sollten aussagekräftig, eindeutig und ohne Abkürzungen benannt sein.
-  Bitte nutzen Sie keine sogenannten „Layouttabellen“, also Tabellen, die nur für die grafische Positionierung von Inhalten dienen. ==Diese sollten unbedingt vermieden werden. Tabellen sollten nur zur strukturierten Darstellung von Datensätzen eingesetzt werden==


## Diagramme, Bilder und Grafiken
Abbildungen sollten (über den Reiter *Format → Zeilenumbruch*) mit "***Text in Zeile***" eingebunden werden, da es sonst zu Problemen bei der Erkennung in Screenreadern kommen kann. (Word) --> Alternative???


### Diagramme
• Benötigen einen ***Alternativtext***:
*Rechtsklick* **Diag. → Diagrammbereich formatieren → Größe und Eigenschaften → Alternativtext → Beschreibung**
• Zusätzlich sollte für blinde Nutzer die Datentabelle eingebunden werden.
Bilder und Grafiken
• Benötigen einen *Alternativtext*, damit blinde Nutzer den Inhalt der Abbildung wahrnehmen können:
Rechtsklick auf die Grafik → Form formatieren → Größe und Eigenschaften → Alternativtext → Beschreibung
• Bitte den Text im Feld „*Beschreibung*“ eingeben.

![[Pasted image 20231209160341.png]]
![[Pasted image 20231209160424.png]]
--> smartart 不用管

### Farben und Kontrast
• Denken Sie bei der Gestaltung von Tabellen an Menschen mit einer *Sehschwäche* oder einer ***Farbfehlwahrnehmung***. ==Achten Sie darauf, dass alle mit Farben dargestellten Informationen auch ohne Farbe verfügbar und Inhalte auch dann verständlich sind, wenn sie ohne Farbe betrachtet werden.==
• Das ***Text-Hintergrund-Kontrast-Verhältnis*** sollte mindestens 4,5:1 für kleinen Text und 3:1 für großen Text betragen.
• Das Kontrast-Verhältnis kann mit dem kostenlosen Tool „Color Contrast Analyser“ der ***Paciello*** Group ermittelt werden: https://developer.paciellogroup.com/resources/contrastanalyser/


### Lesereihenfolge
• Legen Sie für die einzelnen Inhalte eine **sinnvolle Lesereihenfolge** fest. Hier bestimmen Sie, in welcher
Reihenfolge bspw. Screenreader den Inhalt widergeben.
*Registerkarte Start → Anordnen → Auswahlbereich*
• ***Achtung***: Die Objekte werden beginnend beim untersten Listenelement und endend mit dem obersten Listenelement vorgelesen.

> 这段话主要是在讲述如何为某个内容设定一个有意义的阅读顺序，特别是在使用屏幕阅读器时。具体来说，它提到了在用户界面中设置阅读顺序的步骤，并强调了一个重要注意事项。

> 首先，它建议为每个内容确定一种有意义的阅读顺序，以确保屏幕阅读器按照您设定的顺序呈现内容。具体的设置步骤为“Registerkarte Start → Anordnen → Auswahlbereich”（可能是某个软件或界面的具体路径）。

> 其次，它强调了一个警告：“Achtung”表示注意，提醒用户注意一个重要的细节。警告指出，在阅读内容时，对象的顺序将从列表的最底部元素开始，直到最顶部元素结束。这是一个重要的提示，因为如果用户希望阅读顺序与页面布局或逻辑不同，他们需要相应地调整对象的排列顺序。

## Metadaten

• Die Dokumenteigenschaften helfen allen Nutzern und Indizierprogrammen bei der Einordnung des Dokumentes.
• Die Metadaten werden festgelegt unter `Datei → Informationen → Eigenschaften`
• Hier sollte zumindest der Titel sowie der Autor gepflegt werden.

## Barrierefreiheit überprüfen

• Prüfen Sie mit den Bordmitteln内置工具 von PowerPoint die Barrierefreiheit Ihres Dokumentes
*Datei → Auf Probleme prüfen → Barrierefreiheit überprüfen*
• Zudem bietet die **Gliederungsansicht** einen guten Überblick über alle Textinhalte der Präsentation.
Ansicht → Gliederungsansicht

![[Pasted image 20231209162217.png]]


# Barrierefreiheit bei PDF-Dokumenten herstellen
![[Pasted image 20231209162316.png]]
![[Pasted image 20231209162429.png]]


# Übung 3 - Grafik
## Aufgabe : use case
- Grafiken für Beeinträchtigten zugänglich gestalten.
- 4 Punkte der zugänglichen Grafiken --> s.9
	- 1. Bildbeschreibung
	- 2. taktile Darstellung
	- 3. 
	- 4. weitere Techniken


## Aufgabe 1: Bildbeschreibungen
### Rechtliche Grundlage
- WCAG 2.1
- achten auf Ausnahme

### Grundlagen
zugängliche Alternative
Inhalt / Kontext
manuell erstellen
mindestens bereitstellen: Alternativtext --> MS Office
Diagramme: ausführliche Bildbeschreibung
Richtlinien aus VL
Wiedergabe durch Braillezeile oder Screenreader


### Hinweise
#### Was beschreiben?
- Absicht / Zweck des Diagramms
- Aussehen und Anzahl der Bildelemente
- Lage der Elemente absolut bzw. relativ zueinander
- visuelle Besonderheiten, Annotationen
- alle Textelemente, Caption
- Trend der Daten
- Kontext der Grafik (keine redundanten infos)

#### WIE beschreiben?
zweckmäßig
***vom Allgemeinen zum Speziellen***
Zielgruppenangepasst ( Vokabular, Expertise....)
objektiv! --> keine Interpretation oder Meinungen 
kurz und verständlich

### Aufbau
-> s.14 Bsp.
#### 1. Überblick
Diagrammtyp, Titel
Besonderheiten (horizontal oder vertikal)

#### 2. Achsen
Anordnung / Lage
Beschriftung
Einheit
Skala (Wertbereich, Intervalle)
#### 3. Daten
- je nach Diagrammtyp, z.B. Anzahl der Datenreihen , Beschriftung und Anordnung, ggf. allg. Trends

### Herausforderungen
oft nur eine mögliche Interpretation -> abhängig vom Wissen der erstellenden Person

- scatterplot: einzelnen Datenwert aufzulisten ist nicht sinnvoll
	- statistische Zusammenfassung: eine Korrelation? Scatter? Trend? ... 

### Wahrnehmung
- **nur visuelle Aspekte beschreiben! -> Wahrnehmung ist subjektiv** 
	- bspw. wie lief die Kurve? Steil? -> Nein!, man darf nicht so beschreiben. Man soll nur so: steigend, ggf. Winkel


### Daten
- Kurvenverläufe
- Achten auf **Subjektive Beschreibung** 


## Aufgabe 1 a) Anfertigen eines Alt-Textes und einer Beschreibung


## Aufgabe 1 b) HTML
mind 2 unterschiedlichen Varianten (aria-describedby, link -> s.VL Teil 1)

#### Exkurs OSS Screen reader
NVDA

#### Mobil: Talkback, VoiceOver


## Aufgabe 1 Taktile Grafiken
### Allgemeine Richtlinien
- Ursprüngliche Aussage
- Reduzierung der Komplexität
- Texturen, Linienstile und Punktsymbole sparsam verwenden 
- Verwendung von Braille-Schrift
- ...

### Mindestmaße
- Linienlänge
- Versenkung
- sich kreuzende Linien
- Texturen

### Füllmuster / Texturen
s.40







