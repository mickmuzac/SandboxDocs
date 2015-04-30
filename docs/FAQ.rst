How do I import a 3D object?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

There are several ways. You can go to Edit->Load Mesh By URL to enter
just the raw URL of a Collada file, but we prefer that you upload the 3D
object to the repository.

How do I upload a 3D model?
~~~~~~~~~~~~~~~~~~~~~~~~~~~

It's better to upload a 3D model file than to load it directly by URL.
This allows our asset server to condition the model so it had the best
chance of loading properly. To upload a model, first go to Edit->Upload
a 3D Model on the menubar. This will open the upload dialog. Choose a
zip file that contains a 3D model in Collada, FBX, 3DS, OBJ or SKP, and
all the associate textures. Choose a title and hit upload. Note: You'll
have to be logged in for this to work. If the upload and conversion is
successful, you'll see the model appear in the world, and a new object
appear in your inventory.

Why don't uploaded models have animation?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Our asset server currently does not support animated meshes. If you need
to import a mesh and maintain it's animation cycles, use the "Load Mesh
By URL" feature.

Can you explain the general workflow?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

I'm glad you asked. We're in the process of moving from a 'persistent
editable' environment to a system that makes it easier for you to
develop experiences that have well defined beginnings and ends.

The basic idea is this: You log in and create a world - either a blank
one or from a template. After editing the environment by loading models,
sounds, textures and writing code, you 'Publish' the world. Once the
world is published, it will not longer be automatically saved. Each time
the world is loaded, it will start anew from the state it was in when
published. The publish setting also allow you to choose whether or not
the users can use the editing tools, whether or not the system should
create avatars, what camera to use, and a few other options.

My world seems sort of stuck. How do it make it go?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

You're probably in edit mode. When you see the editor tools, and they
appear the normal dark color, the system is in edit mode. Scripts will
not execute, physics will not update and animations will pause. You
should see a play/pause/stop button in the bottom corner. Press 'Play'
and the GUI should turn red. When the world is playing, you won't be
able to use the edit tools, but scripts, physics, and animations will
run. Hit Stop, and the world will reset to the point where it was last
in edit mode.

I've lost the world, and I don't see anything in the view but the skybox. What's going on?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This can happen sometimes when code moved a camera to an undefined
location, or when you click the 'Focus' button while on an object that
has no bounding volume like a light or a behavior. You can fix this by
selecting a 3D object in the scene, and hitting the camera focus button.
Since you can't see anything to click on, use either the Hierarchy panel
on the right, or go to Edit->Select By Name on the menu.

How do I upload a texture?
~~~~~~~~~~~~~~~~~~~~~~~~~~

We currently don't support texture upload, however, you can reference a
texture by URL. Click the big thumbnail in the texture layer on the
material editor. When the map browser appears, look for the plus icon.
Hit the plus and enter the URL of an image file. Note that the server
hosting the file must support CORS.

When I choose a texture, the model disappears! What's the deal?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Sometimes, it's possible to load a model that does not contain any data
about how the texture should map to the polygons. In techy speak, we'd
say it is missing its UV channel. When this happens, the graphics engine
doesn't know what to do, and the mesh disappears. Remove the texture and
it should come back. If you really want to add a texture, you'll need to
fix the model and reload it.

Can I change the time of day?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Yes. The Sandbox comes with a simple model for sunlight, and includes
direction settings. Look for the Sun Direction and Sun Color properties
in the Properties panel after you select the scene.

Can I add a custom skybox?
~~~~~~~~~~~~~~~~~~~~~~~~~~

Not currently, but this is on our TODO list, and should be fairly easy.

What are all the little floating icons. What's that clipboard?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

When you're in edit mode, the Sandbox creates icons that you can click
to select objects that have no visible geometry. These icons will
disappear at about 20 meters from the camera. Click the icons to select
the object they represent. The clipboard represents the scene root.

How is the scene organized? I seem to have some confusion about which objects are part of each other.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Like most 3D environments, the Sandbox organizes the world into a tree
structure. Every object is a child of some other object, except for the
scene. The scene is the root of the tree, and all objects are
descendants of it. When you move an object, it's children move with it.

What are properties? I hear a lot about them.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Properties are values that define what an object is and what it does.
Some properties are things the engine knows about, like 'Visible' or
'Mass'. Many properties are only understood by the engine when they
belong to certain types of objects. For instance, 'Length' means
something when it is part of a box primitive, but nothing if you tried
to change the Length of a sphere

Can I add custom properties to objects?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Absolutely, this is the basis of building an interactive simulation.
Open the Script Editor while an object is selected, and find the
properties tab. Here, you can see the properties that already belong to
the object, or create new ones.

What happens if I change a property value in the Script Editor?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Well, it really depends. All of the editor tools really just change
these values, so you might end up just changing something you already
understand. In this case, you'll even see the GUI update. The script
editor does not validate the inputs you type, so you could really break
something if the engine expects a number but you type a word. Only
change things if you understand what you're doing!

Can I change properties from scripts?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Of course. If you have a node reference, just access the property by
name like a normal JavaScript object. For instance:
``this.DisplayName - 'This is my name!'`` will change the DisplayName
property of the object that ``this`` refers to.

Why do I see some grayed out names on the left side of the Script Editor?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

These are suggestions for methods or events you might want to create.
The system has a few special case method names and event names that will
be called by the engine when something happens. These are suggested to
you with the grayed out options. Click the name to create that method or
event.

Can I play sounds? I don't see any options in the GUI
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Sure, the system contains an audio driver, but it's only accessible from
the API. Type ``this.audioAPI.`` in the script editor and look through
the available functions.

There seems to be an enormous number of properties and methods on each object. What is all this?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The Sandbox has a large set of properties and methods that belong to all
objects. You're seeing a bunch of under the hood engine internals. We're
working on separating out things you should see and things you should
not really mess with.

How do I look through a camera? I created one, but what does it see?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

You should be able to get a preview by selecting it - then you can use
the move and rotate tools to position it. You can double click it's icon
in the viewport to enter it, or from the top menu choose
Camera->Activate Camera.

When I'm in a camera view that is not the Editor Camera, The mouse motions that usually pan or orbit don't work Why not?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

User defined cameras cant be edited in this way. You can select the
camera object even while looking through it, and use the move tool in
the center of the screen.

What's the difference between 'Set Parent' and 'Select Parent'?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This is somewhat confusing just because the words are so similar. 'Set
Parent' allows you to choose an object that will become the parent of
the selected object. 'Select Parent' just selects the parent of the
selected node. If you keep hitting select parent, you'll eventually get
to the scene root node.

Why don't the numbers in the 'Transform' section of the 'Property Editor' make any sense?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

These values are in local coordinates. This means that they are relative
to the selected object's parent. So, if an object is directly at the
center of its parent, the position values will be [0,0,0] even if it
looks like it is far from the center of the world.

Oh no! I've done something and my world no longer loads! What can I do?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

First, don't panic. The Sandbox keeps frequent backups of your world.
From the main page, just find the 'Restore Backup' option. It's also
possible that something external that your world depends on has changed.
Be very careful if you load a mesh by URL - the file needs to stay
there. If you change the file at that URL, you might break a world that
depended on it. Finally - we break things sometimes. It's possible a
software update broke your world. After checking that it's not one of
the above issues, contact us.

How can I prevent someone from accessing my world?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The Sandbox is not configured to protect your IP. Anyone can make a copy
of your worlds and edit it. If you need to work privately, you'll have
to set up your own server.
