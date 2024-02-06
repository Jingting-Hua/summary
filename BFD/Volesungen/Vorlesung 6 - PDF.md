---
date: 2024.2.3
tags:
  - MCI
aliases:
---
# 简介
## 基础功能
![[Pasted image 20240203121317.png]]
- 通常的功能：Test/Graphik
- pdf Formular： XML Schnittstellen
- 签字：Digital Signature (加密算法，生成唯一数字代码）
- Navigation
	- Bookmarks
	- Links
- Metadata: XMP


## Page Objekte
![[Pasted image 20240206135545.png]]

- Pfadobjekte: Kann als Clippingpfad benutzt werden
- Textobjekte
- Externe Objekte (XObjects): Externe Objekte werden außerhalb des Content-Streams definiert und können anschließend innerhalb eines Content-Streams verwendet werden. (外部定义，内部使用)，XObjects werden hauptsächlich dazu benutzt, Grafiken in PDF einzubinden.
- Forms (表单) sind aus Postscript übernommene Datenstrukturen zur Wiederverwendung
-  Inline-Images: Eine Möglichkeit um kleine Grafiken innerhalb von PDF einzubinden.
- Shading Objekte: Shading Objekte bestehen aus einem beliebigen Umriss
- Annotationen
	- ![[Pasted image 20240206135738.png]]
	- Text Annotation: Die Annotation wird im geschlossenen Zustand als Icon dargestellt (<mark style="background: #ADCCFFA6;">Kategorien</mark> Comment, Help oder Note)
	- Free Text Annotation: <mark style="background: #ADCCFFA6;">ständig</mark> auf der Seite angezeigt
	- Line Annotation: eine einfache gerade Linie
- Verweise (Hyperlinks)

## PDF/A

- geräteunabhängig
- abgeschlossen
- selbstdokumentierend (元数据)
- transparent
	- Zugänglich für unmittelbare Auswertungen mittels einfachen Werkzeugen

>[!Note]
> - keine technischen Schutzmassnahmen
>	- keine Verschlüsselung, Passwörter, usw.
> - kann nicht allein die Langzeitarchivierung ermöglichen


## PDF/UA

- [什么是PDF/UA](https://pdfmailmerger.com/zh-hans/blog/%E4%BB%80%E4%B9%88%E6%98%AFpdf-ua%EF%BC%9F/#%25e4%25bb%2580%25e4%25b9%2588%25e6%2598%25afpdfua)
- Bf. wird durch Prüfprotokoll (Matterhorn) abgesichert (2015)
![[Pasted image 20240206135957.png]]
- Checkpoints (31 Gruppen) betreffen auch spezielle Inhaltsarten und Schnellprüfung
	- ![[Pasted image 20240206135936.png]]

## PDF/UA vs. WCAG

- PDF/UA definiert technische Merkmale und bietet einen technischen Rahmen
- PDF/UA kennt (außer bei Bildern) keine alternative Darstellungen (z.B. Redetext)


# PDF UND BARRIEREFREIHEIT

## Acrobat und Barrierefreiheit
- [什么是Acrobat](https://zh.wikipedia.org/zh-cn/Adobe_Acrobat)
- plugin unterstützt Screenreader
- tagging wird eingeführt
	- Automatisches und manuelles Erstellen
	- Automatisches Prüfen
	- PDF/A (ISO 19005-1) berücksichtigt tagging


## PDF 里面的标签

- Article `<Art>`: 用于标记文档中的文章或主要内容。
- Figure `<Figure>`: 用于标记文档中的图像或图表。
- **Block-level Elemente: Container**
	- Division element `<Div>`: Ein generischer Block oder eine Gruppe von Block-level Elemente
- Spezielle Tags
	- `<Figure>`zeichnet Bilder im Text aus
	- `<Form>`für Formularelemente
	- `<Link>`für Veweise
	- `<Note>`für Annotationen
	- `<Reference>` für Daten innerhalb des Dokuments
- nur wenige Screenreader unterstützen PDF (Jaws 7)



## Serialisierung/Reflow

Dokumente mit Tags können kompakt dargestellt werden
- Erhöhung der Lesbarkeit für Sehbehinderte und Dyslexiker
- Die logische Leserichtung wird angewendet

## Screenreader und PDF
mit verschiedene Apps mit verschiedene Probleme


## Barriere - freiheit herstellen
![[Pasted image 20240203153233.png]]
1. 获取pdf
	1. scan-based
	2. selbst pdf
	3. Web pages
2. 如果有需要，添加表单form
3. Tag
4. 检查accessibility
5. 可以的话
	1. lese Reihefolge
	2. tags korriegieren
6. 产生Bookmarks，Lauguage


## PDF für Scannerergebnisse

- OCR Anwendungen notwendig (图片文字识别)
- PDF kann sowohl Bild als auch Text gemeinsam speichern (layer)
- Manuelles Anlegen des Tagstamms sowie automatische Erzeugung von Tags
- Manuelle Reparatur von Fehlern durch Tagkontrolle (auch per Screenreader möglich)


## Artefakte: außertextliche Elem.

Artefakte sind Elemente ohne Zuordnung zum Tagstamm
- **Seitennummern：** 文档中的页码通常不需要与标签关联，因为它们是辅助性质的元素，与文档的主要结构无关。
- **Schmucklinien：** 指装饰性的线条或边框，这些通常是用于美化文档的元素。
- **Kommentare：** 文档中的注释或评论通常被视为附加信息，不影响文档的主要结构。
- **Wasserzeichen：** 类似于水印，这些元素通常是在文档上方或下方添加的半透明文本或图像，用于表示文档的状态或机密性。


Die Bearbeitung erfolgt mit dem Touchup-Werkzeug zur Zuordnung/Bearbeitung des Namens bzw. Entfernung von Tags


## Ausgabehilfeprüfung (注意事项) und Bericht

- Vorhandensein alternativer Beschreibungen für Bilder
- Festlegung einer (!) Sprache eines Texts
- Zeichenkodierung bekannt
- Beschriftung der Formularelemente
- Listen- und Tabellenstruktur
- Tabulatorreihenfolge entspricht Ordnungsstruktur


### PAC 2021

Freies Werkzeug für tagged PDF

#### PAC21 Prüfwerkzeug

- Detailbericht („Report“): Mit Hilfe des Detailberichts die einzelnen Fehler im Dokument analysieren.
- Vorschau-Ansicht („Screenreader Preview“): vereinfachte Strukturansicht für die Qualität („Tags“) und der logischen Reihenfolge („LeseReihenfolge“).
- Dokumentstatistik („Document Statistics“): Übersicht der Anzahl der verwendeten StrukturElemente.
- Logische Struktur („Logical Structure“): Expertenansicht des kompletten Tag-Baums, um sich korrespondierende Elemente zu einem Tag im Dokument anzeigen lassen oder die Rollenzuweisungen zu kontrollieren.



### PDF Checking: PAVE&Tingtun

#### PAVE
analysiert das PDF Dokument und bietet diverse Assistenten an, um Tags zu ergänzen

#### Tingtun
TingTun prüft PDF gegen WCAG 2.0


### Rolemap/Rollen

- Die Rolemap ordnet unbekannt Tags den vordefinierten Tags zu
- Rollen werden (heute) auch von Screenreadern erkannt



### Tabellen in PDF
![[Pasted image 20240203160003.png]]


### Formulare in PDF
先读 Linker刻度表的意义再读符号
![[Pasted image 20240203160218.png]]


### Verweise 

- Verweise werden vor den allgemeinen Tags erstellt
- Automatische Erkennung aus OCR Ergebnis möglich (Menü: Erweitert/Verknüpfungen/alle URL erstellen)
- Verweise müssen explizit beschriftet werden (Optionen/Tag aus Auswahl erstellen/Typ „Verweis“

# Editoren in der Praxis

- LaTeX
- Microsoft
	- Word, PowerPoint, Excel
- GoogleDoc
## Mark-up Vergleich: Überschriften 

- ![[Pasted image 20240206141123.png]]
- ![[Pasted image 20240206141149.png]]

# [[BFD/Volesungen/BFD Übungen#Barrierefreie Dokumente mit Word & PowerPoint|PowerPoint: Prüfen auf Barrierefreiheit]]

- Bilder müssen mit Alternativ beschrieben werden (Grafik formatieren/Web)
- Texte werden nicht als Überschriften strukturiert, evt. manuelle Überarbeitung notwendig
- Masterfolienlayout für Schmuckgrafiken nutzen
- Im PDF werden trotzdem einige Fehler möglich:


# Word: Exportieren als PDF

