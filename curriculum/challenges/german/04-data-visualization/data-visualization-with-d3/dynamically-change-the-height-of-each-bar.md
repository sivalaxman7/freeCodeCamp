---
id: 587d7fa9367417b2b2512bcf
title: Dynamisches Ändern der Höhe jedes Balkens
challengeType: 6
forumTopicId: 301486
dashedName: dynamically-change-the-height-of-each-bar
---

# --description--

The height of each bar can be set to the value of the data point in the array, similar to how the `x` value was set dynamically.

```js
selection.attr("property", (d, i) => {

})
```

Here `d` would be the data point value, and `i` would be the index of the data point in the array.

# --instructions--

Change the callback function for the `height` attribute to return the data value times 3.

**Note:** Remember that multiplying all data points by the same constant scales the data (like zooming in). Die Unterschiede zwischen den Balkenwerten sind in diesem Beispiel gut zu erkennen.

# --hints--

The first `rect` should have a `height` of `36`.

```js
assert($('rect').eq(0).attr('height') == '36');
```

The second `rect` should have a `height` of `93`.

```js
assert($('rect').eq(1).attr('height') == '93');
```

The third `rect` should have a `height` of `66`.

```js
assert($('rect').eq(2).attr('height') == '66');
```

The fourth `rect` should have a `height` of `51`.

```js
assert($('rect').eq(3).attr('height') == '51');
```

The fifth `rect` should have a `height` of `75`.

```js
assert($('rect').eq(4).attr('height') == '75');
```

The sixth `rect` should have a `height` of `54`.

```js
assert($('rect').eq(5).attr('height') == '54');
```

The seventh `rect` should have a `height` of `87`.

```js
assert($('rect').eq(6).attr('height') == '87');
```

The eighth `rect` should have a `height` of `42`.

```js
assert($('rect').eq(7).attr('height') == '42');
```

The ninth `rect` should have a `height` of `27`.

```js
assert($('rect').eq(8).attr('height') == '27');
```

# --seed--

## --seed-contents--

```html
<body>
  <script>
    const dataset = [12, 31, 22, 17, 25, 18, 29, 14, 9];

    const w = 500;
    const h = 100;

    const svg = d3.select("body")
                  .append("svg")
                  .attr("width", w)
                  .attr("height", h);

    svg.selectAll("rect")
       .data(dataset)
       .enter()
       .append("rect")
       .attr("x", (d, i) => i * 30)
       .attr("y", 0)
       .attr("width", 25)
       .attr("height", (d, i) => {
         // Add your code below this line



         // Add your code above this line
       });
  </script>
</body>
```

# --solutions--

```html
<body>
  <script>
    const dataset = [12, 31, 22, 17, 25, 18, 29, 14, 9];

    const w = 500;
    const h = 100;

    const svg = d3.select("body")
                  .append("svg")
                  .attr("width", w)
                  .attr("height", h);

    svg.selectAll("rect")
       .data(dataset)
       .enter()
       .append("rect")
       .attr("x", (d, i) => i * 30)
       .attr("y", 0)
       .attr("width", 25)
       .attr("height", (d, i) => {
         return d * 3
       });
  </script>
</body>
```
