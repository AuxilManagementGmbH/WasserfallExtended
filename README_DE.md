# WasserfallExtended

Dies ist das Repository zur gepackten PowerBi-Visual-Datei. Es beschreibt die Funktionsweise des Visuals. 

## Beschreibung

Das Wasserfall Extended Visual ist eine Wasserfall Darstellung mit Delta Funktion. Das bedeutet, dass mehrere Measure über einen deltabalken miteinander verglichen, oder wie im Wasserfallmodell im Hochlauf gestapelt werden können. Zudem gibt es die Möglichkeit, Endbar hinzuzufügen. Endbars sind Balken, die Wertigkeit eines Mesures zum Ende einer Periode haben soll. Das Delta wird so nicht nur zum Measure, sondern auch zum Endbar dargestellt.

## Begriffsbeschreibung

Im Visual werden folgende Begriffe verwendet: 
1. Balken
2. Zwischenbalken
3. Summenbalken
4. Endbalken
5. Delta
6. Delta Next

### Balken
Ein Balken ist ein hinzugefügtes Measure, welches an der X-Achse bei 0 beginnt.

### Zwischenbalken
Ein Zwischenbalken ist ein Balken, der am Endwert des vorherigen Balkens beginnt. Ist kein Balken vorhanden, ist ein Zwischenbalken von der Logik ein Balken. 
Ist ein Balken, Zwischenbalken oder Endbalken vor einem Zwischenbalken, so beginnt der Zwischenbalken an dem aktuellen Wert der Summe aller vorherigen Balken. 

### Summenbalken
Zusätzlich kann zu jedem gestapelten Balken definiert werden, ob die bisher "erstapelte" Höhe mit einem Balken dargestellt werden soll. (Summen Balken). Dies ist sehr praktisch, wenn zum Beispiel eine Überleitung definiert werden soll. Beispiel: erster Balken ist das Jahresergebnis aus dem letzten Jahr. Im Anschluss kommen mehrere Balken, die die Abweichung zum Jahresendergebnis diesen Jahres darstellen. Anstatt aber den letzten Balken mit einem Measure zu berechnen, kann der Summenbalken definiert werden. Summenbalken können für jeden Zwischenbalken definiert werden, der nicht an erster Stelle der Summenkette steht.

### Endbalken
Ein Endbalken ist ein Balken, der hinter einem vorherigen Zwischenbalken oder Balken platziert werden kann. Ist kein Balken vorhanden, ist ein Endbalken von der Logik ein Balken. 
Endbalken sind gut zu verwenden, wenn in einem Soll-Ist-Abgleich nicht nur das Delta zu einem Wert, sondern zu zweien angezeigt werden soll, ohne, dass das Diagram unnötig breit wird. 
Stellt man sich zum Beispiel ein Soll-Ist Abgleich vor, der den Ist-Wert eines Monats bis zum aktuellen Tag mit dem Soll des Monats bis zum aktuellen Tag vergleicht. Nun kann es durchaus sinnvoll erscheinen ebenfalls darzustellen, wie groß der Unterschied bis zum Soll des Monatsende ist. Das Monatsende wird in diesem Fall mit dem Endbalken dargestellt. Visuell kann dies so darsgestellt werden, als würde der Soll Balken die Hülle des Monatsendbalken ausfüllen. 

### Delta
Ein Delta stellt den Unterschied zwischen zwei aufeinanderfolgende Measures da. Sollten diese beiden Measures als Bar und Endbar konfiguriert sein, so werden diese beiden Balken nicht mehr übereinander dargestellt, sondern werden vom Delta getrennt.

### Delta Next
Ein Delta Next stellt den Unterschied zwischen einem Measure und dem übernächsten Measure dar. Das DeltaNext wird immer über einem Delta dargestellt. Stellt man sich zum Beispiel ein Soll-Ist Abgleich vor, der den Ist-Wert eines Monats bis zum aktuellen Tag mit dem Soll des Monats bis zum aktuellen Tag vergleicht. Nun kann es durchaus sinnvoll erscheinen ebenfalls darzustellen, wie groß der Unterschied bis zum Soll des Monatsende ist. Das Monatsende wird in diesem Fall mit dem Endbalken dargestellt. Mit dem Delta Next könnte man nun die Abweichung zum Monatsende darstellen. Visuell kann auch dies wie beim Endbalken so dargestellt werden, dass das Delta die Hülle des Delta Next auffüllt oder sogar überfüllt.
 

## Formatierungen
Das Visuell kann umfangreich formatiert werden. Folgende Formatierungen sind möglich:

### Visualisierungen

#### X-Achse
Die X-Achse ist die Null-Linie der Balken.

Eingestellt werden kann:
1. Anzeigen
2. Farbe
3. Linienbreite

