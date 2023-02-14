exportlegends
=============

.. dfhack-tool::
    :summary: Exports legends data for external viewing.
    :tags: untested legends inspection

When run from legends mode, you can export detailed data about your world so
that it can be browsed with external programs like
:forums:`World Viewer <128932>` and other similar utilities. The data exported
with this tool is more detailed than what you can get with vanilla export
functionality, and some external tools depend on this extra information.

``exportlegends`` can be especially useful when you are generating a lot of
worlds that you later want to inspect or when you want a map of every site when
there are several hundred.

Usage
-----

::

    exportlegends <command> [<folder name>]

Valid commands are:

:info:   Exports the world/gen info, the legends XML, and an extended info file.
:custom: Exports just the extended info file.
:sites:  Exports all available site maps.
:maps:   Exports all seventeen detailed maps.
:all:    Equivalent to calling all of the above, in that order.

The default folder name is generated from the region number of the world and the
current in-world date: ``legends-regionX-YYYYY-MM-DD``. You can use a different
folder by naming it on the ``exportlegends`` command line. Nested paths are
accepted, but all but the last folder has to already exist. To export to the
top-level DF folder, specify ``.`` as the folder name.

Examples
--------

``exportlegends all``
    Export all information to the ``legends-regionX-YYYYY-MM-DD`` folder.
``exportlegends all legends/myregion``
    Export all information to the ``legends/myregion`` folder.
``exportlegends custom .``
    Export just the extended info file to the DF folder (no subfolder).
