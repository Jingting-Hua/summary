
# Evaluieren mit Benutzern

- Labortest: Thinking-Lound-Potokoll
- Remote Usability Test
- Mockup/Prototyp
- E-mail (E-Mail für blinde Menschen gut geeignet: da Unterschrift und Konsenserklärung einholen ist möglich)

## Manuelle  Evaluation( [[BFD Übungen#Technik WAVE Browser Extension|WAVE Toolbar]])

### Kriterien

- Vollständigkeit: wie umfangreich ist Barrierefreiheit erfasst
	- -> false negative, 既然是检验, 就要考虑4个标准。这里检验无障碍的范围, 那么正常人也要考虑在内
- Korrektheit: falsche Warnungen (false positive)
- Detaillierungsgrad: automatische / manuelle / generische Tests
- Anpassbarkeit: Tool an eine Webseite angepasst ?
- informativ: genügend aktuelle Infos
- Kosten, Reliabilität, Sprache... 

### Sichten

- Checkpoints/ [[Vorlesung 3#Kriterien|Kriterien]]
- Evaluationsanweisungen
- Seite mit CSS
- Code Ansicht
- Evaluations Ergebnisse
- vielfältige Browser und Hilfsmittel und Tools

### Besonderheiten von Manuelle  Evaluation

- CSS abschalten (Textlesbarkeit bestimmen)
- Lineraisierung (text-only)
- Struktur evaluieren (标题)
- Grafik evaluieren: Alt-Text
- Interaktion und Formulare
- Inspektion für Javascript (Firefox Accessibility Extensions (FAE)

### Prüfwerkzeuge fehlen für

- Audio (Spracherkennung)
- Video: Manuelle Erstellung von Untertiteln


## Automatisiertes Testen

### 要点

- Definition einer Teilmenge von [[Vorlesung 3#Beschreibung von Richtlinien|Prüfregeln]]
- Eineindeutige Referenz auf das Testobjekt
- Berichtsgenerierung
### Arten von autom. Werkzeugen
- Evaluationswerkzeuge
- Reparaturwerkzeuge
- Filter- und Transformationswerkzeuge
### Crawling (爬取)
Multithreaded Crawling (加快速度)
### HFA und HPA (状态机)

Es entsteht ein Hypertext Probabilistic Automata (HPA)，der HPA die Navigationsmuster eines Benutzers beschreibt und die Übergangswahrscheinlichkeiten geben wie häufig der Benutzer eine Verknüpfung verfolgt hat.
- HFA
![[Pasted image 20240206112157.png]]
- HPA
![[Pasted image 20240206112258.png]]
### Auswahl der Werkzeugen 
- TAW
	- Mehrere Darstellungsformen
	- Nach Richtlinien grupiert
![[Pasted image 20240206113424.png]]
- Monitoring Systeme
	- Monitoring von Barrieren über einen Zeitraum
![[Pasted image 20240206113602.png]]
### Beschreibung von Richtlinien

- MAUVE (Mauve erlaubt eigene Regeln anzugeben)

- Beschreibungssprachen: 
	- <mark style="background: #ADCCFFA6;">XML-Prüfregeln</mark> in Nauticus bzw. Magenta für Usability Guidlines for the Blind [Leporini]
	- ![[Pasted image 20240206114424.png]]
	- Universal Guideline Language (UGL) (自动和手动的权重: integrierte Berichtserzeugung)
		- integrierte Berichtserzeugung
	- Beschreibungssprachen: Evaluation and Report Language vom W3C durch TAW unterstützt ( 谁用了什么规则测试了什么得到了什么)
		- ![[Pasted image 20240206115040.png]]
		- Wer hat den Test durchgeführt (Assertor)
		- Welche Resource wurde getestet (Test Subject)
		- Welches Kriterium wurd angewendet (Test criterion)
		- Was war das Ergebnis (Test Result)


## Simulation
Simulation von Präsentation bildet Wahrnehungsdefizite nach
- Sehbehinderung 
	- (Netbeans IDE)
		-  Simulation von Netzhautveränderungen
		- Parkinson
		- Dyslexie
	- Simulation der Effekte für die visuelle Präsentation
		- VIS simuliert
- Hörbehinderung 
	- Simulation der akustischen Wahrnehmung
- Sim. physikalischer Behinderung 
	- Modellierung des Verhaltens bei der Eingabe per sequentieller Tastatur („Scanning keyboard“)
		- Wahrnehmungsmodell 
		- Kognitives Modell entscheidet auf Basis visueller Wahrnehmung
		- 8 Richtungen werden im motorischen Modell berücksichtigt
## Barrier Walkthrough

- Definiere Benutzerprofil (z.B. Art der Behinderung)
- definiere Benutzerszenarios (z.B. Hilfsmittel, Ziele)
- Bestimmung möglicher Barrieren
- evaluiere Seiten
- Auswirkungsgrad schätzen (Auswirkung(wie stark) + Nachhaltigkeit(wie oft))