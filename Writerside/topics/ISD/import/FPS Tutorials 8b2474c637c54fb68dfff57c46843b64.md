# FPS Tutorials
















# Enemy Pathfinding

## Create an enemy

<aside>
‼️ The enemy mesh (the object that you can see) can be anything you want. This tutorial shows how to create a simple enemy of just a capsule. If you want to have a specific mesh, you may do so, but you will still need to create the other parts of the enemy object creation.

</aside>

Create a new scene (File→ New Scene) and create the root node as a `KinematicBody`. This will be the root node of the enemy object.

![Screen Shot 2022-09-12 at 10.39.19 am.png](Screen_Shot_2022-09-12_at_10.39.19_am.png)

![Screen Shot 2022-09-12 at 10.39.36 am.png](Screen_Shot_2022-09-12_at_10.39.36_am.png)

Rename the node as `Enemy`. 

![Screen Shot 2022-09-12 at 10.39.57 am.png](Screen_Shot_2022-09-12_at_10.39.57_am.png)

Add a `MeshInstance` as a child of `Enemy`.

![Screen Shot 2022-09-12 at 10.40.39 am.png](Screen_Shot_2022-09-12_at_10.40.39_am.png)

Click on the down arrow next to Mesh and choose New CapsuleMesh.

<aside>
‼️ This can be created as whatever type of object you wish, or a custom Mesh.

</aside>

![Screen Shot 2022-09-12 at 10.41.14 am.png](Screen_Shot_2022-09-12_at_10.41.14_am.png)

Rotate the capsule by 90 degrees on the X axis.

![Screen Shot 2022-09-12 at 10.42.27 am.png](Screen_Shot_2022-09-12_at_10.42.27_am.png)

Click on the Mesh preview and then set the Radius and Height.

These can be changed later, but you’ll need to make a note of them for later steps.

![Screen Shot 2022-09-12 at 10.43.35 am.png](Screen_Shot_2022-09-12_at_10.43.35_am.png)

**If you wish**, you can change the colour of the enemy capsule by clicking on New SpatialMaterial in the inspector.

![Screen Shot 2022-09-12 at 10.46.21 am.png](Screen_Shot_2022-09-12_at_10.46.21_am.png)

Under Albedo you can change the colour by clicking on the colour box and using the colour picker to choose the desired colour.

![Screen Shot 2022-09-12 at 10.47.13 am.png](Screen_Shot_2022-09-12_at_10.47.13_am.png)

![Screen Shot 2022-09-12 at 10.47.42 am.png](Screen_Shot_2022-09-12_at_10.47.42_am.png)

Add a Timer node as a child of enemy.

![Screen Shot 2022-09-12 at 10.48.08 am.png](Screen_Shot_2022-09-12_at_10.48.08_am.png)

![Screen Shot 2022-09-12 at 10.48.16 am.png](Screen_Shot_2022-09-12_at_10.48.16_am.png)

Select the enemy in the hierarchy and set the wait time and autostart options.

![Screen Shot 2022-09-12 at 10.48.33 am.png](Screen_Shot_2022-09-12_at_10.48.33_am.png)

Save the scene as `Enemy.tscn`. 

![Screen Shot 2022-09-12 at 10.49.03 am.png](Screen_Shot_2022-09-12_at_10.49.03_am.png)

## Create the Navmesh

<aside>
‼️ Navmesh is a Navigation Mesh that defines what area is traversable by the enemy objects (NPCs) and what is blocking terrain, such as walls, buildings etc.

</aside>

Open the scene for the main game. Add a child node to the scene root. Choose Navigation.

![Screen Shot 2022-09-12 at 10.49.48 am.png](Screen_Shot_2022-09-12_at_10.49.48_am.png)

Create a child node of Navigation. This time choose `NavigationMeshInstance`.

Any children of this `NavigationMeshInstance` will be part of the Navmesh. This means that you need to move any floor or terrain nodes to be a child of this node. This should include most of your environment assets/nodes, including walls, lightposts, pickup items etc. 

![Screen Shot 2022-09-12 at 10.51.41 am.png](Screen_Shot_2022-09-12_at_10.51.41_am.png)

Select the `NavigationMeshInstance` in the hierarchy and create a new **NavigationMesh** under **Navmesh** in the inspector.

![Screen Shot 2022-09-12 at 10.51.54 am.png](Screen_Shot_2022-09-12_at_10.51.54_am.png)

Select **Bake NavMesh** in the tool bar.

You’ll notice that this has a blue highlight to the terrain. This indicates where the enemy objects can move around (traverse). 

