-> Prüfen der Barrierefreiheit: die in der VL aufgelisteten Evaluationsmethoden:
- [[#E-Methode Evaluieren mit Benutzern]]
- [[#E-Methode Manuelle Prüfung der Barrierefreiheit]]
- [[#E-Methode Automatisiertes Prüfen von Barrierefreiheit]]
- [[#E-Methode Simulation]]
- [[#E-Methode Barrier Walkthrough]]

## **Kriterien von unterschiedlichen Methoden:**
- Vollständigkeit: wie umfangreich ist Barrierefreiheit erfasst
	- -> false negative, 既然是检验, 就要考虑4个标准。这里检验无障碍的范围, 那么正常人也要考虑在内
- Korrektheit: falsche Warnungen (false positive)
- Detaillierungsgrad: automatische / manuelle / generische Tests
- Anpassbarkeit: Tool an eine Webseite angepasst ?
- informativ: genügend aktuelle Infos
- Kosten, Reliabilität, Sprache... 

# E-Methode: Evaluieren mit Benutzern

- Labortest: Thinking-Lound-Potokoll
- Sonderfall: Remote Usability Test
## Mockup/Prototyp
> frühe Evaluation: *Mockup*
- taktile Mockups für blinde Benutzer möglich 
	- 2D: Brailledrucke
	- 3D: Holz, Karton, Papier
	- ![[Pasted image 20240205110024.png|300]]
> späte Evaluation: *Prototyp*
- Aufzeichnung von entfernten und lokalen Abläufen möglich
- Aufzeichnung der AT wird derzeit kaum unterstützt
	- Audio über Mikrofon
	- Braille über Kamera

## Ethik: Helsinki Deklaration
- für medizinische Experimente
- E-mail (E-Mail für blinde Menschen gut geeignet: da **Unterschrift** und **Konsenserklärung** einholen ist möglich)

# E-Methode: Manuelle Prüfung der Barrierefreiheit
## Ablauf der manuellen  Evaluation( WAVE Toolbar)
initiale Form -> [[#Sichten|manueller Evaluationsprozess]] -> Bericht
### Kriterien
[[#**Kriterien von unterschiedlichen Methoden **]]
### Sichten
- Checkpoints/ [[Vorlesung 3 - Evaluation#Kriterien|Kriterien]]
- Evaluationsanweisungen
- Seite mit CSS
- Code Ansicht
- Evaluations Ergebnisse
- vielfältige Browser und Hilfsmittel und Tools

### Besonderheiten von Manuelle  Evaluation
- Farbe
- CSS abschalten (Textlesbarkeit bestimmen)
- Lineraisierung (text-only)
- Textlesbarkeit bestimmen
	- Einsatz von CSS im Quellcode überprüfen
- Textverständlichkeit prüfen
- WebFormator linearisiert
- Struktur evaluieren
	- Überschriften: Quellcode filtern und einblenden
	- Verweise: Zählung einblenden
	- Listen: Quellcode filtern und einblenden
- Grafik evaluieren: Alt-Text
- Dynamische Inhalte: alle zeitlich Änderungen spätestens nach wenigen Sekunden über Schalter kontrollierbar?
- Interaktion und Formulare
	- WAVE Toolbar erlaubt Visualisierung von *Regionen* und Mark-up in der Browseransicht
	- ![[Pasted image 20240205114626.png|400]]
- Inspektion für Javascript (Firefox Accessibility Extensions (FAE)
	- Untersuchung der ARIA Widgets (Role, Tab Index, Wert)

### Prüfwerkzeuge fehlen für
- Audio (Spracherkennung möglich, jedoch nur bei isolierten Sprechern anwendbar)
- Video: Manuelle Erstellung von Untertiteln -> automatische Übersetzung
- Komponenten / Plugins
- Interaktion: Navigation nicht genügend sicher bewertbar

# E-Methode: Automatisiertes Prüfen von Barrierefreiheit
## Automatisiertes Testen
Einige Eigenschaften von Barrierefreiheit lassen sich automatisiert prüfen, dazu ist notwendig:
### 要点
- Definition einer Teilmenge von [[Vorlesung 3 - Evaluation#Beschreibung von Richtlinien|Prüfregeln]]
	- spezifisch vs. allgemein
- Eineindeutige Referenz auf das Testobjekt
	- statisch vs. dynamisch
- Berichtsgenerierung
### Arten von autom. Werkzeugen
- Evaluationswerkzeuge untersuchen Seiten **statisch**
	- **allgemein**, eventuell nach mehreren Richtlinien
	- **speziell**, z.B. nach ausreichendem Farbkontrast
- Reparaturwerkzeuge: darüber hinaus in den HTML Text einzugreifen
- Filter- und Transformationswerkzeuge kritisieren und unterstützen den Benutzer bei der Analyse direkt

### Fehlerquellen in autom. Tests
- Fehlerberichte 
	- zu vorsorglich
	- unvollständig
- HTML Erweiterungen werden derzeit nicht geprüft
	- SMIL. TIME
	- SVG
- meist nicht für ganze Websites anwendbar
- derzeit nicht automatisiert prüfbar, z.B.
	- Navigation
	- einfache Sprache
	- Einfluß des Hilfsmittels

### Websites bewerten: Crawling (爬取)
- URL Sammlung ist meist ein FIFO
- Gefundene URLs müssen normalisiert werden
- VGI Parameter manuell durch Scripte nachbilden
![[Pasted image 20240205121048.png|400]]
Laden und Parsen einer Seite ist zeitintensiv -> Multithreaded Crawling (加快速度 -> 多线程爬取)
#### HFA und HPA (状态机) zu Modellieren der Navigation
- Ein *Hypertext Finite Automaten* (**HFA**) beschreibt das Internet
- Ein *trail* besteht aus einer Sequenz von Seiten, die besucht werden
- ***Problem***: URLs sind zeitabhängig
- -> 不确定能否获取某个URL中的资源, 那就用probabilistischer Ansatz来描述导航过程。Jeder Zustandsübergang in einem **HFA** wird mit einer Wahrscheinlichkeit beschrieben.
- Es entsteht ein *Hypertext Probabilistic Automata* (**HPA**)，der **HPA** die Navigationsmuster eines Benutzers beschreibt und die Übergangswahrscheinlichkeiten geben wie häufig der Benutzer eine Verknüpfung verfolgt hat.
![[Pasted image 20240205121708.png]]

### Beschreibung von Richtlinien
**![[Pasted image 20240205121811.png]]**
- MAUVE (Mauve erlaubt **eigene** Regeln anzugeben)

### Beschreibungssprachen
- Beschreibungssprachen: Universal Guideline Language (UGL) (自动和手动的权重: integrierte Berichtserzeugung)
- Beschreibungssprachen: Evaluation and Report Language vom W3C ( 谁用了什么规则测试了什么得到了什么)


# E-Methode: Simulation
Simulation von Präsentation bildet Wahrnehungsdefizit e nach
- Sehbehinderung (Netbeans IDE)
- Hörbehinderung 
- physikalischer Behinderung

Informationssuche kann modelliert werden

Tools für Sehbehinderung: 
- aDesigner, 
- Netbeans IDE, Simulation von:
	- Netzhautveränderungen (Farbenblindheit, Linsentrübung, Netzhautausfall)
	- Parkinson : Zitter
	- Dyslexie
	- keine dynamischen Abläufe
# E-Methode: Barrier Walkthrough
> **Heuristische** Methode um Barrierefreiheit zu evaluieren
> Grundidee: Liste von typischen Fehlern überprüfen, Reliabilität betonen
> **Expertentext** im Kontext von Benutzungsszenarien

Schrittfolge:
- Definiere Benutzerprofil (z.B. Art der Behinderung)
- definiere Benutzerszenarios (z.B. Hilfsmittel, Ziele)
- Bestimmung möglicher Barrieren
- evaluiere Seiten
- Auswirkungsgrad schätzen (Auswirkung(wie stark) + Nachhaltigkeit(wie oft))

**Eine Barriere wird beschrieben durch:**
1. die Kategorie der Benutzer und die Art der Behinderung
2. der Typ von Hilfsmittel
3. die Art von Ausfall (wie einschränken)
4. welche Merkmale in der Seite die Barriere erzeugen -> 即使是同样的特征, 也会给不同的群体造成不同的障碍

![[Pasted image 20240205125057.png]]
