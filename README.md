#Resources
[frontEnd masters course](https://frontendmasters.com/courses/d3-v4/enter-append)

[d3 API reference](https://github.com/d3/d3/blob/master/API.md)

[online editor with tons of examples to search through and play with](http://blockbuilder.org/)

[examples](https://bl.ocks.org/)

#Scales
Common scales:
Continuous
Default
```javascript
Scale.Linear()
```
Some values are really large and some are really small
```javascript
Scale.Log()
```
Map between dates and numbers
```javascript
Scale.Time()
```
Categorical
```javascript
Scale.Band()
```
define a scale
```javascript
    var yScale = d3.scaleLinear()
        .domain(extent)
        .range([500, 0]);
```
pass the scale into the axis object
```javascript
var yAxis = d3.axisLeft()
    .scale(yScale);
```

g group element - svg container that helps you nest svg elements inside it (like a div)
the only thing you can nest in svg are group elements which are the containers for all other elements.
```javascript
.append('g')
```
move the axis 40 pixels across and 20 pixels down so it's not starting in the top left corner
```javascript
.attr('transform', 'translate( 40, 20)')
```
render axis to screen
```javascript
.call(yAxis)
```