>  Zugängliche Grafiken für Menschen mit Blindheit oder Sehbeeinträchtigung und Grafische Notationen
![[Pasted image 20240120152249.png]]
# Agenda:
**Teil 1 + Übung**
1. Grundlagen Grafiken
2. Zugängliche Grafiken
3. Bildbeschreibungen
4. Taktile Grafiken
5. Taktile Interaktion
6. Taktiles Zeichnen

**Teil 2**
- Anwendungsbeispiel
	- Taktile Diagramme
	- (Gebäude)Karten
# Teil 1:
## 1 Grundlagen Grafiken
- verschiedene Grafiktypen und Anwendungszwecke

### Grafiktypen
unterschiedliche Typen mit teils charakteristischen Elementen und unterschiedlichen Funktionen (Zweck) und Kontexten
![[Pasted image 20240116050328.png]]
![[Pasted image 20240116050404.png]]
## 2 Zugängliche Grafiken
- Grafiken => Barriere v.a. für Menschen mit **Blindheit** und **Sehbeeinträchtigung**
- Auch für Menschen mit weiteren Beeinträchtigungen herausfordernd, z.B. Menschen mit **kognitiven Beeinträchtigungen**
- **Kulturell** unterschiedliche Bedeutung von Grafiken (z.B. Farben, Leserichtung, etc.)
- Zugang zu Grafiken unausweichlich für gleichberechtigte, gesellschaftliche Teilhabe, z.B. für Bildung, soziale Bereiche, Social Media, Kultur & Kunst…
- gleichwertigen Zugang durch **alternative Darstellungsweise** des Inhalts gewähren

### Ansätze
> Grafiken für Menschen mit Beeinträchtigungen zugänglich gestalten.

![[Pasted image 20240116073526.png]]
-> Teil 1 剩余部分对前两种方式进行详细说明, 我会在每种方法开始前插入这张图

## 3 Bildbeschreibungen
> Def.: *Alternative* Bildbeschreibungen für Menschen mit Blindheit oder Sehbeeinträchtigung.
-> Alternativen sind in Textform bereitzustellen für jeden Nicht-Text_Inhalt.
-> 使用屏幕阅读器可以朗读powerpoint中图片的替代文字

### Allgemeine Richtlinien -> 对练习很重要
**Wann beschreiben?**
- Prinzipiell: *alle* Nicht-Text-Inhalte
- Ausnahme: reine *Schmuckgrafiken*
- sonst: mindestens Alternativtext unterstützen

**nicht beschrieben werden müssen:**
- Schmuckgrafiken (reine Dekorationselemente)
- Informationen, die auf andere Weise (z.B. Bildunterschrift, umliegender Text) zugänglich sind.

**Was beschreiben?** 
- Grafiktyp
- Absicht/Zweck des Bildes
- Ort, Objekte, Gebäude, Menschen
- Farben (wenn relevant)
- Atomsphäre
- Handlungen
- Kontext ()
![[Pasted image 20240116075745.png]]

**Context is the key**
- Inhalte der Beschreibung hängen vom Kontext des Bildes ab.
- relevant?
- verfügbare Informationen im Kontext

**Wie beschreiben?**
- vom Allgemeinen zum Speziellen
- zielgruppenangepasst (Vokabular, Expertise...)
- objektiv (keine Interpretationen, Meinungen, Auslassungen oder Emotionen)
- kurz, prägnant und verständlich -> inhaltstragende Wörter, Aufzählungen
- Ton und Sprache (Terminologie, beschreibend, aktiv Verben)
 
大致流程:
![[Pasted image 20240116080404.png]]

### Detailgrad
**unterschiedliche Beschreibungen bereitstellen:**
- unterscheidbar nach Detaillierungsgrad
- Nutzende können selbst entscheiden, ob Grafik für sie *relevant* ist und detaillierte Informationen von *Interesse* sind.
- Drill-Down Organisation:
	- 1. **Alternativtext** : *kurzer* *Überblick* max. 1-2 Sätze
	- 2. **Bildunterschrift** : *kurze* Beschreibung mit zusätzlichen Informationen, die nicht auf visuelle Elemente fokussiert sein muss (für alle Menschen sichtbar)
	- 3. **Bildbeschreibung** : *detaillierte* Beschreibung der Bildinhalte, was den Zugang zu visuellen Konzepten unterstützt.

