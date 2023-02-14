caravan
=======

.. dfhack-tool::
    :summary: Adjust properties of caravans on the map.
    :tags: untested fort armok bugfix

This tool can help with caravans that are leaving too quickly, refuse to unload,
or are just plain unhappy that you are such a poor negotiator.

Usage
-----

::

    caravan <command>

Also see `force` for creating caravans.

Examples
--------

``caravan extend``
    Force a caravan that is leaving to return to the depot and extend their
    stay another 7 days.
``caravan unload``
    Fix a caravan that got spooked by wildlife and refuses to fully unload.

Commands
--------

Commands listed with the argument ``[<ids>]`` can take multiple
(space-separated) caravan IDs (see ``caravan list``). If no IDs are specified,
then the commands apply to all caravans on the map.

``list``
    List IDs and information about all caravans on the map.
``extend [<days> [<ids>]]``
    Extend the time that caravans stay at the depot by the specified number of
    days (defaults to 7). Also causes caravans to return to the depot if
    applicable.
``happy [<ids>]``
    Make caravans willing to trade again (after seizing goods, annoying
    merchants, etc.). Also causes caravans to return to the depot if applicable.
``leave [<ids>]``
    Makes caravans pack up and leave immediately.
``unload``
    Fix endless unloading at the depot. Run this if merchant pack animals were
    startled and now refuse to come to the trade depot.