![Before Navmesh.](Screen_Shot_2022-09-12_at_10.52.22_am.png)

Before Navmesh.

![After Navmesh.](Screen_Shot_2022-09-12_at_10.52.52_am.png)

After Navmesh.

You may also notice that any items that are children of the `NavigationMeshInstance` that are considered too tall, have gaps around the object. This indicates that these areas are **not traversable**.

![Screen Shot 2022-09-12 at 10.54.20 am.png](Screen_Shot_2022-09-12_at_10.54.20_am.png)

Your scene should appear similar to this. All the environment nodes are children of `NavigationMeshInstance`.

![Screen Shot 2022-09-12 at 10.55.25 am.png](Screen_Shot_2022-09-12_at_10.55.25_am.png)

Select `NavigationMeshInstance` in the hierarchy. Select the NavigationMesh in the inspector and set the size and the height of the Cell.

The height needs to be set as half of the enemy height defined when creating the enemy scene.

![Screen Shot 2022-09-12 at 10.56.27 am.png](Screen_Shot_2022-09-12_at_10.56.27_am.png)

Under Agent, set the Height and Radius to match your enemy details.

![Screen Shot 2022-09-12 at 10.57.50 am.png](Screen_Shot_2022-09-12_at_10.57.50_am.png)

Rebake the Navmesh

![Screen Shot 2022-09-12 at 10.59.09 am.png](Screen_Shot_2022-09-12_at_10.59.09_am.png)

Save the Scene. 

$* \normalsize \mathcal {\color{black} \colorbox {orange}  {Save, Commit and Push Changes to Github!}}$ 

## Script the Enemy

Open the enemy scene, Right-click on the root node and choose Attach Script. 

![Screen Shot 2022-09-12 at 11.01.09 am.png](Screen_Shot_2022-09-12_at_11.01.09_am.png)

Define the necessary variables.

| Variable | Purpose |
| --- | --- |
| nav | Stores the link to the Navigation node in the main game scene. |
| path | Array that contains the points the enemy will need to move through to get to the player. |
| path_node | The current index (position) in the path array. |
| speed | The enemies movement speed. This can be changed to whichever speed you wish and is appropriate for your game. |
| player | Links to the Player node in the main game. Important The path indicated needs to match your main game scene and match the node hierarchy.  |

`onready` is defined as - Initializes a variable once the Node the script is attached to and its children are part of the scene tree.

![Screen Shot 2022-09-12 at 11.04.12 am.png](Screen_Shot_2022-09-12_at_11.04.12_am.png)

```python
onready var nav = get_parent()
var path = []
var path_node = 0
var speed = 10
onready var player = $"../../Player"
```

Add the following code to the enemy script.

![Screen Shot 2022-09-12 at 11.07.59 am.png](Screen_Shot_2022-09-12_at_11.07.59_am.png)

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

![Screen Shot 2022-09-12 at 11.08.15 am.png](Screen_Shot_2022-09-12_at_11.08.15_am.png)

Double click on the `timeout()` signal and click **Connect** on the Connect a Signal to a Method popup.

![Screen Shot 2022-09-12 at 11.08.43 am.png](Screen_Shot_2022-09-12_at_11.08.43_am.png)

Add the following code to the new function.

Save the Enemy scene.

![Screen Shot 2022-09-12 at 11.57.42 am.png](Screen_Shot_2022-09-12_at_11.57.42_am.png)

```python
move_to(player.global_transform.origin)
```

Add the Enemy scene to the main game. Add it as a child of the `Navigation` node.

![Screen Shot 2022-09-12 at 11.11.56 am.png](Screen_Shot_2022-09-12_at_11.11.56_am.png)

Save the Main Game scene.

$* \normalsize \mathcal {\color{black} \colorbox {orange}  {Save, Commit and Push Changes to Github!}}$ 

Run the Game and your enemy should stalk you.

- Objects/Enemies Taking Damage


# Objects / Enemies Taking Damage

The bullets and enemy have been created, the bullets fire. Now it’s time to put it together - having the enemies take damage. 

Unlike the player’s health, which is a global variable, each enemy (or any other object with health) will have its own health that will need to be diminished for it to be destroyed. 

**Each object or enemy that you wish to take damage needs to be configured in the same way.**

<aside>
‼️

The object taking damage will need to have a Collision Shape configured as a direct child of the root node.

![Screen Shot 2022-10-06 at 10.02.18 pm.png](Screen_Shot_2022-10-06_at_10.02.18_pm.png)

</aside>

Open the (or attach a) script for the object that you wish to take damage.

Add a simple `take_damage(damage)` function to the script, which simply outputs a test message to ensure that the process works.