-> 按照包含细节的多少, 划分为三类

### Methoden zur Bildbeschreibung
#### Bereitstellung mit HTML
![[Pasted image 20240116082556.png]]
![[Pasted image 20240116082643.png]]
![[Pasted image 20240116082726.png]]
![[Pasted image 20240116082811.png]]
![[Pasted image 20240116082841.png]]

#### Bereitstellung mit SVG
##### Barrierefreies SVG
- Erhöht Verständnis von Grafiken für alle Betrachtenden
- Lesbarkeit ohne Grafikprogramm möglich
- alle Elemente semantisch kennzeichnen:
	- wenn möglich Basistypen statt `path` verwenden (z.B. `circle, rect, line, polygon...`) 
	- Textalternativen und -beschreibungen: title, desc, meta
	- Gruppierungen von Elementen mit `g` 
	- sinnvolle Wiederverwendung gleichbedeutender separat definierter Elemente mit `use`
	- Objekttransformationen vermeiden (Linienstile, Schriftgröße etc. werden mitskaliert.)
- externe SCG Grafik kann via `<img>`-Tag wie Pixelgrafik eingebunden werden (Alternativtext).
	- `<img src="beispiel.svg" alt ="eine beispielhafte Grafik"/>`
- Inline SVG : `<Title>` und `<Desc>` zur Beschreibung der Elemente + arialabelledby im svg-tag (Besserer Browsersupport)
- `tabindex` kann für *einzelne* Elemente festgelegt werden, sodass SVG-Datei **navigierbar** wird
![[Pasted image 20240118210310.png]]

#### Bereitstellung mit Editoren
##### Bildbeschreibung hinzufügen
- von diversen Programmen bspw. Word,  Powerpoint, Acrobat Reader DC unterstützt
- Beschreibungen gegebenenfalls in separater Datei mitliefern (mit entsprechendem Verweis darauf.)
- ![[Pasted image 20240118210609.png]]

#### Herausforderungen
- Oft nur eine mögliche Interpretation -> subjektiv, abhängig von Wissen und Fähigkeiten des Erstellenden.
- Notationscharakteristik schwer verbalisierbar.
- z.B. komplexe Darstellungen, Schalkreis(Elektrotechnik), UML, Aufbau Experiment
- Detaillierungsgrad (Farben? Hintergrundwissen? -> 考虑读者的感受)
- Erstellung sehr aufwändig, bspw. AGSBS -> meist manuelle Erstellung von Personen mit Fachexpertise
- Verstehen komplexer Beschreibungen is anstrengend und benötigt viel Zeit.

## 4 Taktile Grafiken
### Einführung und Gestaltung
![[Pasted image 20240118213753.png]]
触觉感受, 首先尝试把手指静止放在某种材料上, 然后开始移动, 看感受有什么不同。-->MBO中讲的类似, 触觉需要西东手指

### Definition: Taktile Grafiken
> fühlbare Grafiken, die mit dem Tastsinn wahrgenommen werden können.
> bestehen aus erhabenen Punktsymbolen, Linien und Texturen -> Unterscheidung 
> häufig in Kombination mit Braille-Beschriftungen.
> verschiedene Erstellungsverfahren und Techniken verfügbar

--> 下面不同类型的Grafiken需要大致掌握每种的特点。别混淆
#### Distribution Schwellpapier
- Druck auf Spezialpapier -> gleichmäßig erhitzen
- **Heiligkeitswert** entspricht Schwellhöhe: Je dunkler, desto höher geschwellt.

**Vorteil**: 
- Handelsübliche Laserprinter verwendbar
- Glatte Linienverläufe
- Unterschiedliche Reliefhöhen
- Hohe Auflösung

