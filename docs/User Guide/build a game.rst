Introduction
------------

This document will walk you through the entire process of building a
simple game in the VWS environment. It will cover the entire process
from start to finish, including creating an account, setting up the
scene, creating the objects, scripting the game and finally, publishing.
This document assumes that you have some basic knowledge of web browsers
and computers in general, but should not require any special
prerequisites. By the end of this tutorial, you should have a
functioning game you can play, and a good understanding of how to author
content in the VWS application.

Part 1: Getting started
-----------------------

First things first, we’ll need to get step before we can start building.
This section will walk you through the steps necessary to get a user
account and create a world.

1. First, browse to http://vwf.adlnet.gov . You should see a website
   that looks something like the following.

   .. figure:: ./images/building-a-game/testexport.html_Image0.png
      :alt: 

2. Before we can create an application, we’ll need to sign in. I assume
   here that you do not have an account. If you have already signed up
   for an account, go ahead and skip a few steps. Otherwise, You’ll need
   to click the “Sign Up” button.

   .. figure:: ./images/building-a-game/testexport.html_Image1.png
      :alt: 

3. You should now see a screen where you can choose a username and a
   password. Be sure the password is something you can remember! You’re
   username can be anything, so long as it is not currently used by
   another user. I recommend using an email address.

   .. figure:: ./images/building-a-game/testexport.html_Image2.png
      :alt: 

4. Now that you have created a user account, you’ll be automatically
   logged into the website. You’ll know you’re logged in because you’ll
   see your user name in the top right corner.

   .. figure:: ./images/building-a-game/testexport.html_Image3.png
      :alt: 

5. Next, we’ll need to create a new world to work in. To do this, click
   the ‘Create’ button on the home page.

   .. figure:: ./images/building-a-game/testexport.html_Image4.png
      :alt: 

6. You’ll see the following page. This page allows you to create a new
   world based on an existing ‘template’ world. In this case, we’re
   going to just create a blank world. You should see the words “Create
   a world based on an empty world.” When you click on one of the
   template world images, you’ll select this template, and the text
   “Create a world based on …” will change to show the name of the
   selected world. The template we need, the blank world, is the
   default. If you do click on one of the other templates, just scroll
   to the right end of the list, and click the template “an empty
   world”. Give your new world a title and a description.

   .. figure:: ./images/building-a-game/testexport.html_Image5.png
      :alt: 

7. Click the Create button.

   .. figure:: ./images/building-a-game/testexport.html_Image6.png
      :alt: 

8. Great! If everything went according to plan, you should see the new
   world begin to load. Because this world is in editing mode, you’ll
   see a lot of buttons and graphics appear in bars on the top, bottom,
   and sides of your browser. These are the tools that we’ll be using in
   the next section. You’ll also see the default avatar and a white grid
   in the center of the screen. This avatar is you! We won’t be going
   into any details about how the avatar works today, so just ignore it
   for now.

   .. figure:: ./images/building-a-game/testexport.html_Image7.png
      :alt: 

   **Note: **\ The VWS website uses a lot of cutting edge HTML5
   features. If your browser window does not look like the image above,
   check that you are using the most recent version of Chrome, Firefox,
   Safari or Internet Explorer. Many mobile versions of these browsers
   may not be supported.

9. **Congratulations! **\ You’ve made it to the end of part one! Now is
   a good time to get used to moving around in this world. Click and
   hold with the right mouse button, and drag your mouse. Notice how the
   view rotates? This is the primary camera mode we’ll use when
   authoring, so it pays to practice a little bit. You can also roll the
   mouse wheel to zoom in and out, or press and drag with the center
   mouse button (sometimes the wheel itself is the button, can be
   pressed in addition to being rolled) to pan the view. Don’t worry too
   much about the left mouse button. It’s used for selection, which
   you’ll get plenty of practice within the next section.

   **Note: **\ Don’t be afraid to play around. At this point, the worst
   thing that can happen is that you create some junk in the world that
   will mess up our tutorial. You can always create another world to
   start the tutorial again.

Part 2: Setting up the scene
----------------------------

Now that we have a world to work in, we need to create all the objects
that will be part of our game. We’re going to have to create, move,
modify, select, copy and paste a lot of objects for this section. I’m
going to show you the basic tools and how they work, but leave it up to
you to setup all the pieces once you know how. To start, we need to
build some walls to create the game board.

1.  First, rotate your camera so you are looking down at the grid. This
    will help you stay oriented, and makes selecting object and moving
    them around easier. Zoom out a bit too.

    .. figure:: ./images/building-a-game/testexport.html_Image8.png
       :alt: 

    **Remember: **\ Zoom by rolling the mouse wheel, rotate the camera
    by clicking and dragging with the right mouse button

    **Info: **\ You can move the avatar out of the way by pressing and
    holding the ‘W’ button on the keyboard. You’ll see a slight blue
    outline when the window is active and accepting keyboard commands.

2.  Now, we need to activate a tool that will let us draw the level.
    Find the ‘Tools’ menu on the top menubar. Click the ‘Block Painter’
    menu item.

    .. figure:: ./images/building-a-game/testexport.html_Image9.png
       :alt: 

3.  When the Block Painter tool opens, you’ll see it slide out on the
    right, in an area we call the “side panel”. The block painter is a
    quick and easy way to create a lot of geometry quickly. There are
    other ways you could lay out the level, but this is fun! Let’s pick
    a different texture for our walls by clicking right on the “Pick
    Texture” button.

    .. figure:: ./images/building-a-game/testexport.html_Image10.png
       :alt: 

