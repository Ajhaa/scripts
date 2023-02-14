on-new-fortress
===============

.. dfhack-tool::
    :summary: Run commands when a fortress is first started.
    :tags: dfhack

This utility command checks to see if the current fortress has just been created
(that is, the "age" of the fortress is 0, which is only true on the first tick
after the initial embark).

You can specify multiple commands to run, separated with :kbd:`;`, similar to
`multicmd`. However, if the fortress is not brand new, the commands will not
actually run.

Usage
-----

::

    on-new-fortress <command>[; <command> ...]

Example
-------

You can add commands to your ``dfhack-config/init/onMapLoad.init`` file that you
only want to run when a fortress is first started::

    on-new-fortress ban-cooking tallow; ban-cooking honey; ban-cooking oil
    on-new-fortress 3dveins
    on-new-fortress enable autobutcher; autobutcher autowatch
