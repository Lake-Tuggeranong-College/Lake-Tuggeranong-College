# Rapid Development - Environment

# Create a Floor

To start with, the player will need to walk on something, so the first step is to create a `MeshInstance` which will be the floor of the room where the player starts.

Right Click on the Game scene and choose Add Child Node. Search for Mesh Instance.

![Screen Shot 2022-08-05 at 11.05.03 am.png](Rapid%20Development%20-%20Environment%20535471d18126428abc8f851d0bd9452f/Screen_Shot_2022-08-05_at_11.05.03_am.png)

Rename the node “Floor”or “Ground” or whatever is appropriate.

![Screen Shot 2022-08-05 at 11.05.53 am.png](Rapid%20Development%20-%20Environment%20535471d18126428abc8f851d0bd9452f/Screen_Shot_2022-08-05_at_11.05.53_am.png)

In the Inspector, look for the Mesh attribute. int he dropdown box, choose `New PlaneMesh`. 

At this stage, the mesh is there, but the player (created later) will fall straight through it.

![Screen Shot 2022-08-05 at 11.07.29 am.png](Rapid%20Development%20-%20Environment%20535471d18126428abc8f851d0bd9452f/Screen_Shot_2022-08-05_at_11.07.29_am.png)

With the mesh selected, go to the Mesh Menu and choose Create Trimesh Static Body.

![Screen Shot 2022-08-05 at 11.10.35 am.png](Rapid%20Development%20-%20Environment%20535471d18126428abc8f851d0bd9452f/Screen_Shot_2022-08-05_at_11.10.35_am.png)

This updates the mesh to include 2 child nodes.

![Screen Shot 2022-08-05 at 11.11.38 am.png](Rapid%20Development%20-%20Environment%20535471d18126428abc8f851d0bd9452f/Screen_Shot_2022-08-05_at_11.11.38_am.png)

Currently the floor is quite small in size. The player object that will be created later will be quite significantly larger, so the relative scale will need to be addressed.

Edit the mesh.

![Screen Shot 2022-08-05 at 1.04.34 pm.png](Rapid%20Development%20-%20Environment%20535471d18126428abc8f851d0bd9452f/Screen_Shot_2022-08-05_at_1.04.34_pm.png)

Set the x and y size values to something larger. In this case, 20 has been used. This may need to be modified at a later date.

![Screen Shot 2022-08-05 at 1.05.48 pm.png](Rapid%20Development%20-%20Environment%20535471d18126428abc8f851d0bd9452f/Screen_Shot_2022-08-05_at_1.05.48_pm.png)

$* \normalsize \mathcal {\color{black} \colorbox {orange}  {Save, Commit and Push Changes to Github!}}$ 

# Texture the floor

<aside>
‼️ A Texture is simply an image that’s applied to a mesh.

</aside>

 Find an image to suit the environment appropriate for the game. 

<aside>
‼️ TIP: When googling, add the word “seamless” to your image searches. This means that the edges of the image align with the opposite side, meaning that when the image is tiled on a mesh, no edging will be visible.

</aside>

![Screen Shot 2022-08-05 at 11.16.12 am.png](Rapid%20Development%20-%20Environment%20535471d18126428abc8f851d0bd9452f/Screen_Shot_2022-08-05_at_11.16.12_am.png)

In the inspector, expand out the Material dropdown.

![Screen Shot 2022-08-05 at 11.20.17 am.png](Rapid%20Development%20-%20Environment%20535471d18126428abc8f851d0bd9452f/Screen_Shot_2022-08-05_at_11.20.17_am.png)

There is currently no material attached, hence why the mesh is white. Click on the dropdown next to [empty] and choose New Spatial Material.

![Screen Shot 2022-08-05 at 11.21.41 am.png](Rapid%20Development%20-%20Environment%20535471d18126428abc8f851d0bd9452f/Screen_Shot_2022-08-05_at_11.21.41_am.png)

In the menu that appears, expand `Albedo`. 

<aside>
‼️ Albedo is the default type for textures. There are many more as you can see in the list.

</aside>

![Screen Shot 2022-08-05 at 11.22.46 am.png](Rapid%20Development%20-%20Environment%20535471d18126428abc8f851d0bd9452f/Screen_Shot_2022-08-05_at_11.22.46_am.png)

Drag the texture from the FileSystem tab to the Texture option under Albedo. The texture on the plane has been updated.

![2022-08-05 11-24-51.2022-08-05 11_25_46.gif](Rapid%20Development%20-%20Environment%20535471d18126428abc8f851d0bd9452f/2022-08-05_11-24-51.2022-08-05_11_25_46.gif)

<aside>
‼️ This is the same process to texture any of your other assets, unless they’ve been textured prior to importing.

</aside>

The texture can be ‘tiled’ instead of stretched, by editting the x and y values under `Uv 1`. 

Choose values that suit the needs of the game and the desired effect.

![Screen Shot 2022-08-05 at 1.09.05 pm.png](Rapid%20Development%20-%20Environment%20535471d18126428abc8f851d0bd9452f/Screen_Shot_2022-08-05_at_1.09.05_pm.png)

# Add Lighting

The scene at this stage is too dark for the player. Right click on the Root Node, choose Add Child Node, search for and add a `DirectionalLight`.

![Screen Shot 2022-08-05 at 12.25.26 pm.png](Rapid%20Development%20-%20Environment%20535471d18126428abc8f851d0bd9452f/Screen_Shot_2022-08-05_at_12.25.26_pm.png)

With the `DirectionaLight` selected, enable Shadows in the Inspector.

Set the Rotational Degrees so that the light is roughly coming down from ‘the sky’ and creates the appropriate shadows.

The exact values don’t matter.

![Screen Shot 2022-08-05 at 12.29.16 pm.png](Rapid%20Development%20-%20Environment%20535471d18126428abc8f851d0bd9452f/Screen_Shot_2022-08-05_at_12.29.16_pm.png)

# Build your Environment

Find, import and put your environment models into your scene.

You may wish to add walls, or fences. 

At this stage, keep it simple and get a good example of your first scene. 

Similar to the Main Menu, the environment can be further developed at a later stage of the development process.