4.  The Map Browser will appear. This is the tool that is used in many
    parts of the software whenever you need to choose a texture map.
    Clicking on the folder icons will show the textures inside that
    folder, and clicking on an image will select that file as the
    texture. You can also use the plus icon to enter a texture via URL.
    For now, let’s keep it simple and choose the brick texture. Just
    click right on the small image of bricks.

    .. figure:: ./images/building-a-game/testexport.html_Image11.png
       :alt: 

5.  The Painter tool will now show the selected texture, and the Map
    Browser window will disappear. We now need to activate the tool, and
    set it to ‘Build’ mode. Click the “Active” button inside the tool’s
    panel, then click ‘Build’. The “Active” button should remain lit up.

    .. figure:: ./images/building-a-game/testexport.html_Image12.png
       :alt: 

6.  When you hold your mouse within the 3D window, over the grid, you’ll
    see a faint transparent brick box. The tool is previewing where the
    next box will be placed. Click and hold with the left mouse button
    to make a stroke. Boxes will line up along the path of your stroke!

    .. figure:: ./images/building-a-game/testexport.html_Image13.png
       :alt: 

    **Info: **\ You can also delete blocks with the painter tool. Just
    click the ‘delete’ button to put the tool into delete mode. Now,
    when you click and drag, boxes will be destroyed instead of created.
    Click ‘Build’ to start building again.

    **Note: **\ The Sandbox application currently does not support an
    undo feature. You have been warned!

7.  Build a maze! Be sure that each path within the maze is just one
    block thick. This won’t be all that important, but it will make the
    game work better. Take some time to build something simple like the
    image below.

    .. figure:: ./images/building-a-game/testexport.html_Image14.png
       :alt: 

8.  Great! We now have our game board. Now that we’re done with the
    painter tool, we need to deactivate it so that we can go about the
    rest of our project. Click the ‘Active’ button in the tool again, so
    that it is no longer lit up. Now, click the ‘X’ button in the tool’s
    title bar to close the tool. It’s very important that you deactivate
    the tool before you close it – otherwise it can be active, just
    hidden!

9.  Now that we have our game board, we need to create our first actor!
    This actor will become the Player later, when we add scripts. We’ll
    use a sphere for the player. Click the Sphere icon on the main
    toolbar.

    .. figure:: ./images/building-a-game/testexport.html_Image15.png
       :alt: 

10. You should see a sphere object appear right in the center of the
    viewport. By default, that sphere is checkered. We’ll change this in
    a moment. First, we need to select the sphere so we can edit it. To
    do so, we first need to put the software into selection mode. Click
    the ‘Select by clicking’ button on the toolbar. You’ll know select
    mode is active when the button turns blue.

    .. figure:: ./images/building-a-game/testexport.html_Image16.png
       :alt: 

    **Info: **\ You can also enter selection mode with the hotkey ‘Q’ on
    the keyboard

11. Now, click on the sphere in the main 3D window once with the left
    mouse button. You should see a white outline appear around the
    sphere, as well as a brightly colored axis graphic. It should look
    something like this:

    .. figure:: ./images/building-a-game/testexport.html_Image17.png
       :alt: 

    **Remember: **\ IT’s very important that the Painter Tool is
    deactivated. If you are still seeing a faint box following under
    your cursor, the tools it active but hidden. Open is as we did in
    step 2, deactivate it by clicking the Active button. Verify that the
    button is not lit, then close the tool.

12. Because we don’t know exactly where the sphere was created (it’s
    created at the center of your view) let’s go ahead and reset its
    position, rotation, and scale. Find the ‘Edit’ menu on the menu bar,
    then open the sub menu ‘Transforms’ and finally, choose ‘Reset
    Transforms’. This will zero out the position, rotation and scale of
    the sphere.

    .. figure:: ./images/building-a-game/testexport.html_Image18.png
       :alt: 

13. Now, we need to go ahead and name the sphere so that we can find it
    later. All objects have a set of properties you can edit in a window
    called the Property Editor. We need to open the property editor, and
    change the Display Name property of the sphere to something nice,
    like ‘Player’. First, while the sphere is still selected, open the
    Property Editor by finding the ‘Properties’ tab on the right side of
    the screen.

    .. figure:: ./images/building-a-game/testexport.html_Image19.png
       :alt: 

14. Click it to open the **Property Editor**. It will appear in the side
    panel just like the painter tool did. Find the **Display Name
    **\ property, which is the first textbox on the page, and change the
    value to ‘\ **Player’ **\ by clicking in the box and typing.

    .. figure:: ./images/building-a-game/testexport.html_Image20.png
       :alt: 

    **Info: **\ The active text field, where the text from the keyboard
    is input, will be outlined in blue.

15. We also need to make the sphere smaller. The properties that you can
    edit are divided into categories. The parameters for the generation
    of primitive objects like spheres and boxes will be under the
    ‘Primitive’ category. Click the ‘\ **Primitive: Sphere1′ **\ then
    find the **Radius **\ setting. Either type in the box, or use the
    slider to change the radius to **.5**

    **Note: **\ Don’t be confused that the tab says ‘Primitive: Sphere1′
    even though we just changed the object’s name to Player. The UI will
    update the next time it’s loaded.

    .. figure:: ./images/building-a-game/testexport.html_Image21.png
       :alt: 

