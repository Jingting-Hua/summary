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
- gleichwertigen Zugang durch **alternative Darstellungsweise** des Inhalts gewähren (访问图片的公平性和文化差异)

### Ansätze
> Grafiken für Menschen mit Beeinträchtigungen zugänglich gestalten.

![[Pasted image 20240116073526.png]]
-> Teil 1 剩余部分对前两种方式进行详细说明, 我会在每种方法开始前插入这张图

## 3 Bildbeschreibungen
> Def.: *Alternative* Bildbeschreibungen für Menschen mit Blindheit oder Sehbeeinträchtigung.
-> Alternativen sind in Textform bereitzustellen für jeden Nicht-Text_Inhalt.
-> 使用屏幕阅读器可以朗读powerpoint中图片的替代文字

### Allgemeine Richtlinien -> 对练习很重要

**Wann beschreiben?** (不是装饰才，或者说要描述)
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
- <mark style="background: #ADCCFFA6;">Kontext ()</mark>
![[Pasted image 20240116075745.png]]

**Context is the key**
- Inhalte der Beschreibung hängen vom Kontext des Bildes ab.
- relevant?
- verfügbare Informationen im Kontext

**Wie beschreiben?**
- vom Allgemeinen zum Speziellen
- zielgruppenangepasst (Vokabular, Expertise...)
- <mark style="background: #ADCCFFA6;">objektiv (keine Interpretationen, Meinungen, Auslassungen oder Emotionen)</mark>
- kurz, prägnant und verständlich -> inhaltstragende Wörter, Aufzählungen
- Ton und Sprache (Terminologie, beschreibend, aktiv Verben)
 

### Detailgrad

**unterschiedliche Beschreibungen bereitstellen:**
- Drill-Down Organisation:
	- 1. **Alternativtext** : *kurzer* *Überblick* max. 1-2 Sätze
	- 2. **Bildunterschrift** : *kurze* Beschreibung mit zusätzlichen Informationen, die nicht auf visuelle Elemente fokussiert sein muss (für alle Menschen sichtbar)
	- 3. **Bildbeschreibung** : *detaillierte* Beschreibung der Bildinhalte, was den Zugang zu visuellen Konzepten unterstützt.

-> 按照包含细节的多少, 划分为三类

### Methoden zur Bildbeschreibung
#### Bereitstellung mit HTML

##### Alt属性
![[Pasted image 20240116082556.png]]
对于图片的必要组成部分
##### Longdesc
![[Pasted image 20240116082643.png]]
- 视觉上不可见
- 不是所有屏幕阅读器都接受
##### Link 
![[Pasted image 20240116082726.png]]
- 图像旁边的链接
- 没有语义连接
##### aria-describedby
![[Pasted image 20240116082811.png]]
- 和介绍自己的对象链接在一起
- 所有人可见！
##### Bild im Linktext
![[Pasted image 20240116082841.png]]

#### Bereitstellung mit SVG
##### Barrierefreies SVG
- Erhöht Verständnis von Grafiken für alle Betrachtenden
- <mark style="background: #ADCCFFA6;">Lesbarkeit ohne Grafikprogramm möglich</mark>
- <mark style="background: #ADCCFFA6;">alle Elemente semantisch kennzeichnen</mark>:
	- wenn möglich Basistypen statt `path` verwenden (z.B. `circle, rect, line, polygon...`) 
	- Textalternativen und -beschreibungen: title, desc, meta
	- Gruppierungen von Elementen mit `g` 
	- sinnvolle Wiederverwendung gleichbedeutender separat definierter Elemente mit `use`
	- Objekttransformationen vermeiden (Linienstile, Schriftgröße etc. werden mitskaliert.)
- externe SCG Grafik kann via `<img>`-Tag wie Pixelgrafik eingebunden werden (Alternativtext). (SVG放在外部文件img引用， alt属性 )
	- `<img src="beispiel.svg" alt ="eine beispielhafte Grafik"/>`
- Inline SVG : `<Title>` und `<Desc>` zur Beschreibung der Elemente + arialabelledby im svg-tag (Besserer Browsersupport) (内联混用， desc，title，arialabelledby)
- `tabindex` kann für *einzelne* Elemente festgelegt werden, sodass SVG-Datei **navigierbar** wird
![[Pasted image 20240118210310.png]]

- `<title >`是在网页，或者鼠标悬停上才可见
- `desc`不可见，会描述
- `alt`一般情况也不可见，除非找不到图片

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
- Verstehen komplexer Beschreibungen is anstrengend und benötigt viel Zeit.