**Nachteil**:
- Schlecht für Braille-Schrift -> 因为是用Fuser对智障进行加工, 不适用盲文的打印, 有点大材小用的感觉
- keine harten Kanten
- benötigt Spezialgerät zum "Schwellen" (Fuser,  熔凝器)
- Schwellpapier ist preisintensiv (ca. 1€ pro A4 Blatt)
![[Pasted image 20240118215843.png]]
#### Distribution Braille Drucker
- Für Braille-Schrift-Druck **optimiert**
- Punktabstand lässt sich verändern (Braille-Schrift, äquidistant)

**Vorteile:**
- tiefe Prägung
- variable Auflösung
- kann aus Text generiert werden
- Duplexdruck möglich -> 双面打印

**Nachteile:**
- geringe Auflösung (ca. 10 dpi)
- nur eine Reliefhöhe

![[Pasted image 20240118220430.png]]

#### Distribution Taktile Druker
- für Grafikdruck optimiert
- automatische Umsetzung von Helligkeitswerten in Reliefhöhen. (Reliefkarte:  地形图)

**Vorteil:**
- 8 Stufen von Prägungstiefen (praktisch max.3 unterscheidbar)
- scharfe Kanten und Linien
- große Papierformate
- kombinierbar mit Schwarzschrift, Farben

**Nachteil:**
- Auflösung (ca. 20 dpi)
- kostenintensive Hardware
- unüblicher als Braille-Druck -> geringe Verfügbarkeit

#### Distribution Kollagen
Bildkomposition aus verschiedenen Materialien

**Vorteile:**
- kann sehr detailliert und **realitätsnah** gestaltet werden
- Verwendung verschiedener Oberflächenstrukturen möglich.

**Nachteile:**
- hoher Erstellungsaufwand
- Vervielfältigung aufwendig --> 很难制作副本, 每件样品都是独一无二的
![[Pasted image 20240120143931.png]]
#### Distribution Punktreliefs
- Manuelles Prägen von Punkten in *Zinkblech*
- Vervielfältigung der *punzierten* Platte im Blindendruck (用样板打出（冲出）标志（Edelmetalllegierungen贵金属合金)
- Ergebnis ist ein Papierblatt analog einer Punktschriftseite

**Vorteile:**
- schnelle und kostengünstige Vervielfältigung

**Nachteile:**
- keine Fehlerkorrektur möglich
- Zinkverbrauch
![[Pasted image 20240120144057.png]]

#### Distribution Folienreliefs
##### 1. Erstellung einer Basismatrize
- als Kollage
- durch Plotten von Materialschichten
	- Auflösung einer Vektorgrafik in Schnittmasken mittels CAD
	- Ebenenzüge werden mittels Schneideplotter oder CAD-Fräse erstellt
	- auf Basisplatte zu einer Master-Matrize kombiniert
	- nachträgliche Detaillierung
![[Pasted image 20240120144816.png]]
##### 2. Tiefziehen einer Folie. --> 成型过程
- Matrize im Vakuum-Tiefziehverfahren(真空)  vervielfältigt (Hitzebeständigkeit)
- Kunststofffolien über Matrize eingespannt
- Erhitzen der Folien bis sie plastisch ist
- Ansaugen der weichen Folien durch eine Vakuumpumpe
- nach Abkühlung formstabiles Relief.
![[Pasted image 20240120151447.png]]

#### Distribution 3D-Modelle
3-dimensionale Körper zur Vermeidung perspektivischer Abbildungen (Projektionsbilder in 2D)

**Vorteile:**
- Veranschaulichung von Volumina möglich
- Realitätsnahe, haptisch angepasste Modelle
- beliebige Druckhöhen und Detailgrad möglich
- auch Braille-Schrift druckbar
- Einsatz von Farben möglich
- unterschiedliche Materialien

**Nachteile:**
- zeitintensive Erstellung der 3D-Modelle
- lange Druckzeiten
- Erstellung erfordert Expertise

### -> Verbreitung taktiler Medien
![[Pasted image 20240120151859.png]]
->了解趋势

