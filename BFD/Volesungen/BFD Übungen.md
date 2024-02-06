# Übung 1
## Ziele
- Wissen aus Vorlesung
- Selbststudium zu **ARIA** und **WCAG**

## ARIA

> Accessible Rich Internet Applications Suite
- Spezifikation der [W3C](https://www.runoob.com/w3c/w3c-intro.html)
- Anreicherung von Mark-up Elementen durch *zusätzliche Information*
- <mark style="background: #ADCCFFA6;">ohne ARIA: -> bestimmte Elemente von Webseiten nicht zugänglich, z.B. dynamische Inhalte & UIs</mark>
- Beschreiben z.B. von Regionen (不同的区域), Navigation, Widgets
- <mark style="background: #ADCCFFA6;">Umsetzung durch **Attribute** </mark>

3 个重要的ARIA 标签, 注意结合HTML语法以及标签的位置:
***Rollen:*** `(roles)`
![[Pasted image 20240116035732.png|475]]

***Eigenschaften:*** `(properties)` (描述的是关系)
- Beschreibung von Elementen
- Auszeichnung von <mark style="background: #ADCCFFA6;">**Beziehungen**</mark>
- Wert bleibt **konstant**

> Name/Beschreibung
> - `aria-descibedby, aria-label, aria-labelledby`

![[Pasted image 20240116040248.png]]

1. `aria-label` 
	1. 用于为一个元素提供一个可读的标签 (Beschriftung)，以描述该元素的目的。
	2. 例子：如果有一个使用图标作为按钮的情况，你可以使用`aria-label`来提供按钮的描述。
```HTML
<button aria-label="Search">
  <img src="search-icon.png" alt="Search">
</button> 
```


1. `aria-labelledby`
	1. 用于将一个元素与一个或多个元素的ID相关联，以作为该元素的标签。
	2. 例子：如果有一个标题和相关的段落，你可以使用`aria-labelledby`将段落与标题关联。 

```HTML
<h2 id="section-title">Section 1: Introduction</h2> 
<div aria-labelledby="section-title"> 
<p>This is the introduction to the section.</p> </div>
```
`<div>`表示的是一个区块控制


1. `aria-descibedby`
	1. 用于将一个元素与提供<mark style="background: #ADCCFFA6;">该元素附加信息的另一个元素</mark>相关联。
	2. 例子：假设有一个包含错误消息的`div`元素，你可以使用`aria-describedby`将错误消息与相应的输入框关联起来。 
```HTML
<label for="username">Username:</label>
<input type="text" id="username" aria-describedby="username-error">
<div id="username-error">Please enter a valid username.</div>
```
`label for`用来描述input对象

![[Pasted image 20240204200101.png]]
***Zustände:*** `(states)`
- veränderliche Zustandsinformation
- Bsp.: `aria-hidden="true"`
	- deaktiviert "Sichtbarkeit" des Elements für Screenreader
	- bspw. für dekorative oder ausgeblendete Elemente wie icons.
	- 用于为了屏幕阅读器隐藏装饰性元素
	- ![[Pasted image 20240116040529.png]]
- `<span>` 标签没有固定的格式表现。当对它应用样式时，它才会产生视觉上的变化。
## WCAG: Web Content Accessibility Guidelines
- Web-Standard des W3C
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
4. Gutachtenerstellung (给出专家意见)

> Aber: **keine** finale Aussage zur Barrierefreiheit basierend auf WAVE möglich!


# Übung 2
# Einleitung
## Barrierefreie Dokumente mit Word & PowerPoint

Vorteile Powerpoint:
- MS Bürostandard
- Präsentationen
- Poster
- Flyer (宣传单页或传单)
- auf andere Office-Programme übertragbar

## Titel, Format und Schrift 

### Titel

- Der Titel ist die erste und wichtigste Information für jede **Folie**.
- Zum Anlegen des Titels muss der<mark style="background: #ADCCFFA6;"> vordefinierte Textrahmen</mark> von PowerPoint genutzt werden.
- Alternativ können Texte durch Höherstufen der Gliederungsebene zum Titel gemacht werden.

Ansicht → Gliederungsansicht → Rechtsklick auf einen Inhalt → Höher stufen

### Format und Schrift

- Schriftart ist frei wählbar, es sollte darauf geachtet werden, dass die Schrift gut lesbar ist und sich die Buchstaben in ihrer Form gut unterscheiden.
- Das korrekte <mark style="background: #ADCCFFA6;">**Dokumentenformat** (bspw. A0 bei Postern) sollte in den *Dokumenteigenschaften*</mark> festgelegt werden.

## Textinhalte  
Alle Textabsätze sollten mithilfe von <mark style="background: #ADCCFFA6;">**Absatzformatvorlagen** (段落样式)</mark> definiert werden. Benutzen Sie dafür die Palette „**Formatvorlagen**“. Für Textauszeichnungen innerhalb von Absätzen sollten **Zeichenformatvorlagen** erstellt werden (z. B. für einen Hyperlink).


### Überschriften

<mark style="background: #ADCCFFA6;">Für Überschriften verwenden Sie die Formate Überschrift 1, Überschrift 2 und Überschrift 3.</mark> 

*Zwischen* zwei Überschriften sollte immer<mark style="background: #ADCCFFA6;"> **Fließtext**</mark> stehen. Bei Überschriften in absteigender Folge sollte keine Ebene übersprungen werden (Beispiel: auf eine Überschrift 1 darf keine Überschrift 3 folgen). 
Die Überschriftformatvorlagen können selbstverständlich Ihren Wünschen gemäß angepasst werden.


### Fließtext
Für Text sollte die <mark style="background: #ADCCFFA6;">**Formatvorlage** *Standard*</mark> eingesetzt werden. Diese kann selbstverständlich Ihren Wünschen gemäß angepasst werden. Es sollte darauf geachtet werden, dass die Schrift gut lesbar ist und sich die Buchstaben in ihrer Form gut unterscheiden.

### Abkürzungen
*Abkürzungen sollten vermieden werden.* 
Ist dies nicht möglich, sollten Abkürzungen ==beim ersten Vorkommen im Text erläutert werden==. 
==Sonst sollten nur Abkürzungen verwendet werden, die im Verzeichnis des **Dudens** aufgeführt werden.
尽量避免，第一次得声明


### Sonderzeichen

Verwenden Sie ausschließlich typografisch korrekte Sonderzeichen, wie etwa ==**„deutsche Anführungszeichen“** – in der Regel erledigt das Microsoft Word automatisch.

## Aufzählungen und Listen

Aufzählungen werden mit der Vorlage *Listenpunkt* formatiert. Die Vorlage *Listenstrich* erlaubt Gliederungen innerhalb einer Auflistung. 

Nummerierte Listen werden mit der Vorlage *Listennr*. formatiert.

## Tabellen
-  Sollten immer als Datentabelle angelegt werden; Bitte nicht als Bild importieren!
-  ==Tabellen sollten einen **Alternativtext** aufweisen, der den *Zweck* der Tabelle beschreibt:==
	- `Rechtsklick auf Tabelle → Form formatieren → Größe und Eigenschaften → Alternativte`
-  Um Tabellen für ==blinde Nutzer== gut wahrnehmbar umzusetzen, sollte darauf geachtet werden, dass **diese einfach strukturiert sind** und eine **Kopfzeile** besitzen. Die jeweiligen ***Spaltenüberschriften*** sollten aussagekräftig, eindeutig und ohne Abkürzungen benannt sein.
-  Bitte nutzen Sie keine sogenannten <mark style="background: #ADCCFFA6;">„Layouttabellen“</mark>, also Tabellen, die nur für die grafische Positionierung von Inhalten dienen. ==Diese sollten unbedingt vermieden werden. Tabellen sollten nur zur strukturierten Darstellung von Datensätzen eingesetzt werden==


## Diagramme, Bilder und Grafiken (Alternativtext festlegen) 

Abbildungen sollten (über den Reiter *Format → Zeilenumbruch*) mit "***Text in Zeile***" eingebunden werden, da es sonst zu Problemen bei der Erkennung in Screenreadern kommen kann. (Word) --> Alternative???


### Diagramme
• Benötigen einen ***Alternativtext***:
*Rechtsklick* **Diag. → Diagrammbereich formatieren → Größe und Eigenschaften → Alternativtext → Beschreibung**
• Zusätzlich sollte für blinde Nutzer die Datentabelle eingebunden werden.
Bilder und Grafiken
• Benötigen einen *Alternativtext*, damit blinde Nutzer den Inhalt der Abbildung wahrnehmen können:
Rechtsklick auf die Grafik → Form formatieren → Größe und Eigenschaften → Alternativtext → Beschreibung
• Bitte den Text im Feld „*Beschreibung*“ eingeben.
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

## Sprache

Einzelne fremdsprachige Worte oder Abschnitte sollten entsprechend gekennzeichnet werden, damit der Screenreader blinden Nutzern die Inhalte richtig intoniert wiedergibt. (标记外语以便于屏幕阅读器正确的使用)

## Metadaten

• Die Dokumenteigenschaften helfen allen Nutzern und Indizierprogrammen bei der Einordnung des Dokumentes.
• Die Metadaten werden festgelegt unter `Datei → Informationen → Eigenschaften`
• <mark style="background: #ADCCFFA6;">Hier sollte zumindest der Titel sowie der Autor gepflegt werden.</mark>

## Barrierefreiheit überprüfen

• Prüfen Sie mit den <mark style="background: #ADCCFFA6;">Bordmitteln内置工具 von PowerPoint</mark> die Barrierefreiheit Ihres Dokumentes
*Datei → Auf Probleme prüfen → Barrierefreiheit überprüfen*
• Zudem bietet die **Gliederungsansicht** einen guten Überblick über alle Textinhalte der Präsentation.
Ansicht → Gliederungsansicht




# Barrierefreiheit bei PDF-Dokumenten herstellen
![[Pasted image 20240204210340.png]]


# Übung 3 - [[Vorlesung 5 - Zugängliche Graphiken|Grafik]]





