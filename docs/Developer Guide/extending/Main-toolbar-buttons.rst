|Login Icon| Login (File->Login)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The VWF Sandbox application requires user to log into a world before
making any changes to that world. User accounts are stored on the
server, and are valid for all worlds on the server. However, you must
log in to each separate world when joining. If you do not have an
account, you can create one from the log in dialog by selecting 'Create
Profile...' from the list of user names.

|Logout Icon| Logout (File->Logout)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

You can use this to remove your character from the world, while keeping
your browser pointer at that world. You will be able to see changes
happening in the world, but you will not be able to interact.

|Move Icon| Move (Edit->Transform->Move)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Activate the move tool. This will place a 'gizmo' over the selected
object. Click and drag on the colored lines to move the object in the
direction of that line. Hold your mouse between lines to select the
plane made from those two lines. Clicking and dragging while a plane
handle is selected will move the object along the selected plane.

|Rotate Icon| Rotate (Edit->Transform->Rotate)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Activate the rotate tool. This will place a 'gizmo' over the selected
object. Click and drag around the circumference of the circle to rotate
the object around the vector that defines the center of that circle.
TIP: drag around the circle, not tangent to it.

|Scale Icon| Scale (Edit->Transform->Scale)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Activate the Scale tool. This will place a 'gizmo' over the selected
object. Click and drag the center box to scale uniformly on all axis.
Click and drag on one of the colored boxes to scale only in the
direction of the selected box. TIP: scaling always happens in local
space - you cannot rotate an object, then scale in worldspace to produce
a skew.

|World Coordinates Icon| World Coordinates (Edit->Transform->World Coords)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Align the selected tool's gizmo with the world coordinate system. Thus,
the X handle of the move gizmo will point toward the absolute X of the
world, and Z will always be 'up', toward the sky. TIP: coordinate space
selections currently do not work properly for objects that are children
of other objects.

|Local Coordinates Icon| Local Coordinates (Edit->Transform->Local Coords)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Align the selected tool's gizmo with the selected object. Use this if
you want to move an object toward its own 'front', even if that 'front'
does not point strait along a world axis line because the object has
been rotated. TIP: coordinate space selections currently do not work
properly for objects that are children of other objects.

|Select by Clicking Icon| Select By Clicking (Edit->Select->Pick)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

When this mode is activated, clicking on an object will select it for
editing. The object selection is used by all tools and windows to
display properties. This button will light up blue when in 'Select'
mode. TIP: if you find that you are clicking and not selecting the
object you wish, check the status bar at the bottom of the screen. If
you see 'Pick: None' in the 4th box, you are not in select mode. TODO:
Add support for selecting multiple objects.

|Select None Icon| Select None (Edit->Select->Select None)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Unselect the selected object, and exit select mode. Note that clicking
the button will change the select mode to none, and you will have to
click the 'Select By Clicking' button to enter selection mode again.

|Copy Icon| Copy (Edit->Copy)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Copy the selected node to be pasted later. You must have a node selected
for this operation. When copying, the entire hierarchy of the selected
object will be copied as well. If the bounding box that marks the
selection is red, you have selected a node that controls a part of a
model that was loaded by and asset file (most likely from the 3DR).
These objects cannot be copied.

|Paste Icon| Paste (Edit->Paste)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Paste the copied node into the scene. This will make a new node with all
the properties of the copied node. You will be assigned as the new nodes
owner. This new node will be placed at the center of your view, at z=0.
Note that when looking at the world at very shallow angles, this may
place the object farther away then you expect.

|Duplicate Icon| Duplicate (Edit->Duplicate)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

A shortcut for copy, then paste. The only notable difference is that the
new node will be placed exactly on top of the original.

|Save Icon| Save Copy (Edit->Save Copy)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This will allow you to save a copy of the node to your inventory. From
the inventory, you will be able to recreate a new instance of this node
at any point. When you select this option, the inventory panel will be
shown, and the new node selected. The new object in the inventory will
have a randomly generated name. TIP: rename this object right away to
keep things organized.

