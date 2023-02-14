hfs-pit
=======

.. dfhack-tool::
    :summary: Creates a pit straight to the underworld.
    :tags: fort armok map

This script creates a pit to the underworld, starting at the cursor position and
going down, down down.

Usage
-----

::

    hfs-pit [<size> [<walls> [<stairs>]]]

The first parameter is the "radius" in tiles of the (square) pit, that is, how
many tiles to open up in each direction around the cursor. The default is ``1``,
meaning a single column.

The second parameter is ``1`` to wall off the sides of the pit on all layers
except the underworld, or anything else to leave them open.

The third parameter is ``1`` to add stairs in the middle of the pit or anything
else to just have an open channel.

Note that stairs are buggy; they will not reveal the bottom until you dig
somewhere, but underworld creatures will path in.

Examples
--------

``hfs-pit``
    Create a single-tile wide pit with no walls or stairs.
``hfs-pit 4 1 0``
    A seven-across pit (the center tile plus three on each side) with stairs but
    no containing walls.
``hfs-pit 2 0 1``
    A five-across pit with no stairs but with containing walls.
