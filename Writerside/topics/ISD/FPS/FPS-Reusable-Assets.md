# FPS - Reusable Assets


One of the areas of game development that can save you a lot of work in the long run is building assets that you can reuse throughout your game.

For instance, you can build one ‘master’ copy of a traffic light object, and then have multiple traffic lights throughout the game, all based on the same asset.

<aside>
‼️ The added benefit to this is that once you have multiple copies of an asset, if you update the master, then all the copies get updated too.

</aside>

This will be demonstrated here by building a segment of wall that can be duplicated and be used to build a complex room structure.

Start by creating a new scene and set the root node to be a Node3D.

![Untitled](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Untitled%2025.png)

Rename the node from Node3D to Wall.

![Untitled](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Untitled%2026.png)

Build the mesh of the asset you are building. This part of the process will depend on what you’re developing. 

<aside>
‼️ Anything beyond the simple ‘block’ shapes may require some 3D modelling software, such as Blender, but that’s beyond the scope of this tutorial. If you’re interested in 3D modelling, there are many tutorials available on Youtube.

</aside>

For the wall segment, this can be built by creating a `CSGBox3D` as a child node of `Wall`.

![Untitled](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Untitled%2027.png)

Change to scale mode to resize the box into the shape that you want.

Use the scale controls of the widget to reshape the basic box object.

![Screen Shot 2022-08-25 at 2.00.13 pm.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-08-25_at_2.00.13_pm.png)

![Untitled](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Untitled%2028.png)

Save the Scene. 

![Screen Shot 2022-08-25 at 2.00.48 pm.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-08-25_at_2.00.48_pm.png)

Open the scene that you wish to edit, and drag the `tscn` file you just saved into the position you wish to to be in.

![2022-08-25 14-05-07.2022-08-25 14_06_16.gif](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/2022-08-25_14-05-07.2022-08-25_14_06_16.gif)

You can duplicate the node and place the duplicates in position.

Save the Scene once completed.

![2022-08-25 14-06-53.2022-08-25 14_09_36.gif](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/2022-08-25_14-06-53.2022-08-25_14_09_36.gif)

To edit the master, for instance by applying a texture, open the `tscn` file you saved, make changes and save. 

Once you save the `tscn` file, the instances are automatically updated in the other scene.

![2022-08-25 14-13-03.2022-08-25 14_17_41.gif](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/2022-08-25_14-13-03.2022-08-25_14_17_41.gif)
