---
date: 2024.1.29
aliases:
  - Barrierefreies Web
tags:
  - BFD
---

## Anforderungen/Barrieren im Web
- Grafik, Audio, Video (Zugänglichkeit)
- Zeitgesteuerte Änderungen
- Eingabe- und Ausgabegeräte (Unabhängigkeit)
- Stand der Technik (Kompatibilität 兼容性)

## [[BFD Übungen#WCAG Web Content Accessibility Guidelines|WCAG]]

- Vier Bereichen
	- Wahrnehmbarkeit: Darstellungen erfahrbar (lesbar) gestalten (呈现方式)
	- Bedienbarkeit: Eingaben zur Steuerung von Websites und Anwendungen ermöglichen (输入)
	- Verständlichkeit: Menschen mit kognitiven Einschränkungen erreichen
	- Robustheit: technische Neuerungen schließen ältere assistive Technologien nicht aus
- 14 Richtlinien (所有非文本都有文本替代)
- Drei Stufen

## Einteilung nach Barrieren

1. Farbe: 
	1. ausreichender Kontrast (WCAG 2.0 verlangt einen Unterschied der Farbhelligkeit L von 1:3 im sRGB Farbraum)
	2. Kontrast (min.  4,5:1)
	
2. Text 
	1. Komplexität
	2. Verständlichkeit
	3. benötigen [[Vorlesung 2#Mark-up for Text|Mark-up]]
	4. Sprachliche Besonderheiten
3.  Navigation
	1. tabindex bestimmen
	2. Undo ermöglichen
	3. InvisibleLabel (不可见标签，但是对屏幕阅读器很重要，了解`<li>`的结构)
	4. Benannte Anker (Seitenanfang, Inhaltsverzeichnis...)
	5. Breadcrumb trails (面包屑导航)
4. Suche 
	1. einfaches Texteingabefeld mit <mark style="background: #ADCCFFA6;">Beschriftung</mark>
5. Graphik
	1. alt="" wird vom Screen Reader ignoriert, alternativ: title für ausführliche Darstellung verwenden
	2. ASCII Grafiken vermeiden
	
6. Multimedia
	1. Aufzeichnungen von Audio erhalten eine Textalternative
	2. Aufzeichnungen von Video erhalten entweder eine Textalternative oder eine zeitlich abgestimmte Audioalternative (Untertitel)
7.  Dynamischer Inhalt
	1. durch Javascript
	2. AJAX (asynchrones Laden von Webinhalten während Website angezeigt wird)
	3. Beschreibung mittels [[Vorlesung 2#ARIA|ARIA]] (z.B. aria-label, aria-hidden)
 8. Interaktion
 Accesskey (快捷键) erlaubt interaktive HTML Elemente mit Tastaturunterstützung zu versehen.
 9. Formulare 
 Beschriftung und Bedienelement assoziieren 
 ```HTML
<label for="name">Name:</label>
<input id="name" type="text">
```
 
## ARIA
- Mark-up und Javascript sollen Zugänglichkeit zu Widgets herstellen (roles)
- Landmarks
	- main
	- navigation
	- complementary
- aria describedby (提供Beschreibung)
- aria-labelledby (wird eine Region mit seinen Labels verknüpft)
## Mark-up for Text



### Überschriften
- wichtig für Navigation des Screenreader
- bei `<h1>` beginnen
- nach `<h1>` folgend `<h2>` dann `<h3>`

### Listen
- ohne Mark-up vom Screenreader nicht interpretierbar
- `<ul>` (ungeordnete Liste) oder Gestaltung per CSS


### Sprachinhalt
Die vorherrschende Sprache soll kenntlich gemacht werden: lang="de"

### Tabellen

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


>[!note]
>推崇Linearisierbare Tabellen