|Link Icon| Link (Hierarchy->Link)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This tool allows you to make one object a child of another. You must be
the owner of both objects to complete this operation. You must first
select an object before clicking this tool. When activated, the cursor
will change to a cross hair, and allow you to pick a second object. When
you choose the second object, the selected object will be added as a
child of the object you pick. TODO: When linking an object, we need to
calculate the new transforms such that the object appears to the user in
the same world space location.

|Unlink Icon| Unlink (Hierarchy->Unlink)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This button will unlink the selected object from its parent. The
selected object must be a child of another object in the scene. TODO:
When unlinking an object, we need to calculate the new transforms such
that the object appears to the user in the same world space location.

|Select Parent Icon| Select Parent (Hierarchy->Select Parent)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

When a node is selected, clicking this button will select the node's
parent, if the node has one.

|Orbit Camera Icon| Orbit Camera (Camera->Orbit)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Activate 'Camera Orbit' mode. See the Camera Modes section for details
on how the camera controls work.

|First Person Camera Icon| First Person Camera (Camera->First Person)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Activate 'First Person' mode. See the Camera Modes section for details
on how the camera controls work.

|Navigate Camera Icon| Navigate Camera (Camera-> Navigate)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Activate 'Navigate' mode. See the Camera Modes section for details on
how the camera controls work.

|Free Camera Icon| Free Camera (Camera-> Free)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Activate 'Free Camera' mode. See the Camera Modes section for details on
how the camera controls work.

|Focus Camera Icon| Focus (Camera->Focus Selected)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Move the camera such that it frames the selected object in the view.
This will reset the camera mode to 'Orbit'. TODO: make sure the Orbit
icon lights as selected when this is clicked.

|Create Sphere Icon| Create Sphere (Create-Primitives->Sphere)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Create a new sphere object at the center of the view. See the Primitive
Objects sections for information on the object settings.

|Create Box Icon| Create Box (Create-Primitives->Box)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Create a new box object at the center of the view. See the Primitive
Objects sections for information on the object settings.

|Create Cylinder Icon| Create Cylinder (Create-Primitives->Cylinder)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Create a new Cylinder object at the center of the view. See the
Primitive Objects sections for information on the object settings.

|Create Cone Icon| Create Cone (Create-Primitives->Cone)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Create a new cone object at the center of the view. See the Primitive
Objects sections for information on the object settings.

|Create Pyramid Icon| Create Pyramid (Create-Primitives-> Pyramid)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Create a new pyramid object at the center of the view. See the Primitive
Objects sections for information on the object settings.

|Create Plan Icon| Create Plane (Create-Primitives-> Plane)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Create a new plane object at the center of the view. See the Primitive
Objects sections for information on the object settings.

|Users Icon| Users Window (Windows->Users)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Show the Users window. See Tool Windows for more information.

|Chat Icon| Chat Window (Windows->Chat)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Show the Chat window. See Tool Windows for more information.

|Material Editor Icon| Material Editor Window (Windows->Material Editor)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Show the Material Editor window. You should have an object selected when
opening this window. See Tool Windows for more information.

|Script Editor Icon| Script Editor Window (Windows->Script Editor)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Show the Script Editor window. You should have an object selected when
opening this window. See Tool Windows for more information.

|Object Properties Icon| Object Properties Window (Windows-> Object Properties)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Show the Object Properties window. You should have an object selected
when opening this window. See Tool Windows for more information.

|Asset Library Icon| Asset Library Window (Windows-> Models)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Show the Asset Library window. See Tool Windows for more information.

|Inventory Icon| Inventory Window (Windows-> Inventory)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Show the Inventory window. See Tool Windows for more information.

