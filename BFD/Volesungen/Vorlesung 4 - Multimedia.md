---
date: 2024.2.2
tags:
  - BFD
aliases:
---
-> Multimedia: Ein Dokument für Alle
本章重点在三个领域以及一个Techniken für Benutzerprofile (收集用户特征以便针对不同用户提供客制化的服务)

# Agenda
- Fallstudien
	- 1. DAISY Hörbuch
	- 2. MathML
	- 3. Multimedia Barriere
- Techniken für Benutzerprofile
- Infrastruktur für Inklusion
- Kollaborative Barrierefreiheit

# Fallstudie 1: DAISY Hörbücher
-> Digital Accessible Information System

## DAISY enthält:
- package file
	- package identity
	- metadata
	- Manifest
	- spine, tours, guide
- Text des Buches (einschließlich Mark-up gemäß OpenBook)
- die entsprechenden Audio-Dateien (Sprecher od. Synthetische Stimme)
- SMIL Datei
- NCX Datei

## XHTML und SMIL - Datei
- **SMIL Datei** zur Verknüpfung von Audio (MP3) und Text
- **Ressourcen Datei** mit *zusätzlichen Medien*, die dem Leser nicht zugänglich sein sollen
- *einer Datei zur navigation control (NCX)* mit allen Lesezeichen zu denen der Leser navigieren kann

## wichtige Elemente in DAISY
### a) Struktur
- audio file
- synchronization file
- navigation control file 
- resource file 
- presentation style file (CSS)
- transform file (XSL für GUI, Audio, und Braille)

### b) Inhalte
- <\sent> -> Sätze, <\p> -> Absätze
- <\level1> - <\level6> -> Buchstrukturen (Kapitel, Abschnitte)
- <\img> und <\imggroup> -> Bilder und deren Beschreibung
- <\pagenum> -> Seitenzahlen

### Beispielaufbau
![[Pasted image 20240206153533.png]]
.opf -> package file
.smil -> Synchronisation
.xml -> Text
.mp3 -> Audio
## Lesetechniken für DAISY
- Text lesen
- fast forward , reverse
- variable Lesegeschwindigkeit
- Inhaltsverzeichnis
- Navigation Control File
- Notizen
- Highlighting
- Bookmarks
- Suchen
- Buchstabieren, ......

## DAISY E-Books Timeline
Formate in DAISY sind Auszeichnungen wie `dtb:audio` und teilweise aus verschiedenen Modulen des Standards
![[Pasted image 20240206153316.png]]

## DT Book
一本书通常包含以下部分: 
![[Pasted image 20240206154022.png]]
-> 将这些不同内容使用mark up转换成DAISY格式, 从而适配专用的阅读器

### Markup des Front Matter
![[Pasted image 20240206154148.png]]
注意markup和上图的一一对应, 以及tag的用法, 大体了解就行
![[Pasted image 20240206154410.png]]
### Markup des Body Matter
- meist durch Kapitel, Abschnitte und Unterabschnitte, hier "**parts**" genannt
- Ein **Part** wird durch <\level> beschrieben
- ![[Pasted image 20240206154607.png]]
### Markup des Rare Matter
一本书的最后部分, tag跟前面一样
了解就行

## DAISY und Mathematik
![[Pasted image 20240206155605.png|400]]
![[Pasted image 20240206155553.png]]

# Fallstudie 2: Mathematik

| Entwurfskriterium | Mathematik-Interaktion                                                                                                                  |
| ------------------ | --------------------------------------------------------------------------------------------------------------------------------------- |
| Kohärenz           | Ausgabe-Modalität und Eingabe Modalität sollen sich entsprechen, (Braille Eingabe und Braille Ausgabe, Spracheingabe und Sprachausgabe) |
| Erkundung          | Räumliche oder hierarchische Navigation je nach mathematischem Konstrukt                                                                |
| graphische Symbole | verbalisieren durch Namen oder nicht-verbale Klänge                                                                                     |
| Lernbarkeit        | Einsatz existierender BrailleNotationen oder natürlicher Sprache                                                                       |
| Adaptierbarkei                   |    Einsatz der BrailleNotation/Sprechweise je nach Kenntnissen des Lesers                                                                                                                                     |