16. Now, since the sphere was centered at (0, 0, 0). So that the object
    is not intersecting the ground, let’s move it up. We’ll do so
    precisely by typing in the Z value. Still in the Property Editor,
    Open the **Transform Tab**, and find the 3rD text box from the left
    under the Translation label. This value is the Z coordinate of the
    spheres position. Enter **“.6″. **\ You’ll see the sphere move
    slightly.

    .. figure:: ./images/building-a-game/testexport.html_Image22.png
       :alt: 

17. Next, let’s go ahead and make the sphere yellow, just for kicks.
    Find the **Material **\ tab. Its right below the Properties tab on
    the right of the screen. When you click this tab, the **Material
    **\ Editor will load into the side panel.

    .. figure:: ./images/building-a-game/testexport.html_Image23.png
       :alt: 

18. So, we want to do two things. First, click the little white square
    next to **“Diffuse Color.” **\ This will let you change the color of
    the object. Click and drag in the color preview to set the diffuse
    color to yellow.

    .. figure:: ./images/building-a-game/testexport.html_Image24.png
       :alt: 

19. Let’s also remove the default texture layer. The material editor
    allows you to link several different images to different properties
    of the surface, like a color map or a bump map. The default material
    has a checker texture for the diffuse map. Each texture gets a small
    tab at the bottom of the Material Editor. Click the “\ **Texture
    Layer 0**\ ” tab to open the settings for the layer, then find the
    ‘\ **Delete Layer’ **\ button. The sphere should now be a solid
    yellow. I’ve deselected it so you can see it better in the image
    below, but you should still see the selection outline and the
    brightly colored axis graphic.

    .. figure:: ./images/building-a-game/testexport.html_Image25.png
       :alt: 

20. Now, I’ve got a challenge for you. We need to create a cube with a
    **width length and height **\ of .25. I’d also like you to color it
    blue, and remove its default checker texture as well. Finally, I
    want you to position it so that it’s in the center of a path, with
    its Z coordinate at .6. Look over the instructions above, and I’m
    sure you can figure it out. Also, go ahead and name it
    ‘\ **Food1′**. When you’re done, you should have something that
    looks like this:

    .. figure:: ./images/building-a-game/testexport.html_Image26.png
       :alt: 

21. The next step is vital. We need to mark this object so that we can
    identify it from within the code later. Because there are going to
    be a lot of food objects, remembering all their names is going to be
    hard. Instead, we’ll assign a custom property to the object called
    ‘\ **gametype’**. We’ll make the value of this property
    ‘\ **food’**. While the first food object is selected, click the
    ‘\ **Scripts’ **\ tab on the right of the screen to open the Script
    Editor. When the Script Editor opens, find and click the **Property
    **\ tab.

    .. figure:: ./images/building-a-game/testexport.html_Image27.png
       :alt: 

    **Note: **\ We’ll take much more about the Script Editor in part 3.
    For now, let’s just add the property and not worry about the rest.

22. Now, find the button in the bottom right that says **‘New Property’.
    **\ Click it.

    .. figure:: ./images/building-a-game/testexport.html_Image28.png
       :alt: 

23. When the prompt opens, type ‘\ **gametype’**. This will be the name
    of the new property. Click **OK**

    .. figure:: ./images/building-a-game/testexport.html_Image29.png
       :alt: 

24. On the next prompt, enter ‘\ **food’**. This will be the value of
    the new property. Click **OK**

    .. figure:: ./images/building-a-game/testexport.html_Image30.png
       :alt: 

25. You can now close the Script Editor. Use the **down arrow **\ on the
    right at the top of the panel.

    .. figure:: ./images/building-a-game/testexport.html_Image31.png
       :alt: 

    **Note: **\ It’s very important that this step is successful. You
    can verify that the property was created by finding it in the list
    of properties on the left of the Properties Tab. If you see a button
    labeled ‘gametype’, we’re good to go.

26. We also need to mark the food object as ‘passable’. This will allow
    the player to move through the food without colliding with it later
    in part 3. In the Properties Editor for the Food object, find and
    select the ‘\ **passable’ **\ checkbox.

    .. figure:: ./images/building-a-game/testexport.html_Image32.png
       :alt: 

27. We now have to copy the Food0 object to each point on the game along
    the paths. While keyboard focus is on the main 3D view, you can hit
    **CTRL+D **\ duplicate the selected object. Duplicate the object,
    the click and drag along the RED or GREEN axis of the brightly
    colored axis graphic. You should see a new box move under the
    cursor.

    .. figure:: ./images/building-a-game/testexport.html_Image33.png
       :alt: 

28. Take some time and fill the game board with food objects as
    necessary. The editor tools have many options to make this faster.
    With some practice, you can do this in just a few minutes.

    .. figure:: ./images/building-a-game/testexport.html_Image34.png
       :alt: 

    **Info: **\ You can select more than one object at a time, and move
    or duplicate whole rows of food! Click and drag with the left mouse
    button to draw a rectangle on the screen. All objects in the
    rectangle will be selected. You can hold CTRL or ALT to add or
    subtract from the selection as well.

    **Remember: **\ You must be in selection mode before you can click
    to select objects.

29. Using the same technique you’ve now mastered, duplicate the player
    object. Change its color to red, move it to the corner of the board,
    and name it Ghost.

    .. figure:: ./images/building-a-game/testexport.html_Image35.png
       :alt: 

30. Now, let’s just remove that black and white grid. The texture of the
    default ground grid can be changed by editing the material of the
    Scene object. To select the scene, use the dropdown menu. Find
    **Edit->Select->Select Scene.**

    .. figure:: ./images/building-a-game/testexport.html_Image36.png
       :alt: 

