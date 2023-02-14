remove-wear
===========

.. dfhack-tool::
    :summary: Remove wear from items in your fort.
    :tags: fort armok items

If your clothes are all wearing out and you wish you could just repair them
instead of having to make new clothes, then this tool is for you! This tool will
set the wear on items in your fort to zero, as if they were new.

Usage
-----

``remove-wear all``
    Remove wear from all items in your fort.
``remove-wear <item id> ...``
    Remove wear from items with the given ID numbers.

You can discover the ID of an item by selecting it in the UI and running the
following command::

    :lua !item.id
