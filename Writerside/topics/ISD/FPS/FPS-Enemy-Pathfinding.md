# FPS - Enemy Pathfinding

## Create an enemy

<aside>
‼️ The enemy mesh (the object that you can see) can be anything you want. This tutorial shows how to create a simple enemy of just a capsule. If you want to have a specific mesh, you may do so, but you will still need to create the other parts of the enemy object creation.

</aside>

Create a new scene (File→ New Scene) and create the root node as a `KinematicBody`. This will be the root node of the enemy object.

![Screen Shot 2022-09-12 at 10.39.19 am.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-12_at_10.39.19_am.png)

![Screen Shot 2022-09-12 at 10.39.36 am.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-12_at_10.39.36_am.png)

Rename the node as `Enemy`. 

![Screen Shot 2022-09-12 at 10.39.57 am.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-12_at_10.39.57_am.png)

Add a `MeshInstance` as a child of `Enemy`.

![Screen Shot 2022-09-12 at 10.40.39 am.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-12_at_10.40.39_am.png)

Click on the down arrow next to Mesh and choose New CapsuleMesh.

<aside>
‼️ This can be created as whatever type of object you wish, or a custom Mesh.

</aside>

![Screen Shot 2022-09-12 at 10.41.14 am.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-12_at_10.41.14_am.png)

Rotate the capsule by 90 degrees on the X axis.

![Screen Shot 2022-09-12 at 10.42.27 am.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-12_at_10.42.27_am.png)

Click on the Mesh preview and then set the Radius and Height.

These can be changed later, but you’ll need to make a note of them for later steps.

![Screen Shot 2022-09-12 at 10.43.35 am.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-12_at_10.43.35_am.png)

**If you wish**, you can change the colour of the enemy capsule by clicking on New SpatialMaterial in the inspector.

![Screen Shot 2022-09-12 at 10.46.21 am.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-12_at_10.46.21_am.png)

Under Albedo you can change the colour by clicking on the colour box and using the colour picker to choose the desired colour.

![Screen Shot 2022-09-12 at 10.47.13 am.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-12_at_10.47.13_am.png)

![Screen Shot 2022-09-12 at 10.47.42 am.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-12_at_10.47.42_am.png)

Add a Timer node as a child of enemy.

![Screen Shot 2022-09-12 at 10.48.08 am.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-12_at_10.48.08_am.png)

![Screen Shot 2022-09-12 at 10.48.16 am.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-12_at_10.48.16_am.png)

Select the enemy in the hierarchy and set the wait time and autostart options.

![Screen Shot 2022-09-12 at 10.48.33 am.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-12_at_10.48.33_am.png)

Save the scene as `Enemy.tscn`. 

![Screen Shot 2022-09-12 at 10.49.03 am.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-12_at_10.49.03_am.png)

## Create the Navmesh

<aside>
‼️ Navmesh is a Navigation Mesh that defines what area is traversable by the enemy objects (NPCs) and what is blocking terrain, such as walls, buildings etc.

</aside>

Open the scene for the main game. Add a child node to the scene root. Choose Navigation.

![Screen Shot 2022-09-12 at 10.49.48 am.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-12_at_10.49.48_am.png)

Create a child node of Navigation. This time choose `NavigationMeshInstance`.

Any children of this `NavigationMeshInstance` will be part of the Navmesh. This means that you need to move any floor or terrain nodes to be a child of this node. This should include most of your environment assets/nodes, including walls, lightposts, pickup items etc. 

![Screen Shot 2022-09-12 at 10.51.41 am.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-12_at_10.51.41_am.png)

Select the `NavigationMeshInstance` in the hierarchy and create a new **NavigationMesh** under **Navmesh** in the inspector.

![Screen Shot 2022-09-12 at 10.51.54 am.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-12_at_10.51.54_am.png)

Select **Bake NavMesh** in the tool bar.