![Screen Shot 2022-10-06 at 10.37.49 pm.png](Screen_Shot_2022-10-06_at_10.37.49_pm.png)

```python
func take_damage(damage):
    print("ouch")
```

Run the game at this stage to test the collision. 

![2022-10-06 23-02-38.2022-10-06 23_04_11.gif](2022-10-06_23-02-38.2022-10-06_23_04_11.gif)

<aside>
‼️ You may find it useful to slow the bullets down to properly test, as can be seen in this example.

</aside>

Open the script for the object. Add a `health` variable at the top of the script and set the value to 100.

![Screen Shot 2022-10-06 at 11.14.44 pm.png](Screen_Shot_2022-10-06_at_11.14.44_pm.png)

```python
var health = 100
```

Update `take_damage()` to reduce the amount of health, and then check if the health has reached zero. If so, then delete the object.

![Screen Shot 2022-10-06 at 11.16.23 pm.png](Screen_Shot_2022-10-06_at_11.16.23_pm.png)

```python
func take_damage(damage):
    health -= 50
    if health <=0:
        queue_free()
```

Run the project and you should see the object be destroyed as health reaches 0.

![2022-10-06 23-13-27.2022-10-06 23_14_08.gif](2022-10-06_23-13-27.2022-10-06_23_14_08.gif)

<aside>
‼️ Remember this process can work for any damageable object in the game - enemies, walls, doors etc.

</aside>

- Simple Texturing of a Mesh


# Simple Texturing of a mesh

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

![Screen Shot 2022-08-25 at 9.13.24 pm.png](Screen_Shot_2022-08-25_at_9.13.24_pm.png)

<aside>
‼️ Simple objects can be modelled in Godot, however to create more complex objects, you would need to use an external 3D modelling piece of software such as Blender. 
For a quick development process, create simple objects that you can quickly texture.

</aside>

When texturing objects, you can use Google Images to search for appropriate textures. If you’re creating an object that requires a repeating texture (like grass on the ground) it is advisable that you search for `<object> texture seamless`, for instance `grass texture seamless` as the images that it offers will not show any edges when tiled next to each other.

Find the images that you wish to texture your object. Import the image into the Godot project.

Select the mesh that you wish to texture.

![Screen Shot 2022-08-25 at 9.23.58 pm.png](Screen_Shot_2022-08-25_at_9.23.58_pm.png)

Click the down arrow next to Material and choose New ShaderMaterial.

![Screen Shot 2022-08-25 at 9.24.30 pm.png](Screen_Shot_2022-08-25_at_9.24.30_pm.png)

Drag the texture file from the file system tab to the Material. The mesh should then be textured with the image.

![2022-08-25 21-25-56.2022-08-25 21_27_22.gif](2022-08-25_21-25-56.2022-08-25_21_27_22.gif)

Continue the process until all the meshes in the scene are textured as desired.

- Game Mechanic - Points


# Points Mechanic

## Global Script

Create a new script called `Global.gd` (unless it’s already created).

![Screen Shot 2022-09-06 at 1.59.04 pm.png](Screen_Shot_2022-09-06_at_1.59.04_pm.png)

![Screen Shot 2022-09-06 at 1.59.39 pm.png](Screen_Shot_2022-09-06_at_1.59.39_pm.png)

Replace the contents of the file with this code.

<aside>
‼️ If you already have a Global.gd simply include the var current_score=0 line of code.

</aside>

Save the File.

```python
extends Node

var current_score = 0
```

In Project Settings (Project → Project Settings). Click on the AutoLoad tab. Browse to the Global.gd and enter the Node Name as `Global`.

![End Result](Screen_Shot_2022-09-06_at_2.10.46_pm.png)

End Result

Click Close.

## Pickup Item

The pickup item can be any object you wish. It could be a simple cube or cylinder or a complex object that you’ve imported from 3D modelling software such as Blender. Regardless of the object itself, the object needs to be saved as it’s own Scene.

In this case, the file is saved as `Pickup.tscn` and there is a cylinder object created.

![Screen Shot 2022-09-06 at 2.14.32 pm.png](Screen_Shot_2022-09-06_at_2.14.32_pm.png)

Create child nodes of the original object to include a mesh that the player can collide with.

![Screen Shot 2022-09-06 at 2.15.18 pm.png](Screen_Shot_2022-09-06_at_2.15.18_pm.png)

Right Click on the Pickup node and attach a script, named `Pickup.gd`. Save the script. There is no need to change the code at this stage.

![Screen Shot 2022-09-06 at 2.18.05 pm.png](Screen_Shot_2022-09-06_at_2.18.05_pm.png)