31. Not much will appear to change, but the material editor will now
    control the texture of the background grid. Use the material editor
    just like before to create a solid white background.

Part 3: Scripting
-----------------

Alright! Now we are cooking with fire. The whole scene is set up, and we
just need to make the game work. To do so, we need to add some behaviors
to the objects. This means we’ll have to write some code. This isn’t a
programming course, and I’m not going to discuss every line of text.
Instead, I’ll give you the code, and you can apply it to the objects.
For anyone familiar with JavaScript, you’ll immediately see hundreds of
way to make this game more interesting, but let’s stick with the basics
for now.

1. First, let’s do the player code. Select the Player object, and open
   up the script editor. Make sure you’re on the Methods tab, and scroll
   down the list on the left until you see the word ‘tick’. It should
   appear grayed out. Click it.

   .. figure:: ./images/building-a-game/testexport.html_Image37.png
      :alt: 

2. The system will ask you if you want to create a new method called
   ‘tick’. Click ok. ‘Tick’ is the method that the engine will call at
   every frame of animation to update your objects.

   .. figure:: ./images/building-a-game/testexport.html_Image38.png
      :alt: 

3. Now, paste the below code in the script window.

::

        function tick(){
            if (this.motionVec)
            {
                var oldpos = this.transformAPI.getPosition();
                this.transformAPI.move(this.motionVec, 'parent');
                var hit = _SceneManager.SphereCast(this.transformAPI.getPosition(), .35,
                {
                    ignore: [_Editor.findviewnode(this.id).children[0].children[0], _Editor.GetMoveGizmo()],
                    filter: function(n)
                    {
                        if (n.passable) returnfalse;
                        returntrue;
                    }
                });
                if (hit & amp; & amp; hit.length)
                {
                    this.transformAPI.setPosition(oldpos);
                }
            }
        }

4.  Click ‘Save Method’ to save this code on the object as the Tick
    method.

    .. figure:: ./images/building-a-game/testexport.html_Image39.png
       :alt: 

5.  Now, move over to the ‘Events’ tab, and click the ‘\ **keyDown’
    **\ suggestion on the left. This process is very similar to the
    process to create the ‘Tick’ method. Enter the code below into the
    ‘\ **KeyDown’ **\ event, and save it.

    ::

        function keyDown(eventData, nodeData){
        if (eventData.keysDown.rightarrow)
        {
            this.motionVec = [0, -.5, 0];
            this.movestate = 'up';
        }
        if (eventData.keysDown.leftarrow)
        {
            this.motionVec = [0, .5, 0];
            this.movestate = 'down';
        }
        if (eventData.keysDown.uparrow)
        {
            this.motionVec = [.5, 0, 0];
            this.movestate = 'left';
        }
        if (eventData.keysDown.downarrow)
        {
            this.motionVec = [-.5, 0, 0];
            this.movestate = 'right';
        }
        }

6.  Finally, insert and save the following code in the ‘\ **keyUp’
    **\ event.

    ::

        function keyUp(eventData, nodeData){
        if (eventData.keysUp.rightarrow & amp; & amp; this.movestate == 'up')
        {
            this.motionVec = null;
        }
        if (eventData.keysUp.leftarrow & amp; & amp; this.movestate == 'down')
        {
            this.motionVec = null;
        }
        if (eventData.keysUp.uparrow & amp; & amp; this.movestate == 'left')
        {
            this.motionVec = null;
        }
        if (eventData.keysUp.downarrow & amp; & amp; this.movestate == 'right')
        {
            this.motionVec = null;
        }
        }

7.  That’s it for the player. Deselect the player object, then click in
    the main 3D window. Use the arrow keys on the keyboard. You should
    see the player move!

    **Note: **\ The movement directions may appear wrong, as if the keys
    are mapped the wrong way. Don’t worry about this – it depends on the
    camera orientation. In part 4, we’ll be sure to make a camera that
    looks in the right direction, so the keys seem to work properly.

8.  Now, we need to create an object to hold some additional logic. This
    is the object that will check for the intersection of the player and
    to food, and make the food disappear. It will also monitor for when
    the game is complete. Use the skills you have learned above, and
    create a new box. Name it **GameManager**, and add the following
    code as its ‘\ **tick’ **\ method.

    ::

        function tick(){
        if (!this.pacman) this.pacman = this.Scene.children_by_name.Player;
        if (!this.piplist)
        {
            this.piplist = [];
            for (var i = 0; i & lt; this.Scene.children.length; i++)
            {
                if (this.Scene.children[i].gametype == 'food')
                {
                    this.piplist.push(
                    {
                        pip: this.Scene.children[i],
                        pos: this.Scene.children[i].transformAPI.getPosition()
                    });
                    this.Scene.children[i].visible = true;
                }
            }
            console.log(this.piplist);
        }
        var playerpos = this.pacman.transformAPI.getPosition();
        var activecount = this.piplist.length;
        for (var i = 0; i & lt; this.piplist.length; i++)
        {
            var pip = this.piplist[i].pip;
            if (pip.visible == true)
            {
                var pos = this.piplist[i].pos;
                if (Vec3.distanceSquared(playerpos, pos) & lt;.25)
                {
                    pip.visible = false;
                }
            }
            else
            {
                activecount--;
            }
        }
        if (activecount == 0)
        {
            alertify.alert('You win!');
            this.reset();
        }
        }

9.  Now, when you move across a food object, it will disappear. Move
    around and collect all the food!