## Brailleschriften und Mark-up (用于数学符号的盲文)
- Marburger Mathematik Schriftgröße 
	- 6-Punktschrift
- ASCII Mathematikschr. (AMS)
	- 8 Punktschrift mit sieben Punkten
	- Verwendet in Uni KA und TUD
- frz., engl., span., russ. Schrift für Mathematik, Nemeth-Code in USA
- Stuttgarter Schrift (SMSB)
	- 8 Punktschrift
## Braille, Sprache und Klänge 
- Problem: Mathematik wird als Grafik behandelt
- **Dynamisches** Braille: Terme ersetzen durch Termbegriffe
- Sprachausgabe (mit korrekter Prosodie -> viele Tonhöhenstufen)
- Klangausgabe

## Projekt MATHS (1994-1997)
- Mathematik lesen und schreiben
- integriert mit
	- Brailleausgabe/Brailleeingabe
	- Sprachausgabe/Klangausgabe/Spracheingabe (Pilotstudie)
	- mit Baum Modell
	- ![[Pasted image 20240206131524.png]]
		- fraction
		- numera : 分母
		- denomi : 分子


## Lambda Project
- ein System zum Schreiben und Bearbeiten von mathematischen Texten für *blinde* Schüler und Studierende
- Linearer **Lambda-Math-Code**
	- direkt von MathML abgeleitet
	- effiziente Benutzung von Braille-Geräten (8-Punkt-Notation) und Sprachsystemen
	- mächtiges und flexibles MathematikschriftSystem, das zu den bekannten Standards kompatibel insight 
	- in Echtzeit in MathML und in ein gebräuchliches grafisches Format **transformierbar**.
- ![[Pasted image 20240206132656.png|400]]

## HTML und Mathematik 
![[Pasted image 20240206124604.png]]
其实也不是很好，引出MathML


## MathML (数学标记语言)

MathML 是一种用于描述数学和科学公式的标记语言。它的全称是 "Mathematical Markup Language"，即数学标记语言。MathML 是由 W3C（World Wide Web Consortium）制定的一种XML（可扩展标记语言）应用，旨在使数学内容能够在Web页面中以结构化的方式呈现和交互。
die Erstellung und Darstellung geeignet für Menschen und maschinelle Verarbeitung sind

Präsentation Markup in MathML:
- Token Elemente
- $mi$ für identities (Variablen)
- $mo$ für Operatoren
- $mn$ für Zahlen
- `<apply>` Funktionen


![[Pasted image 20240202181606.png]]

### Layout steuern
![[Pasted image 20240206161756.png]]
- `<msup>`上标, hochgestellt
- `<msub>` tiefgestellt
- `apply` 代表Funktion
- -> 大体了解
## OCR Analyse

- Analysieren von Bildschirminhalten durch Schrifterkennung (OCR)
- Erzeugt LaTeX, ASCIIMaths oder MathsML aus Pixeln -> Screenshots
- ![[Pasted image 20240206133554.png]]
## Box Modell
![[Pasted image 20240206161459.png]]
Ziel: visuelle Zusammenhänge in Boxes abbilden


# Fallstudie 3: Multimedia Barriere
## Projekt MultiReader
A multimodal multimedia navigation and reading system
-> 为了克服多媒体障碍, 
## Benutzer-Anforderungen
> 这里讲义不严谨, 用户还包括作者. 
- Alle Leser
	- unterschiedliche Lesestrategien
	- Lesezeichen (书签)
	- Index/Inhaltsangabe (目录，摘要)
- blinde Leser
	- steuerbare Sprache
	- Bildbeschreibung
	- Audiodeskription
- sehbehinderte Benutzer
	-  variable Zeichensätze und Farben
	- Vergrößerung
- gehörlose Leser
	- Text-basierte Beschreibung von akustischen Inhalten
	- Bilder, Filme statt Text
	- kurze Texte (Text-basierte Beschreibung von akustischen Inhalten)
	- Gebärdensprachelexikon
	- Gebärdensprachübersetzung von Text
- dyslexische Leser
	- variable Zeichensätze, Farben, Abstände
	- dynamische Hervorhebung

