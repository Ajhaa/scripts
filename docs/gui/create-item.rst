gui/create-item
===============

.. dfhack-tool::
    :summary: Magically summon any item.
    :tags: fort armok items

This tool provides a graphical interface for creating items of your choice. It
walks you through the creation process with a series of prompts, asking you
for the type of item, the material, the quality, and (if ``--multi`` is passed
on the commandline) the quantity.

Be sure to select a unit before running this tool so the created item can have
a valid "creator" assigned.

See also `createitem` or `modtools/create-item` for different interfaces for
creating items.

Usage
-----

::

    gui/create-item [<options>]

Examples
--------

``gui/create-item --multi``
    Only provide options for creating items that normally exist in the game.
    Also include the prompt for quantity so you can create more than just one
    item at a time.
``gui/create-item --unrestricted``
    Create one item made of anything in the game. For example, you can create
    a bar of vomit, if you please.

Options
-------

``--multi``
    Also prompt for the quantity of items to create.
``--unit <id>``
    Use the specified unit as the "creator" of the generated item instead of the
    selected unit.
``--unrestricted``
    Don't restrict the material options to only those that are normally
    appropriate for the selected item type.
``--startup``
    Instead of showing the item creation interface, start monitoring reactions
    for a modded reaction with a code of ``DFHACK_WISH``. When a reaction with
    that code is completed, show the item creation gui. This allows you to mod
    in "wands of wishing" that can let your adventurer make wishes for items.
