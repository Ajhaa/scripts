remove-stress
=============

.. dfhack-tool::
    :summary: Reduce stress values for fortress dwarves.
    :tags: fort armok units

Generally happy dwarves have stress values in the range of 0 to 500,000. If they
encounter things that stress them out, or if their needs are not being met, that
value will increase. When it increases too high, your dwarves will start to have
negative repercussions. This tool can magically whisk away some (or all) of
their stress so they can function normally again.

Usage
-----

::

    remove-stress [--all] [--value <value>]

Examples
--------

``remove-stress``
    Makes the currently selected dwarf blissfully unstressed.
``remove-stress --all``
    Makes all dwarves blissfully unstressed.
``remove-stress --all --value 10000``
    Reduces stress to 10,000 for all dwarves whose stress value is currently
    above that number.

Options
-------

``--all``
    Apply to all dwarves instead of just the currently selected dwarf.
``--value <value>``
    Decrease stress level to the given value. If the value is negative, prepend
    the negative sign with a backslash (e.g. ``--value \-50,000``).
