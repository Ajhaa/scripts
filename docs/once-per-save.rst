once-per-save
=============

.. dfhack-tool::
    :summary: Run commands only if they haven't been run before in this world.
    :tags: dfhack

If you are looking for a way to run commands once when you start a new fortress,
you probably want `on-new-fortress`.

This tool is better for commands that you want to run once per world.

You can specify multiple commands to run, separated with :kbd:`;`, similar to
`multicmd`. However, if the command has been run (successfully) before with
``once-per-save`` in the context of the current savegame, the commands will not
actually run.

Usage
-----

``once-per-save [--rerun] <command>[; <command> ...]``
    Run the specified commands if they haven't been run before. If ``--rerun``
    is specified, run the commands regardless of whether they have been run
    before.
``once-per-save --reset``
    Forget which commands have been run before.
