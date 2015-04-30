This page details how files are organized in the repo.

::

      /Sandbox
         /data
         /support
            /client
               /lib
                  /vwf
                     /views
                       /Editorview
                     /models
                       /threejs
            /server
            /proxy
              /vwf.example.com
         /public
            /ADL
              /Sandbox
                /views
                /examples
                /skys
                /textures
                /terrain

/Support/Server/
~~~~~~~~~~~~~~~~

The server files for the NodeJS application

/support/client/proxy/
~~~~~~~~~~~~~~~~~~~~~~

The VWF uses this location to store object definition files for the
common object types. Here you'll find many of the YAML files for root
object types like node3.vwf.yaml and scene.vwf.yaml. A few of these have
been extended in Sandbox.

/public/adl/Sandbox
~~~~~~~~~~~~~~~~~~~

This is the root directory of the client side application. Here is the
index.vwf.yaml that defines the scene, and object definitions that are
specific to the Sandbox, like Prim.vwf.yaml and Asset.vwf.yaml. There
are also some default textures and assets that are part of the system,
like the texture for the home grid. Resources that are used in the
examples live here as well.

/public/adl/Sandbox/examples
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This directory holds all the example scenes you find when you access the
/examples/ page. Each example directory must start with 'example\_'.

/public/adl/Sandbox/skys
~~~~~~~~~~~~~~~~~~~~~~~~

The skyboxes. Notice how each is names with the BK,UP,DN,FR,RT or FL
suffix.

/public/adl/Sandbox/textures
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Not to be confused with the textures that are available through the API
and are stored with the data

/public/adl/Sandbox/terrain
~~~~~~~~~~~~~~~~~~~~~~~~~~~

Just some example assets

/data
~~~~~

This is where all the data that is specific to a given install lives (by
default. Can be overridden by the config file) See `Data
Organization <Data%20Organization>`__

/support/client/lib
~~~~~~~~~~~~~~~~~~~

This is where libraries required by the client side application live.
Most of the system lives under /vwf/

/support/client/lib/vwf/
~~~~~~~~~~~~~~~~~~~~~~~~

The VWF system, and the associated boot files. The application is
bootstrapped from here, and most of the client side app is in these
subfolders

/support/client/lib/vwf/views
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This is where all the vwf view code lives. Many of the Sandbox features
are implemented as vwf views.

/support/client/lib/vwf/views/EditorView
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This is location of all the editor interface elements, as well as a few
other bits of logic. The Editorview is responsible for creating all the
widgets you normally see on the screen.

/support/client/lib/vwf/models
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The VWF model drivers. All the services that are provided to a running
application are implemented as model drivers.

/support/client/lib/vwf/models/threejs
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The threejs model driver contains a lot of functionality, and is
modularized into subdrivers. Files in this directory are loaded as
required to provide threejs related services.
