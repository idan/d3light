# Conduct

Conduct is a set of SVG primitives implemented as React components, with useful hooks for orchestrating these components with D3.

Both D3 and React want to have their hands on the steering wheel when it comes to the DOM. This leads to one of two approaches:

1. Generate the SVG DOM nodes using D3 in a React "leaf" component. React is effectively blind to the D3-generated DOM nodes.

2. Generate the SVG DOM nodes using React, and use D3 as a utility library for deciding when and how they ought to update themselves.

Conduct takes the latter approach, supplying React components for the common SVG elements (`g`, `line`, `rect`, etc…) Each of these components has additional lifecycle hooks which correspond to D3's [enter-update-exit pattern](http://bl.ocks.org/mbostock/3808218). Conduct codifies the ways in which new data affects the rendering of components, allowing D3 to step in and work its transitional magic.

Conduct is _not_ a charting library for React, in the same sense that D3 is not a charting library but a visualization toolkit. You could build full-featured chart components using Conduct and D3; the process will