Select the Area node, and switch to the Node tab.

![Screen Shot 2022-09-06 at 2.16.31 pm.png](Screen_Shot_2022-09-06_at_2.16.31_pm.png)

Double click on the Body Entered signal. Make sure the Pickup node is selected and click Connect. 

![Screen Shot 2022-09-06 at 2.18.58 pm.png](Screen_Shot_2022-09-06_at_2.18.58_pm.png)

Enter the following code for the `_on_Area_body_entered(body)` function.

This code check to see if the object that collides with the pickup item is the player. If so, it will add 10 points to the `current_score` variable in the Global script.

Then it deletes the pickup item.

![Screen Shot 2022-09-06 at 2.19.59 pm.png](Screen_Shot_2022-09-06_at_2.19.59_pm.png)

```python
if (body.name == "Player"):
        Global.current_score += 10
        queue_free()
```

## Displaying the score

Open the Player scene, and make a child node of the Camera. The node needs to be a label. Name the label `playerScore`. 

<aside>
‼️ You can use HBoxes, VBoxes and other methods to place the score label where you wish it to go. This is just a quick example.

</aside>

Open the Player script and look for the `_process()` function.

Add the following line of code at the end of the function.

Every frame refresh, this code will take the current_score value and update the playerScore label.

![Screen Shot 2022-09-06 at 2.24.42 pm.png](Screen_Shot_2022-09-06_at_2.24.42_pm.png)

```python
$Camera/playerScore.text = str(Global.current_score)
```

- Game Mechanic - Player Health


# Player Health

This stage of the tutorial will demonstrate how to implement a simple health system, where there is a player health and when the enemy collides with the player, the health reduces. As with many other aspects of game development, the exact implementation will depend on the requirements for the project, so apply as necessary.

<aside>
‼️ This process can be applied to ANY object that you wish to reduce the players health when a collision occurs.

</aside>

## Player Script

Open `Global.gd` and add a new variable named `player_health`. Set the initial value to be 100.

Save the file.

![Screen Shot 2022-09-12 at 9.05.32 pm.png](Screen_Shot_2022-09-12_at_9.05.32_pm.png)

## Update Enemy

Open `Enemy.tscn` to edit the Enemy scene, adding an `Area` node as a child of the root node. Add a CollisionShape node a child of that one.

![Screen Shot 2022-09-12 at 8.56.53 pm.png](Screen_Shot_2022-09-12_at_8.56.53_pm.png)

Select `CollisionShape` and change the shape attribute to a `CapsuleShape`.

![Screen Shot 2022-09-12 at 8.58.22 pm.png](Screen_Shot_2022-09-12_at_8.58.22_pm.png)

Select Area in the hierarchy, change to the Node tab, and double click on `body_entered()` in the list of signals.

![Screen Shot 2022-09-12 at 8.59.56 pm.png](Screen_Shot_2022-09-12_at_8.59.56_pm.png)

Click Connect.

![Screen Shot 2022-09-12 at 9.02.37 pm.png](Screen_Shot_2022-09-12_at_9.02.37_pm.png)

Replace the contents of the function with the code shown.

This code checks first if the object the enemy has collided with is the player, and if so, reduce  `player_health` by 10. Then delete the enemy object from the game.

<aside>
‼️ The exact value the health gets reduced by can be set to whatever value you chose. Just change the 10.

</aside>

![Screen Shot 2022-09-12 at 9.06.39 pm.png](Screen_Shot_2022-09-12_at_9.06.39_pm.png)

```python
if (body.name == "Player"):
        Global.player_health -= 10
        queue_free()
```

Save the Enemy script.

## Lose Scene

If not already done, create a new scene and save it as `Lose.tscn`. This scene will be loaded if the player has lost, or in this example, run out of health.

Design the scene in whichever way you wish, just ensure there is a way for the user to return to the main menu.

## Update Player Script

Open the Player script (`Player.gd`) and add the code to the end of the `_process()` function.

![Screen Shot 2022-09-12 at 9.42.29 pm.png](Screen_Shot_2022-09-12_at_9.42.29_pm.png)

```python
if Global.player_health <= 0:
        print("Dead")
        get_tree().change_scene("res://Lose.tscn")
```

$* \normalsize \mathcal {\color{black} \colorbox {orange}  {Save, Commit and Push Changes to Github!}}$ 

- Hiding the mouse Pointer


# Hiding the Mouse Pointer

Open `Player.gd`.  Update the _ready() function to set the mouse to be hidden.

```arduino
Input.set_mouse_mode(Input.MOUSE_MODE_HIDDEN)
```