10. We still need a way to reset the game. Go to the '**Events' **\ tab
    of the script editor, and find the '**New Event' **\ button. Click
    it, and when prompted, type '**reset'**.

    .. figure:: ./images/building-a-game/testexport.html_Image40.png
       :alt: 

11. When prompted for the number of parameters, just leave the value at
    0 and click **OK. **\ Paste the code below into the script window
    for the reset event.

    ::

        function reset(){
        deletethis.piplist;
        this.Scene.children_by_name.Ghost.transformAPI.setPosition(4, -17, .5);
        this.Scene.children_by_name.Player.transformAPI.setPosition(-2, -10, .5);
        }

12. Save the event code with the button labeled 'Save Event'. Now,
    clicking the 'Trigger Event' button will reset the game. Note that
    the exact values used above depend on the exact setup of your level.

    **Remember: **\ You can find the proper values for your level by
    selecting the Ghost or the player, and reading the translation out
    of the property editor.

    .. figure:: ./images/building-a-game/testexport.html_Image41.png
       :alt: 

13. Finally, we just need to add the code to make the Ghost work. Use
    the code below, but notice where I've added a note. This value
    should be the same value you used above - the default position for
    the player. Select the Ghost object, open the script editor, create
    a tick method, and paste in the code below.

    ::

        function tick(){
        if (window.paused) return;
        if (!this.pacman) this.pacman = this.Scene.children_by_name.Player;
        if (!this.pacman) return;
        var random = Math.random() * 2000;
        if (random & gt; 0 & amp; & amp; random & lt; 10)
        {
            this.motionVec = [0, .5, 0];
        }
        if (random & gt; 10 & amp; & amp; random & lt; 20)
        {
            this.motionVec = [0, -.5, 0];
        }
        if (random & gt; 20 & amp; & amp; random & lt; 30)
        {
            this.motionVec = [.5, 0, 0];
        }
        if (random & gt; 30 & amp; & amp; random & lt; 40)
        {
            this.motionVec = [-.5, 0, 0];
        }
        var oldpos = this.transformAPI.getPosition();
        oldpos[0] = Math.floor(oldpos[0] * 2) / 2;
        oldpos[1] = Math.floor(oldpos[1] * 2) / 2;
        oldpos[2] = Math.floor(oldpos[2] * 2) / 2;
        this.transformAPI.setPosition(oldpos);
        if (Vec3.distance(oldpos, this.pacman.transformAPI.getPosition()) & lt; 1.3)
        {
            alertify.log('Got you!');
            this.pacman.transformAPI.setPosition(-2, -10, .6);
        }
        if (this.motionVec)
        {
            this.transformAPI.move(this.motionVec, 'parent');
            var hit = _SceneManager.SphereCast(this.transformAPI.getPosition(), .35,
            {
                ignore: [_Editor.findviewnode(this.id).children[0].children[0], _Editor.GetMoveGizmo()],
                filter: function(n)
                {
                    if (n.passable) returnfalse;
                    returntrue;
                }
            });
            if (hit & amp; & amp; hit.length)
            {
                this.transformAPI.setPosition(oldpos);
                var random = Math.random() * 40;
                if (random & gt; 0 & amp; & amp; random & lt; 10)
                {
                    this.motionVec = [0, .5, 0];
                }
                if (random & gt; 10 & amp; & amp; random & lt; 20)
                {
                    this.motionVec = [0, -.5, 0];
                }
                if (random & gt; 20 & amp; & amp; random & lt; 30)
                {
                    this.motionVec = [.5, 0, 0];
                }
                if (random & gt; 30 & amp; & amp; random & lt; 40)
                {
                    this.motionVec = [-.5, 0, 0];
                }
            }
        }
        }

14. Congratulations! That's it! The game now works, and just needs a bit
    of polish to be completely finished!

Part 4: Finishing touches
-------------------------

Great! At this point, our game basically works. The last thing we need
to do is create a camera and publish the world. This is pretty easy
stuff from here on out.

1.  First, let's create a camera object, so that the user of our game
    does not have to mess with positioning the camera. Use the drop down
    menu, and find **Create->Cameras->Perspective**

    .. figure:: ./images/building-a-game/testexport.html_Image42.png
       :alt: 

2.  When you click this, a camera object will be created at the center
    of your view. You should see a camera icon appear. If you don't,
    zoom closer, and make sure you are in selection mode. The icon
    should look like this:

    .. figure:: ./images/building-a-game/testexport.html_Image43.png
       :alt: 

3.  This icon helps you select and place the camera. Click on the camera
    to select it. You'll see a preview appear in the lower left of the
    main window that shows you what the camera sees. Move the camera so
    that it points down at the game board. You'll also see a helpful
    graphic that shows you in the main view where the camera is
    pointing. Aim for something like this:

    .. figure:: ./images/building-a-game/testexport.html_Image44.png
       :alt: 

4.  Let's enter the camera to see exactly what it sees. Find the
    **Camera->Activate Camera **\ item on the dropdown list.

    .. figure:: ./images/building-a-game/testexport.html_Image45.png
       :alt: 

5.  When you click it, you'll see this prompt. Choose Camera1, and click
    ok.

    .. figure:: ./images/building-a-game/testexport.html_Image46.png
       :alt: 

6.  You are now looking exactly out of the camera. Use the arrow keys to
    move the player. Does it seem to go in the right direction? If not,
    you might need to go back to the Editor Camera, and reposition the
    camera object. If you're happy with the camera's view, then we're
    all done inside the editor, and we can move on to publish our game.

    **Note: **\ You will probably need to rotate your camera - it really
    depends on how your level is laid out. Look for the rotate tool on
    the toolbar. This will switch the axis graphic to a series of rings.
    Click and drag the rings to rotate the selected object.