## 4 Taktile Grafiken
### Einführung und Gestaltung
![[Pasted image 20240118213753.png]]
触觉感受, 首先尝试把手指静止放在某种材料上, 然后开始移动, 看感受有什么不同。-->MBO中讲的类似, 触觉需要手指

### Definition: Taktile Grafiken
> fühlbare Grafiken, die mit dem Tastsinn wahrgenommen werden können.
> bestehen aus erhabenen Punktsymbolen, Linien und Texturen (点符号，线，以及纹理) -> Unterscheidung 
> häufig in Kombination mit Braille-Beschriftungen.
> verschiedene Erstellungsverfahren und Techniken verfügbar

--> 下面不同类型的Grafiken需要大致掌握每种的特点。别混淆

#### Distribution Schwellpapier （分布膨胀纸）
- Druck auf Spezialpapier -> gleichmäßig erhitzen
- **Heiligkeitswert** entspricht Schwellhöhe: Je dunkler, desto höher geschwellt.

**Vorteil**: 
- Handelsübliche Laserprinter verwendbar (可以使用普通的打印机)
- Glatte Linienverläufe
- Unterschiedliche Reliefhöhen
- Hohe Auflösung (高分辨率)

**Nachteil**:
- Schlecht für Braille-Schrift -> 因为是用Fuser对智障进行加工, 不适用盲文的打印, 有点大材小用的感觉，不适合盲文
- keine harten Kanten
- benötigt Spezialgerät zum "Schwellen" (Fuser,  熔凝器)
- Schwellpapier ist preisintensiv (ca. 1€ pro A4 Blatt)
![[Pasted image 20240118215843.png]]
#### Distribution Braille Drucker(分布式盲文打印机)
- Für Braille-Schrift-Druck **optimiert**
- Punktabstand lässt sich verändern (Braille-Schrift, äquidistant)

**Vorteile:**
- tiefe Prägung
- variable Auflösung (可变分辨率)
- kann aus Text generiert werden (TText直接过来的)
- Duplexdruck möglich -> 双面打印

**Nachteile:**
- geringe Auflösung (ca. 10 dpi)  (但是低分辨率)
- nur eine Reliefhöhe (一种凸起高度)

![[Pasted image 20240118220430.png]]

#### Distribution Taktile Druker (分布式触觉打印机)

- für Grafikdruck optimiert
- automatische Umsetzung von Helligkeitswerten in Reliefhöhen. (Reliefkarte:  地形图)

**Vorteil:**
- 8 Stufen von Prägungstiefen (praktisch max.3 unterscheidbar)
- scharfe Kanten und Linien (清晰的边界线和线条)
- große Papierformate
- kombinierbar mit Schwarzschrift, Farben (可以彩色！)

**Nachteil:**
- Auflösung (ca. 20 dpi)
- kostenintensive Hardware
- unüblicher als Braille-Druck -> geringe Verfügbarkeit

#### Distribution Kollagen （分布式拼贴画）
Bildkomposition aus verschiedenen Materialien

**Vorteile:**
- kann sehr detailliert und **realitätsnah** gestaltet werden
- Verwendung verschiedener Oberflächenstrukturen möglich.

**Nachteile:**
- hoher Erstellungsaufwand
- Vervielfältigung aufwendig --> 很难制作副本, 每件样品都是独一无二的
![[Pasted image 20240120143931.png]]
#### Distribution Punktreliefs (分发点浮雕)
- Manuelles Prägen von Punkten in *Zinkblech* (锌板)
- Vervielfältigung der *punzierten* Platte im Blindendruck (用样板打出（冲出）标志（Edelmetalllegierungen贵金属合金)
- Ergebnis ist ein Papierblatt analog einer Punktschriftseite

**Vorteile:**
- schnelle und kostengünstige Vervielfältigung

**Nachteile:**
- keine Fehlerkorrektur möglich
- Zinkverbrauch
![[Pasted image 20240120144057.png]]

#### Distribution Folienreliefs （分布式薄膜浮雕）
##### 1. Erstellung einer Basismatrize
- als Kollage (拼接画)
- durch Plotten von Materialschichten (材料层的绘制)
![[Pasted image 20240120144816.png]]
##### 2. Tiefziehen einer Folie. --> 成型过程
- Matrize
- Kunststofffolien über Matrize eingespannt
- Erhitzen der Folien bis sie plastisch ist
- Ansaugen der weichen Folien durch eine Vakuumpumpe
- nach Abkühlung 
- 在模板上加热塑料冷却得到
![[Pasted image 20240120151447.png]]

