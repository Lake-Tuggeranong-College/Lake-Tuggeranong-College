# Content

Welcome to this tutorial on building a First-Person Shooter (FPS) game using Godot. 

This tutorial is designed to guide you through the process of creating an FPS game from scratch, providing step-by-step instructions and explanations along the way.  Godot is a powerful, open-source game engine that is highly flexible and customizable, making it an excellent choice for game development. It supports a variety of platforms and offers a unique and intuitive scene system.  In this tutorial, we will cover key aspects of game development such as setting up the player character, implementing movement and shooting mechanics, creating enemies, and designing levels. We will also delve into more advanced topics such as raycasting and scripting.  By the end of this tutorial, you will have a fully functional FPS game that you can further customize and expand upon. Whether you're a seasoned developer or just starting out in game development, this tutorial will provide valuable insights into the process of creating an FPS game in Godot.  Please note that this tutorial is written for Godot v3.5.1. If you're using a different version of Godot, some steps may vary.  Let's get started!

> These instructions are written for Godot v3.5.1
{style="note"}

## Main Menu {id="MainMenu"}

### Create the Main Menu Scene

Click on the 2D Scene option under Create Root Node.

![Screen Shot 2022-08-05 at 10.31.31 am.png](Screen_Shot_2022-08-05_at_10.31.31_am.png)

Rename the Node “Main Menu”

![Screen Shot 2022-08-05 at 10.32.19 am.png](Screen_Shot_2022-08-05_at_10.32.19_am.png)

Right Click on the Main Menu Node and choose “Create Child Node” and add a Button.

![Screen Shot 2022-08-05 at 10.33.06 am.png](Screen_Shot_2022-08-05_at_10.33.06_am.png)

Set the Text of the button to “Play” or whatever you want.

![Screen Shot 2022-08-05 at 10.33.34 am.png](Screen_Shot_2022-08-05_at_10.33.34_am.png)

Right-click on the Button node and choose Attach Script. Change the name of the script to `SceneChange.gd` as this may be used in different circumstances.

![Screen Shot 2022-08-05 at 10.35.42 am.png](Screen_Shot_2022-08-05_at_10.35.42_am.png)

With the button selected, change to the Node tab and double click the `pressed()` signal.

![Screen Shot 2022-08-05 at 10.34.23 am.png](Screen_Shot_2022-08-05_at_10.34.23_am.png)

Select the Button in the list and click Connect.

![Screen Shot 2022-08-05 at 10.37.22 am.png](Screen_Shot_2022-08-05_at_10.37.22_am.png)

Save the Scene as `MainMenu.tscn`.

<include from="reusableContent.topic" element-id="commitPush"/>

### Create the Game Scene

Choose Scene→New Scene. And Choose 3D Scene as the root Node.

![Screen Shot 2022-08-05 at 10.43.46 am.png](Screen_Shot_2022-08-05_at_10.43.46_am.png)

Rename the scene node appropriate for your game.

![Screen Shot 2022-08-05 at 10.45.38 am.png](Screen_Shot_2022-08-05_at_10.45.38_am.png)

Save the scene, naming it appropriate to your game.


### Create a Button


> You can configure the main menu in any way you want, displaying the button/s wherever you want. These steps just show creating the button and the functionality.
{style="note"}

Right click on the Main Menu node and create a child Button node.

![Screen Shot 2022-08-15 at 10.32.09 am.png](Screen_Shot_2022-08-15_at_10.32.09_am.png)

Right-click on the button and Attach a Script. Call this script `SceneChange.gd`. This script will be used for any and all scripts where the button changes scenes.

![Screen Shot 2022-08-15 at 10.35.33 am.png](Screen_Shot_2022-08-15_at_10.35.33_am.png)

With the button selected, click on the Node tab, next to the Inspector, and double click on the `pressed(`) signal.

![Screen Shot 2022-08-15 at 10.36.02 am.png](Screen_Shot_2022-08-15_at_10.36.02_am.png)

Make sure Button is selected in the “Connect To script” section. Leave the Receiver Method as is, and just click connect.

