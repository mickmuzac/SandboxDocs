This is just a quick list of things we've discussed doing in the future.
If anyone out there is interested in taking on one of these projects,
please let us know, and we'll get you started!

Content
~~~~~~~

1. Develop a more extensive library of demo content
2. Update the "EntityLibrary" UI and backend to allow the load of a
   library from an external location
3. Develop more complete applications as part of the "Examples"
4. Create a more detailed "about" page for each of these new examples
   describing what they do and how to use them

Database
~~~~~~~~

1. Allow a choice in the config file to use the NEDB in process
   database, or a MongoDB server
2. Assign Metadata to worlds relating them together geographically, as
   in "World B is north of world A".
3. Possibly allow direct file upload to the server, maybe establish disk
   quotas per user.
4. Limit the number of backup states that each world can save.

Server
~~~~~~

1. Implement/document a way for clients to get information about the
   world. Maybe allow an API for "GetProperty" that will return to the
   requesting client the value of the property. This could allow clients
   that are not full simulators to connect.
2. Implement authoritative state on the server. Spin up a copy of the
   world in a PhantomJS process and delegate all load/save actions to
   use the data from this client. This could bypass the problem of local
   synchronization errors becoming the definitive world state, or
   prevent griefing the system by modifying your own local memory and
   allowing that data to be saved into the DB.
3. Allow a client to specify that it is not a full simulator, so never
   send it the "getState" command, since the client can never answer
   that query.
4. AAR. Some socket message should cause the server to start recording
   data, some other message should start playing it back. Should record
   all network traffic. Save in DB? Need to think this one over.
5. DIS/HLA bridge. Allow for connection of clients that just bridge to
   other systems. Write a server that receives DIS messages and
   translates into VWF messages.
6. Make a clean import/export function for worlds. The may optionally
   include the download of external dependencies. Perhaps a web front
   end for this as well, so users can download their whole worlds from
   the cloud to a local server.
7. Work on supporting the work flow where an author has direct access to
   the server, and wants to manually author the world without the GUI.

Front End
~~~~~~~~~

1. Add a page to capture/view the data over the wire for a running
   world.
2. Add more/better explanation on the front page or a top level link
   about all the available features
3. Create a special case world which is sort of the "how to get started
   tutorial world"
4. Can we make the current AWS demo site use the load balancer script
   and run in multiprocess mode? This depends on getting the DB working
   on Mongo. See database section. Could also auto scale with AWS tools.

Physics
~~~~~~~

1. Finish work on integrating joints
2. Anyone care to try to compile Bullet 3 with Enscriptem? The
   determisism in Bullet 3 would really help the network sync for
   physics
3. Integrate the terrain engine with physics. This one is going to be
   tricky.
4. Allow modified shapes - via the geometry modifiers - to use any type
   of collision body
5. Add a center of mass offset parameter to all physics objects
6. Add a collisions body offset from pivot center property for all
   physics objects
7. Implement collision filtering - allow application level code to
   reject collisions
8. Add an API for physics level raycast

World
~~~~~

1. Establish some boundary beyond which objects cannot be placed. Align
   with world geography data.
2. Fix up the skybox stuff so it is easier for users to add new skyboxes

Asset Management
~~~~~~~~~~~~~~~~

1. Create better path for loading animated meshes. Currently must upload
   as either DAE or GLTF.
2. Create a "world inventory" and associated API so that scenes can save
   an object and 'rez' it from code. User inventory is not useful for
   this due to security. This is nice also in that there is one less
   server roundtrip.
3. Do a better job of preloading assets. Maybe allow a special metadata
   field so authors can specify additional assets to preload, since they
   may be created by code and not picked up by the current system.
4. Develop an LOD node. Use level 0 for picking, so that LOD display
   does not effect stateful world data. Load level 0 synchronously a la
   normal VWF, load others when available.
5. Do we need a global repo for entity definitions that lives outside of
   any one server?
6. Create a repo for vwf format smart objects.

Avatars
~~~~~~~

1. Use much of the work from DigitalEdge - allow morph targeted faces,
   animations, bone scaling... Much of this exists under the hood, but
   is lacking art. Please contact us to get started.
2. Teleport avatars from one world to another if they try to cross the
   world bounds?
3. Should avatar system use physics for collision? Currently uses the
   graphics engine, which required enormous work to make fast enough.
   It's a shame to loose this (though the work already done has other
   benefits), but with physics world, would be much much faster.
   Downside is that avatars won't automatically collide with just any 3D
   graphic asset

Code Quality
~~~~~~~~~~~~

1. Move editor camera code into view/threejs.js. Editor camera
   interactions are not part of the model state and should not be in
   index.vwf.yaml
2. JSFormat any code that is still not formatted.
3. Add license headers
4. Add sourceURL tags for debugging.
5. Remove dead code from character controller.
6. Test shaders on differnet mobile hardware. Much mobile hardware fails
   to compile different shaders. Maybe check GL\_LINK\_STATUS for new
   materials one frame after allocation in materialdef.js, and fallback
   on shader link fail.

Features
~~~~~~~~

1. Add a keyframe animation engine and GUI. Implement animation as top
   level VWF layer construct.
2. Prediction. Refactor VWF to receive/send messages through some proxy
   object. Update proxy object to loopback sends to separate VWF kernel
   that include only the js driver and object driver. Have renderer use
   data from this system for display, to compensate for latency. This
   requires quite some thought.
3. Do a better job of integrating XAPI. Create some sort of reusable
   behaviors, which trigger a configurable XAPI post based on a VWF
   event or method call. Create corresponding GUI
4. Integrate a cloud data provider as a terrain data provider. We did
   some work with the Cesium database in the past, but this needs much
   more work. Explore other data providers.

Other Stuff
~~~~~~~~~~~

1. Develop a better "stats" panel. Show networking load, time spent in
   javascript driver, time spent in physics, rendering time, memory
   used, other useful info.
2. Integrate Intelligent Tutor (e.g., GIFT) with Sandbox
