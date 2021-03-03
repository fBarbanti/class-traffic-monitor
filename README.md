# class-traffic-monitor

```class-traffic-monitor``` implements a module to view road traffic in the MASA area detected by smart cameras.

The goal is to provide the user with the ability to monitor traffic at various time aggregates, with the ability to differentiate traffic based on the type of vehicle. The aggregate data used in this phase were previously calculated using the software present in the following repository: https://github.com/fBarbanti/class-real-time-aggregator.git

In particular, the interactive map has the task of showing traffic on the basis of a palette composed of the following colors: green, orange and red.
The traffic evaluation criterion, that is the rule that determines when it is flowing or heavy, derives directly from the traffic flows made available by the Regione Emilia Romagna. It has been noted how, up to a transit of 8000 vehicles per day, the region evaluates the traffic as smooth, from 8000 to 18,000 slowdowns and from 18,000 onwards heavy traffic. For this reason, if the density of vehicles in each road section is:

- < 6 traffic is flowing and the corresponding color is green
-  \>=6 and < 13 the traffic is flowing with some slowdown and the corresponding color is orange
- \>= 13 traffic is heavy and the corresponding color is red 

## Dependencies
- Jupyter Notebook
- ipywidgets
- matplotlib
- Python 3
- Folium 
- Numpy
- pandas
- findspark
- PySpark
- Apache Spark (version 2.4.5)


## Use

```
jupyter notebook Done.ipynb
```
A test aggregate data set has been loaded into the sink directory, which is the reason why the interactive map always shows green.