#### Distribution 3D-Modelle
3-dimensionale Körper zur Vermeidung perspektivischer Abbildungen (Projektionsbilder in 2D)


**Nachteile:**
- zeitintensive Erstellung der 3D-Modelle
- lange Druckzeiten
- Erstellung erfordert<mark style="background: #ADCCFFA6;"> Expertise</mark> (专业知识)

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

左手食指定位，右手食指移动，右手移到中间，移动左手
##### 2. Initiales Abtasten (大概)
- Vor der detaillierten Erkundung -> initiales Abtasten mit beiden Händen 
	- um Überblick zu erfassen:
		- Größe
		- Ausmaß
		- Grafiktypen
		- ...
![[Pasted image 20240204222836.png]]

##### 3. Linienverfolgung (Edge-Strategy) (边缘)
Erfassen konkrete Umrisse, Formen und Figuren durch Abfahren der Außenlinie -> in Schulen vermittelte Strategie zur **Objekterkennung**
![[Pasted image 20240120153232.png]]

##### 4. Systematische Strategien (horizontales / vertikales Erkunden) (双手四指)
![[Pasted image 20240120153314.png]]

##### 5. Perimeter / Speicherrad-Strategie (兴趣点法)
Erkundung rundum einen Point-of-Interest
![[Pasted image 20240120153406.png]]

#### Herausforderungen
- fehlender sukzessiver Erkundungsvorgang
- zu großes Format (> A3)
- überladen mit Information
- mangelhafte taktile Unterschied- und Erkennbarkeit
- Braille auf Texturen nicht erkennbar
- zu wenige Tastebenen verwendet (Reliefs)
- fehlende Zeichenerklärung (Legende)

### Richtlinien （触觉图的Richtlinien）
#### 1. Wahrung der ursprünglichen Aussage (不删改)
- Aussage des Bildes darf nicht gefälscht oder geändert werden 
	- keine Informationen weglassen oder hinzufügen

#### 2. Reduzierung der Komplexität （删装饰）
- nur zum Verständnis notwendige Elemente übernehmen
	- -> Schumuchgrafiken, Dekorationen weglassen
- Grafik so einfach wie möglich gestalten
- Änderungen ggf. in **Annotationen** vermerken

#### 3. Texturen, Linienstile und Punktsymbole sparsam verwenden (节制使用条纹，纹理，符号)
- Max. 5 Texturen in einer Grafik
- Referenzieren verwendeter Texturen, Linienstile, Symbole und Keys in einer Legende

#### 4. Perspektive vermeiden (避免透视)
- 3-dimensionale Darstellungen in 2-dimensionale überführen
- Überschneidungen von Objekten vermeiden

#### 5. Aufteilen komplexer Objekte (分解复杂对象)
- Zerlegung komplexer Objekte in Teilgrafiken
- Zusammengehörigkeit deutlich kennzeichnen

#### 6. Unterscheidbarkeit （可辨识性）
- Mindestabstände und -größen beachten (大小)
- Geprüfte Texturensets mit geringer Ähnlichkeit untereinander verwenden (纹理可以区分)

#### 7. Verwendung von Braille-Schrift
- geeignete Brailleschrift in richtiger Schriftgröße verwenden (大小合适)
- *kleine* Braille-Beschriftungen mit einem Rahmen hervorheben 
- Braille-Schrift immer horizontal und linkbündig anordnen (左对齐)


# Teil 2
![[Pasted image 20240120163653.png]]

### Erstellung Taktiler Grafiken

