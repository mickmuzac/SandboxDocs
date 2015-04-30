The name of this class is somewhat out of date - it now handles editing
all objects which expose an ``EditorData`` property.

The class builds a GUI for a given ``EditorData``. If more than one
object is selected, it will use the ``EditorData`` from the first. When
setting properties, if multiple objects are selected, *it will set the
same property name and value for all selected objects*.

In addition to setting up a GUI for the EditorData, it contains 2 tabs
for properties of all objects. These tabs are the *Transform* and
*Flags* tabs. See `Object Flags <Object%20Flags>`__ and the `Transform
Property <Transform%20Property>`__.

.. figure:: http://i.imgur.com/JfUylH4.png
   :alt: 
