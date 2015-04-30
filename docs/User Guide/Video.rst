The sandbox can support any video files that HTML5 naively supports.

If you desire to load a video in a popup window or overlayed on the
screen, you should look into standard HTML5 APIs for the 'Video' tag.
Simply code up your video to play as you normally would in any web page,
and attach that code to an object so that the sandbox will execute it.

We've recently added support for using video files as textures.
Currently, when a video is applied to a surface as a texture, it has no
material settings. For instance, you cannot use a video in place of an
image in a normal map. This may or may not become possible in the
future. However, you can play still use a video texture to display a
movie file on an object in the world, such as a monitor or projector
screen.

Select the object you want to modify, and open the material editor. On
the first tab, under 'Basic Material Settings' find the button that says
'Material Type: '. The default material type is the `Phong
Material <Phong%20Material>`__, but we will need to change this. Click
the button, and choose 'Video'. The GUI in the material editor will
change, and a button labeled 'Choose Video URL' will appear. Click this
button, and enter a URL to a video file.

You're video file should appear on the object, mapped as per the object
UV coordinates.