### Erkundung taktiler Grafiken
- muss erlernt werden (meist in Schule)
- Kognitiver Prozess: Zusammensetzung eines Bildes aus vielen Einzelbildern
- unterschiedliche **Strategien** zum Bildverständnis
- Minimalverständnis des **Grafiktyps** wichtig
- meist Braillekenntnisse erforderlich

#### Erkundungsstrategien
##### 1. Braille Lesen
- Beide Hände mit 4 Fingern -> Unterstützung beim Verfolgen der Zeile
	- ![[Pasted image 20240120152757.png]]

- Linker Zeigerfinger referenziert und rechter Zeigerfinger liest.
	- ![[Pasted image 20240120152903.png]]
- Linker Zeigerfinger liest zur Mitte, danach rechter Zeigerfinger:
	- ![[Pasted image 20240120152947.png]]
##### 2. Initiales Abtasten
- Vor der detaillierten Erkundung -> initiales Abtasten mit beiden Händen 
	- um Überblick zu erfassen:
		- Größe
		- Ausmaß
		- Grafiktypen
		- ...

##### 3. Linienverfolgung (Edge-Strategy)
Erfassen konkrete Umrisse, Formen und Figuren durch Abfahren der Außenlinie -> in Schulen vermittelte Strategie zur **Objekterkennung**
![[Pasted image 20240120153232.png]]

##### 4. Systematische Strategien (horizontales / vertikales Erkunden)
![[Pasted image 20240120153314.png]]

##### 5. Perimeter / Speicherrad-Strategie
Erkundung rundum einen Point-of-Interest
![[Pasted image 20240120153406.png]]

##### Nutzendeneingenschaften / Kontext
![[Pasted image 20240120154309.png]]

#### Herausforderungen
- fehlender sukzessiver Erkundungsvorgang
- zu großes Format (> A3)
- überladen mit Information
- mangelhafte taktile Unterschied- und Erkennbarkeit
- Braille auf Texturen nicht erkennbar
- zu wenige Tastebenen verwendet (Reliefs)
- fehlende Zeichenerklärung (Legende)

### Richtlinien
#### 1. Wahrung der ursprünglichen Aussage
- Aussage des Bildes darf nicht gefälscht oder geändert werden 
	- keine Informationen weglassen oder hinzufügen

#### 2. Reduzierung der Komplexität
- nur zum Verständnis notwendige Elemente übernehmen
	- -> Schumuchgrafiken, Dekorationen weglassen
- Grafik so einfach wie möglich gestalten
- Änderungen ggf. in **Annotationen** vermerken

#### 3. Texturen, Linienstile und Punktsymbole sparsam verwenden
- Max. 5 Texturen in einer Grafik
- Referenzieren verwendeter Texturen, Linienstile, Symbole und Keys in einer Legende

#### 4. Perspektive vermeiden
- 3-dimensionale Darstellungen in 2-dimensionale überführen
- Überschneidungen von Objekten vermeiden

#### 5. Aufteilen komplexer Objekte
- Zerlegung komplexer Objekte in Teilgrafiken
- Zusammengehörigkeit deutlich kennzeichnen

#### 6. Unterscheidbarkeit
- Mindestabstände und -größen beachten
- Geprüfte Texturensets mit geringer Ähnlichkeit untereinander verwenden

#### 7. Verwendung von Braille-Schrift
- geeignete Brailleschrift in richtiger Schriftgröße verwenden
- *kleine* Braille-Beschriftungen mit einem Rahmen hervorheben
- Braille-Schrift immer horizontal und linkbündig anordnen


# Teil 2
![[Pasted image 20240120163653.png]]

### Erstellung Taktiler Grafiken

- häufig aufwendiger, manueller Prozess
- Richtlinien für taktile Grafiken müssen eingehalten werden
- häufig als Transkription von visuellen Grafiken
- **Optimalfall**: Autor erstellt taktile und visuelle Grafik
![[Pasted image 20240120164130.png]]

**Herausforderungen:**
- Menschen mit Blindheit und Sehbeeinträchtigung selbstständige Erstellung ermöglichen
- Qualitätskontrolle durch Zielgruppe
- Balance: Vereinfachung vs. Informationsgehalt vs. Überblick
- Beachtung der Eigenschaften verschiedener Herstellungsverfahren

