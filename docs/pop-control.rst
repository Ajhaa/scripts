pop-control
===========

.. dfhack-tool::
    :summary: Controls population and migration caps persistently per-fort.
    :tags: unavailable fort auto gameplay

This script controls `hermit` and the various population caps per-fortress.
It is intended to be run from ``dfhack-config/init/onMapLoad.init`` as
``pop-control on-load``.

If you edit the population caps using `gui/settings-manager` after
running this script, your population caps will be reset and you may
get more migrants than you expect.

Usage
-----

``pop-control on-load``
    Load population settings for this site or prompt the user for settings
    if not present.
``pop-control reenter-settings``
    Revise settings for this site.
``pop-control view-settings``
    Show the current settings for this site.
