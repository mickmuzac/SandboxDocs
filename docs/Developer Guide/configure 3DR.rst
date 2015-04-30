The ADL Sandbox application allows users to load 3D assets from an ADL
3D Repository instance. Out of the box (and on the hosted copy at
`http:// vwf.adlnet.gov <http://vwf.adlnet.gov>`__), the server is
configured to connect to the main ADL 3D repository, at
http://3dr.adlnet.gov. However, as of version 0.4.11, this can be
configured to use any 3DR installation. The VWS server now proxies
traffic to and from the connected 3DR instance, so you don’t even
necessarily need to make your 3DR publicly visible, so long as the VWF
server can connect to it.

Configuring the 3DR settings
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The settings for connecting to the 3DR server are stored in the
``config.json`` file, located in the root of the servers directory. Here
is an example configuration file.

::

    //REMEMBER: Delete the comments when deploying. Comments are not valid JSON

    {
        "port": 3000,             //the port to serve on
        "datapath": "c:/vwfData", //the database location
        "admin": "admin",         //the username of the administrator
        "logLevel": 1,            //the verbosity of the console output
        "build": false,           //build the require js modules
        "minify": false,          //minify JavaScript on serve
        "compile": false,         //compile with the closure compiler
        "version": 1,             //the version number to use for URL versioning. Must be an integer!
        "useVersioning": false,   //when true, the server will use a url prefix to identify the software version
        "_3DRAPI": null,          //the endpoint to use to access the service. Null uses the public 3DR instance
        "_3DRAPIKey": null,       //the api key to use for all requests. Null defaults to the public API key
        "_3DRUser": null,         //username server identifies itself as. Null defaults to Anonymous
        "_3DRPassword": null,     //password for the server user. Null defaults to Anonymous
        "_3DRUseAuth": false      //use anonymous access or not. Null defaults to anonymous.
    }

*Note:* The comments are not valid JSON, and need to be removed from
your actual ``config.json`` file.

The relevant settings are:

::

        "_3DRAPI": null,          //the endpoint to use to access the service. Null uses the public 3DR instance
        "_3DRAPIKey": null,       //the api key to use for all requests. Null defaults to the public API key
        "_3DRUser": null,         //username server identifies itself as. Null defaults to Anonymous
        "_3DRPassword": null,     //password for the server user. Null defaults to Anonymous
        "_3DRUseAuth": false      //use anonymous access or not. Null defaults to anonymous.

1. ``_3DRAPI``

   -  Use this to configure the endpoint of the 3DR service
   -  Example: ``"_3DRAPI":"https://3dr.adlnet.gov/api/rest/"``

2. ``_3DRAPIKey``

   -  Requests to the 3DR API must include a valid API key. You can
      create a new key under the Account page on your 3DR instance. The
      public key on the ADL 3DR site is the default, ``00-00-00``
   -  Example: ``"_3DRAPIKey":"00-00-00"``

3. ``_3DRUser``

   -  The user name to use when the VWS server connects to the 3DR. You
      can leave this blank, but in doing so, you will only be able to
      access publicly accessible models. When you input a 3DR username
      (usually an email address), the permissions of this user will
      control the access of anyone using the VWS server
   -  Example: ``"_3DRUser":"robert.chadwick.ctr@adlnet.gov"``

4. ``_3DRPassword``

   -  The plain text password for the 3DR user. Because the server
      proxies the traffic, this password will not be visible to VWS
      users.
   -  Example: ``"_3DRPassword":"Password1234_is_very_strong"``

5. ``_3DRUseAuth``

   -  When set to false, the system will ignore the ``_3DRUser`` and
      ``_3DRPassword`` settings. When true, these setting will be used.
   -  Example: ``"_3DRUseAuth": true``

*Note:* The GUI in the Sandbox Editor currently prevents users from
loading models that do not have public access, even though, if
requested, the server would actually be able to load them. Look for a
fix in the future.

*Remember:* You must restart the VWS server when making changes to the
configuration file.
