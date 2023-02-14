add-recipe
==========

.. dfhack-tool::
    :summary: Add crafting recipes to a civ.
    :tags: untested adventure fort gameplay

Civilizations pick randomly from a pool of possible recipes, which means not all
civs get high boots, for instance. This script can help fix that. Only weapons,
armor, and tools are currently supported; things such as instruments are not.

Usage
-----

``add-recipe native``
    Add all crafting recipes that your civ could have chosen from its pool, but
    did not.
``add-recipe all``
    Add *all* available weapons and armor, including exotic items like
    blowguns, two-handed swords, and capes.
``add-recipe single <item token>``
    Add a single item by the given item token.

Example
-------

``add-recipe single SHOES:ITEM_SHOES_BOOTS``
    Allow your civ to craft high boots.
