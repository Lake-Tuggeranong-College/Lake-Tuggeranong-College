# FPS - Simple Texturing of a Mesh

<aside>
‼️ Texturing is the process of applying an image to a 3D object.

</aside>

<aside>
‼️ For more information on texturing, see these resources:

</aside>

[Texturing and Materials - Game Dev Insider](https://gamedevinsider.com/making-games/game-artist/texturing-and-materials/)

Before you can texture, you need to have completed a mesh. A Mesh is a 3D shape which has a shape, but by default has no texture and appears as a grey object.

For instance, this simple light pole. This is made up of a number of different meshes (CSGBoxes and a CSGCylinder).

It’s basic, however it works for this purpose. However the colour is bland.

![Screen Shot 2022-08-25 at 9.13.24 pm.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-08-25_at_9.13.24_pm.png)

<aside>
‼️ Simple objects can be modelled in Godot, however to create more complex objects, you would need to use an external 3D modelling piece of software such as Blender. 
For a quick development process, create simple objects that you can quickly texture.

</aside>

When texturing objects, you can use Google Images to search for appropriate textures. If you’re creating an object that requires a repeating texture (like grass on the ground) it is advisable that you search for `<object> texture seamless`, for instance `grass texture seamless` as the images that it offers will not show any edges when tiled next to each other.

Find the images that you wish to texture your object. Import the image into the Godot project.

Select the mesh that you wish to texture.

![Screen Shot 2022-08-25 at 9.23.58 pm.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-08-25_at_9.23.58_pm.png)

Click the down arrow next to Material and choose New ShaderMaterial.

![Screen Shot 2022-08-25 at 9.24.30 pm.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-08-25_at_9.24.30_pm.png)

Drag the texture file from the file system tab to the Material. The mesh should then be textured with the image.

![2022-08-25 21-25-56.2022-08-25 21_27_22.gif](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/2022-08-25_21-25-56.2022-08-25_21_27_22.gif)

Continue the process until all the meshes in the scene are textured as desired.