The Sandbox supports 2 main modes of operation - play and edit.

Editing
~~~~~~~

When you're in edit mode, you see all the usual GUI tools in the
interface, and can interact with the world. This is the default mode for
a world - when you create one, you'll be in this state.

Edit mode has a few special features - you can pause and play the entire
simulation with the buttons in the bottom left of the screen. Clicking
Play will cause the simulation to execute, and stop will cause it to
reset. When the world is 'playing', the GUI is disabled. This gives you
a quick way to test behaviors or interactivity.

While in Edit mode, the server will keep backups of the world every few
minutes.

Playing
~~~~~~~

When you are happy with the world (or game, or simulation....), you can
'publish' it. Publishing the world allows you some special options, like
whether or not the system should generate avatars for each user, what
camera the users should be assigned, and whether or not the users can
see the editing tools.

Published worlds do not get saved - when the last user logs out, the
world resets to the state it was in when it was published.

Published worlds can be set to 'Single Player'. This means that when a
user logs in, they are actually in a private copy of the simulation.
This copy is not connected to the server - it neither saves its state,
nor sends messages to the server about interactions. In some cases, this
can result in significantly better performance for the end user, because
server round trim latency is eliminated.

Testing
~~~~~~~

While in Edit mode, you should have an option on the file menu called
"Test World" and one called "World Settings". In "World Settings", you
have the same options as are available on the Publish page. Fill these
out as you would when publishing the world. You can use the "Test World"
command to get a real time view of exactly how the published world will
behave. This feature will create a clone of your world on the server,
set the publish settings, and launch it in a child window. The main
window will be disabled. When the child window closes, the temporary
world is delete off the server, and the main window is re-enabled.

Usually, the play/pause feature of the editor should be enough to test,
but you can use the above workflow to test aspects of your scene that
play/pause cannot simulate - for instance, you might want to test code
that responds to a users log in.

Workflow
~~~~~~~~

So, you'll go through these steps to create and share a world.

1. Create your world
2. Edit the world
3. Test the world
4. Publish the world
