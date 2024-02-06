---
date: 2024.2.2
tags:
  - BFD
aliases:
---
# Mathematik

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
- Dynamisches Braille: Terme ersetzen durch Termbegriffe
- Sprachausgabe 
- Klangausgabe
## Projekt MATHS (1994-1997)
- Mathematik lesen und schreiben
- integriert mit
	- Brailleausgabe/Brailleeingabe
	- Sprachausgabe/Klangausgabe/S pracheingabe (Pilotstudie)
	- mit Baum Modell
	- ![[Pasted image 20240206131524.png]]
		- fraction
		- numera : 分母
		- denomi : 分子


## Lambda Project
- ein System zum Schreiben und Bearbeiten von mathematischen Texten für blinde Schüler und Studierende
- Linearer Lambda-Math-Code
	- direkt von MathML abgeleitet
	- mächtiges und flexibles MathematikschriftSystem, das zu den bekannten Standards kompatibel insight 
- ![[Pasted image 20240206132656.png]]


## HTML und Mathematik 
![[Pasted image 20240206124604.png]]
其实也不是很好，引出MathML


## MathML (数学标记语言)

MathML 是一种用于描述数学和科学公式的标记语言。它的全称是 "Mathematical Markup Language"，即数学标记语言。MathML 是由 W3C（World Wide Web Consortium）制定的一种XML（可扩展标记语言）应用，旨在使数学内容能够在Web页面中以结构化的方式呈现和交互。

- Token Elemente
- mi für identities (Variablen)
- mo für Operatoren
- mn für Zahlen
- `<apply>` Funktionen


![[Pasted image 20240202181606.png]]

- `<msup>`上标
- `apply` 代表Funktion
## OCR Analyse

- Analysieren von Bildschirminhalten durch Schrifterkennung (OCR)
- Erzeugt LaTeX, ASCIIMaths oder MathsML aus Pixeln
- ![[Pasted image 20240206133554.png]]

# Multimedia Barriere



## Benutzer-Anforderungen

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
	- Bilder, Filme statt Text
	- kurze Texte (Text-basierte Beschreibung von akustischen Inhalten)
	- Gebärdensprachübersetzung von Text

## Ein Dokument für Alle

- angereicherte Dokumente (xHTML (bassiert auf XML)→SMIL + Widgets für Navigation(`<tour>`,自定义标签) (多标签属性提供文字信息)
	-  XHTML: tags () and attributes (alt="...") provide redundancy
	- Synchronous Multimedia Integration Lang. (SMIL): 多媒体同一个时间轴播放
- <mark style="background: #ADCCFFA6;">Trennen von Inhalt und Präsentation</mark> (CSS+Container)
- Mark-up Techniken zur Beschreibung der Lesergruppen (XML)
- Personalisierung (XSLT)
- temporalem Mark-up
	-  Teilen der Medien/Dokumente und der
	- Interaktion


## Multireader Dokumente

- Auswählen des Inhalts (Video mit Gebärdensprache, Zusammenfassung) (内容的选择)
- adaptierbaren Sichten (Schriftgröße, Farbe, temporale Adaptierungen) des angereicherten Inhalts (自适应系统)
- Navigationstechniken basierend auf semantisch modellierten Interaktionsobjekten (语义的导航)
- Für den Einsatz ist zu unterscheiden
	- Server-basierte Anpassung (transaktions-basierte Verarbeitung der Profildaten)
	- Client-basierte Anpassung (lokale Anwendung der Profildaten) (类似于自己调整)


![[Pasted image 20240202184940.png]]
`<span>` verbietet für Inhalte "Container" zur verfügung


## Techniken für Benutzerprofile
Dienen der Erstellung adaptierbarer und adaptiver Systeme
- Profilematching erfordert Algorithmen (E-Learning Angebote personalisieren)


# INFRASTRUKTUR FÜR INKLUSION(包容性基础设施)


## GPII
![[Pasted image 20240202190732.png]]
1. U盘里存储了ID
2. 在库或者云端里查询偏好
3. 插入的设备能够干什么
4. 将偏好和功能匹配，提供可能的方案
5. Verwaltung系统
### Cloud4All

基于云端的技术，GPII 一部分

## Konflikte in Profilen

一群人一起看电视
解决方案：选出较多数人觉得不错的那个设置

- Feedback: Change preview
- Stil: Tap Method

# KOLLABORATIVE BARRIEREFREIHEIT

- Crowd Sourcing (让群众解决问题)
- Kollaborative Bf.: Barrierefreiheit wird durch Beteiligung anderer Menschen hergestell
- Auftragsarbeiten
- Crowd-Sourcing von Gebärden
- Erstellen von Untertiteln (Scribe: 不同时间段的听写和合成)
- BeMyEyes nutzt Kommunikation mit sehenden Menschen
- LookTell erkennt Gegenstände autonom und nutzt Kommunikation