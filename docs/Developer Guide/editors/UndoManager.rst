The UndoManager is loaded with the Editorview, and provides undo/redo
services. Most of the other editors depend on this because their
commands up to the reflector pass through it.

The Undo Manager keeps a record of messages sent up to the reflector,
and stores the information necessary to undo those operations. For
instance, if you delete a node, the Undomanager keeps a copy of the node
definition. When you undo, the UndoManager sends a command up to the
reflector with a 'createNode' command and the old object definition.

Note that the UndoManager cannot undo changes to the application state
that happen within the VWF model. For instance, you cannot undo the
effects of a mouse click on an inworld script. This should not be an
issue, as the `Publisher <Publisher>`__ should reset world state after
you test an application.
