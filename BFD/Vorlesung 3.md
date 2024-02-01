
# Evaluieren mit Benutzern

- Labortest: Thinking-Lound-Potokoll
- Remote Usability Test
- Mockup/Prototyp
- E-mail (E-Mail für blinde Menschen gut geeignet: da Unterschrift und Konsenserklärung einholen ist möglich)

## Manuelle  Evaluation( WAVE Toolbar)

### Kriterien
- Vollständigkeit
- Korrektheit
- Detailierungsgrad
- Anpassbarkeit
- Informativ: genügend aktuelle Informationen
- Sprache
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
### Beschreibung von Richtlinien
- MAUVE (Mauve erlaubt eigene Regeln anzugeben)
- Beschreibungssprachen: Universal Guideline Language (UGL) (自动和手动的权重: integrierte Berichtserzeugung)
- Beschreibungssprachen: Evaluation and Report Language vom W3C ( 谁用了什么规则测试了什么得到了什么)


## Simulation
Simulation von Präsentation bildet Wahrnehungsdefizit e nach
- Sehbehinderung (Netbeans IDE)
- Hörbehinderung 
## Barrier Walkthrough

- Definiere Benutzerprofil (z.B. Art der Behinderung)
- definiere Benutzerszenarios (z.B. Hilfsmittel, Ziele)
- Bestimmung m ̈oglicher Barrieren
- evaluiere Seiten
- Auswirkungsgrad sch ̈atzen (Auswirkung(wie stark) + Nachhaltigkeit(wie oft))