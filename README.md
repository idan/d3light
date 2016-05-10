# D3light

Both D3 and React want to have their hands on the steering wheel when it comes to the DOM. This leads to one of two approaches:

1. Generate the SVG DOM nodes using D3 in a React "leaf" component. React is effectively blind to the D3-generated DOM nodes.

2. Generate the SVG DOM nodes using React, and use D3 as a math library for computing the properties of those elements.

D3light takes the latter approach, supplying a base React component with conventions for passing in data, as well as components for common SVG elements (`g`, `line`, `rect`, etc…)  D3light codifies the ways in which new data affects the rendering of components, and sets up common listeners for things that trigger re-renders, like component dimension changes.

D3light is _not_ a charting library for React, in the same sense that D3 is not a charting library but a visualization toolkit.
