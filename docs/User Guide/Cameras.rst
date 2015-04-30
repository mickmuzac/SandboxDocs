There are 2 major things to understand about cameras in the VWF. First,
the camera you are looking through by default in the editor is a special
camera that is not shared with other users. Each user has his or her own
viewpoint when editing that is not shared between users. There is a
function for temporarily broadcasting the position of your camera to
other users - see `Camera Modes <Camera%20Modes>`__ for more info.

Second, you can also create camera objects within the scene. These
cameras are full VWF entities, and can be scripted, copied, or deleted.
They can even have behaviors applied, just as any other object.

To create a camera, use the drop down menu. Choose
Create->Camera->Perspective. The camera will be created at the center of
your view. If you move your viewpoint within about 10 meters of the
camera, and you are in a selection mode, you will see an icon appear to
show you the location of the new camera object. If you do not see this
icon, you may be too far away. That's OK, you can select the camera by
name on the Hierarchy panel.

When you have a camera selected in the editor, you will see a preview of
the selected camera's view. This view will update in real time as you
use the editor tools to move around the camera. You will also see in the
main view a helper graphic to show you where the camera is pointing.
This helper may show a camera viewpoint that is slightly behind the
camera's position. This is normal. We actually use the near clip plane
of the camera as the cameras 'position'.

If you see the camera icon, you can double click it to activate the
selected camera as the main camera. You can also activate different
cameras by choosing Camera->Activate Camera from the drop down menu.
Note: All the existing camera modes, such as 'Fly', or 'Orbit', apply
only to the default editor camera. Selecting one of these modes will
active the default camera.

When a camera is selected, you may edit some of it's properties in the
Properties panel.

Field of View - The width of the camera view. A good default is 60, but
you can simulate a telescopic view with a much smaller number.

Near - the near clip plane. Objects nearer than this will not be shown.
Clip planes are used primarily to focus the depth buffer resolution
around the area of interest in a scene. A full discussion of this topic
is out of scope for this article. Just please note that you may see some
visual artifacts if the near is set too low, or the far too high.

Far - the far clip plane. Objects farther than this will not be shown.
