# 2. Fruchtfolge erstellen
Aus den Pflanzen die Sie sich ausgesucht haben können in der Tabelle Fruchtfolgezyklen erstellt werden. Spezifische Konfigurationen liefern dabei unterschiedliche Fruchtfolgen.

---
## Inputleiste
In der Inputleiste lassen sich Fruchtfolgetabellen erstellen, löschen und speichern.

Durch das drücken des Erstellen-Buttons in der Inputleiste wird ein Dialog ausgelöst in dem sie 
spezifische Optionen auswählen, um ihre Fruchtfolge einfach und schnell zu erstellen.

- [**Fruchtfolge Name**](#fruchtfolge-name)

- [**Zehrerlänge**](#zehrerlange) 

- [**Pflanzenfamilie**](#pflanzenfamilie)

### Fruchtfolge Name
Muss eingegeben werden um die Fruchtfolge sinnvoll darzustellen und  abzuspeichern.
Es ist hilfreich  jede Tabelle einen einzigartigen Namen zu geben um im späteren planen die Handhabung zu erleichtern. 

### Zehrerlänge

Diese bestimmt wie die Fruchtfolgelänge in Bezug auf die Zehrertypen die vertreten sind.  Und gibt dementsprechend die Folgefrüchte aus. 

Im Dialog muss sich für ein Zehrertypzyklus entschieden werden da er die Grundlage für die Tabelle darstellt. 
Zudem muss sich ein Startzehrertyp ausgesucht werden. Diese Auswahl hat Einfluss auf die [Startfrucht](#startfrucht).
Es gibt zwei voreingestellte Zehrertypzyklen. 


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

Bestimmt  welche Pflanzenfamilien als Folgefrucht erlaubt sind. Es sind 2 Regelwerke dafür voreingestellt.

Optional kann eine Startpflanzenfamilie eingestellt werden, was jedoch Auswirkungen auf die [Startfrucht](#startfrucht) hat.

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


### Startfrucht

Geben Sie  in das Eingabefeld  Gemüse  ein, die Sie gerne anbauen möchten oder die sich in der [Pflanzenliste](./pflanzenliste.md) befinden. Die  Autovervollstänigung schlägt  gleich Pflanzen vor, die in der Datenbank hinterlegt sind, dem Zehrertypzyklus und der Pflanzenfamilie entsprechen. 

!!! tip "Planung beginnen"
	Es ist zu empfehlen, mit der Eingabe der Starkzehrer anzufangen, da sie am wenigsten Spielraum bieten, und meißtens auch der Fokus sind.

## Tabelle
Die Tabelle wird erstellt nach den Einstellungen die im Dialog getroffen wurden.
Dabei können sich nacheinander die Fruchtfolgeglieder über ein [Dropdown](#dropdown) ausgesucht werden. 
Die Fruchtfolgezyklen können gespeichert werden, wenn sie in die [Checkbox](#checkbox) der Tabelle einen Haken setzen.. 
 

!!! info "Erweiterung geplant"
	*Momentan können nur Fruchtfolgen gespeichert werden die pro Zehrer nur ein Vertreter haben. Die Planung mit mehreren Pflanzen als Folgefrucht auf eine Vorfrucht ist noch nicht möglich. So kann z.B  auf Gurke nicht 2 Pflanzen an Folgefrucht gewählt werden, im Fall, dass man von der Folgefrucht nicht so viel braucht.*

### Dropdown
Hinter den Dropdown  verbergen sich alle Pflanzen die dort als Folgefrucht angebaut werden können. Da es von z.B Mittelzehrer/Gänsefußgewächs mehrere Vertreter gibt(Spinat, Rote Bete).

### Checkbox
Mit setzen des Hakens in der Checkbox kann der Zyklus gespeichert werden.
Diese wird dann in der [Zyklustabelle](zyklustabelle.md) gespeichert.


---

Wenn sie alle Fruchtfolgezyklen geplant haben, die sie für Ihren Garten brauchen können Sie diese Fruchtfolgezyklen auf Beete verteilen: [Anleitung Fruchtfolge Verteilung](./fruchtfolge-verteilung.md)