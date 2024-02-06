# Einführung
## Barrierefreiheit (Accessibility)
> Def. *Barriere*:
> Einschränkungen bei wichtigen täglichen Aktivitäten (zur Schule gehen, Buch lesen...) vermeiden
> 
> **Nicht** definiert sind: "barrierearm", "zugänglich"
> 
> Barrierefreiheit ist das Ausmaß in dem Systeme oder Dienstleistungen von Menschen im weitesten Sinne genutzt werden können.

### **障碍的产生**
Neue Formen der MC-Kommunikation erzeugen Barrieren, wenn ihre **Adaptierung** nicht bekannt ist, (bspw. GUI->Pixel-Barriere, VR->Nicht-visuelle Immersion, Sprachassistenten->Sprechvermögen als Barriere).

### 区分: Usability vs. Accessibility
- Wahrnehmbarkeit (Multimedien 来传达信息)
- Bedienbarkeit (易用性和可操作性)
- Verständlichkeit (符合用户的认知水平)
- Robustheit (不同的环境和用户需求)

-> 两者有交集
![[Pasted image 20240203160941.png]]
>[!NOTE]
>1. Barrieren entstehen mit neuen Technologien
>2. Demographie bestätigt Anforderungen an Diversität

### Dimensionen digitaler Barrierefreiheit
![[Pasted image 20240203161643.png]]

-> Barrierefreiheit weiter entwickeln: Reifegrad erhöhen
- ![[Pasted image 20240203161803.png]]

## Universelles Design - Design4All
**Was ist ~**
- Breite Nutzbarkeit 
	- -> viele und unterschiedliche Anforderungen
		- -> **WIE?** Verwendung von *Personas* zur Verdeutlichung (inkl. Demographische Abbildung) oder Storytelling
- Flexibilität in der Benutzung 
	- -> vielfältige Ein- und Ausgabeformen
- Einfache und intuitive Benutzung
	- -> ohne weitere Hilfe
- Sensorisch wahrnehmbare Usability Accessibility Informationen
- Fehlertoleranz
	- -> keine **exakte** Eingabe des Benutzers erforderlich
- Niedriger körperlicher Aufwand
- Größe und Platz für Zugang und Benutzung

**Bsp.:** Ein Buch für Alle
![[Pasted image 20240203162541.png]]


## Index of Inclusion
**Index of Inclusion** ist ein Prozess zur Förderung der Inklusion


# Users
-> BFD 的目标群体, 记住这些群体的名字
## Blinde Menschen
### Braille 
- Braille (6/8-Punkt, Basis-, Voll- und Kurzschrift)
	- Übersetzung: Vollautomatische ~ keine triviale Aufgabe
	- #123 = 123, $a=A
	- Von Braille in Schwarzschrift einfach, umgekehrt jedoch nicht
- ~ ist eine Sammlung mehrerer Notationen (Lesen bei Nacht, Musik, Chemie, Mathematik...)
- Der Zeichenaufbau ist **nicht** äquidistant.
#### Papierlose Brailleanzeigen
![[Pasted image 20240203165554.png]]
- elektro-mechanisch ist veraltet
- Heute: Piezokristalle werden mit Keramik und Metallstreifen verbunden

### Screen Reader Konzepte -> Wichtig!!!!
![[Pasted image 20240203165834.png]]
- Screenreader: Screenreader unterstützen Verfolgen, Erkunden (zeilenweise), Routing (Navigation) und Adaptierung (Personalisierung)

### Mobilität blinder Menschen
- Blindenstock und Blindenhund zur Kennzeichnung im Straßenverkehr, inkl. bekannte und unbekannte Wege -> oft Verletzungen
- Elektronische Hilfsmittel:
	- Zusatz am Blindenstock
	- Datenbrillen
	- Mobiltelefon
- Navigationssoftware für Indoor und Outdoor
	- Blindsquare
	- Google pedetrian

- Sprachsynthese: blinde Menschen verwenden Braille und/oder Sprachsynthese als Ausgabemedium sowie die Tasten, Sprache oder Gesten als Eingabegerät

## Sehbehinderte Menschen

