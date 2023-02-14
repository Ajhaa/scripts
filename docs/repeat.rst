repeat
======

.. dfhack-tool::
    :summary: Call a DFHack command at a periodic interval.
    :tags: dfhack

You can use this utility command to periodically call other DFHack commands.
This is especially useful for setting up "maintenance" commands that you want
called every once in a while but don't want to have to remember to run yourself.

Usage
-----

``repeat [--name <name>] --time <delay> [--timeUnits <units>] --command [ <command> ]``
    Register the given command to be run periodically.
``repeat --list``
    Show the currently registered commands and their names.
``repeat --cancel <name>``
    Unregister the given registered command.

Examples
--------

``repeat --name orders-sort --time 600 --command [ orders sort ]``
    Sort your manager workorders every 600 ticks (about half a day).
``repeat --time 10 --timeUnits days --command [ warn-starving ]``
    Check for starving dwarves and pets every 10 game days.
``repeat --cancel warn-starving``
    Unregister the warn-starving command registered above.

Options
-------

``--name <name>``
    Registers the command under the given name. This ensures you have a
    memorable identifier for the ``--list`` output so you can unregister the
    command if you want. It also prevents the same command from being
    registered twice. If not specified, it's set to the first argument after
    ``--command``.
``--time <delay>``
    Sets the delay between invocations of the command. It must be a positive
    integer.
``--timeUnits <units>``
    A unit of time for the value passed with the ``--time`` option. Units can be
    ``frames`` (raw FPS), ``ticks`` (unpaused game frames), or the in-world time
    measurements of ``days``, ``months``, or ``years``. If not specified,
    ``ticks`` is the default.
``--command [ ... ]``
    The ``...`` specifies the command to be run, just as you would write it on
    the commandline. Note that the command must be enclosed in square brackets.

Registering commands
--------------------

It is common that you want to register the same set of commands every time you
load a game. For this, it is convenient to add the ``repeat`` commands you want
to run to the ``dfhack-config/init/onMapLoad.init`` file so they are run
whenever you load a fort.