![Untitled](Untitled.png)

# Showing the Mouse Pointer

To reenable the mouse pointer, for instance if the player returns to the main menu, add the following function below the _ready() function in the `Player.gd` script. 

This function runs automatically, when the player object is removed from the tree. In other words, when the player instance is removed from the game.

```arduino
func _exit_tree():
    Input.set_mouse_mode(Input.MOUSE_MODE_VISIBLE)
```

![Untitled](Untitled%201.png)

- Raycasting


# Raycasting

<aside>
‼️ Raycasting is an alternative to firing projectiles in your game. Projectiles (bullets, lasers etc) that have a ‘physical’ object being fired in the game take up processing power, memory etc. Raycasting is a more efficient method of determining if shots hit, or if an object can see another etc.

</aside>

To implement raycasting for shooting or another method, you can extend the current functionality of your game without impacting existing functionality.

## Input Map

First, you can choose to create a new input trigger for raycasting. Go to Project → Project Settings → Input Map and create a new input map called `ray` and assign a key to it.

<aside>
‼️ In this example the key `r` has been assigned. You can choose another key or mouse button as required.

</aside>

![Untitled](Untitled%202.png)

## Player Object

Open the Player object (`player.tscn`) and create a **RayCast** child object of the Camera node.

![Untitled](Untitled%203.png)

With RayCast selected, set the Enabled option to be true in the Inspector. Additionally, get the **Cast To** settings to the 0, 0, -10. This will set the ray cast to be set to be in the direction of the camera.

<aside>
‼️ If your player’s camera is configured differently, you may need to change these settings.

</aside>

![Untitled](Untitled%204.png)

Create a **MeshInstance** as a child of the Player root node, calling it **HitPoint**.

![Untitled](Untitled%205.png)

In the inspector, Create a new SphereMesh, and change the radius and height to 0.1 and 0.2 respectively.

Set the colour of the mesh to red (or any other colour) to make it stand out in the game.

![Untitled](Untitled%206.png)

Save the `player.tscn` file.

## Player.gd script

Open `[player.gd](http://player.gd)` and add two new variables at the top of the script to store the raycast and the hitpoint nodes.

![Untitled](Untitled%207.png)

```python
onready var ray = $Camera/RayCast
export(NodePath) var hit_point
```

Update `_input()` to include a check to see if the user has pressed the `ray` input.

If they have, then the code will check to see if the raycast is actually colliding with a collider.

If it does collide with a collider, then it will check if that object has a function called `raycast_collision()` in it’s script (to be written later). If it does, run that function.

<aside>
‼️ Using this check for the raycast_collision() allows you to have objects in the game which will be impacted by the raycast (such as enemies) and other objects which don’t react (such as walls).

</aside>

![Untitled](Untitled%208.png)

```python
if Input.is_action_pressed("ray"):
        if ray.is_colliding():
            var collider = ray.get_collider()
            
            get_node(hit_point).transform.origin = ray.get_collision_point()
            #print("Collided with " + collider.get_parent().name + " at %s " % ray.get_collision_point())
        
            if collider.get_parent().has_method("raycast_collision"):
                collider.get_parent().raycast_collision()
```

$$
\utilde {\color{black} \fcolorbox{darkorange}{darkorange}  {Commit and Push to Github}}
$$

## Modifying objects

For objects to be detected by raycasts in this implementation there **must** be two things:

- a collider on the object.
- the parent object **must** have a script with a `raycast_collision()` function included.

### Wall Example

Objects can be quickly edited to add a CSG shape, such as CSGBox enabled for collisions. For example, the wall objects can be modified to include this.

![Untitled](Untitled%209.png)

Attach a script to the Wall root node. Include the function and at this stage simply output that the raycast has been detected.

```python
func raycast_collision():
    print("ray hit")
```

![Untitled](Untitled%2010.png)

Save the Wall scene.

When the game is now run, aim at a wall and press the `ray` input. The “ray hit” output should be visible in the Output.

![Untitled](Untitled%2011.png)

$$
\utilde {\color{black} \fcolorbox{darkorange}{darkorange}  {Commit and Push to Github}}
$$

Any other objects in the game can react to raycasts but following the same process of adding a collider as a child, such as a CSGBox, and including a script with a `raycast_collision()` function included.

The `raycast_collision()` can delete the object, add points etc - whatever you need the object to do when it is “shot”.

- Win Conditions


# Win Condition/s

TBA

- Lose Conditions


# Lose Condition/s

There may be many different conditions in which the player dies, as such, this tutorial cannot cover all the desired options.

## Condition: Player Health = 0