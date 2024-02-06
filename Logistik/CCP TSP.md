---
date: 2024.2.3
tags:
  - Logistik
---


| Traveling-Salesman-Problem(TSP)                                                                                    | Chinese-Postman-Problem(CCP)                                                                                            |
| ------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------- |
| Kürzeste Rundreise, die jeden Knoten mindestens 1x enthält. Anfang und Endeder Tour sind jeweils am selben Knoten. | Optimale Rundreise (minimale Kosten/Wege), die alle Kanten mindestens 1x enthält. Anfang und Ende sind jeweils im Depot |

**Euler Tour**: CCP-Rundreise, in der jede Kante genau einmal enthalten ist
**Euler Graph**: Graph der eine Eulertour besitzt
**Satz von Euler**: Ein ungerichteter Graph enthält einen Euler-Kreis, wenn jeder Knoten einen geraden Grad besitzt. Ein schwach zusammenhängenderDigraph enthält einen Euler-Zyklus, wenn für jeden Knoten positiver und negativer Grad übereinstimmen.



# CPP (线条加出来加到原图里面！)

- 转换成Graph (perfektes Matching)
- 转换成Digraph (Transportprobleme)
- 通常因为要经过每一条路跑得更远hh


# TSP (线条加出来加到Minimalgerüst里面！)

- symmetrisch
- asymmetrisch

基本思路就是Minimalgerüst然后把这个T来做CPP


| Eröffnungsverfahren für das TSP                                                                                                                                                         | Verbesserungsverfahren für das TSP                                                                                                             |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| Verfahren des besten Nachfolgers (für STSP und ATSP)                                                                                                                         | r-opt-Verfahren (r=2,3) (für STSP, ATSP und vollständige Graphen). r Kanten streichen und durch r (nicht zwingend verschiedene) Kanten ersetzt |
| Verfahren von Christofides für <mark style="background: #ADCCFFA6;">STSP</mark> (über Verfahren von Christofides bestimmter Hamilton-Kreis ist max. 50% länger als die optimale Lösung)对应perfektes Matching|                                                                                                                                                |
| Verfahren der sukzessiven Einbeziehung (für STSP und ATSP)                                                                                                                              |                                                                                                                                                |
| Verfahren von Akl für <mark style="background: #ADCCFFA6;">ATSP</mark> 对应Transportprobleme                                                                                                                 |                                                                                                                                                |


>[!Note]
>所有算长度，都是dij,添加线，都是按照原图添加

## relativer Gap
- Gap = UB – LB
- relativer Gap =  Gap/LB
- UB=Upper Bound= maximale Länge der Rundreise der unbekannten exakten Lösung des TSP
- LB = Lower Bound = minimale Länge der Rundreise der unbekannten exakten Lösung des TSP 
	- bestimme für Knoten (除了开始点以外的点)<mark style="background: #ADCCFFA6;">2,...,n</mark> ein Minimalgerüst und binde anschließend den Startknoten kostengünstigst an zwei andere Knoten an
	- 然后把线都加起来hh