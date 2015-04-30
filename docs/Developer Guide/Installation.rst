Installing a copy of the ADL Sandbox server on your own machine.
================================================================

The ADL Sandbox server runs under NodeJS, a cross platform server
technology.

For your convenience, we've included in the source repository the
necessary binary executable to run the server under Windows. If you are
using a Mac or Linux, you'll need to download and install NodeJS for
your platform from http://nodejs.org/download/

**FOR WINDOWS**
^^^^^^^^^^^^^^^

To start, download the entire repository as a ZIP file (be sure to get
the node\_threejs branch). Unzip this file onto a directory on your
local computer. Lets say, for example, c:.

Download the supporting media assets. You can find them at
http://3dr.adlnet.gov/dev/VWFSupportFiles.zip.

Unzip this file into another directory. Lets say c:. Be sure to keep the
directory structure inside the zip file intact, as it is important.

Now, you can run the server. Navigate into the folder where you unzipped
the source repository (for example, c:). Execute the command:

``node.exe app.js -d "C:\SandboxData" -p 80``

This tells the server to run, serving the media assets from the
c:directory, and using port 80.

The server has several command line switches. Switches and values should
be seperated by spaces, and surrounded by quotes when the value contains
a space.

-  -p - the port to use. Default is 3000
-  -d - the path to the data directory. The default is "./data"

*NOTE:* If the data directory, either specified or unspecified, doesn't
exist, the Sandbox will attempt to create it.

-  -a - the username of the user who should be treated as the
   administrator. Default is 'admin'
-  -l - the verbosity level of the console log
-  -v - enable versioning. All requests will forward to a URL with the
   version number in Version.js
-  -nocache - the FileCache will not retain files in memory. Not much
   reason to disable this these days.
-  -compile - the server will build the main RequireJS module. This
   takes a long time on startup, but reduces the number of requests the
   client will make by almost 50.
-  -min - the server will minify using Uglyify.js.

So, production settings:
``node.exe app.js -d "C:\SandboxData" -p 80 -minify -compile -v``

**FOR MACINTOSH**
^^^^^^^^^^^^^^^^^

1. Download Node.js from http://nodejs.org/download/
2. Download the entire ADL Sandbox repository as a ZIP file (be sure to
   get the master branch) from
   https://github.com/adlnet/Sandbox/archive/master.zip
3. Download the supporting VWF media assets from
   http://3dr.adlnet.gov/dev/VWFSupportFiles.zip.

4. Install Node.js , afterwards you'll be asked to confirm
   /usr/local/bin is in your $PATH
5. Open up the Terminal and execute "ls /usr/local/bin" you should see
   "node" and "npm" as an output. NPM is Node Package Manager, it is
   installed along with Node.
6. If you like, you can verify the installation of node and npm by
   executing "node -v" and "npm -v" respectively.

7. Unzip the Node\_threejs.zip file into another folder, lets say
   "SandboxServer" on your local computer.
8. Unzip VWFSupportFiles.zip into another folder, lets say
   "SandboxData". Be sure to keep the directory structure inside the zip
   file intact, as it is important.
9. Now, you can run the server. Navigate into the folder where you
   unzipped the source repository (for example, SandboxServer). Execute
   the command:

   ::

       % node app.js -d SandboxData
