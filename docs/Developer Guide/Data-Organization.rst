This page describes the layout of data in the data directory created by
the DAL. For files of the application itself, see `File
Organization <File%20Organization>`__.

::

      /data
         /DataFiles
            /Models
            /Textures
            /Sounds
         /Logs
         /Profiles
         /States
         /Textures
         /Thumbnails

/data/Datafiles
~~~~~~~~~~~~~~~

All files and sub-folders from here are simply served by the file server
as ``vwfdatamanager.svc/datafile/...`` where ``...`` is the path to the
file. You can place anything here you need for your own servers scenes,
like models or textures

/data/Logs
~~~~~~~~~~

This folder will fill over time with log traces from the server and from
each running world.

/data/Profiles
~~~~~~~~~~~~~~

Each user will have a folder here, and inventory asset blobs will be
saved in it. Actual user profiles are stored in the DB, not as
filesystem blobs.

/data/States
~~~~~~~~~~~~

Each world will have a folder here, named with the UUID of the world.
The ``state`` file in this folder is the current JSON for the world. You
can manually edit the world data in this file, if you choose. Each
backup is stored here as well. Note that if you move the database or
create or delete these files manually, you may have references in the DB
to binary data that is not on the disk.

/data/Textures
~~~~~~~~~~~~~~

This subdirectory will be served to the client as part of the 'Map
Browser' component. All files and directories will be indexed and
downloadable. Files in this directory are assumed to be images.

/data/Thumbnails
~~~~~~~~~~~~~~~~

This directory should mirror the Textures directory, with the same files
and the same folders. However, each file in this directory should be a
thumbnail of its pair in the /textures/ directory.
