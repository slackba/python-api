.. _example_sg_instance:

Create a ShotGrid API instance
=============================

This example shows you how to establish your initial connection to ShotGrid using script-based 
authentication. ``sg`` represents your ShotGrid API instance. Be sure you've read 
:ref:`Setting Up ShotGrid for API Access <setting_up_shotgrid>`.
::

    import pprint # Useful for debugging

    import shotgun_api3

    SERVER_PATH = "https://my-site.shotgrid.autodesk.com"
    SCRIPT_NAME = 'my_script'     
    SCRIPT_KEY = '27b65d7063f46b82e670fe807bd2b6f3fd1676c1'

    sg = shotgun_api3.Shotgun(SERVER_PATH, SCRIPT_NAME, SCRIPT_KEY)

    # Just for demo purposes, this will print out property and method names available on the 
    # sg connection object
    pprint.pprint([symbol for symbol in sorted(dir(sg)) if not symbol.startswith('_')])

For further information on what you can do with this ShotGrid object you can read the 
:ref:`API reference <apireference>`.