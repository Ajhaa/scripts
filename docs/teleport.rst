teleport
========

.. dfhack-tool::
    :summary: Teleport a unit anywhere.
    :tags: fort armok units

This tool teleports any unit, friendly or hostile, to somewhere else on the map.

.. note::

    `gui/teleport` is an in-game UI for this script.

Usage
-----

::

    teleport [--unit <id>] [-x <x> -y <y> -z <z>]

When teleporting, if no unit id is specified, the unit under the cursor is used.
If no coordinates are specified, then the coordinates under the cursor are used.
Either the unit id or the coordinates must be specified for this command to be
useful.

You can use the `cprobe <probe>` command to discover a unit's id, or the
`position` command to discover the map coordinates under the cursor.

Examples
--------

Discover the id of the unit beneath the cursor and then teleport that unit to a
new cursor position::

    cprobe
    teleport --unit 2342

Discover the coordinates under the cursor, then teleport a selected unit to that
position::

    position
    teleport -x 34 -y 20 -z 163

Teleport unit ``1234`` to ``56,115,26``::

    teleport -unit 1234 -x 56 -y 115 -z 26
