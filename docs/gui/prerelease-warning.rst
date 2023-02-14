gui/prerelease-warning
======================

.. dfhack-tool::
    :summary: Shows a warning if you are using a pre-release build of DFHack.
    :tags: dfhack

This tool shows a warning on world load for pre-release builds.

Usage
-----

::

    gui/prerelease-warning [force]

With no arguments passed, the warning is shown unless the "do not show again"
option has been selected. With the ``force`` argument, the warning is always
shown.