## Ein Dokument für Alle
要实现这一目的, 就需要基于相同的内容生成多种表现形式:
![[Pasted image 20240206162753.png]]

具体实现方式:
- angereicherte Dokumente (xHTML (bassiert auf XML)→SMIL + Widgets für Navigation(`<tour>`,自定义标签) (多标签属性提供文字信息)
	-  XHTML: tags () and attributes (alt="...") provide redundancy
	- Synchronous Multimedia Integration Lang. (SMIL): 多媒体同一个时间轴播放
- <mark style="background: #ADCCFFA6;">Trennen von Inhalt und Präsentation</mark> (CSS+Container)
- Mark-up Techniken zur Beschreibung der Lesergruppen (XML)
- Personalisierung (XSLT)
- temporalem Mark-up
	-  Teilen der Medien/Dokumente und der
	- Interaktion
- Scalable Vector Graphics (SVG)

> s.49-53 Interaction 部分我不确定重要程度, 等再查一下
## MultiReader Dokumente
> Ein MR Dokument ermöglicht die Betrachtung eines **personalisierten** Transformationsergebnisses des Inhalts durch: 
- Auswählen des Inhalts (Video mit Gebärdensprache, Zusammenfassung) (内容的选择)
- adaptierbaren Sichten (Schriftgröße, Farbe, temporale Adaptierungen) des angereicherten Inhalts (自适应系统)
- Navigationstechniken basierend auf semantisch modellierten Interaktionsobjekten (语义的导航)

- Für den Einsatz ist zu unterscheiden
	- **Server-basierte** Anpassung (*transaktions*-basierte Verarbeitung der Profildaten)
	- **Client-basierte** Anpassung (*lokale* Anwendung der Profildaten) (类似于自己调整)


![[Pasted image 20240202184940.png]]
`<span>` verbietet für Inhalte "Container" zur verfügung


# Techniken für Benutzerprofile
- Benutzerprofile mit behinderungsspezifischen Merkmalen
	- Dienen der Erstellung *adaptierbarer* und *adaptiver* Systeme
- Profilematching erfordert Algorithmen (E-Learning Angebote personalisieren)
- Problem des **Systems**: Datensicherheit vs. Barrierefreiheit
- Problem der **Benutzer**: Verknüpfung von Usability und Accessibility

## Ein Model des Profileinsatzes
- Fähigkeiten bestimmte Aufgaben und Fertigkeiten auszuführen & bestimmte Interaktionstechniken einzusetzen
![[Pasted image 20240206164442.png]]

# INFRASTRUKTUR FÜR INKLUSION(包容性基础设施)
## Anwendungsskizze : GPII
![[Pasted image 20240206164646.png]]
-> 多种方式

## GPII Architektur
![[Pasted image 20240202190732.png]]
1. U盘里存储了ID
2. 在库或者云端里查询偏好
3. 插入的设备能够干什么
4. 将偏好和功能匹配，提供可能的方案
5. Verwaltung系统
### Cloud4All

基于云端的技术，GPII 一部分 --> imagine if you could pick up any device

## Konflikte in Profilen

一群人一起看电视
解决方案：选出较多数人觉得不错的那个设置

- Feedback: Change preview
- Stil: Tap Method

# KOLLABORATIVE BARRIEREFREIHEIT

- Crowd Sourcing (让群众解决问题)
- Kollaborative Bf.: 
	- Barrierefreiheit wird durch Beteiligung **anderer Menschen** hergestellt
	- ->老师用了轮椅地图的例子, 实质是一种分布式和去中心化的思维方式。谷歌街景地图也利用了这个方式
- Auftragsarbeiten
	- einmaliger Auftrag eines Bearbeiters
	- Bearbeitung ähnlicher Probleme durch **einen Bearbeiter**
	- Bearbeitung identische Aufgaben durch mehrere Bearbeiter
	- -> 逐渐分散
- Crowd-Sourcing von Gebärden
- Erstellen von Untertiteln (Scribe: 不同时间段的听写和合成)
- **Kollaborative Barrierefreiheit:** 
	- BeMyEyes nutzt Kommunikation mit *sehenden* Menschen
	- LookTell erkennt Gegenstände autonom und nutzt Kommunikation