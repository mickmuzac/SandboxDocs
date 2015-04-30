All objects in the world can be assigned a friendly name. These names
appear in the GUI for all action, but need not be unique - they are just
for your convenience. To name an object, select the object and open the
Object Properties window. Under the 'Flags' heading, find the 'name'
field. Type the name here.

When you copy, duplicate, or paste an object, the name will be
incremented automatically if it ends with a number.

The name is stored in the ``DisplayName`` property of an object. From
script, all objects are indexed by name under ``this.children_by_name``.
