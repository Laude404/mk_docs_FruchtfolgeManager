# 2. Fruchtfolge erstellen
Aus den Pflanzen die Sie sich ausgesucht haben können in der Tabelle Fruchtfolgezyklen erstellt werden. Spezifische Konfigurationen liefern dabei unterschiedliche Fruchtfolgen.

---
## Inputleiste
In der Inputleiste können Sie spezifische Optionen auswählen um Fruchtfolgen einfach und schnell zu erstellen.


- [**Fruchtfolge automatisch/manuell**](#fruchtfolge-automatischmanuell)  
 
- [**Zehrerlänge**](#zehrerlange) 

- [**Pflanzenfamilie**](#pflanzenfamilie)

- [**Detaillierte Beetverteilung**](#pflanzenfilter)  


### Fruchtfolge automatisch/manuell

Hier wird festgelegt, ob ein kompletter Fruchtfolge-Zyklus automatisch generiert werden soll oder ob jede Folgefrucht manuell ausgewählt werden kann. 



#### Automatische Fruchtfolge
Generiert automatisch  alle  Fruchtfolgezyklen, die möglich sind. Die Fruchtfolgezyklen sind so aufgebaut, dass sie so immer wieder angebaut werden können.

!!! info "Fruchtfolgeglieder"
	Die Anzahl der Fruchtfolgeglieder richtet sich dabei nach der eingestellten [Zehrerlänge](#zehrerlange). 

#### Manuelle Fruchtfolge
Generiert nur ein Fruchtfolgezyklus. Die Folgefrucht kann sich immer wieder neu ausgesucht werden. Diese Einstellung garantiert dabei keine Zyklen die so immer wieder angebaut werden können. Die Anzahl der Fruchtfolgeglieder ist frei wählbar.

!!! info "Auswahl pro Fruchtfolgeglied"
	Die Einstellung der [Pflanzenfamilien](#pflanzenfamilie)-Regel steuert die Anzahl und Auswahl der Pflanzen pro Fruchtfolgeglied.

### Eingabe

Geben Sie  in das Eingabefeld  Gemüse  ein, die Sie gerne anbauen möchten oder die sich in der [Pflanzenliste](./pflanzenliste.md) befinden. Die  Autovervollstänigung schlägt  gleich Pflanzen vor, die in der Datenbank hinterlegt sind. 

!!! tip "Planung beginnen"
	Es ist zu empfehlen, mit der Eingabe der Starkzehrer anzufangen, da sie am wenigsten Spielraum bieten, und meißtens auch der Fokus sind.

### Zehrerlänge

Diese bestimmt wie die Fruchtfolgelänge in Bezug auf die Zehrertypen die vertreten sind.  Und gibt dementsprechend die Folgefrüchte aus in der manuellen und der automatischen Fruchtfolgeerstellung.


!!! info "Fruchtfolge-Schema"
    Fruchtfolge wird nach folgendem Schema aufgebaut:

    === "Kurze Fruchtfolge"
        ```mermaid
        graph LR
            A[Starkzehrer] --> B[Mittelzehrer] --> C[Schwachzehrer] --> A
        ```
	=== "Lange Fruchtfolge"
		``` mermaid
		graph LR
		  	A[Starkzehrer]-->B[Mittelzehrer]-->C[Schwachzehrer]-->D[Gründüngung]-->A;
		```

!!! warning "Fruchtfolgeglieder fehlen"
	Wenn die Gründüngung planen, achten Sie darauf "Lange Fruchtfolge"
	einzustellen, da diese sonst nicht angezeigt werden.

### Pflanzenfamilie

Bestimmt  welche Pflanzenfamilien als Folgefrucht erlaubt sind.

#### Einfache Pflanzenfamilien Auswahl
Die Folgefrucht, kann von jeder  Pflanzenfamilie sein, ausser von der Vorfrucht. So werden nicht zwei gleiche Pflanzenfamilien hintereianander angebaut.

#### Strenge Pflanzenfamilien Auswahl
Folgefrüchte werden nach besonderen Schema ausgesucht. Dieses Schema wurde veröffentlicht von der Landwirtschaftskammer Schleswig-Holstein.
[PDF in neuen Tab anzeigen](https://www.lksh.de/fileadmin/PDFs/Gartenbau/Fruchtfolge_im_Garten.pdf){target=blank}

!!! info "Pflanzenfamilien Schema"
	=== "Kreuzblütler"
        ```mermaid
        graph LR
            A[Kreuzblütler]-->B[Liliengewächse] & C[Nachtschattengewächse]
        ```
	=== "Korbblütler"
        ```mermaid
        graph LR
            A[Korbblütler]-->B[Gänsefußgewächse] & C[Nachtschattengewächse] & D[Liliengewächse]
        ```
	=== "Nachtschattengewächse"
        ```mermaid
        graph LR
            A[Nachtschattengewächse]-->B[Kreuzblütler] & C[Gänsefußgewächse]
        ```
	=== "Doldenblütler"
        ```mermaid
        graph LR
            A[Doldenblütler]-->B[Gänsefußgewächse] & C[Nachtschattengewächse]
        ```
	=== "Gänsefußgewächse"
        ```mermaid
        graph LR
            A[Gänsefußgewächse]-->B[Doldenblütler] & C[Nachtschattengewächse] & D[Hülsenfrüchte] & E[Liliengewächse]
        ```
	=== "Hülsenfrüchte"
        ```mermaid
        graph LR
            A[Hülsenfrüchte]-->B[Gänsefußgewächse] & C[Nachtschattengewächse] &  D[Liliengewächse]
        ```
	=== "Kürbisgewächse"
        ```mermaid
        graph LR
            A[Kürbisgewächse]-->B[Gänsefußgewächse] & C[Hülsenfrüchte] &  D[Liliengewächse]
        ```
	=== "Liliengewächse"
        ```mermaid
        graph LR
            A[Liliengewächse]-->B[Kreuzblütler] & C[Korbblütler] &  D[Doldenblütler] & E[Gänsefußgewächse] & F[Hülsenfrüchte] & G[Kürbisgewächse] & H[Nachtschattengewächse]
        ```
	=== "Baldriangewächse"
        ```mermaid
        graph LR
            A[Baldriangewächse]-->B[alle anderen Pflanzenfamilien] 
        ```
	=== "Gräser"
        ```mermaid
        graph LR
            A[Gräser]-->B[alle anderen Pflanzenfamilien] 
        ```
	=== "Wasserblattgewächse"
        ```mermaid
        graph LR
            A[Wasserblattgewächse]-->B[alle anderen Pflanzenfamilien] 
        ```
### Pflanzenfilter
Wenn die Checkbox aktiv ist, werden die erstellten Fruchtfolgen nach den Pflanzen gefiltert die in der [Pflanzenliste](pflanzenliste.md) sich befinden und auch gecheckt sind.
Am besten geeignet für die [automatische](#automatische-fruchtfolge) Generierung von Fruchtfolgen.


## Tabelle
Die Tabelle stellt alle Fruchtfolgen dar die mit den gewählten Optionen möglich sind. Fruchtfolgeglieder können teilweise mehrere Pflanzen beinhalten([Dropdown](#dropdown)). Die Fruchtfolgezyklen können gespeichert werden([Merken-Button](#merken)). 
 

!!! info "Erweiterung geplant"
	*Momentan können nur Fruchtfolgen gespeichert werden die pro Zehrer nur ein Vertreter haben. Die Planung mit mehreren Pflanzen als Folgefrucht auf eine Vorfrucht ist noch nicht möglich. So kann z.B  auf Gurke nicht 2 Pflanzen an Folgefrucht gewählt werden, im Fall, dass man von der Folgefrucht nicht so viel braucht.*

### Dropdown
Hinter den Dropdown  verbergen sich alle Pflanzen die dort als Folgefrucht angebaut werden können. Da es von z.B Mittelzehrer/Gänsefußgewächs mehrere Vertreter gibt(Spinat, Rote Bete).

### Merken
Fruchtfolgezyklus kann gespeichert werden, unter Eingabe eines selbstgewählten Namens. Diese wird dann in der [Zyklustabelle](zyklustabelle.md) gespeichert.


---

Wenn sie alle Fruchtfolgezyklen geplant haben, die sie für Ihren Garten brauchen können Sie diese Fruchtfolgezyklen auf Beete verteilen: [Anleitung Fruchtfolge Verteilung](./fruchtfolge-verteilung.md)