To add a new item to the menus:

1. Add the item to the menus.html file under
   ``support/client/lib/vwf/views/editorview/``
2. It should look something like this:
   ``<li><a  id="MenuSnapOff">Off</a></li>``
3. Hook up the click handler to do something.
4. We generally use the ``Menubar.js`` file for this.

::

     $('#MenuGlobalInventory').click(function(e) {
                if (_InventoryManager.isOpen())
                    _InventoryManager.hide();
                else {
                    _InventoryManager.show();
                    $("#InventoryTypeChoiceGlobal").click()
                }

            });
