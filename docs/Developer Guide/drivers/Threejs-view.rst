Three.js View Driver
====================

The THREE.js View Driver manages all the rendering of the scene. It also
includes the code for dealing with user input events and sending them
over the VWF socket.

This component is also responsible for displaying the inset selected
camera view, and for rendering the object selection lines.

This driver is responsible for manipulating the graphics engine objects.
Much of the actual functionality has been moved into the subdrivers, but
some remains for historical reasons.
