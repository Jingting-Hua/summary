---
date: 2024.1.29
aliases:
  - Barrierefreies Web
tags:
  - BFD
---
-> Techniken für Inhalte
# Anforderungen/Barrieren im Web
- Grafik, Audio, Video (Zugänglichkeit)
- Zeitgesteuerte Änderungen
- Eingabe- und Ausgabegeräte (Unabhängigkeit)
- Stand der Technik (Kompatibilität 兼容性)

# Regelungen Barrierefreiheit
## Digitale Barrierefreiheit: WCAG
-> Web Content Accessibility Guidelines
### 4 Bereichen / Prinzipien
- **Wahrnehmbarkeit**: Darstellungen *erfahrbar* (lesbar) gestalten (呈现方式) -> 内容可感知
- **Bedienbarkeit**: Eingaben zur *Steuerung* von Websites und Anwendungen ermöglichen (输入) -> 可控制
- **Verständlichkeit**: Menschen mit *kognitiven Einschränkungen* erreichen -> 降低特殊人群理解障碍
- **Robustheit**: technische *Neuerungen* schließen ältere assistive Technologien nicht aus -> 新旧内容可兼容

### Richtlinien nach WCAG 2
- 14 Richtlinien (所有非文本都有文本替代) -> mit jeweils einzelnen Kriterien
- 注意这14个Richtlinien按照4个领域进行分类, 不用背但是需要理解这4个领域/原则的含义
- Bsp.: [[BFD Übungen#WCAG: Web Content Accessibility Guidelines]] -> 练习里涉及更多内容
- Drei Stufen

# Einteilung nach Barrieren
-> web上潜在的障碍, 其实每部分都很重要, 尤其是需要结合现实思考每种障碍的具体表现形式。

## 1. Farbe: 
1. ausreichender Kontrast (WCAG 2.0 verlangt einen Unterschied der Farbhelligkeit L von 1:3 im sRGB Farbraum)
2. Kontrast (min.  4,5:1)
-> siehe auch [[BFD Übungen#Farben und Kontrast]]
### Farbsehschwäche
- Grün-Farbsehschwäche = Deuteranomalie
- Blauschwäche = Trianomalie
-> Farbe nicht alleine einsetzen, z.B. manche Kombinationen der Farben sind zu vermeiden (Rot-Grün, Gelb-Weiß, Blau-Orange...)

除了使用颜色进行标注以外, 考虑额外添加信息, 例如形状、文本...
![[Pasted image 20240204142027.png|400]]

-> 针对不同的色弱群体, 采用不同的配色方案:
Bsp.: Kartendesign:
![[Pasted image 20240204141435.png]]


## 2. Lesbarkeit von Text 
### Lesbarkeit
> betrifft:
- Erkennbarkeit -> [[#1. Farbe]]
- Nachvollziehbarkeit (Komplexität)
- Verständlichkeit (Satzbau)

> Schriften sind keine Bilder und benötigen [[Vorlesung 2 - Barrierefreies Web#Mark-up for Text|Mark-up]]
- Schriftgröße soll relativ angegeben werden

> Beweglicher Text ist für Screenreader nicht definiert.
- blinken vermeiden oder steuerbar gestalten. -> 可暂停

> Auto-refresh ist abschaltbar zu gestalten

> Textauszeichnungen zur Präsentation wie *kursiv*, **fett** sind durch semantischen Mark-up (strong, em) auch für Screenreader kenntlich zu machen.
> 
> *span* und *div* erlauben Textbereiche darüber hinaus abzutrennen --> Seitenlayout auch beachten

> ASCII Grafik vermieden

### Mark-up for Text
#### Überschriften
- wichtig für Navigation des Screenreader
- bei `<h1>` beginnen
- nach `<h1>` folgend `<h2>` dann `<h3>`

#### Listen
- ohne Mark-up vom Screenreader nicht interpretierbar
- `<ul>` (ungeordnete Liste) oder Gestaltung per CSS

#### Sprachinhalt
Die vorherrschende Sprache soll kenntlich gemacht werden: lang="de"

## 3. Tabellen
- Tabellen werden vom Screenreader serialisiert und es obliegt dem Autor diesen Vorgang zu unterstützen, z.B. durch eine Zusammenfassung oder durch Abkürzungen für Spaltentitel
	- Zusammenfassung: `<summary>`
	- Abk: `<th abbr='Kilometer'>Länge der Grenze in km</th>`
- Elemente in Datentabellen: `<caption><th><td>`
```HTML
<caption>Gemeinsame Grenzen Deutschlands mit 
Anliegerstaaten</caption><!-- 标题 -->
 <thead><!-- 页眉 -->
 <tr><!-- 一行 -->
 <th>Anliegerstaat</th>
 <th>Länge der Grenze<br>(in km)</th>
 </tr>
 </thead>
 <tfoot>
 <tr>
 <td colspan="2">Stand 31.12.2000. Nach Angaben 
der beteiligten Landvermessungsämter</td>
 </tr>
 </tfoot>
 <tbody>
 <tr><th>Dänemark</th><td>67</td></tr><!-- 表头和表格 -->
 <tr><th>Niederlande</th><td>567</td></tr>
 <tr><th>Belgien</th><td>156</td></tr>
 <tr><th>Luxemburg</th><td>135</td></tr>
 <tr><th>Frankreich</th><td>448</td></tr>
 <tr><th>Schweiz</th><td>316</td></tr>
 <tr><th>Österreich</th><td>815</td></tr>
 <tr><th>Tschechische Republik</th><td>811</td></tr>
 <tr><th>Polen</th><td>442</td></tr>
 </tbody>
 <tbody>
 <tr><th>Insgesamt</th><td>3757</td></tr>
 </tbody>
```
![[Pasted image 20240204145512.png]]
### Linearisierbare Tabelle
![[Pasted image 20240204145639.png]]


## 3.  Navigation und Verweise
### Verweise
**WAS**: interaktives Element, meist implizit mit einem Typ versehen
- Steuerung des Dialogs
	- Undo ermöglichen (Shift->Tab)
	- Konsistenz fördern
	- aufgabengerechte "Tab-Folge" durch Typisierung der Verweise und Angabe des `tabindex`
- Bsp.:![[Pasted image 20240204152740.png|300]]
### Navi
![[Pasted image 20240204150006.png]]



#### Benannte Anker  (Navi in der Seite)
- Navigation innerhalb einer Seite, auch verdeckt.
- Bsp.:
	- Sprünge am Anfang einer Seite zu späteren Abschnitten
	- Sprung zurück zum Anfang (in einer langen Seite)
- Für Screenreader sinnvoll am Anfang oder am Ende einer Seite

#### Navigation zwischen Seiten
- unterschiedliche Navigationsmöglichkeiten einsetzen:
	- Inhaltsverzeichnis
	- Sitemap
- Beschriftungen für Verweise sollen eine **Bedeutung** wiedergeben, auch wenn der Kontext nicht erfasst wurde
- Linktexte sollen knapp gehalten sein:
- Bsp.:
- ![[Pasted image 20240204151754.png|400]]
#### Breadcrumb trails (面包屑导航)
- Weg oder Struktur darstellen
- Fehlerrobustheit fördern
- auch als *Verweise* ohne Probleme für Screenreader
![[Pasted image 20240204151948.png]]

### Suche
![[Pasted image 20240204152128.png]]
-> 大体了解, 什么情况下添加搜索功能是有助于导航的

## 4. Graphik
### Alternativtexte
-  `alt=""` wird vom Screen Reader ignoriert, 
-  alternativ: `title` für ausführliche Darstellung verwenden
- `longdesc` wird von Screenreadern nicht immer beherrscht und in HTML5 abgeschafft.
- Inhalt der Alternativtexte:
	- Objekt, Gebäude, Menschen im Bild nennen
	- Was passiert im Bild
	- Zweck des Bildes
	- **Farben** im Bild
	- Emotionen, Atmosphäre des Bildes
	- Informationen zu Ortsangaben mit Bezug zum Bild
	- -> 先描述最重要的信息, 并且不能太长
这里还需要有代码例子

### Lange Beschreibungen
![[Pasted image 20240204165542.png]]

## 5. Multimedia
### WCAG 1.2: Audio & Video
-  Aufzeichnungen von **Audio** erhalten eine *Textalternative* -> Stufe A
-  Aufzeichnungen von **Video** erhalten entweder eine *Textalternative* oder eine zeitlich abgestimmte *Audioalternative* -> Stufe A
	- Transkript in Textform ist keine Bildbeschreibung (Word, Html, Pdf)
	- in den Sprechpausen den visuellen Eindruck erklären -> Audiodeskription
- Aufzeichnungen von **Video** erhalten *Untertitel* -> Stufe A
- Aufzeichnungen von **Audio** erhalten eine zeitlich abgestimmte *Alternative in Gebärdensprache* -> Stufe AAA

### Audio
- Verbale und nichtverbale akustische **Inhalte** werden für gehörlose Menschen umgesetzt (Kanaltrennung von Sprache und Hintergrundgehäuschen und Musik)
- Aufbereitung der Inhalte:
	- einfache Satzstruktur
	- verständlicher Untertitel 
	- keine Worttrennung
	- relevante Lieder usw.
	- maximal 2 Zeilen pro Untertitel

### Video / Animation
??


## 6.  Dynamischer Inhalt
-  ~ entstehen meist bei Verwendung von **Javascript**
	- Dynamik ist abhängig oder unabhängig von Benutzereingaben (Timer)
- Screenreader können keine Fokusverfolgung realisieren, da dies keine Eigenschaft des Mark-up ist.
- Tastaturbedienung wird meist nicht vorgesehen

### AJAX ermöglicht Dynamik
-  AJAX (asynchrones Laden von Webinhalten während Website angezeigt wird)
- ![[Pasted image 20240204172728.png]]
-  Beschreibung mittels [[Vorlesung 2 - Barrierefreies Web#ARIA|ARIA]] (z.B. aria-label, aria-hidden)

### ARIA
- **bisher**: Seiten sollen ohne Javascript bedienbar sein (`<noscript>`) 
	- Accessible Rich Internet Applications beschreiben Aufbau des OSM
- Mark-up und Javascript sollen Zugänglichkeit zu **Widgets** herstellen (roles)
	- aria的正确用法:
	- each **element** or **widget** is marked with full and corrected semantics that fully describes it's behavior -> using element names or roles
	- The **relationship** between elements and groups are known
	- **States**, properties and relationships are valid for each elements behavior and are accessible via the DOM
- Roles werden in RDF beschrieben.
-> aria 和landmarks的例子:
![[Pasted image 20240204174543.png]]
### Landmarks
![[Pasted image 20240204174348.png]]

### ARIA Live regions
- `aria-describedby=id list` :wird verwendet, um eine Region mit einer Beschreibung zu verknüpfen(提供Beschreibung)
- `aria-labelledby=id list` : wird eine Region mit seinen Labels verknüpft
- `aria-atomic=false`: ob der Screenreader die Live-Regionen als Ganzes präsentieren soll, auch wenn sich nur ein Teil dieser Region ändert. Default = false -> 默认不看作整体
- `aria-relevant=[list of changes]`: welche Art von Veränderungen relevant für eine Live-Region sind

## 7. Interaktion
- Tastaturbedienung
	 - Accesskey (快捷键) erlaubt interaktive HTML Elemente mit Tastaturunterstützung zu versehen.
- Ereignisbehandlung
	- logische Behandlung vs. geräteabhängige Behandlung
- Popup-Fenster vermeiden

## 8. Formulare 
- Beschriftung und Bedienelement assoziieren 
- Vorbesetzen der leeren Texteingabefelder ist abhängig vom Screenreader

-> Assoziierte Beschriftung
![[Pasted image 20240204180751.png]]
 ```HTML
<label for="name">Name:</label>
<input id="name" type="text">
```
 

>[!note]
>推崇Linearisierbare Tabellen