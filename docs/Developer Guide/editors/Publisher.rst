This class manages the play/pause state of the world. It is responsible
for creating a local world state backup, and restoring it when the stop
button is hit.

It also contains some logic for testing the world. It may interface with
the server to create a temporary copy of the world and launch that world
in a child window. When that child window is closed, the world is
deleted.