![Screen Shot 2022-08-15 at 10.37.35 am.png](Screen_Shot_2022-08-15_at_10.37.35_am.png)

At the top of the script after the `extends` line, add `export(String) var scene_to_load.`

Change the `pass` line of code to `get_tree().change_scene(scene_to_load)`.

![Screen Shot 2022-08-15 at 10.39.00 am.png](Screen_Shot_2022-08-15_at_10.39.00_am.png)

<include from="reusableContent.topic" element-id="commitPush"/>


### Link the Main Menu to the Game Scene.

Open the Main Menu scene.

Right-Click on the game scene you just saved in the FileSystem tab and choose Copy Path.

![Screen Shot 2022-08-05 at 10.50.17 am.png](Screen_Shot_2022-08-05_at_10.50.17_am.png)

Paste that Path into the `Scene To Load` field for the Button created earlier.

![Screen Shot 2022-08-05 at 10.51.13 am.png](Screen_Shot_2022-08-05_at_10.51.13_am.png)


### Run the Game

Press the play button to run the game. If this is the first time the project has been run, you’ll be asked to choose a Main Scene.

If the Main Menu Scene is open, you can just choose Select Current.

If you have another scene open, choose Select, and then double-click on the `MainMenu.tscn`.

![Screen Shot 2022-08-05 at 10.54.49 am.png](Screen_Shot_2022-08-05_at_10.54.49_am.png)


<procedure title="Changing Starting Scene" collapsible="true">
    <step>Changing the Starting Scene can be set in the Project Settings</step>
    <step><img src="Screen_Shot_2022-08-05_at_10.55.43_am.png">Screen_Shot_2022-08-05_at_10.55.43_am.png</img>
</step>
</procedure>


### Continue developing the Main Menu