7.  Finally, before we leave the game, let's set the thumbnail that
    users will see on the main page. While looking out of your camera,
    use the dropdown menu item **File->Set World Thumbnail**. You should
    see a slight flicker in the main window. The exact image you see
    will now be the thumbnail for this world on the world's page.

    .. figure:: ./images/building-a-game/testexport.html_Image47.png
       :alt: 

8.  Since we're done editing the game, let's leave this world. Use the
    Log out button in the upper left of the screen. Your game will be
    saved automatically.

    .. figure:: ./images/building-a-game/testexport.html_Image48.png
       :alt: 

9.  Now, we need to find your world so we can publish it. Go to the
    Worlds page. Use the search box to search for your world. Since I
    named the world Tutorial Demo, I'll search 'Tut'

    .. figure:: ./images/building-a-game/testexport.html_Image49.png
       :alt: 

10. When you find your world, click the title or the thumbnail to get to
    the worlds landing page. If you are logged in, you should see an
    option to publish the world. Click the **Publish **\ button.

    .. figure:: ./images/building-a-game/testexport.html_Image50.png
       :alt: 

    **Note: **\ You can change the publish settings in the future. If
    you need to keep editing, come back to the publish page, uncheck the
    publish button, then click publish. The world is now editable again.

11. Now, we just have to set a few settings. First, check the '**Publish
    World' **\ checkbox. Since this is a single player game, check the
    '**Single Player' **\ checkbox as well. Be sure that "**Create and
    Avatar for each user**\ ", "**Allow Editor Tools**\ ", and
    "\*\*\*\*Use Default Camera\*\*\*\*" are unchecked. In the box that
    appears under "\*\*\*\*Use Default Camera\*\*\*\*" choose the name
    of your camera. You should have an option called '**Camera1'**.

    .. figure:: ./images/building-a-game/testexport.html_Image51.png
       :alt: 

12. Click the publish button! You're done! You now have a completely
    working game published on the VWS website. To play the game, just
    click on the world's title from the World's page to load it.

Conclusion
----------

You can share this game with others by copying and emailing the direct
link or your friends can search for it on the worlds page. By the end of
this tutorial, you should have a firm foundation for building more
complex games in the future. Hopefully, you'll also get comfortable with
the user interface of the VWS software, and start thinking of other
things to create! Here are a few challenges that build on this lesson.
Make 3 Ghosts. Make a bigger level. Make the food come back after a
certain time. If you're feeling really ambitious, make the Ghost behave
with more intelligence. There is literally an infinite amount of ideas
for expanding this simple tutorial. Check out the appendix below for
more info on how the code works, if you're interested in making a more
complex game. You can play the finished (with a few improvements) game
here: http://vwf.adlnet.gov/472/adl/sandbox/yU4EixCOyfp6RQaW/

Appendix 1: Code explanation
----------------------------

It's not absolutely necessary for you to understand what the code is
doing in order to make the game work. However, if you do know a bit of
JavaScript, you might want to expand on this tutorial to build a more
complex game. In that case, I'm providing here some explanation for the
code you see above. I'll break it down by each object's methods and
events, and each major portion of each of those scripts.

The code for the **tick **\ method on the player object.

::

    function tick(){
        if (this.motionVec)
        {
            var oldpos = this.transformAPI.getPosition();
            this.transformAPI.move(this.motionVec, 'parent');
            var hit = _SceneManager.SphereCast(this.transformAPI.getPosition(), .35,
            {
                ignore: [_Editor.findviewnode(this.id).children[0].children[0], _Editor.GetMoveGizmo()],
                filter: function(n)
                {
                    if (n.passable) returnfalse;
                    returntrue;
                }
            });
            if (hit & amp; & amp; hit.length)
            {
                this.transformAPI.setPosition(oldpos);
            }
        }
    }

    function tick()
    {...
    }

Below, we are just declaring the function. Its name, 'tick', is a
special case name within the VWS system. Tick functions on objects are
called 20 times a second. This is where you can change values over time
to create motion or other animations.

