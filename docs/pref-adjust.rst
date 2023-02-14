pref-adjust
===========

.. dfhack-tool::
    :summary: Set the preferences of a dwarf to an ideal.
    :tags: fort armok units

This tool replaces a dwarf's preferences with an "ideal" set which is easy to
satisfy::

    ... likes iron, steel, weapons, armor, shields/bucklers and plump helmets
    for their rounded tops.  When possible, she prefers to consume dwarven
    wine, plump helmets, and prepared meals (quarry bush). She absolutely
    detests trolls, buzzards, vultures and crundles.

Usage
-----

``pref-adjust all|goth_all|clear_all``
    Changes/clears preferences for all dwarves.
``pref-adjust one|goth|clear``
    Changes/clears preferences for the currently selected dwarf.
``pref-adjust list``
    List all types of preferences. No changes will be made to any dwarves.


Examples
--------

``pref-adjust all``
    Change preferences for all dwarves to an ideal.

Goth mode
---------

If you select goth mode, this tool will apply the following set of preferences
instead of the easy-to-satisfy ideal defaults::

    ... likes dwarf skin, corpses, body parts, remains, coffins, the color
    black, crosses, glumprongs for their living shadows and snow demons for
    their horrifying features.  When possible, she prefers to consume sewer
    brew, gutter cruor and bloated tubers.  She absolutely detests elves,
    humans and dwarves.