Once the initial configuration is complete (connecting the main menu to the first game scene, you are free to improve the main menu as much as you want. Add `VBoxContainers` and `HBoxContainers` to organise the layout to assist with placement of items.

- Add Headings and graphics. 
- The Main menu developed can be continued in the future at any stage of the development process.

## Environment - Rapid Development

### Create a Floor

To start with, the player will need to walk on something, so the first step is to create a `MeshInstance` which will be the floor of the room where the player starts.

Right-Click on the Game scene and choose Add Child Node. Search for Mesh Instance.

![Screen Shot 2022-08-05 at 11.05.03 am.png](Screen_Shot_2022-08-05_at_11.05.03_am.png)

Rename the node “Floor” or “Ground” or whatever is appropriate.

![Screen Shot 2022-08-05 at 11.05.53 am.png](Screen_Shot_2022-08-05_at_11.05.53_am.png)

In the Inspector, look for the Mesh attribute. in the dropdown box, choose `New PlaneMesh`.

At this stage, the mesh is there, but the player (created later) will fall straight through it.

![Screen Shot 2022-08-05 at 11.07.29 am.png](Screen_Shot_2022-08-05_at_11.07.29_am.png)

With the mesh selected, go to the Mesh Menu and choose Create Trimesh Static Body.

![Screen Shot 2022-08-05 at 11.10.35 am.png](Screen_Shot_2022-08-05_at_11.10.35_am.png)

This updates the mesh to include 2 child nodes.

![Screen Shot 2022-08-05 at 11.11.38 am.png](Screen_Shot_2022-08-05_at_11.11.38_am.png)

Currently, the floor is quite small. The player object that will be created later will be quite significantly larger, so the relative scale will need to be addressed.

Edit the mesh.

![Screen Shot 2022-08-05 at 1.04.34 pm.png](Screen_Shot_2022-08-05_at_1.04.34_pm.png)

Set the x and y size values to something larger. In this case, 20 has been used. This may need to be modified at a later date.

![Screen Shot 2022-08-05 at 1.05.48 pm.png](Screen_Shot_2022-08-05_at_1.05.48_pm.png)

### Texture the floor

> A Texture is simply an image that’s applied to a mesh.
{style="note"}

Find an image to suit the environment appropriate for the game.

> TIP: When googling, add the word “seamless” to your image searches. This means that the edges of the image align with the opposite side, meaning that when the image is tiled on a mesh, no edging will be visible.
{style="note"}

![Screen Shot 2022-08-05 at 11.16.12 am.png](Screen_Shot_2022-08-05_at_11.16.12_am.png)

In the inspector, expand out the Material dropdown.

![Screen Shot 2022-08-05 at 11.20.17 am.png](Screen_Shot_2022-08-05_at_11.20.17_am.png)

There is currently no material attached, hence why the mesh is white. Click on the dropdown next to [empty] and choose New Spatial Material.

![Screen Shot 2022-08-05 at 11.21.41 am.png](Screen_Shot_2022-08-05_at_11.21.41_am.png)

In the menu that appears, expand `Albedo`.

> Albedo is the default type for textures. There are many more as you can see in the list.
{style="note"}

![Screen Shot 2022-08-05 at 11.22.46 am.png](Screen_Shot_2022-08-05_at_11.22.46_am.png)

Drag the texture from the FileSystem tab to the Texture option under Albedo. The texture on the plane has been updated.

![2022-08-05 11-24-51.2022-08-05 11_25_46.gif](2022-08-05_11-24-51.2022-08-05_11_25_46.gif)

> This is the same process to texture any of your other assets, unless they’ve been textured prior to importing.
{style="note"}

The texture can be ‘tiled’ instead of stretched, by editting the x and y values under `Uv 1`.

Choose values that suit the needs of the game and the desired effect.

![Screen Shot 2022-08-05 at 1.09.05 pm.png](Screen_Shot_2022-08-05_at_1.09.05_pm.png)

### Add Lighting

The scene at this stage is too dark for the player. Right click on the Root Node, choose Add Child Node, search for and add a `DirectionalLight`.

![Screen Shot 2022-08-05 at 12.25.26 pm.png](Screen_Shot_2022-08-05_at_12.25.26_pm.png)

With the `DirectionaLight` selected, enable Shadows in the Inspector.

Set the Rotational Degrees so that the light is roughly coming down from ‘the sky’ and creates the appropriate shadows.

The exact values don’t matter.

![Screen Shot 2022-08-05 at 12.29.16 pm.png](Screen_Shot_2022-08-05_at_12.29.16_pm.png)

### Build your Environment

Find, import and put your environment models into your scene.

You may wish to add walls, or fences.

At this stage, keep it simple and get a good example of your first scene.

Similar to the Main Menu, the environment can be further developed at a later stage of the development process.

## First-Person Player Scene

As this game is a First-Person Shooter, there is no need to create a mesh for the player object; as in the game, the player will never see it.

Therefore, the player object can be initially created with a simple collider and camera.

There are two main steps to creating the player:

1. Making the player scene, creating nodes etc, and
2. Coding the functionality.

### The Player Scene

Create a new Scene.

Create the root node as `KinematicBody`. To do this, click on Other Node and search for `KinematicBody` and choose Create.

Save the scene as `Player.tscn`.

![Screen Shot 2022-08-05 at 12.38.36 pm.png](Screen_Shot_2022-08-05_at_12.38.36_pm.png)

Add a child node—`CollisionShape`.

This will represent the boundaries of the player node in the game. It will be used as the players ‘hit box’ (officially the **collider**) to detect collisions - walls, floors, projectiles etc.

![Screen Shot 2022-08-05 at 12.39.42 pm.png](Screen_Shot_2022-08-05_at_12.39.42_pm.png)

With the CollisionShape selected, create a new Capsule Shape.

![Screen Shot 2022-08-05 at 12.40.19 pm.png](Screen_Shot_2022-08-05_at_12.40.19_pm.png)

Rotate the capsule so it’s vertical (to represent the boundaries of the player).

![Screen Shot 2022-08-05 at 12.41.46 pm.png](Screen_Shot_2022-08-05_at_12.41.46_pm.png)

Resize the dimensions of the capsule, but clicking drop down box next to Capsule Shape and choose Edit.

![Screen Shot 2022-08-05 at 12.45.27 pm.png](Screen_Shot_2022-08-05_at_12.45.27_pm.png)

Set the Radius and height to values that suit your game.

> You may find these values need to be modified later to better suit your game.
{style="note"}

![Screen Shot 2022-08-05 at 12.46.13 pm.png](Screen_Shot_2022-08-05_at_12.46.13_pm.png)

### Camera

The player has been created, however, the player cannot ‘see’ as a camera has not been added. The camera is what the user sees in game. In a FPS, the mouse is attached to the player object and therefore the camera. When the mouse moves, the camera moves to match.

Add a Camera child node to the Player node.

![Screen Shot 2022-08-05 at 12.49.30 pm.png](Screen_Shot_2022-08-05_at_12.49.30_pm.png)

Set the Environment attribute to the `default_env.tres` already created in the project.

![2022-08-05 12-50-55.2022-08-05 12_51_22.gif](2022-08-05_12-50-55.2022-08-05_12_51_22.gif)

Set this camera to be the ‘main’ camera by setting the Current attribute to True.

![Screen Shot 2022-08-05 at 12.54.02 pm.png](Screen_Shot_2022-08-05_at_12.54.02_pm.png)

Move the camera up the ‘body’ to appear as if the camera ‘sees’ through the players eyes.

> Exact value is not critical, but it has to suit your capsule size set earlier.
{style="note"}

Only change the `Y` value. This is the vertical value. The coordinate system will be discussed at a later time.

![Screen Shot 2022-08-05 at 12.56.18 pm.png](Screen_Shot_2022-08-05_at_12.56.18_pm.png)

### Key Actions

Before any scripting can be done, some keyboard and mouse inputs need to be mapped to actions (to be coded later).

<procedure title="Set Input Keys" id="inject-a-procedure">
    <step>
        <p>Open the `Project` menu</p>
    </step>
    <step>
        <p>Select Project Settings</p>
    </step>
    <step>
        <p>Select Input Map</p>
    </step>
</procedure>

Add the following actions and set the keys and mouse inputs as directed.

`player_forward`

`player_backward`

`player_left`

`player_right`

`jump`

`shoot`

> Pay close attention to the spelling and capitalisation. These will be linked to in the script later.
{style="note"}

![Screen Shot 2022-08-05 at 1.25.04 pm.png](Screen_Shot_2022-08-05_at_1.25.04_pm.png)

### Mouse Look

Open `Player.tscn`. Right click on the root node and attach a script. Leave the settings as they are, and click Create.

![Screen Shot 2022-08-05 at 1.30.19 pm.png](Screen_Shot_2022-08-05_at_1.30.19_pm.png)

Clear out the commented code, and add some variables which will be used later in the script.

These variables define how fast the player moves and how jumping and gravity impact the players movement.

![Screen Shot 2022-08-05 at 1.33.52 pm.png](Screen_Shot_2022-08-05_at_1.33.52_pm.png)

```
extends KinematicBody

# Physics
var movementSpeed = 1.0 		# How fast the player can move.
var jumpStrength = 1.0 		# How much force used to make player jump
var gravity = 10.0			# Gravity's strength.

# Called when the node enters the scene tree for the first time.
func _ready():
    pass # Replace with function body.
```
{collapsible="true"}

Add other variables. These variables define the player movement and camera movement limitations.

![Screen Shot 2022-08-05 at 1.43.29 pm.png](Screen_Shot_2022-08-05_at_1.43.29_pm.png)

```
# cam look
var minCamVerticalAngle = -90.0		# Limit camera view to straight down.
var maxCamVerticalAngle = 90.0		# Limit camera view to straight up.
var lookSensitivity = 0.5			# How fast camera moves. 'mouse sensitivity'. 

# vectors
var playerVelocity : Vector3 = Vector3() 	# Players Velocity
var mouseDelta : Vector2 = Vector2()			# How much the mouse has moved since last frame refresh.

# player components
onready var camera = get_node("Camera")		# "attach" the camera to access from script.
```
{collapsible="true"}


Add the function to detect mouse movement.

![Screen Shot 2022-08-05 at 1.45.25 pm.png](Screen_Shot_2022-08-05_at_1.45.25_pm.png)

```
# called when an input is detected
func _input (event):
    # did the mouse move?
    if event is InputEventMouseMotion:
        mouseDelta = event.relative
```
{collapsible="true"}


Add the function to rotate the camera to match the mouse movements.

![Screen Shot 2022-08-05 at 1.49.14 pm.png](Screen_Shot_2022-08-05_at_1.49.14_pm.png)

```
# called every frame
func _process (delta):
    # rotate camera along X axis
    camera.rotation_degrees -= Vector3(rad2deg(mouseDelta.y), 0, 0) * lookSensitivity * delta
    # clamp the vertical camera rotation
    camera.rotation_degrees.x = clamp(camera.rotation_degrees.x, minCamVerticalAngle, maxCamVerticalAngle)
  
    # rotate player along Y axis
    rotation_degrees -= Vector3(0, rad2deg(mouseDelta.x), 0) * lookSensitivity * delta
  
    # reset the mouse delta vector
    mouseDelta = Vector2()
```
{collapsible="true"}


At this stage, you can run the game to test the mouse movement. Run the project, click the button on the main menu to play the game, and you should be able to look around your environment.

![2022-08-05 13-50-38.2022-08-05 13_52_09.gif](2022-08-05_13-50-38.2022-08-05_13_52_09.gif)

### Player Movement

Add the `_physics_process` function for player movement. This function can go at the bottom of the `Player.gd` script.

![Screen Shot 2022-08-05 at 2.22.17 pm.png](Screen_Shot_2022-08-05_at_2.22.17_pm.png)

```
# called every physics step
func _physics_process (delta):
    # reset the x and z velocity
    playerVelocity.x = 0
    playerVelocity.z = 0
    var input = Vector2()
    # movement inputs
    if Input.is_action_pressed("player_forward"):
        input.y -= 1
    if Input.is_action_pressed("player_backward"):
        input.y += 1
    if Input.is_action_pressed("player_left"):
        input.x -= 1
    if Input.is_action_pressed("player_right"):
        input.x += 1
    # normalize the input so we can't move faster diagonally
    input = input.normalized()
    # get our forward and right directions
    var forward = global_transform.basis.z
    var right = global_transform.basis.x
    # set the velocity
    playerVelocity.z = (forward * input.y + right * input.x).z * movementSpeed
    playerVelocity.x = (forward * input.y + right * input.x).x * movementSpeed
    # apply gravity
    playerVelocity.y -= gravity * delta
#	print(playerVelocity.y)
    # move the player
    playerVelocity = move_and_slide(playerVelocity, Vector3.UP)
    # jump if we press the jump button and are standing on the floor
    if Input.is_action_pressed("jump") and is_on_floor():
        playerVelocity.y = jumpStrength
```
{collapsible="true"}


Run the game and move around the world.


> At this stage, you may find that some dimensions are not perfect. You may find you need to change one or more of the following options:
> - Camera’s vertical position in the Player Scene.
> - Scale of the floor node.
> - Jump Strength
> - Gravity
> - Etc.
{style="note"}


NOTE: If you change the scale of the floor, you’ll need to delete the Static Body child and recreate it by selecting Mesh→Create Trimesh Static Body.

### Add the Player to the Scene

Open the Scene/s that you wish to add the player to.

Drag the player tscn file into the hierarchy.

![Screen Shot 2022-08-23 at 2.00.47 pm.png](Screen_Shot_2022-08-23_at_2.00.47_pm.png)

Run the game or scene and you should be able to ‘see’ through the cameras ‘eye’.

### Player Run Functionality

To implement a simple run functionality, `Player.gd` can be updated to modify `movementSpeed` based on whether the shift key is held down or not.

First, add a new Input into the Project Settings → Input Map page.

Then add the shift key to that map.

![Screen Shot 2022-10-17 at 10.03.27 am.png](Screen_Shot_2022-10-17_at_10.03.27_am.png)

Open `Player.gd` and find the `_physics_process(delta)` function. Add the following if statement to set `movementSpeed` to change based on the button press.


> The exact speed values can be modified based on the requirements of the game.
{style="note"}

![Screen Shot 2022-10-17 at 10.11.49 am.png](Screen_Shot_2022-10-17_at_10.11.49_am.png)

```
if Input.is_action_pressed("run"):
        movementSpeed = 20
    else:
        movementSpeed = 10
```
{collapsible="true"}

## Reusable Assets

One of the areas of game development that can save you a lot of work in the long run is building assets that you can reuse throughout your game.

For instance, you can build one ‘master’ copy of a traffic light, and then have multiple traffic lights throughout the game, all based on the same asset.

> The added benefit to this is that once you have multiple copies of an asset, if you update the master, then all the copies get updated too.
{style="note"}

This will be demonstrated here by building a segment of wall that can be duplicated and be used to build a complex room structure.

Start by creating a new scene and set the root node to be a 3D Scene.

![Screen Shot 2022-08-25 at 1.52.37 pm.png](Screen_Shot_2022-08-25_at_1.52.37_pm.png)

Rename the node from Spatial to Wall.

![Screen Shot 2022-08-25 at 1.55.41 pm.png](Screen_Shot_2022-08-25_at_1.55.41_pm.png)

Build the mesh of the asset you are building. This part of the process will depend on what you’re developing.

> Anything beyond the simple ‘block’ shapes may require some 3D modelling software, such as Blender, but that’s beyond the scope of this tutorial. If you’re interested in 3D modelling, there are many tutorials available on Youtube.
{style="note"}


For the wall segment, this can be built by creating a CSGBox as a child node of `Wall`.

![Screen Shot 2022-08-25 at 1.58.14 pm.png](Screen_Shot_2022-08-25_at_1.58.14_pm.png)

Change to scale mode to resize the box into the shape that you want.

![Screen Shot 2022-08-25 at 1.59.03 pm.png](Screen_Shot_2022-08-25_at_1.59.03_pm.png)

![Screen Shot 2022-08-25 at 2.00.13 pm.png](Screen_Shot_2022-08-25_at_2.00.13_pm.png)

Save the Scene.

![Screen Shot 2022-08-25 at 2.00.48 pm.png](Screen_Shot_2022-08-25_at_2.00.48_pm.png)

Open the scene that you wish to edit, and drag the `tscn` file you just saved into the position you wish to to be in.

![2022-08-25 14-05-07.2022-08-25 14_06_16.gif](2022-08-25_14-05-07.2022-08-25_14_06_16.gif)

You can duplicate the node and place the duplicates in position.

Save the Scene once completed.

![2022-08-25 14-06-53.2022-08-25 14_09_36.gif](2022-08-25_14-06-53.2022-08-25_14_09_36.gif)

To edit the master, for instance by applying a texture, open the `tscn` file you saved, make changes and save.

Once you save the `tscn` file, the instances are automatically updated in the other scene.

![2022-08-25 14-13-03.2022-08-25 14_17_41.gif](2022-08-25_14-13-03.2022-08-25_14_17_41.gif)


## Bullet Implementation

There are many ways to implement shooting in an FPS (or other type of) game. One method is to use **raycast**s, where the there is an imaginary line drawn from the camera, and seeing what object it hits first (if any).

Another method, which is the focus of this tutorial, is to create projectiles (such as bullets) for the player to shoot. The bullets will hit objects in their direct path, and can cause damage.

> What are the pros and cons of each approach? Why choose one over the other?
{style="note"}

### Bullet Mesh

> This tutorial is going to demonstrate how to create a simple bullet. Your implementation for the model may differ, however the process should be the same.
{style="note"}

Create a new Scene (Scene→New Scene).

Set the Root Node as `Area` by selecting Other Node and search for Area.

![Screen Shot 2022-10-04 at 9.30.46 pm.png](Screen_Shot_2022-10-04_at_9.30.46_pm.png)

Create your bullet model. You can create your own mesh, or you can follow the instructions shown below.

#### Simple Bullet

For a simple bullet shape, this can be done by creating a CSGCylinder and a CSGSphere and manipulating (move and rotate) them into a bullet shape.

![Screen Shot 2022-10-04 at 9.47.38 pm.png](Screen_Shot_2022-10-04_at_9.47.38_pm.png)

Create both of these CSG objects with Union Operation selected

![Screen Shot 2022-10-04 at 9.45.55 pm.png](Screen_Shot_2022-10-04_at_9.45.55_pm.png)

Then place them as children of a `CSGCombiner`. Name the new node as appropriate.

![Screen Shot 2022-10-04 at 9.48.24 pm.png](Screen_Shot_2022-10-04_at_9.48.24_pm.png)

Texture the object as you would normally.

![Screen Shot 2022-10-04 at 9.51.14 pm.png](Screen_Shot_2022-10-04_at_9.51.14_pm.png)

Attach a `CollisionShape` node as a child of the scene root.

![Screen Shot 2022-10-04 at 9.53.33 pm.png](Screen_Shot_2022-10-04_at_9.53.33_pm.png)

With the CollisionShape selected, set the Shape to be Capsule.

![Screen Shot 2022-10-04 at 9.55.49 pm.png](Screen_Shot_2022-10-04_at_9.55.49_pm.png)

Manipulate the Capsule shape so that it completely surrounds the mesh.

![Screen Shot 2022-10-04 at 9.57.32 pm.png](Screen_Shot_2022-10-04_at_9.57.32_pm.png)

Rename the Scene Root as `Bullet`.

![Screen Shot 2022-10-04 at 9.59.07 pm.png](Screen_Shot_2022-10-04_at_9.59.07_pm.png)

Save the scene as `Bullet.tscn`

![Screen Shot 2022-10-04 at 9.50.35 pm.png](Screen_Shot_2022-10-04_at_9.50.35_pm.png)

### Bullet Script

Still in the Bullet scene, attach a new script to the root node (Bullet) and name it `Bullet.gd`.

![Screen Shot 2022-10-04 at 10.00.27 pm.png](Screen_Shot_2022-10-04_at_10.00.27_pm.png)

![Screen Shot 2022-10-04 at 10.00.41 pm.png](Screen_Shot_2022-10-04_at_10.00.41_pm.png)

Aside from `extends Area`, remove the default code, and add two new variables.

`speed` defines how fast the bullet will move through the game.

`damage` is how much damage the bullet can deal out.

> These can be set to whatever values are appropriate.
{style="note"}


> This can be used to allow for different weapons with different bullet speeds and damage.
{style="note"}

![Screen Shot 2022-10-04 at 10.03.35 pm.png](Screen_Shot_2022-10-04_at_10.03.35_pm.png)

```
var speed : float = 30.0
var damage : int = 1
```
{collapsible="true"}

Add code, within the `_process` function to move the bullet instance forward.

![Screen Shot 2022-10-04 at 10.04.26 pm.png](Screen_Shot_2022-10-04_at_10.04.26_pm.png)

```
func _process (delta):
    # move the bullet forwards
    translation += global_transform.basis.z * speed * delta
```
{collapsible="true"}

Save the Script.

Select the root node (Bullet) and change to the Node tab.

![Screen Shot 2022-10-04 at 10.10.15 pm.png](Screen_Shot_2022-10-04_at_10.10.15_pm.png)

Double click on `body_entered`. Press **Connect.**

This code will be used to detect when the bullet instance has collided with another object - when the bullet collider enters another node’s collider.

![Screen Shot 2022-10-04 at 10.13.16 pm.png](Screen_Shot_2022-10-04_at_10.13.16_pm.png)

In order to only destroy objects that need to be destroyed, this code will first check if the other collider has a function called `take_damage` in its script. This means that a script attached to the enemy objects can have that function, and will take damage, however a wall doesn’t need that function, so it won’t be destroyed.

`_on_Bullet_body_entered(body)` executes when the bullet enters another object. If that object has the `take_damage()` function (or method), it will then run that function on the other node, passing the `damage` value.

Also added is the `destroy()` function. This simply deletes the bullet from the game.

This has been added in such a way to allow for future modification as required.

<tabs>
<tab title="Image"><img src="Screen_Shot_2022-10-04_at_10.17.09_pm.png"/></tab>
<tab title="Code">

```
func _on_Bullet_body_entered(body):
    if body.has_method("take_damage"):
        body.take_damage(damage)
        destroy()

func destroy ():
    # destroys the bullet
    queue_free()
```

</tab>
<tab title="Logic">

```mermaid
graph LR
    A[TODO]
    A -- Yes --> B[TODO]
    A -- No --> C[TODO]
```
</tab>
</tabs>



### Automatically deleting the bullet

A potential problem with creating instances of bullets is that the player could create 1000s of bullets that would continue running in the game, flying off into the distance, taking up valuable processing power. A solution for this problem is to automatically delete the bullets after a set time.

In the bullet scene, create a **Timer** child node of the root note

![Screen Shot 2022-10-04 at 10.22.24 pm.png](Screen_Shot_2022-10-04_at_10.22.24_pm.png)

Set the wait time to something appropriate, and Autostart to On.

![Screen Shot 2022-10-04 at 10.22.56 pm.png](Screen_Shot_2022-10-04_at_10.22.56_pm.png)

Change to the Node tab and double-click on the `timeout()` signal.

Set the Receiver Method to `destroy`.

Select Connect.

![Screen Shot 2022-10-04 at 10.26.03 pm.png](Screen_Shot_2022-10-04_at_10.26.03_pm.png)

Save the Bullet Scene.


## Shooting Bullet Instances

> **Prerequisites** - A bullet scene needs to have been created and saved according to the instructions given on this site. If you have created your own method, you will have to adapt this as necessary.
{style="note"}

With the bullet created, the game now needs to be configured to *shoot* the bullet. Initially, this will be done in the player script.

First, the code will need to know **where** to create the bullet instances.

Open `Player.tscn` and create a Spatial node as a child of the Camera. Name it `bulletSpawn`.

![Screen Shot 2022-10-04 at 11.23.07 pm.png](Screen_Shot_2022-10-04_at_11.23.07_pm.png)

In 3d mode, move `bulletSpawn` to be in front of the camera.

> It might take some experimentation to make it look correct during game play. You may need to change the position a number of times.
{style="note"}

![Screen Shot 2022-10-06 at 11.00.35 pm.png](Screen_Shot_2022-10-06_at_11.00.35_pm.png)

Open `[Player.gd](http://Player.gd)` and add the code to preload the bullet and configure the spawn point.

`onready` is a keyword that creates the variable once the scene has been fully loaded.

> Important—the path to the bullet scene and the bulletSpawn point need to be **exactly** as you’ve defined them in your project. If they are named as something else, your code needs to reflect that.
{style="note"}

![Screen Shot 2022-10-04 at 11.22.13 pm.png](Screen_Shot_2022-10-04_at_11.22.13_pm.png)

```
onready var bulletScene = preload("res://Bullet.tscn")
onready var bulletSpawn = get_node("Camera/bulletSpawn")
```
{collapsible="true"}

Add a new variable to keep track of the ammunition the player is carrying.

Set the value to something appropriate for your project.

![Screen Shot 2022-10-04 at 10.55.29 pm.png](Screen_Shot_2022-10-04_at_10.55.29_pm.png)

```
var ammo : int = 15
```

Update `process()` to check to see if the player has pressed the `shoot` input.

![Screen Shot 2022-10-04 at 10.52.25 pm.png](Screen_Shot_2022-10-04_at_10.52.25_pm.png)

```
if Input.is_action_just_pressed("shoot"):
        shoot()
```
{collapsible="true"}

Create a new function - `shoot()`- which will run when the shoot input is detected.


> Change `/Root/Doom` to the name of your root node in the game scene. E.g. `/Root/MainGame`
{style="note"}

![Screen Shot 2022-10-05 at 12.36.51 am.png](Screen_Shot_2022-10-05_at_12.36.51_am.png)

```
func shoot ():
    var bullet = bulletScene.instance()
    get_node("/root/Doom").add_child(bullet)
    bullet.global_transform = bulletSpawn.global_transform
    bullet.scale = Vector3(0.1,0.1,0.1)

    ammo -= 1
```
{collapsible="true"}

Run the game at this stage to test the creation and shooting of bullet instances.

