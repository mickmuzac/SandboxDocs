The Sandbox is composed of two major components - the server side and
the client application.

Server Side
-----------

The Sandbox server is a Node.js application that makes heavy use of
Express. It's composed of several sub systems:

1. Reflector
2. File Server
3. Service API
4. Data Access Layer
5. Views

Session is currently handled with Express middleware, although this was
not always the case. We are currently using Cookie-Session from
(https://github.com/expressjs/cookie-session).

Reflector
~~~~~~~~~

The reflector is a portion of the system that synchronizes worlds. It's
job is to accept messages from clients and send them to all participants
in the world. This allows the simulation to only move forward when all
clients receive the message. This system also keeps track of all the
running worlds, and detects when all uses have left so a world can be
shut down. See `VWF <VWF>`__ for more information. This the system is
implemented in **reflector.js**. See `File
Organization <File%20Organization>`__ for more info.

File Server
~~~~~~~~~~~

The file server is a simple tool that responds to request for files by
the client. Each file is GZipped and loaded into memory before being
served. The File Server component is implemented in **filecache.js**.
See `File Organization <File%20Organization>`__ for more info.

Services API
~~~~~~~~~~~~

The web front end uses many services on the server to manipulate worlds
and users. This system includes the endpoints for CRUD operations on
worlds and users, as well as upload of files, thumbnails, and a few
other odds and ends. The Express routes send any request that includes
``/vwfdatamanager.svc/`` to this system. It's implemented in
**sandboxAPI.js**. See `File Organization <File%20Organization>`__ for
more info.

Data Access Layer
~~~~~~~~~~~~~~~~~

The DAL interacts with the database to perform CRUD operation as
requested by the Services API. It does not do any validation or
verification, as it assumes that the front end has handled this. It does
wrap several asyncronous steps into simple calls. It handles all
storage. Currently, we write blobs to the filesystem and store metadata
about worlds, users, and inventory in NeDB
(https://github.com/louischatriot/nedb). See `Database <Database>`__.
The actual database interaction is implemented in **DB\_nedb.js**. You
can replace this to access a different DB. See `File
Organization <File%20Organization>`__ for more info.

Views
~~~~~

We use Hogan and Mustache to template the view files. These render all
the front end GUI like the login page, the home page, and all the
create/delete world logic.

Client Application
------------------

Most of the client side application is wrapped up in the VWF application
architecture. So, each feature is implemented as either a view driver or
a models driver, depending on whether or not it provides services that
can be accessed by the runtime reasoning of the world. See `VWF
Overview <VWF%20Overview>`__.

Model Drivers
~~~~~~~~~~~~~

These modules actually affect the state of the running simulation.
Together, they completely define the state of the world, and storing all
their data represents a snapshot of the environment.

**ThreeJS** The ThreeJS model driver loads all asset files, and is one
of the more complex parts of the system. Its responsible for
interpreting information from the VWF nodes and creating the graphic
representation. The current implementation is itself modular, with bits
of functionality implemented in subdrivers that mirror the same VWF API.
See `ThreeJS Model Driver <ThreeJS%20Model%20Driver>`__.

**AmmoJS** This is the physics driver. It is responsible for reading
simulation state data and applying collision detection and Newtonian
motion. See `AmmoJS Model Driver <AmmoJS%20Model%20Driver>`__.

**JQueryUI** The actual driver does very little. Most GUI code is in the
views. See `JQueryUI Model Driver <JQueryUI%20Model%20Driver>`__.

**javascript** This driver does the actual execution of the code
attached to VWF nodes through scripts. See `JavaScript Model
Driver <JavaScript%20Model%20Driver>`__.

**object** Part of the core VWF, last chance data storage for object
property data.

View Drivers
~~~~~~~~~~~~

View drivers do all the work in the system that is not available to
applications. These modules may only interact with the application state
by sending messages to the reflector. The internal state of these
modules is not considered part of the replicated application data.

**JQueryUI** This driver created JQueryUI objects to track the changing
state of UI VWF nodes, and hooks up all the UI functionality so the
nodes properly represent the UI state.

**EditorView** This is the main entrypoint for the entire suite of
editing tools. See `EditorView Driver <EditorView%20Driver>`__

**Audio** This driver wraps up the Buzz audio library.
(http://buzz.jaysalvat.com/). It responds to method calls on nodes and
creates sounds.

**ThreeJS** This is the graphics engine view component. It does the
actual render, and is responsible for non-stateful UI bits like
selection rectangles, highlights, and camera previews. See `ThreeJS View
Driver <ThreeJS%20View%20Driver>`__.

**xapi** This module creates the interaction with the ExperienceAPI
(http://www.adlnet.gov/tla/experience-api/).

**webRTC** Provides the hookups for the Video chat function.