- Zoom (放大)
- Bildverfremdung (Kontrastverstärkung und Weitwinkeltechnik )
- Anforderungen an Text ( ̈anderbare Schriftgröße, Hintergrundfarbe, Zeilenhöhe und -abstand) 
- Falschfarben (无法分辨正确的颜色)

### Skalieren von Bildern
- Problem: Beim Vergrößern entstehen Artifakte, z.B. Treppenstufeneffekt
- -> Lösung: SVG

## Gehörlosigkeit (聋哑人！)

- Gebärdensprach, Gebärdenschrift 
- Sprachkompetenz ist niedrig (Grundniveau bei geburtstauben Menschen -> 区分先天性和后天性耳聋, 其他组类似)
- Videotelefonie (mit Gebärdensprach -> Gebärdendolmetscher)
- Probleme mit Text (weil wie Fremdsprache für Gehörlosen)
- Probleme mit vielen Icons (Lösung z.B. Tooltip mit Gebärdensprachevideo)

### Automatisierte Verarbeitung der Gebärdensprache
![[Pasted image 20240203173652.png]]

#### HamNoSys
![[Pasted image 20240203173840.png]]
![[Pasted image 20240203173908.png]]

### Gebärdenschrift / SignWriting
- Graphische Notation für Gebärdensprache
- anwendbar auf nationale Gebärdensprache

### Interaktion mit Gebärden: Zugang zu Icons
- Icons erscheinen leicht verständlich, da bildlich und nicht verbal.
- Aber: viele Icons mit komplexen Funktionen, die oft verbal zu erschliessen sind
- ->**Tooltip** zu bauen. 列举并区分不同的种类

#### Tooltips: Sign Language
![[Pasted image 20240203174737.png]]

#### Tooltips: Human Mouth
![[Pasted image 20240203174851.png]]
#### Tooltips: Detailed Picture
![[Pasted image 20240203174922.png]]
#### Tooltips: Digital Lips
![[Pasted image 20240203175016.png]]
-->满意度和可理解性逐渐提升

## Hörbehinderung

- Hörgeräte bieten
- Sichtbare Sprache: Lippenbewegungen unterstützen das Verstehen

### Untertitelung

- ist keine Transkription fremdsprachlicher Inhalte
- -> Caption vs. Subtitle:
	- Captions are a transcription of dialogue and are primarily used to help viewers who cannot hear video audio. Meanwhile, subtitles provide a translation for viewers who don't understand the language being spoken.
- Untertitelung (Sprecher benennen, Geräusche, Klänge umschreiben, Genauigkeit, Geschwindigkeit)
## Taubblinde Menschen (盲聋)
- Buchstaben mit den Fingern malen (Daktylieren) und abtasten Handfläche (lormen)

### Geräte zum Lormen
> Def.: 
> Das Lormen oder Lorm-Alphabet dient der Kommunikation von Taubblinden mit anderen Menschen. Der „Sprechende“ tastet dabei auf die Handinnenfläche des „Lesenden“. Dabei sind einzelnen Fingern sowie bestimmten Handpartien bestimmte Buchstaben zugeordnet.

- mechanisch
	- Lormen in die Hand
	- Lormhandschuh
- elektronisch
	- Alltagsgeräte:
		- Vibrationsuhr, Wecker, Kissen
		- Wasserstandsanzeiger (Vibration)
		- Küchen-Stoppuhr
	- Tabli: kleine Braillezeile und Display

 
## Leseschwäche - Dyslexie (阅读障碍)
- viel mit hören, da vertauschen der Buchstaben. (视觉上他们可能会把字母颠倒混淆。)

## Sprachbehinderung/Aphasie（语言障碍/如失语症）

- viel mit Bildern
- Bildtastatur
- Bildsprache (z.B. BLISS)


## Körperbehinderung
- Rollstuhlfahrer： anpassbarer Tisch
- Einhändige Bedienung 
- kleine Tastatur, große Tastatur, keine Maus direkt benutzbar aber eine „Kopfmaus“
- Zittern: Wiederholte Anschläge unterdrücken (StickyKeys) (保持按下)