#### Linien
Die Linien sind die Verbindungen zwischen den Balken. Ist ein Balken negativ, so beginnt die Verbindung am unteren Ende des Balkens. Ist der verbundene Balken negativ, endet die Verbindung am oberen Ende des nächsten Balkens. Ist ein Balken positiv, so beginnt die Verbindung am oberen Ende des Balkens. Ist der verbundene Balken positiv, endet die Verbindung am unteren Ende des nächsten Balkens. Verbindungen existieren nur in folgenden Konstellationen:  
Balken - Delta
Balken - Zwischenbalken
Balken - Delta Next
Delta - Balken
Delta - Endbalken
Delta Next - Balken
Delta Next - Endbalken
Delta Next - Zwischenbalken
Zwischenbalken - Delta
Zwischenbalken - Delta Next
Zwischenbalken - Summenbalken
Summenbalken - Delta
Summenbalken - Delta Next
Summenbalken - Zwischenbalken

Eingestellt werden kann:
1. Anzeigen
2. Farbe
3. Linienbreite

#### Bar Zahlen
Dies sind die Werte der Measures, sowie Summenbalken, Delta und Delta Next.

Eingestellt werden kann:
1. Anzeigen
2. Position Wert Endbalken (Oben - Außerhalb, Mitte, Unten - Außerhalb, Auto)
3. Position Wert Delta (Oben - Außerhalb, Mitte, Unten - Außerhalb, Auto)
4. Position Wert Delta Next (Oben - Außerhalb, Mitte, Unten - Außerhalb, Auto)
5. Abstand zum Balken
6. Schriftart
7. Schriftgröße
8. Styling (Fett, Kursiv, Unterstrichen)
9. Schriftfarbe (Funktion und Fix)

#### Kategorien
Die Kategorien sind die Namen der Measures und der Delta, Delta Next und Summenbalken. Diese werden immer unterhalb der Visualisierung dargestellt. 

Eingestellt werden kann:
1. Anzeigen
5. Abstand zur X-Achse
6. Schriftart
7. Schriftgröße
8. Styling (Fett, Kursiv, Unterstrichen)
9. Schriftfarbe (Funktion und Fix)

### Balken Einstellungen
Für jedes Measure wird in diesem Abschnitt eine Gruppe erscheinen. In jeder Gruppe kann man die EInstellungen für das jeweilige Measure definieren.

Eingestellt werden kann: 
1. Typ des Balkens (Balken, Zwischenbalken, Endbalken)
2. Ob der Balken ausgefüllt werden soll
 2.1. Farbe des Blakens (Funktion und Fix)
3. Ob der Balken einen Rand haben soll
 3.1 Typ des Randes (Solide, Gepunktet)
  3.1.1 Die Strichelungsart des Randes ( Tupel bestehend aus [Anteil Freiraum, Anteil Gefärbt])
 3.2 Dicke des Randes
 3.3 Farbe des Randes (Funktion und Fix)
4. Position des Balkenwertes  (Oben - Außerhalb, Mitte, Unten - Außerhalb, Auto)
5. Ob ein Summenbalken angezeigt werden soll
 5.1 Name des Balkens
 5.2 Ob der Summenbalken ausgefüllt werden soll (Funktion und Fix)
 5.3. Ob der Balken einen Rand haben soll
  5.3.1 Typ des Randes (Solide, Gepunktet)
   5.3.1.1 Die Strichelungsart des Randes ( Tupel bestehend aus [Anteil Freiraum, Anteil Gefärbt])
  5.3.2 Dicke des Randes
  5.3.3 Farbe des Randes (Funktion und Fix)
6. Ob ein Delta hinzugefügt werden soll
 6.1 Name des Deltas
  6.1.1 Farbe des Deltas wenn Positiv (Funktion und Fix)
  6.1.2 Farbe des Deltas wenn Negativ (Funktion und Fix)
 6.2. Ob der Balken einen Rand haben soll
  6.2.1 Typ des Randes (Solide, Gepunktet)
   6.2.1.1 Die Strichelungsart des Randes ( Tupel bestehend aus [Anteil Freiraum, Anteil Gefärbt])
  6.2.2 Dicke des Randes
  6.2.3 Farbe des Randes (Funktion und Fix)
7. Ob ein Delta Next hinzugefügt werden soll
 7.1 Name des Deltas
  7.1.1 Farbe des Deltas wenn Positiv (Funktion und Fix)
  7.1.2 Farbe des Deltas wenn Negativ (Funktion und Fix)
 7.2. Ob der Balken einen Rand haben soll
  7.2.1 Typ des Randes (Solide, Gepunktet)
   7.2.1.1 Die Strichelungsart des Randes ( Tupel bestehend aus [Anteil Freiraum, Anteil Gefärbt])
7.2.2 Dicke des Randes
7.2.3 Farbe des Randes (Funktion und Fix)
