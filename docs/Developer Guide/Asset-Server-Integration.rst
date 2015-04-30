We use a separate system called the ADL 3D Repository for our asset
hosting. You can find the running instance of this system at
https://3DR.adlnet.gov, or visit its repo at
https://github.com/adlnet/3D-Repository.

Because we can't currently align the permissions between the Sandbox and
the 3DR servers, all requests for assets should be proxied through the
Sandbox server. The address of the 3DR server to use can be found in the
configuration file. See `Configuration <Configuration>`__ or `Asset
Server
Config <http://vwf.adlnet.gov/r/documentation/tutorials/configuring-the-3dr-integration-feature/>`__

The 3DR integration features are implemented in
``/support/server/3dr_proxy.js``. See `File
Organization <File%20Organization>`__
