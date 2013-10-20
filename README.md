Wavefront OBJ renderer using pyglet's Batch class
=================================================

Based on `pyglet/contrib/model/model/obj.py` this module can load a Wavefront
object to be added to a Batch.

The module can be invoked directly for testing, for example:

    python obj_batch.py player.obj

Requires Pyglet 1.2 (alpha1 or later).

USAGE
-----

First load the object:

    obj = OBJ("object.obj")

Alternatively you can use `OBJ.from_resource(filename)` to load the object,
material, textures, etc using pyglet's resource framework.

After the object is loaded, add it to a batch:

    obj.add_to(batch)

Then you only have to draw your batch!

You can also apply transformations to the meshes before adding them to the
batch:

    obj.load_identity() # only needed to discard any existing transformation
    obj.translate(0, 1, 0)
    obj.rotate(90, 1, 0, 0)
    obj.scale(2, 2, 2)
    obj.add_to(batch)


LICENSE
-------

I think the original source is in the public domain, so I keep the same
license for this version.

Part of this code has been contributed to pyglet and it can be found on `contrib/`
directory of pyglet's distribution.

The example model is licensed CC BY-NC 3.0.

Juan J. Martinez <jjm@usebox.net>

