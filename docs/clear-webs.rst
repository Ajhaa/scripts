clear-webs
==========

.. dfhack-tool::
    :summary: Removes all webs from the map.
    :tags: adventure fort armok map units

In addition to removing webs, this tool also frees any creatures who have been
caught in one. Usable in both fortress and adventurer mode.

Note that it does not affect sprayed webs until they settle on the ground.

See also `fix/drop-webs`.

Usage
-----

::

    clear-webs [--unitsOnly|--websOnly]

Examples
--------

``clear-webs``
    Remove all webs and free all webbed units.

Options
-------

``--unitsOnly``
    Free all units from webs without actually removing any webs
``--websOnly``
    Remove all webs without freeing any units.
