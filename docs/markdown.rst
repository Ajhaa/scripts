markdown
========

.. dfhack-tool::
    :summary: Exports the text you see on the screen for posting online.
    :tags: unavailable dfhack

This tool saves a copy of a text screen, formatted in markdown, for posting to
Reddit (among other places). See `forum-dwarves` if you want to export BBCode
for posting to the Bay 12 forums.

This script will attempt to read the current screen, and if it is a text
viewscreen (such as the dwarf 'thoughts' screen or an item 'description') then
append a marked-down version of this text to the output file. Previous entries
in the file are not overwritten, so you may use the ``markdown`` command
multiple times to create a single document containing the text from multiple
screens, like thoughts from several dwarves or descriptions from multiple
artifacts.

The screens which have been tested and known to function properly with this
script are:

#. dwarf/unit 'thoughts' screen
#. item/art 'description' screen
#. individual 'historical item/figure' screens
#. manual pages
#. announcements screen
#. combat reports screen
#. latest news (when meeting with liaison)

There may be other screens to which the script applies. It should be safe to
attempt running the script with any screen active. An error message will inform
you when the selected screen is not appropriate for this script.

Usage
-----

::

    markdown [-n] [<name>]

The output is appended to the ``md_export.md`` file by default. If an alternate
name is specified, then a file named like ``md_{name}.md`` is used instead.

Examples
--------

``markdown``
    Appends the contents of the current screen to the ``md_export.md`` file.
``markdown artifacts``
    Appends the contents of the current screen to the ``md_artifacts.md`` file.

Options
-------

``-n``
    Overwrite the contents of output file instead of appending.
