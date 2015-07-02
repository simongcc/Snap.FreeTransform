# Snap.FreeTransform

Adaptation of [Raphael.FreeTransform](https://github.com/ElbertF/Raphael.FreeTransform) plugin for [Snap](http://snapsvg.io/). This is a fork with a few adjustments.
Provides a free transform tool to move, rotate and scale elements.

##Usage
`Snap.freeTransform(element, options, callback);`
```
element - Snap element
options - optional, default options:
  animate: false,
  attrs: { fill: '#fff', stroke: '#000' },
  bboxAttrs: { fill: 'none', stroke: '#000', 'stroke-dasharray': '4, 4', opacity: 0.5},
  axesAttrs: { fill: '#fff', stroke: '#000', 'stroke-dasharray': '4, 4', opacity: 0.5},
  discAttrs: { fill: '#fff', stroke: '#000' },
  boundary: { x: paper._left || 0, y: paper._top || 0, width: null, height: null },
  distance: 1.3,
  drag: true,
  draw: false,
  keepRatio: false,
  range: { rotate: [ -180, 180 ], scale: [ -99999, 99999 ] },
  rotate: true,
  scale: true,
  snap: { rotate: 0, scale: 0, drag: 0 },
  snapDist: { rotate: 0, scale: 0, drag: 7 },
  size: 5,
  bodyCursor: 'auto',
  cornerCursors: ['nwse-resize', 'nesw-resize', 'nwse-resize', 'nesw-resize'],
  sideCursors: ['ns-resize', 'ew-resize', 'ns-resize', 'ew-resize']
callback - optional, default is null
```

## TODO
- split into chunks for easier maintenance and testing
- leverage groups; remove reliance on `toFront()` / `toBack()`
- test suite; write tests
- animate: false, does not work with 0.4.1 need bug fix
- when hideHandles() is applied, restore the element cursor to default instead of keeping `move`