.. |Login Icon| image:: http://vwf.adlnet.gov/adl/sandbox/images/icons/logout.png
.. |Logout Icon| image:: http://vwf.adlnet.gov/adl/sandbox/images/icons/login.png
.. |Move Icon| image:: http://vwf.adlnet.gov/adl/sandbox/images/icons/move.png
.. |Rotate Icon| image:: http://vwf.adlnet.gov/adl/sandbox/images/icons/rotate.png
.. |Scale Icon| image:: http://vwf.adlnet.gov/adl/sandbox/images/icons/scale.png
.. |World Coordinates Icon| image:: http://vwf.adlnet.gov/adl/sandbox/images/icons/worldspace.png
.. |Local Coordinates Icon| image:: http://vwf.adlnet.gov/adl/sandbox/images/icons/localspace.png
.. |Select by Clicking Icon| image:: http://vwf.adlnet.gov/adl/sandbox/images/icons/pick.png
.. |Select None Icon| image:: http://vwf.adlnet.gov/adl/sandbox/images/icons/selectnone.png
.. |Copy Icon| image:: http://vwf.adlnet.gov/adl/sandbox/images/icons/copy.png
.. |Paste Icon| image:: http://vwf.adlnet.gov/adl/sandbox/images/icons/paste.png
.. |Duplicate Icon| image:: http://vwf.adlnet.gov/adl/sandbox/images/icons/duplicate.png
.. |Save Icon| image:: http://vwf.adlnet.gov/adl/sandbox/images/icons/save.png
.. |Link Icon| image:: http://vwf.adlnet.gov/adl/sandbox/images/icons/link.png
.. |Unlink Icon| image:: http://vwf.adlnet.gov/adl/sandbox/images/icons/unlink.png
.. |Select Parent Icon| image:: http://vwf.adlnet.gov/adl/sandbox/images/icons/up.png
.. |Orbit Camera Icon| image:: http://vwf.adlnet.gov/adl/sandbox/images/icons/camera.png
.. |First Person Camera Icon| image:: http://vwf.adlnet.gov/adl/sandbox/images/icons/firstperson.png
.. |Navigate Camera Icon| image:: http://vwf.adlnet.gov/adl/sandbox/images/icons/navigate.png
.. |Free Camera Icon| image:: http://vwf.adlnet.gov/adl/sandbox/images/icons/free.png
.. |Focus Camera Icon| image:: http://vwf.adlnet.gov/adl/sandbox/images/icons/target.png
.. |Create Sphere Icon| image:: http://vwf.adlnet.gov/adl/sandbox/images/icons/sphere.png
.. |Create Box Icon| image:: http://vwf.adlnet.gov/adl/sandbox/images/icons/cube.png
.. |Create Cylinder Icon| image:: http://vwf.adlnet.gov/adl/sandbox/images/icons/cylinder.png
.. |Create Cone Icon| image:: http://vwf.adlnet.gov/adl/sandbox/images/icons/cone.png
.. |Create Pyramid Icon| image:: http://vwf.adlnet.gov/adl/sandbox/images/icons/pyramid.png
.. |Create Plan Icon| image:: http://vwf.adlnet.gov/adl/sandbox/images/icons/plane.png
.. |Users Icon| image:: http://vwf.adlnet.gov/adl/sandbox/images/icons/users.png
.. |Chat Icon| image:: http://vwf.adlnet.gov/adl/sandbox/images/icons/chat.png
.. |Material Editor Icon| image:: http://vwf.adlnet.gov/adl/sandbox/images/icons/material.png
.. |Script Editor Icon| image:: http://vwf.adlnet.gov/adl/sandbox/images/icons/script.png
.. |Object Properties Icon| image:: http://vwf.adlnet.gov/adl/sandbox/images/icons/properties.png
.. |Asset Library Icon| image:: http://vwf.adlnet.gov/adl/sandbox/images/icons/models.png
.. |Inventory Icon| image:: http://vwf.adlnet.gov/adl/sandbox/images/icons/inventory.png