### Editoren
- klassische oder spezielle Grafikeditoren (z.B. mit speziellen Texturen) -> Helligkeitswert bestimmt Prägehöhe für z.B. Schwellpapier und Grafikdrucker
- Erstellung taktiler Grafiken mit Hilfe von ASCII-Zeichen -> durch Aneinandersetzen dieser zu einem Bild
- kann mit **Standardeditor** erstellt  und mit Braille-Drucker geprägt werden.
- ![[Pasted image 20240120164818.png]]

### Teilautomatisierte Erstellung
> Häufigster Ansatz: Anpassung einer bestehenden visuellen Grafiken für die taktile Ausgabe (Transkription).

Bsp.: TGA (Tactile Graphics Assistant)
-> Algorithmus zur automatischen Vereinfachung und Optimierung herkömmlicher Grafiken in taktile Grafiken:
- manuelles Eingruppierung der Bilder in Klassen sowie Training
- Separieren und Entfernen von Text innerhalb einer Grafik
- OCR und Umwandlung in Braille
	- ![[Pasted image 20240120165619.png]]

### Mathematische Darstellungen
~ sind Kombination aus definierten Visualisierungstechniken und Illustrationen

**Anwendungsgebiete**: Visualisierung mathematischer Funktionen, Geometrie (Dreieck + Winkel)

**Darstellung**: 
- 2.5D: Hilfslinien und Funktionsverlauf als Relief
- Linearisierung, z.B. von Graphen, ermöglicht selbstständiges Schreiben
- spezielle Darstellungsformen für bestimmte Anwendungsgebiete, z.B. Schachschrift
- ![[Pasted image 20240120170026.png]]

**DotsPlus Braille**
![[Pasted image 20240120170208.png]]
### Vollautomatische Erstellung
- geeignet für. ´wohldefinierte Grafiktypen (z.B. Diagramme)
- *wenige* Anwendungen mit gutem Ergebnis vorhanden 
- Qualitätskontrolle sollte dennoch sichergestellt sein
- Ermöglicht *selbstständige Erstellung* durch Menschen mit Blindheit oder Sehbeeinträchtigung
- Kontrolle des Ergebnisses ohne Ausdruck schwierig
- Bsp. beim Thema "Diagramme"

---
## 5 Taktile Interaktion - Interagieren mit taktilen Grafiken
-> 注意记一下有哪些用于交互的技术

### Audio-haptische Systeme
**Nachteile taktiler Grafiken**
- begrenzte Auflösung -> geringe *Informationsdichte*
- Unterscheidbarkeit der Elemente (max. 5 Texturen / Symbole / Linienstile)
- muss erlernt werden -> hoher kognitiver Aufwand 

### Audio-Taktile Ansätze
- *multimodale* Systeme-> Kombination verschiedener Ein- und Ausgabemöglichkeiten , z.B. haptischer und auditiver Elemente
- Ansprechen verschiedener Sinne
- talking tactile tablet: 
	- Berührungsempfindliches Tablet erlaubt akustische Rückmeldung bei Fingerkontakt
	- Grafikverwaltung durch Barcodes
![[Pasted image 20240202170631.png|400]]

### Technologien
viele Ansätze, um ***Interaktion*** zu ermöglichen:
- *Videobasiertes Tracken* des Fingers bei der Exploration der Grafik
- Verwendung *digitaler Stifter*, die Position erkennen
- Eibetten von *RFID Tags*
- 3D-Druck mit *leitfähigen Filamenten* (导电丝)

### Technik der Interaktion: 
#### AuthOMathic Block System
> Def: taktile/haptische Interaktionstechniken durch Legen von *Blöcken mit Braille-Beschriftung*
- grafische Anordnung wird durch Rahmen auf IVEO gefördert.
- Identifikation der Blöcke am Lesegerät erforderlich.
- Förderung der Kollaboration zwischen sehenden und blinden Erstellenden durch visuelle Darstellung.
![[Pasted image 20240202172023.png|400]]

