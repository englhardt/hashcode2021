# Hashcode 2021

Our solution for the coding challenge [Hashcode 2021](https://codingcompetitions.withgoogle.com/hashcode).<br>
Our code contains a implementation of the simulation and a scoring function.

### Competition results
Place 2650 out of 9004 teams.

```
A           2,000
B       4,566,384
C       1,298,723
D       1,571,622
E         684,513
F         806,897
-----------------
Total:  8,930,139
```

### Approach

* *Baseline*: every light is green for 1s
* *Greedy*: baseline + ignore streets where no car will ever drive

Improvements:

* *Reorder*: green light first for streets where cars start
* *Adjust Timings*: distribute a green-time budget in seconds (default 1.5x amount of streets per intersection) for each intersection based on the busyness of all ingoing street. The busyness of a street is measured by its total appearance in all paths of all cars.

#### Post-competition results
Available in the [notebook](https://github.com/englhardt/hashcode2021/blob/main/hashcode2021.ipynb).
Changes to competition results in brakets
```
A           2,002   (+       2)
B       4,566,896   (+     512)
C       1,300,791   (+   2,068)
D       1,592,534   (+  20,912)
E         729,272   (+  44,759)
F       1,371,587   (+ 564,690)
------------------------------
Total:  9,563,082   (+ 632,943)
```
