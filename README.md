Wavefront OBJ renderer using pyglet's Batch class
=================================================

Based on `pyglet/contrib/model/model/obj.py` this module can load a Wavefront
object to be added to a Batch.

The module can be invoked for testing, for example:

    python obj_batch.py player.obj

Requires Pyglet 1.2 (alpha1 or later).

USAGE
-----

First load the object:

    obj = OBJ("object.obj")

Alternatively use you can use `OBJ.from_resource(filename)` to load the object,
material, textures, etc using pyglet's resource framework.

After the object is loaded, add it to a Batch:

    obj.add_to(batch)

Then you only have to draw your batch!


LICENSE
-------

I think the original source is in the public domain, so I keep the same
license for this version.

The example model is licensed CC BY-NC 3.0.

Juan J. Martinez <jjm@usebox.net>