#### Taktile Displays
- unterschiedliche Auflösung 
- Ein- und Ausgabemöglichkeiten (multimodal: Toucheingabe, Sprachausgabe...)
- ![[Pasted image 20240202172303.png|300]]
- ![[Pasted image 20240202172314.png|500]]

#### Projekt HyperBraille
HyperBraille Display
- 120 * 60 Stifte (2.5mm Punktabstand)
- berührungsempfindlich: 2 Stellen / Modul
- touchsensitiv (multitouch)
- Sprachausgabe

**Forschungsfragen:**
- Wie können taktile Displays gewinnbringend eingesetzt werden?
- Welche Interaktionskonzepte eigenen sich für taktile Displays?
- Wie können *Fenstersysteme* mit taktilen Displays dargestellt werden?

**Eigenschaften:**
- Konzept zur taktilen Darstellung und Interaktion mit Anwendungen (Fenstersystemen)
- Evaluation mit der Zielgruppe innerhalb von empirischen Studien
- Unterstützung thematischer Ansichten für verschiedene Anwendungsfälle
- äquidistantes Braille erfordert Änderungen er Lesegewohnheiten
![[Pasted image 20240202175115.png|350]]

HyperBraille Fenstersystem:
![[Pasted image 20240202175205.png|450]]

**注意:** 结合下图和学过的内容, 思考怎么评估系统的好坏, 这个图不用背
![[Pasted image 20240202175424.png]]

## 6 Zeichensysteme
> Zeichnen ist schwierig, erfordert handwerkliches Können
![[Pasted image 20240202175543.png|300]]

Problem: kein Feedback des Gezeichneten

**Ansatz:** Entwicklung von *Werkzeugen* zur Unterstützung des Zeichenprozesses.

### a) Analoge Werkzeuge
知道有这些工具就行

![[Pasted image 20240202175916.png|400]]
![[Pasted image 20240202175951.png|400]]
![[Pasted image 20240202180015.png|450]]
![[Pasted image 20240202180047.png|450]]
![[Pasted image 20240202180219.png|450]]

### b) digitale Werkzeuge - Zeichnen durch Programmieren
> Braille-Buchstaben werden zu Bildpunkten

![[Pasted image 20240202180505.png]]

#### BPLOT 
- Erzeugung von Ausdrucken für Brailledrucker mittels *plotter control language*
	- keine Überprüfung während des Zeichnens möglich
- Abpausen von taktilen Objekten über Touchpad
- ![[Pasted image 20240202180744.png]]
#### IC2D (integrated communication 2 draw)
- Navigation von Malen auf dem Bildschirm mit Hilfe von Sprachausgabe und Musik
- Punktauswahl durch rekursives Schema basierend auf 3 * 3 Gitter (Telefontasten) -> Bedienung durch Tasten 1-9 bzw. Pfeilnavigation
- ![[Pasted image 20240202181356.png]]

#### Taktile Displays
- erlauben Freihandzeichen
- Zugang zu Mathematik
- Eingabefläche = Ausgabefläche
- ![[Pasted image 20240202181706.png|450]]
#### 3D - Drucker
**Line Space**
- Erkundung großflächiger taktiler Inhalte
- Steuerung eines 3D-Druckers mit Gesten oder Sprache
- ermöglicht direkte Interaktion
- ![[Pasted image 20240202181849.png|400]]

### Zusammenfassung
|  | Analog | Digital |
|----| --------|-------|
|Pro | - schnell und einfach <br>- günstig <br>- detaillierte und naturgetreue Darstellung möglich |- gute Fehlerkorrektur<br>- hohe Veränderbarkeit und Reproduzierbarkeit<br>- leichte Distribution | 
|Kontra |- schwierige Fehlerkorrektur<br>- schwer reproduzierbar<br>- wenig Unterstützung bei **Zeichnen** |- erfordert hohe kognitive Ressourcen<br>- begrenztes Anwendungsgebiet<br>- Spezialequipment (Hardware) notwendig -> Kosten  |