- häufig aufwendiger, manueller Prozess
- [[Vorlesung 5 - Zugängliche Graphiken#Richtlinien （触觉图的Richtlinien）|Richtlinien(触觉图的Richtlinien)]] müssen eingehalten werden
- häufig als Transkription von visuellen Grafiken
- **Optimalfall**: Autor erstellt taktile und visuelle Grafik
![[Pasted image 20240120164130.png]]

**Herausforderungen:**
- <mark style="background: #ADCCFFA6;">Menschen mit Blindheit und Sehbeeinträchtigung selbstständige Erstellung ermöglichen</mark>
- Qualitätskontrolle durch Zielgruppe
- Balance: Vereinfachung vs. Informationsgehalt vs. Überblick
- Beachtung der Eigenschaften verschiedener Herstellungsverfahren

### Editoren
- kann mit **Standardeditor** erstellt  und mit Braille-Drucker geprägt werden.
- ![[Pasted image 20240120164818.png]]

### Teilautomatisierte Erstellung
> Häufigster Ansatz: Anpassung einer bestehenden visuellen Grafiken für die taktile Ausgabe (Transkription).

Bsp.: TGA (Tactile Graphics Assistant)
-> Algorithmus zur automatischen Vereinfachung und Optimierung herkömmlicher Grafiken in taktile Grafiken:
- manuelles Eingruppierung der Bilder in Klassen sowie Training
- Separieren und Entfernen von Text innerhalb einer Grafik (图形内部分离和移除文本)
- OCR und Umwandlung in Braille (识别图中的文字转换成盲文)
	- ![[Pasted image 20240120165619.png]]

### Mathematische Darstellungen
- 2.5D: Hilfslinien und Funktionsverlauf als Relief
- ![[Pasted image 20240120170026.png]]
- **DotsPlus Braille** (数学表达式)
![[Pasted image 20240120170208.png]]
### Vollautomatische Erstellung
- geeignet für. ´wohldefinierte Grafiktypen (z.B. Diagramme)
- *wenige* Anwendungen mit gutem Ergebnis vorhanden 


---
## 5 Taktile Interaktion - Interagieren mit taktilen Grafiken
-> 注意记一下有哪些用于交互的技术

### Audio-haptische Systeme

#### Audio-Taktile Ansätze

- *multimodale* Systeme-> Kombination verschiedener Ein- und Ausgabemöglichkeiten , z.B. haptischer und auditiver Elemente
- Ansprechen verschiedener Sinne
- talking tactile tablet: 
	- <mark style="background: #ADCCFFA6;">Berührungsempfindliches Tablet erlaubt akustische Rückmeldung bei Fingerkontakt</mark>
	- Grafikverwaltung durch Barcodes
![[Pasted image 20240202170631.png|400]]

#### Technologien
viele Ansätze, um ***Interaktion*** zu ermöglichen:
- *Videobasiertes Tracken* des Fingers bei der Exploration der Grafik (基于视频的点读笔)
- Verwendung *digitaler Stifter*, die Position erkennen (点读笔)


### Technik der Interaktion: 
#### AuthOMathic Block System
> Def: taktile/haptische Interaktionstechniken durch Legen von <mark style="background: #ADCCFFA6;">*Blöcken mit Braille-Beschriftung*</mark>

![[Pasted image 20240202172023.png|400]]

#### Taktile Displays (触觉显示器)
- unterschiedliche Auflösung 
- Ein- und Ausgabemöglichkeiten (multimodal: Toucheingabe, Sprachausgabe...)
- ![[Pasted image 20240202172303.png|300]]
- ![[Pasted image 20240202172314.png|500]]

#### Projekt HyperBraille
HyperBraille Display
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
- Erzeugung von Ausdrucken <mark style="background: #ADCCFFA6;">für Brailledrucker mittels *plotter control language*</mark>
	- keine Überprüfung während des Zeichnens möglich
- Abpausen von taktilen Objekten über Touchpad
- ![[Pasted image 20240202180744.png]]
#### IC2D (integrated communication 2 draw)
- Navigation von Malen auf dem Bildschirm mit Hilfe <mark style="background: #ADCCFFA6;">von Sprachausgabe und Musik</mark>
- ![[Pasted image 20240202181356.png]]

#### Taktile Displays
- erlauben <mark style="background: #ADCCFFA6;">Freihandzeichen</mark>
- Zugang zu Mathematik
- Eingabefläche = Ausgabefläche
- ![[Pasted image 20240202181706.png|450]]
#### 3D - Drucker
**Line Space**
- S<mark style="background: #ADCCFFA6;">teuerung eines 3D-Druckers mit Gesten oder Sprache</mark>
- ermöglicht direkte Interaktion
- ![[Pasted image 20240202181849.png|400]]

### Zusammenfassung
|        | Analog                                                                                            | Digital                                                                                                                     |
| ------ | ------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| Pro    | - schnell und einfach <br>- günstig <br>- detaillierte und naturgetreue Darstellung möglich       | - gute Fehlerkorrektur<br>- hohe Veränderbarkeit und Reproduzierbarkeit<br>- leichte Distribution                           |
| Kontra | - schwierige Fehlerkorrektur<br>- schwer reproduzierbar<br>- wenig Unterstützung bei **Zeichnen** | - erfordert hohe kognitive Ressourcen<br>- begrenztes Anwendungsgebiet<br>- Spezialequipment (Hardware) notwendig -> Kosten |



