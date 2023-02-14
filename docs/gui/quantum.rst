gui/quantum
===========

.. dfhack-tool::
    :summary: Quickly and easily create quantum stockpiles.
    :tags: untested fort productivity stockpiles

This tool provides a visual, interactive interface for creating quantum
stockpiles.

Quantum stockpiles simplify fort management by allowing a small stockpile to
contain an infinite number of items. This reduces the complexity of your storage
design, lets your dwarves be more efficient, and increases FPS.

Quantum stockpiles work by linking a "feeder" stockpile to a one-tile minecart
hauling route. As soon as an item from the feeder stockpile is placed in the
minecart, the minecart is tipped and all items land on an adjacent tile. The
single-tile stockpile in that adjacent tile that holds all the items is your
quantum stockpile.

Before you run this tool, create and configure your "feeder" stockpile. The
size of the stockpile determines how many dwarves can be tasked with bringing
items to this quantum stockpile. Somewhere between 1x3 and 5x5 is usually a good
size. Make sure to assign an appropriate number of wheelbarrows to feeder
stockpiles that will contain heavy items like corpses, furniture, or boulders.

The UI will walk you through the steps:

1) Select the feeder stockpile by clicking on it or selecting it with the cursor
   and hitting Enter.
2) Configure the orientation of your quantum stockpile and select whether to
   allow refuse and corpses with the onscreen options.
3) Select a spot on the map to build the quantum stockpile by clicking on it or
   moving the cursor so the preview "shadow" is in the desired location. Then
   hit :kbd:`Enter`.

If there are any minecarts available, one will be automatically assigned to the
hauling route. If you don't have a free minecart, ``gui/quantum`` will enqueue a
manager order to make one for you. Once it is built, run
`assign-minecarts all <assign-minecarts>` to assign it to the route, or enter
the (h)auling menu and assign one manually. The quantum stockpile needs a
minecart to function.

Quantum stockpiles work much more efficiently if you add the following line to
your ``dfhack-config/init/onMapLoad.init`` file::

    prioritize -a StoreItemInVehicle

This prioritizes moving of items from the feeder stockpile to the minecart.
Otherwise, the feeder stockpile can get full and block the quantum pipeline.

See :wiki:`the wiki <Quantum_stockpile>` for more information on quantum
stockpiles.

Usage
-----

::

    gui/quantum
