# WasserfallExtended

Dies ist das Repository zur gepackten PowerBi-Visual-Datei. Es beschreibt die Funktionsweise des Visuals. 

## Beschreibung

Das Wasserfall Extended Visual ist eine Wasserfall Darstellung mit Delta Funktion. Das bedeutet, dass mehrere Measure über einen deltabalken miteinander verglichen, oder wie im Wasserfallmodell im Hochlauf gestapelt werden können. Zudem gibt es die Möglichkeit, Endbar hinzuzufügen. Endbars sind Balken, die Wertigkeit eines Mesures zum Ende einer Periode haben soll. Das Delta wird so nicht nur zum Measure, sondern auch zum Endbar dargestellt.
Im Weiteren sind die Funktion erneut detailreicher erklärt: 

## Funktionen

### Wasserfall Modell
Dem Visual können bis zu 10 Measures hinzugefügt werden. Für jedes Measure kann definiert werden, ob es sich bei dem Balken um einen 
1. Balken handelt, der ab der Null Line beginnt.
2. Balken handelt, der gestapelt wird und somit einen Hochlauf darstellt
3. Ein Endbalken ist, der über dem vorherigen Balken dargestellt wird und die Wertigkeit des vorherigen Measures bis zum Ende einer Periode darstellt. (Jahr, Monat, Tag, etc)
   
Zusätzlich kann zu jedem gestapelten Balken definiert werden, ob die bisher "erstapelte" Höhe mit einem Balken dargestellt werden soll. (Summen Balken). Dies ist sehr praktisch, wenn zum Beispiel eine Übertragungsbrücke definiert werden soll. Beispiel: erster Balken ist das Jahresergebnis aus dem letzten Jahr. Im Anschluss kommen mehrere Balken, die die Abweichung zum Jahresendergebnis diesen Jahres darstellen. Anstatt aber den letzten Balken mit einem Measure zu berechnen, kann der Summenbalken definiert werden.

### Delta Model
