fix/dead-units
==============

.. dfhack-tool::
    :summary: Remove dead units from the list so migrants can arrive again.
    :tags: fort bugfix units

If so many units have died at your fort that your dead units list exceeds about
3000 units, migrant waves can stop coming. This fix removes uninteresting units
(like slaughtered animals and nameless goblins) from the unit list, allowing
migrants to start coming again.

Usage
-----

::

    fix/dead-units