You’ll notice that this has a blue highlight to the terrain. This indicates where the enemy objects can move around (traverse). 

![Before Navmesh.](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-12_at_10.52.22_am.png)

Before Navmesh.

![After Navmesh.](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-12_at_10.52.52_am.png)

After Navmesh.

You may also notice that any items that are children of the `NavigationMeshInstance` that are considered too tall, have gaps around the object. This indicates that these areas are **not traversable**.

![Screen Shot 2022-09-12 at 10.54.20 am.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-12_at_10.54.20_am.png)

Your scene should appear similar to this. All the environment nodes are children of `NavigationMeshInstance`.

![Screen Shot 2022-09-12 at 10.55.25 am.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-12_at_10.55.25_am.png)

Select `NavigationMeshInstance` in the hierarchy. Select the NavigationMesh in the inspector and set the size and the height of the Cell.

The height needs to be set as half of the enemy height defined when creating the enemy scene.

![Screen Shot 2022-09-12 at 10.56.27 am.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-12_at_10.56.27_am.png)

Under Agent, set the Height and Radius to match your enemy details.

![Screen Shot 2022-09-12 at 10.57.50 am.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-12_at_10.57.50_am.png)

Rebake the Navmesh

![Screen Shot 2022-09-12 at 10.59.09 am.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-12_at_10.59.09_am.png)

Save the Scene. 

$* \normalsize \mathcal {\color{black} \colorbox {orange}  {Save, Commit and Push Changes to Github!}}$ 

## Script the Enemy

Open the enemy scene, Right-click on the root node and choose Attach Script. 

![Screen Shot 2022-09-12 at 11.01.09 am.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-12_at_11.01.09_am.png)

Define the necessary variables.

| Variable | Purpose |
| --- | --- |
| nav | Stores the link to the Navigation node in the main game scene. |
| path | Array that contains the points the enemy will need to move through to get to the player. |
| path_node | The current index (position) in the path array. |
| speed | The enemies movement speed. This can be changed to whichever speed you wish and is appropriate for your game. |
| player | Links to the Player node in the main game. Important The path indicated needs to match your main game scene and match the node hierarchy.  |

`onready` is defined as - Initializes a variable once the Node the script is attached to and its children are part of the scene tree.

![Screen Shot 2022-09-12 at 11.04.12 am.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-12_at_11.04.12_am.png)

```python
onready var nav = get_parent()
var path = []
var path_node = 0
var speed = 10
onready var player = $"../../Player"
```

Add the following code to the enemy script.

![Screen Shot 2022-09-12 at 11.07.59 am.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-12_at_11.07.59_am.png)

```python
func _physics_process(delta):
    if path_node < path.size():
        var direction = (path[path_node] - global_transform.origin)
        if direction.length() < 1:
            path_node +=1
        else:
            move_and_slide(direction.normalized() * speed, Vector3.UP)
            
func move_to(target_pos):
    path = nav.get_simple_path(global_transform.origin, target_pos)
    path_node = 0
```

Select the Timer node and change from the Inspector tab to the Node tab.

![Screen Shot 2022-09-12 at 11.08.15 am.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-12_at_11.08.15_am.png)

Double click on the `timeout()` signal and click **Connect** on the Connect a Signal to a Method popup.

![Screen Shot 2022-09-12 at 11.08.43 am.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-12_at_11.08.43_am.png)

Add the following code to the new function.

Save the Enemy scene.

![Screen Shot 2022-09-12 at 11.57.42 am.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-12_at_11.57.42_am.png)

```python
move_to(player.global_transform.origin)
```

Add the Enemy scene to the main game. Add it as a child of the `Navigation` node.

![Screen Shot 2022-09-12 at 11.11.56 am.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-12_at_11.11.56_am.png)

Save the Main Game scene.

$* \normalsize \mathcal {\color{black} \colorbox {orange}  {Save, Commit and Push Changes to Github!}}$ 

Run the Game and your enemy should stalk you.