::

    ...if(this.motionVec)
        {
            var oldpos = this.transformAPI.getPosition();
            this.transformAPI.move(this.motionVec, 'parent');......

If **this** object (the \*\*\*\*Player\*\*\*\*), has a
\*\*\*\*\*\*motionVec \*\*\*\*\*\*variable, then get and store the
current object position in a variable called **oldpos**. Then move the
object (\*\*\*\*Player\*\*\*\*) by the motion vector. So, if the
\*\*\*\*Player\*\*\*\* is at [1,0,0], and \*\*\*\*\*\*motionVec
\*\*\*\*\*\*is [1,0,0], make the new position of the player [2,0,0]. You
can see how, by calling **this** at every tick, the value of the X
coordinate of the player's position increases over time. This is the
basic mechanism for moving the player. The **KeyDown **\ and **KeyUp
**\ events control what the value of **this**.\*\*\*\*\*\*motionVec
\*\*\*\*\*\*is.

::

        ...var hit = _SceneManager.SphereCast(this.transformAPI.getPosition(), .35,
        {
            ignore: [_Editor.findviewnode(this.id).children[0].children[0], _Editor.GetMoveGizmo()],
            filter: function(n)
            {
                if (n.passable) returnfalse;
                returntrue;
            }
        });...

This is a much more interesting bit of code. It's what prevents the
character from intersecting the walls.
\*\*\_\ **SceneManager.**\ SphereCast \*\*\*\*\*\*is a function that
allows you to query the geometry of the world, to decide if any of the
objects in the world intersect a sphere. The first parameter is the
center of the sphere you would like to use to check for intersections.
The second parameter, in this case .\ **35**, is the radius of the
sphere. Notice how we are basically saying "Now that we've moved the
player, does a sphere at his new position with a radius of .\ **35**
interesect any of the world geometry?".
\*\*\_\ **SceneManager.**\ SphereCast \*\*\*\*\*\*also takes an options
object as the final parameter. This object here contains a list of
graphics objects to ignore - namely, the sphere itself, and the Axis
control you've been using to move objects around. This is sort of a
leaky abstraction - from game code, your objects should have no knoledge
of the Axis "gizmo" that you use to move objects. We'll fix this in
time. Also, eventaully you'll be able to ignore objects by the names you
give them, rather than the ugly \*\*\_Editor.findviewnode(this.id)....
**Because the **\ SphereCast **function operates over the graphic
objects, it currently expects you to provide the actaul 3D sphere object
from the graphics engine. **\ \_Editor.findviewnode(this.id) \*\*is how
you access this (for now).

::

        if (hit & amp; & amp; hit.length)
        {
            this.transformAPI.setPosition(oldpos);
        }

This last bit is much easier. It just says "Well, if we did hit
something, put the **Player **\ back where he was!" That's all there is
to preventing intersections for this simple game.

The code for **keyDown**

::

        function keyDown(eventData, nodeData)
        {
            if (eventData.keysDown.rightarrow)
            {
                this.motionVec = [0, -.5, 0];
                this.movestate = 'up';
            }
            if (eventData.keysDown.leftarrow)
            {
                this.motionVec = [0, .5, 0];
                this.movestate = 'down';
            }
            if (eventData.keysDown.uparrow)
            {
                this.motionVec = [.5, 0, 0];
                this.movestate = 'left';
            }
            if (eventData.keysDown.downarrow)
            {
                this.motionVec = [-.5, 0, 0];
                this.movestate = 'right';
            }
        }

This one is much simpler, and I won't spend too much time on it. The
engine notifies your objects about user input events by calling the
Event code you inserted in the Script Editor panel. Because we had the
**Player **\ selected when we created the code above, '**this' **\ means
the player. So, think about the code above in the **tick **\ section.
You can see how the value of the player motion depends on the
**motionVec**, and the value of **motionVec** is controlled by the
**keyDown **\ events. We also track **this.movestate **\ just to make it
easier to figure out what key is currently pressed. This information is
also contained in the **motionVec** variable, but I've done it this way
just for readability. I won't go into any detail on the keyUp code. It
should be self explanatory.

The Ghost object is a very simple example of AI. It just randomly moves
around the scene, and detects when it gets close to the player. Here is
the total code for the Ghost. It's all located inside the objects tick
method.

::

        if (window.paused) return;
        if (!this.pacman) this.pacman = this.Scene.children_by_name.Player;
        if (!this.pacman) return;...

In this first section, we just try to get a reference to the **player
**\ object. If can't get one for some reason, we just end the code by
calling **return**. Notice how we save the reference to the **player
**\ in the variable **this.pacman**? Looking up the object by its name
is a somewhat expensive operation. It makes much more sense to find it
once and hold onto it in a variable, then to look it up each time.

::

        var random = Math.random() * 2000;
        if (random & gt; 0 & amp; & amp; random & lt; 10)
        {
            this.motionVec = [0, .5, 0];
        }
        if (random & gt; 10 & amp; & amp; random & lt; 20)
        {
            this.motionVec = [0, -.5, 0];
        }
        if (random & gt; 20 & amp; & amp; random & lt; 30)
        {
            this.motionVec = [.5, 0, 0];
        }
        if (random & gt; 30 & amp; & amp; random & lt; 40)
        {
            this.motionVec = [-.5, 0, 0];
        }

The Ghost code will work a lot like the player code. Every frame, we
move the object by some value. Because the Ghost does not accept
keyboard inputs, it instead uses a random number. Here, we randomly
choose a direction to move.

::

        var oldpos = this.transformAPI.getPosition();
        oldpos[0] = Math.floor(oldpos[0] * 2) / 2;
        oldpos[1] = Math.floor(oldpos[1] * 2) / 2;
        oldpos[2] = Math.floor(oldpos[2] * 2) / 2;
        this.transformAPI.setPosition(oldpos);

This block of code is just some housekeeping. In this game, it's
important that objects move in strait lines, and that they never end up
with fractional positions, other than half steps between numbers. If the
X position of the Ghost object is 1.34324343 or something like that, it
can get stuck in walls. While the code normally does not allow the
object to get into that sort of a state, this code just ensures it never
happens. We read the position, clamp it to half steps with Math.floor,
and write it back.

::

        if (Vec3.distance(oldpos, this.pacman.transformAPI.getPosition()) & lt; 1.3)
        {
            alertify.log('Got you!');
            this.pacman.transformAPI.setPosition(-2, -10, .6);
        }

This simple block of code is the code that checks if the player got too
near the Ghost. We could have used SphereCast like above, but this is
simpler and works just as well. When the player gets too close, we send
the player back to the start position, and make a little popup that says
'Got you!' Note that the value in the **setPosition **\ will depend on
the layout of your level.

::

        if (this.motionVec)
        {
            this.transformAPI.move(this.motionVec, 'parent');
            var hit = _SceneManager.SphereCast(this.transformAPI.getPosition(), .35,
            {
                ignore: [_Editor.findviewnode(this.id).children[0].children[0], _Editor.GetMoveGizmo()],
                filter: function(n)
                {
                    if (n.passable) returnfalse;
                    returntrue;
                }
            });

This is the code that moves the ghost, just like the player. The ghost
moves the amount of his **motionVec**. We use the exact same collision
detection code, filtering out the ghosts own polygons, and any polygons
of passable objects.

::

            if (hit & amp; & amp; hit.length)
            {
                var random = Math.random() * 40;
                if (random & gt; 0 & amp; & amp; random & lt; 10)
                {
                    this.motionVec = [0, .5, 0];
                }
                if (random & gt; 10 & amp; & amp; random & lt; 20)
                {
                    this.motionVec = [0, -.5, 0];
                }
                if (random & gt; 20 & amp; & amp; random & lt; 30)
                {
                    this.motionVec = [.5, 0, 0];
                }
                if (random & gt; 30 & amp; & amp; random & lt; 40)
                {
                    this.motionVec = [-.5, 0, 0];
                }

This final bit of code is very similar to the first block that randomly
changed the **motionVec**. The difference is that this code is in the
block with if(hit). This means that the code will only execute when the
object hits something. Notice how the random chance of changing the
value is much higher. Since the ghost has hit an object, it must change
direction!

Like the Ghost, the GameManager has only a tick method. However, unlike
the Ghost, the GameManager is not all that interested in its own
location or movement. Instead, we use the GameManager object to hold
some global code that implements the game logic. The gamemanager also
has the necessary code to reset the game implemented in an event call
'reset'

::

                if (!this.pacman) this.pacman = this.Scene.children_by_name.Player;

First, we just find and cache a reference to the player object. It's
more efficient to cache this value then to find it at every tick.

::

                if (!this.piplist)
                {
                    this.piplist = [];
                    for (var i = 0; i & lt; this.Scene.children.length; i++)
                    {
                        if (this.Scene.children[i].gametype == 'food')
                        {
                            this.piplist.push(
                            {
                                pip: this.Scene.children[i],
                                pos: this.Scene.children[i].transformAPI.getPosition()
                            });
                            this.Scene.children[i].visible = true;
                        }
                    }
                }

This block of code is part of the setup of the game. Notice how it's
surrounded by "**if(!this.piplist)". **\ So, if the object is not
initialized with that value, we go ahead and set that value up. The
**this.piplist **\ variable is an array that holds references to each
food item in the scene, and the position of that object. We iterate over
all the objects in the scene with "**for (var i = 0; i <
this.Scene.children.length; i++)". **\ Notice how we next check each
object to see if its '**gametype' **\ property is equal to '**food'**.
You'll remember where we set this up in part 2. When you copied all the
copies of the food object, this property copied as well. That's how we
can check to see if each object is a food object, or something else like
a wall. You'll also notice that this block of code caches the positions
of each food inside of **this.piplist[i].pos. **\ Caching these values
is efficient, because the objects never move! This block of code also
sets each food object back to visible.

::

                var playerpos = this.pacman.transformAPI.getPosition();
                var activecount = this.piplist.length;

Here, we simply get the current position of the player, and the total
number of food objects.

::

                for (var i = 0; i & lt; this.piplist.length; i++)
                {
                    var pip = this.piplist[i].pip;
                    if (pip.visible == true)
                    {
                        var pos = this.piplist[i].pos;
                        if (Vec3.distanceSquared(playerpos, pos) & lt;.25)
                        {
                            pip.visible = false;
                        }
                    }
                    else
                    {
                        activecount--;
                    }
                }

Here is the real meat of the goal of the game. Loop over every bit of
food. If that food is visible, and if the distance from the food to the
player is less than .25, make the food object invisible by calling
.\ **visible=false**; If the food is not visible, just subtract 1 from
the total count. So, after this loop has run, **activecount **\ tells us
how much food is still not eaten. What do we do with that?

::

                if (activecount == 0)
                {
                    alertify.alert('You win!');
                    this.reset();
                }

It's as simple as that. If there is not more active food (food which is
visible, then we show a message, and **reset **\ the game.
**This.reset() **\ triggers the **reset **\ event.

::

                function reset()
                {
                    deletethis.piplist;
                    this.Scene.children_by_name.Ghost.transformAPI.setPosition(4, -17, .5);
                    this.Scene.children_by_name.Player.transformAPI.setPosition(-2, -10, .5);
                }

In the **reset **\ function, we just place the ghost and player back at
their staring positions, and delete the list of food. Remember that, at
the next tick, if the GameManager does not have a list of food, it will
create that list, and make all the food visible.

::

    **Note: **The positions that the ghost and player need to be set to will differ in your level from these values. 

Appendix 2: About the VWS
-------------------------

The Virtual World Sandbox is a project from Advanced Distributed
Learning to bring game based training and scenario design to more people
by building a completely HTML5, web based, multiuser simulation engine.
The VWS application is built on top of the Virtual World Framework, a
next generation simulation foundation. The VWS website is a
demonstration site, and should be used for exploration and entertainment
only. To setup your own server, check out the installation documents on
GitHub. You can learn more about the Virtual World Framework at
http://www.virtualworldframework.com. Contribute to the VWS project at
https://github.com/adlnet/Sandbox. Send questions and comments to:
Robert.chadwick.ctr@adlnet.gov. This tutorial was built with VWS version
0.4.7.2 on November 18, 2013.
