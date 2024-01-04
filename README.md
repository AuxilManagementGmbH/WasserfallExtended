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


