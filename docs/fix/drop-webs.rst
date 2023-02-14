fix/drop-webs
=============

.. dfhack-tool::
    :summary: Make floating webs drop to the ground.
    :tags: fort bugfix items

Webs can be left floating in mid-air for a variety of reasons, such as getting
caught in a tree and the tree subsequently being chopped down (:bug:`595`). This
tool finds the floating webs and makes them fall to the ground.

See `clear-webs` if you want to remove webs entirely.

Usage
-----

``fix/drop-webs``
    Make webs that are floating in mid-air drop to the ground
``fix/drop-webs --all``
    Make webs that are above the ground for any reason (including being stuck in
    tree branches) fall to the ground.
