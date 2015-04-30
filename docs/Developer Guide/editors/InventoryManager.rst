This class manages the user's interface to their personal inventory. It
communicates with the server over AJAX, and does not interface with the
socket or the VWF directly. Instead, it will download an object
definition from the server and then inject it over the client connection
as a VWF node.
