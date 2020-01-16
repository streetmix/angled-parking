## some notes

we've created a compressed glb file (a binary gltf) by importing the original car.dae into blender and exporting it back out. there are some issues with this:

- the tops of the car mirrors have the wrong color
- the rear of the car window and part of the area above the window have the wrong color (and what looks like z-fighting)
- the tailpipe should not have a visible backface so that it's hidden when the car is viewed from the front or sides

additionally it seems that more recent versions of threejs have issues loading the original car.dae, which appear that objects that were mirrored now have inverted faces. i will try to describe this using 3d modeling words i've heard: some transformation of those meshes caused the winding order to be reversed, which flips the front and back surfaces, and now the wrong faces are being culled. while blender loads this model just fine, it doesn't fix it if you then re-export to another dae file...
