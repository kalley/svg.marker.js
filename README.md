svg.marker.js
=============

A plugin for [svg.js](http://svgjs.com) adding marker functionality.

Svg.marker.js is licensed under the terms of the MIT License.

## Usage
Include this plugin after including the svg.js libarary in your html document.

### Creating a marker
Two parameters are required to create a marker: `width` and `height`.

```javascript
var marker = draw.defs().marker(20, 10);

// Add that which will be used be rendered
marker.path('M0,0L20,5L0,10z').attr({
  fill: '#999',
  'stroke-width': 0
});


// ... then later
draw.polyline([[0, 3], [5, 16]]).attr('marker-end', marker);
```

Alternatively, you can give your marker an id, and set it as it would be traditionally:

```javascript
marker.attr('id', 'triangle');

draw.polyline('0,3 5,16').attr('marker-end', 'url(#triangle)');
```

You'll probably want to add some of the following attributes ( if not all )

 * `markerWidth` _default: `3`_
 * `markerHeight` _default: `3`_
 * `orient` _default: `'auto'`_ (this is the only one that is set by the plugin)
 * `refX` _default: `0`_
 * `refY` _default: `0`_

For more information on each of these attributes (and markers in general) see [http://www.w3.org/TR/SVG/painting.html#MarkerElement](http://www.w3.org/TR/SVG/painting.html#MarkerElement)

