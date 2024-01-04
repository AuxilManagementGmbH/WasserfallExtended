This is the repository for the packed PowerBi visual file. It describes how the visual works. 

## Description

The waterfall extended visual is a waterfall visualisation with a delta function. This means that several measures can be compared with each other via a delta bar or stacked in a run-up as in the waterfall model. There is also the option of adding end bars. End bars are bars that should have the value of a measure at the end of a period. The delta is thus not only displayed for the measure, but also for the end bar.

## Description of terms

The following terms are used in the visual: 
1. bar
2. intermediate bar
3. total bar
4. end bar
5. delta
6. delta next

### Bar
A bar is an added measure that starts at 0 on the X-axis.

### Intermediate bar
An intermediate bar is a bar that starts at the end value of the previous bar. If there is no bar, an intermediate bar is a bar by logic. 
If a bar, intermediate bar or end bar precedes an intermediate bar, the intermediate bar starts at the current value of the sum of all previous bars. 

### Total bar
In addition, you can define for each stacked bar whether the previously "stacked" height should be displayed with a bar. (Totals bar). This is very practical if, for example, a transition is to be defined. Example: The first bar is the annual result from the previous year. This is followed by several bars that represent the deviation from the year-end result for this year. However, instead of calculating the last bar with a measure, the totals bar can be defined. Totals bars can be defined for each intermediate bar that is not at the top of the totals chain.

### End bar
An end bar is a bar that can be placed after a previous intermediate bar or bar. If there is no bar, an end bar is a bar in terms of logic. 
End bars are good to use if you want to display not just the delta for one value in a target/actual comparison, but for two, without making the diagram unnecessarily wide. 
For example, imagine a target/actual comparison that compares the actual value of a month up to the current day with the target value of the month up to the current day. Now it may also make sense to show how big the difference is up to the target at the end of the month. In this case, the end of the month is shown with the end bar. This can be visualised as if the target bar were filling the shell of the end-of-month bar. 

### Delta
A delta represents the difference between two consecutive measures. If these two measures are configured as bar and end bar, these two bars are no longer displayed one above the other, but are separated by the delta.

### Delta Next
A delta next represents the difference between a measure and the next but one measure. The DeltaNext is always displayed above a delta. Imagine, for example, a target/actual comparison that compares the actual value of a month up to the current day with the target of the month up to the current day. Now it may also make sense to show how big the difference is up to the target at the end of the month. In this case, the end of the month is shown with the end bar. The Delta Next could now be used to show the deviation from the end of the month. As with the end bar, this can also be visualised in such a way that the delta fills or even overfills the envelope of the delta next.

## Formatting
The visual can be formatted extensively. The following formatting is possible:

### Visualisations

#### X-axis
The X-axis is the zero line of the bars.

can be set:
1. display
2. colour
3. line width

#### Lines
The lines are the connections between the bars. If a bar is negative, the connection starts at the lower end of the bar. If the connected bar is negative, the connection ends at the upper end of the next bar. If a bar is positive, the connection starts at the upper end of the bar. If the connected bar is positive, the connection ends at the lower end of the next bar. Connections only exist in the following constellations:  
Bar - delta
Bar - Intermediate bar
Bar - Delta Next
Delta - bar
Delta - end bar
Delta Next - Bar
Delta Next - end bar
Delta Next - Intermediate bar
Intermediate bar - Delta
Intermediate bar - Delta Next
Intermediate bar - Total bar
Totals bar - Delta
Totals bar - Delta Next
Total bar - Intermediate bar

can be set:
1. display
2. colour
3. line width

#### Bar numbers
These are the values of the measures, as well as the totals bar, delta and delta next.

The following can be set:
1. display
2. position value end bar (top - outside, centre, bottom - outside, auto)
3. position value Delta (Top - Outside, Centre, Bottom - Outside, Auto)
4. position value delta next (top - outside, centre, bottom - outside, auto)
5. distance to the bar
6. font
7. font size
8. styling (bold, italic, underline)
9. font colour (function and fixed)

#### Categories
The categories are the names of the measures and the delta, delta next and totals bars. These are always displayed below the visualisation. 

The following can be set:
1. display
5. distance to the X-axis
6. font
7. font size
8. styling (bold, italic, underline)
9. font colour (function and fixed)

### Bar settings
A group will appear in this section for each measure. In each group, you can define the settings for the respective measure.

The following can be set: 
1. type of bar (bar, intermediate bar, end bar)
2. whether the bar should be filled in
 2.1 Colour of the bar (function and fixed)
3. whether the bar should have a border
 3.1 Type of border (solid, dotted)
  3.1.1 The stroke type of the border (tuple consisting of [proportion free space, proportion coloured])
 3.2 Thickness of the border
 3.3 Colour of the border (function and fixed)
4. position of the bar value (top - outside, centre, bottom - outside, auto)
5. whether a totals bar should be displayed
 5.1 Name of the bar
 5.2 Whether the totals bar should be filled (function and fixed)
 5.3 Whether the bar should have a border
  5.3.1 Type of border (Solid, Dotted)
   5.3.1.1 The stroke type of the border (tuple consisting of [proportion free space, proportion coloured])
  5.3.2 Thickness of the border
  5.3.3 Colour of the border (function and fixed)
6 Whether a delta should be added
 6.1 Name of the delta
  6.1.1 Colour of the delta if positive (function and fix)
  6.1.2 Colour of the delta if negative (function and fix)
 6.2 Whether the bar should have a border
  6.2.1 Type of border (solid, dotted)
   6.2.1.1 The stroke type of the border (tuple consisting of [proportion free space, proportion coloured])
  6.2.2 Thickness of the border
  6.2.3 Colour of the border (function and fixed)
7. whether a Delta Next should be added
 7.1 Name of the delta
  7.1.1 Colour of the delta if positive (function and fix)
  7.1.2 Colour of the delta if negative (function and fix)
 7.2 Whether the bar should have a border
  7.2.1 Type of border (solid, dotted)
   7.2.1.1 The stroke type of the border (tuple consisting of [proportion free space, proportion coloured])
7.2.2 Thickness of the border
7.2.3 Colour of the border (function and fixed)
