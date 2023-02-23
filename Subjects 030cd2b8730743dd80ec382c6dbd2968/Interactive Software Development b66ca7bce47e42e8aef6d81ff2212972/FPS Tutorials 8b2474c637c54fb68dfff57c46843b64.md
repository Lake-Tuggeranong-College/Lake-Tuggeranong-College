# FPS Tutorials

# Rapid Development - Main Menu

## Create the Main Menu Scene

Click on the 2D Scene option under Create Root Node.

![Screen Shot 2022-08-05 at 10.31.31 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-05_at_10.31.31_am.png)

Rename the Node “Main Menu”

![Screen Shot 2022-08-05 at 10.32.19 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-05_at_10.32.19_am.png)

Right Click on the Main Menu Node and choose “Create Child Node” and add a Button.

![Screen Shot 2022-08-05 at 10.33.06 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-05_at_10.33.06_am.png)

Set the Text of the button to “Play” or whatever you want.

![Screen Shot 2022-08-05 at 10.33.34 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-05_at_10.33.34_am.png)

Right click on the Button node and choose Attach Script. Change the name of the script to `SceneChange.gd` as this may be used in different circumstances.

![Screen Shot 2022-08-05 at 10.35.42 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-05_at_10.35.42_am.png)

With the button selected, change to the Node tab and double click the `pressed()` signal.

![Screen Shot 2022-08-05 at 10.34.23 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-05_at_10.34.23_am.png)

Select the Button in the list and click Connect.

![Screen Shot 2022-08-05 at 10.37.22 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-05_at_10.37.22_am.png)

Save the Scene as `MainMenu.tscn`.

$* \normalsize \mathcal {\color{black} \colorbox {orange}  {Save, Commit and Push Changes to Github!}}$ 

## Create the Game Scene

Choose Scene→New Scene. And Choose 3D Scene as the root Node.

![Screen Shot 2022-08-05 at 10.43.46 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-05_at_10.43.46_am.png)

Rename the scene node appropriate for your game.

![Screen Shot 2022-08-05 at 10.45.38 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-05_at_10.45.38_am.png)

Save the scene, naming it appropriate to your game.

## Create a Button

<aside>
‼️ You can configure the main menu in any way you want, displaying the button/s wherever you want. These steps just show creating the button and the functionality.

</aside>

Right click on the Main Menu node and create a child Button node.

![Screen Shot 2022-08-15 at 10.32.09 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-15_at_10.32.09_am.png)

Right-click on the button and Attach a Script. Call this script `SceneChange.gd`. This script will be used for any and all scripts where the button changes scenes.

![Screen Shot 2022-08-15 at 10.35.33 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-15_at_10.35.33_am.png)

With the button selected, click on the Node tab, next to the Inspector, and double click on the `pressed(`) signal.

![Screen Shot 2022-08-15 at 10.36.02 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-15_at_10.36.02_am.png)

Make sure Button is selected in the “Connect To script” section. Leave the Receiver Method as is, and just click connect.

![Screen Shot 2022-08-15 at 10.37.35 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-15_at_10.37.35_am.png)

At the top of the script after the `extends` line, add `export(String) var scene_to_load.` 

Change the `pass` line of code to `get_tree().change_scene(scene_to_load)`.

![Screen Shot 2022-08-15 at 10.39.00 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-15_at_10.39.00_am.png)

$* \normalsize \mathcal {\color{black} \colorbox {orange}  {Save, Commit and Push Changes to Github!}}$ 

## Link the Main Menu to the Game Scene.

Open the Main Menu scene.

Right Click on the game scene you just saved in the FileSystem tab and choose Copy Path.

![Screen Shot 2022-08-05 at 10.50.17 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-05_at_10.50.17_am.png)

Paste that Path into the `Scene To Load` field for the Button created earlier.

![Screen Shot 2022-08-05 at 10.51.13 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-05_at_10.51.13_am.png)

## Run the Game

Press the play button to run the game. If this is the first time the project has been run, you’ll be asked to choose a Main Scene. 

If the Main Menu Scene is open, you can just choose Select Current.

If you have another scene open, choose Select, and then double click on the `MainMenu.tscn`.

![Screen Shot 2022-08-05 at 10.54.49 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-05_at_10.54.49_am.png)

<aside>
‼️ If this starting scene needs to be changed later, this can be set in the Project Settings.

![Screen Shot 2022-08-05 at 10.55.43 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-05_at_10.55.43_am.png)

</aside>

## Continue developing the Main Menu

Once the initial configuration is complete (connecting the main menu to the first game scene, you are free to improve the main menu as much as you want. Add `VBoxContainers` and `HBoxContainers` to organise the layout to assist with placement of items. 

Add Headings and graphics.

The Main menu developed can be continued in the future at any stage of the development process.

# First Person Player Scene

As this game is a First Person Shooter, there is no need to create a mesh for the player object, as in game, the player will never see it.

Therefore the player object can be initially created with a simple collider and camera.

There are two main steps to creating the player:

1. Making the player scene, creating nodes etc, and 
2. Coding the functionality.

## The Player Scene

Create a new Scene. 

Create the root node as `KinematicBody`. To do this, click on Other Node and search for `KinematicBody` and choose Create.

Save the scene as `Player.tscn`.

![Screen Shot 2022-08-05 at 12.38.36 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-05_at_12.38.36_pm.png)

Add a child node - CollisionShape.

This will represented the boundaries of the player node in game. It will be used as the players ‘hit box’ (officially the **collider**) to detect collisions - walls, floors, projectiles etc.

![Screen Shot 2022-08-05 at 12.39.42 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-05_at_12.39.42_pm.png)

With the CollisionShape selected, create a new Capsule Shape.

![Screen Shot 2022-08-05 at 12.40.19 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-05_at_12.40.19_pm.png)

Rotate the capsule so it’s vertical (to represent the boundaries of the player).

![Screen Shot 2022-08-05 at 12.41.46 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-05_at_12.41.46_pm.png)

Resize the dimensions of the capsule, but clicking drop down box next to Capsule Shape and choose Edit.

![Screen Shot 2022-08-05 at 12.45.27 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-05_at_12.45.27_pm.png)

Set the Radius and height to values that suit your game.

<aside>
‼️ You may find these values need to be modified later to better suit your game.

</aside>

![Screen Shot 2022-08-05 at 12.46.13 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-05_at_12.46.13_pm.png)

## Camera

The player has been created, however the player cannot ‘see’ as a camera has not been added. The camera is what the user sees in game. In a FPS, the mouse is attached to the player object and therefore the camera. When the mouse moves, the camera moves to match.

Add a Camera child node to the Player node.

![Screen Shot 2022-08-05 at 12.49.30 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-05_at_12.49.30_pm.png)

Set the Environment attribute to the `default_env.tres` already created in the project.

![2022-08-05 12-50-55.2022-08-05 12_51_22.gif](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/2022-08-05_12-50-55.2022-08-05_12_51_22.gif)

Set this camera to be the ‘main’ camera by setting the Current attribute to True.

![Screen Shot 2022-08-05 at 12.54.02 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-05_at_12.54.02_pm.png)

Move the camera up the ‘body’ to appear as if the camera ‘sees’ through the players eyes.

<aside>
‼️ Exact value is not critical, but it has to suit your capsule size set earlier.

</aside>

Only change the `Y` value. This is the vertical value. The coordinate system will be discussed at a later time.

![Screen Shot 2022-08-05 at 12.56.18 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-05_at_12.56.18_pm.png)

## Key Actions

Before any scripting can be done, some keyboard and mouse inputs need to be mapped to actions (to be coded later).

Open Project → Project Settings → Input Map.

Add the following actions and set the keys and mouse inputs as directed.

`player_forward`

`player_backward`

`player_left`

`player_right`

`jump`

`shoot`

<aside>
‼️ Pay close attention to the spelling and capitalisation. These will be linked to in the script later.

</aside>

![Screen Shot 2022-08-05 at 1.25.04 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-05_at_1.25.04_pm.png)

## Mouse Look

Open `Player.tscn`. Right click on the root node and attach a script. Leave the settings as they are, and click Create.

![Screen Shot 2022-08-05 at 1.30.19 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-05_at_1.30.19_pm.png)

Clear out the commented code, and add some variables which will be used later in the script.

These variables defines how fast the player moves and how jumping and gravity impact the players movement.

![Screen Shot 2022-08-05 at 1.33.52 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-05_at_1.33.52_pm.png)

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

Add other variables. These variables define the players movement and camera movement limitations.

![Screen Shot 2022-08-05 at 1.43.29 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-05_at_1.43.29_pm.png)

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

Add the function to detect mouse movement.

![Screen Shot 2022-08-05 at 1.45.25 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-05_at_1.45.25_pm.png)

```
# called when an input is detected
func _input (event):
	# did the mouse move?
	if event is InputEventMouseMotion:
		mouseDelta = event.relative
```

Add the function to rotate the camera to match the mouse movements.

![Screen Shot 2022-08-05 at 1.49.14 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-05_at_1.49.14_pm.png)

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

At this stage, you can run the game to test the mouse movement. Run the project, click the button on the main menu to play the game, and you should be able to look around your environment.

![2022-08-05 13-50-38.2022-08-05 13_52_09.gif](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/2022-08-05_13-50-38.2022-08-05_13_52_09.gif)

## Player Movement

Add the `_physics_process` function for player movement. This function can go at the bottom of the `Player.gd` script.

![Screen Shot 2022-08-05 at 2.22.17 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-05_at_2.22.17_pm.png)

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

Run the game and move around the world.

<aside>
‼️ At this stage, you may find that some of the dimension are not perfect. You may find you need to change one or more of the following options:
Camera’s vertical position in the Player Scene.
Scale of the floor node.
Jump Strength
Gravity
Etc.

</aside>

NOTE: If you change the scale of the floor, you’ll need to delete the Static Body child and recreate it by selecting Mesh→Create Trimesh Static Body.

## Add the Player to the Scene

Open the Scene/s that you wish to add the player to.

Drag the player tscn file into the hierarchy. 

![Screen Shot 2022-08-23 at 2.00.47 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-23_at_2.00.47_pm.png)

Run the game or scene and you should be able to ‘see’ through the cameras ‘eye’.

## Player Run Functionality

To implement a simple run functionality, `[Player.gd](http://Player.gd)` can be updated to modify `movementSpeed` based on whether the shift key is held down or not.

First, add a new Input into the Project Settings → Input Map page.

Then add the shift key to that map.

![Screen Shot 2022-10-17 at 10.03.27 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-10-17_at_10.03.27_am.png)

Open `[Player.gd](http://Player.gd)` and find the `_physics_process(delta)` function. Add the following if statement to set `movementSpeed` to change based on the button press.

<aside>
‼️ The exact speed values can be modified based on the requirements of the game.

</aside>

![Screen Shot 2022-10-17 at 10.11.49 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-10-17_at_10.11.49_am.png)

```arduino
if Input.is_action_pressed("run"):
		movementSpeed = 20
	else:
		movementSpeed = 10
```

# Reusable Assets

One of the areas of game development that can save you a lot of work in the long run is building assets that you can reuse throughout your game.

For instance, you can build one ‘master’ copy of a traffic light, and then have multiple traffic lights throughout the game, all based on the same asset.

<aside>
‼️ The added benefit to this is that once you have multiple copies of an asset, if you update the master, then all the copies get updated too.

</aside>

This will be demonstrated here by building a segment of wall that can be duplicated and be used to build a complex room structure.

Start by creating a new scene and set the root node to be a 3D Scene.

![Screen Shot 2022-08-25 at 1.52.37 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-25_at_1.52.37_pm.png)

Rename the node from Spatial to Wall.

![Screen Shot 2022-08-25 at 1.55.41 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-25_at_1.55.41_pm.png)

Build the mesh of the asset you are building. This part of the process will depend on what you’re developing. 

<aside>
‼️ Anything beyond the simple ‘block’ shapes may require some 3D modelling software, such as Blender, but that’s beyond the scope of this tutorial. If you’re interested in 3D modelling, there are many tutorials available on Youtube.

</aside>

For the wall segment, this can be built by creating a CSGBox as a child node of `Wall`.

![Screen Shot 2022-08-25 at 1.58.14 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-25_at_1.58.14_pm.png)

Change to scale mode to resize the box into the shape that you want.

![Screen Shot 2022-08-25 at 1.59.03 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-25_at_1.59.03_pm.png)

![Screen Shot 2022-08-25 at 2.00.13 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-25_at_2.00.13_pm.png)

Save the Scene. 

![Screen Shot 2022-08-25 at 2.00.48 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-25_at_2.00.48_pm.png)

Open the scene that you wish to edit, and drag the `tscn` file you just saved into the position you wish to to be in.

![2022-08-25 14-05-07.2022-08-25 14_06_16.gif](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/2022-08-25_14-05-07.2022-08-25_14_06_16.gif)

You can duplicate the node and place the duplicates in position.

Save the Scene once completed.

![2022-08-25 14-06-53.2022-08-25 14_09_36.gif](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/2022-08-25_14-06-53.2022-08-25_14_09_36.gif)

To edit the master, for instance by applying a texture, open the `tscn` file you saved, make changes and save. 

Once you save the `tscn` file, the instances are automatically updated in the other scene.

![2022-08-25 14-13-03.2022-08-25 14_17_41.gif](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/2022-08-25_14-13-03.2022-08-25_14_17_41.gif)

# Bullet Implementation

There are numerous ways to implement shooting in an FPS (or other type of) game. One method is to use **raycast**s, where the there is an imaginary line drawn from the camera, and seeing what object it hits first (if any). 

Another method, which is the focus of this tutorial, is to create projectiles (such as bullets) for the player to shoot. The bullets will hit objects in their direct path, and can cause damage.

<aside>
‼️ What are the pros and cons of each approach? Why choose one over the other?

</aside>

## Bullet Mesh

<aside>
‼️ This tutorial is going to demonstrate how to create a simple bullet. Your implementation for the model may differ, however the process should be the same.

</aside>

Create a new Scene (Scene→New Scene).

Set the Root Node as `Area` by selecting Other Node and search for Area.

![Screen Shot 2022-10-04 at 9.30.46 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-10-04_at_9.30.46_pm.png)

Create your bullet model. You can create your own mesh, or you can follow the instructions shown below.

### Simple Bullet

For a simple bullet shape, this can be done by creating a CSGCylinder and a CSGSphere and manipulating (move and rotate) them into a bullet shape.

![Screen Shot 2022-10-04 at 9.47.38 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-10-04_at_9.47.38_pm.png)

Create both of these CSG objects with Union Operation selected

![Screen Shot 2022-10-04 at 9.45.55 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-10-04_at_9.45.55_pm.png)

Then place them as children of a `CSGCombiner`. Name the new node as appropriate.

![Screen Shot 2022-10-04 at 9.48.24 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-10-04_at_9.48.24_pm.png)

Texture the object as you would normally.

![Screen Shot 2022-10-04 at 9.51.14 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-10-04_at_9.51.14_pm.png)

Attach a `CollisionShape` node as a child of the scene root.

![Screen Shot 2022-10-04 at 9.53.33 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-10-04_at_9.53.33_pm.png)

With the CollisionShape selected, set the Shape to be Capsule.

![Screen Shot 2022-10-04 at 9.55.49 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-10-04_at_9.55.49_pm.png)

Manipulate the Capsule shape so that it completely surrounds the mesh.

![Screen Shot 2022-10-04 at 9.57.32 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-10-04_at_9.57.32_pm.png)

Rename the Scene Root as `Bullet`.

![Screen Shot 2022-10-04 at 9.59.07 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-10-04_at_9.59.07_pm.png)

Save the scene as `Bullet.tscn`

![Screen Shot 2022-10-04 at 9.50.35 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-10-04_at_9.50.35_pm.png)

## Bullet Script

Still in the Bullet scene, attach a new script to the root node (Bullet) and name it `Bullet.gd`.

![Screen Shot 2022-10-04 at 10.00.27 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-10-04_at_10.00.27_pm.png)

![Screen Shot 2022-10-04 at 10.00.41 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-10-04_at_10.00.41_pm.png)

Aside from `extends Area`remove the default code, and add two new variables. 

`speed` defines how fast the bullet will move through the game.

`damage` is how much damage the bullet can deal out.

<aside>
‼️ These can be set to whatever values are appropriate.

</aside>

<aside>
‼️ This can be used to allow for different weapons with different bullet speeds and damage.

</aside>

![Screen Shot 2022-10-04 at 10.03.35 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-10-04_at_10.03.35_pm.png)

```python
var speed : float = 30.0
var damage : int = 1
```

Add code, within the `_process` function to move the bullet instance forward. 

![Screen Shot 2022-10-04 at 10.04.26 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-10-04_at_10.04.26_pm.png)

```python
func _process (delta):
	# move the bullet forwards
	translation += global_transform.basis.z * speed * delta
```

Save the Script.

Select the root node (Bullet) and change to the Node tab. 

![Screen Shot 2022-10-04 at 10.10.15 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-10-04_at_10.10.15_pm.png)

Double click on `body_entered`. Press **Connect.**

This code will be used to detect when the bullet instance has collided with another object - when the bullet collider enters another node’s collider.

![Screen Shot 2022-10-04 at 10.13.16 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-10-04_at_10.13.16_pm.png)

In order to only destroy objects that need to be destroyed, this code will first check if the other collider has a function called `take_damage` in its script. This means that a script attached to the enemy objects can have that function, and will take damage, however a wall doesn’t need that function, so it won’t be destroyed.

 `_on_Bullet_body_entered(body)` executes when the bullet enters another object. If that object has the `take_damage()` function (or method), it will then run that function on the other node, passing the `damage` value.

Also added is the `destroy()` function. This simply deletes the bullet from the game.

This has been added in such a way to allow for future modification as required.

![Screen Shot 2022-10-04 at 10.17.09 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-10-04_at_10.17.09_pm.png)

```python
func _on_Bullet_body_entered(body):
	if body.has_method("take_damage"):
		body.take_damage(damage)
		destroy()

func destroy ():
	# destroys the bullet
	queue_free()
```

## Automatically deleting the bullet

A potential problem with creating instances of bullets is that the player could create 1000s of bullets that would continue running in the game, flying off into the distance, taking up valuable processing power. A solution for this problem is to automatically delete the bullets after a set time.

In the bullet scene, create a **Timer** child node of the root note

![Screen Shot 2022-10-04 at 10.22.24 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-10-04_at_10.22.24_pm.png)

Set the wait time to something appropriate, and Autostart to On.

![Screen Shot 2022-10-04 at 10.22.56 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-10-04_at_10.22.56_pm.png)

Change to the Node tab and double-click on the `timeout()` signal. 

Set the Receiver Method to `destroy`.

Select Connect.

![Screen Shot 2022-10-04 at 10.26.03 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-10-04_at_10.26.03_pm.png)

Save the Bullet Scene.

# Shooting Bullets

<aside>
‼️ **Prerequisites** - A bullet scene needs to have been created and saved according to the instructions given on this site. If you have created your own method, you will have to adapt this as necessary.

</aside>

With the bullet created, the game now needs to be configured to *shoot* the bullet. Initially, this will be done in the player script.

First, the code will need to know **where** to create the bullet instances. 

Open `Player.tscn` and create a Spatial node as a child of the Camera. Name it `bulletSpawn`.  

![Screen Shot 2022-10-04 at 11.23.07 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-10-04_at_11.23.07_pm.png)

In 3d mode, move `bulletSpawn` to be in front of the camera. 

<aside>
‼️ It might take some experimentation to make it look correct during game play. You may need to change the position a number of times.

</aside>

![Screen Shot 2022-10-06 at 11.00.35 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-10-06_at_11.00.35_pm.png)

Open `[Player.gd](http://Player.gd)` and add the code to preload the bullet and configure the spawn point.

`onready` is a keyword which creates the variable once the scene has been fully loaded.

<aside>
‼️ Important - the path to the bullet scene and the bulletSpawn point need to be **exactly** as you’ve defined them in your project. If they are named as something else, your code needs to reflect that.

</aside>

![Screen Shot 2022-10-04 at 11.22.13 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-10-04_at_11.22.13_pm.png)

```python
onready var bulletScene = preload("res://Bullet.tscn")
onready var bulletSpawn = get_node("Camera/bulletSpawn")
```

Add a new variable to keep track of the ammunition the player is carrying.

Set the value to something appropriate for your project.

![Screen Shot 2022-10-04 at 10.55.29 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-10-04_at_10.55.29_pm.png)

```python
var ammo : int = 15
```

Update `process()` to check to see if the player has pressed the `shoot` input. 

![Screen Shot 2022-10-04 at 10.52.25 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-10-04_at_10.52.25_pm.png)

```python
if Input.is_action_just_pressed("shoot"):
		shoot()
```

Create a new function - `shoot()`- which will run when the shoot input is detected.

<aside>
‼️ Change `/Root/Doom` to the name of your root node in the game scene. E.g. `/Root/MainGame`

</aside>

![Screen Shot 2022-10-05 at 12.36.51 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-10-05_at_12.36.51_am.png)

```python
func shoot ():
	var bullet = bulletScene.instance()
	get_node("/root/Doom").add_child(bullet)
	bullet.global_transform = bulletSpawn.global_transform
	bullet.scale = Vector3(0.1,0.1,0.1)

	ammo -= 1
```

Run the game at this stage to test the creation and shooting of bullet instances.

# Objects/Enemies Taking Damage

The bullets and enemy have been created, the bullets fire. Now it’s time to put it together - having the enemies take damage. 

Unlike the player’s health, which is a global variable, each enemy (or any other object with health) will have its own health that will need to be diminished for it to be destroyed. 

**Each object or enemy that you wish to take damage needs to be configured in the same way.**

<aside>
‼️

The object taking damage will need to have a Collision Shape configured as a direct child of the root node.

![Screen Shot 2022-10-06 at 10.02.18 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-10-06_at_10.02.18_pm.png)

</aside>

Open the (or attach a) script for the object that you wish to take damage.

Add a simple `take_damage(damage)` function to the script, which simply outputs a test message to ensure that the process works.

![Screen Shot 2022-10-06 at 10.37.49 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-10-06_at_10.37.49_pm.png)

```python
func take_damage(damage):
	print("ouch")
```

Run the game at this stage to test the collision. 

![2022-10-06 23-02-38.2022-10-06 23_04_11.gif](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/2022-10-06_23-02-38.2022-10-06_23_04_11.gif)

<aside>
‼️ You may find it useful to slow the bullets down to properly test, as can be seen in this example.

</aside>

Open the script for the object. Add a `health` variable at the top of the script and set the value to 100.

![Screen Shot 2022-10-06 at 11.14.44 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-10-06_at_11.14.44_pm.png)

```python
var health = 100
```

Update `take_damage()` to reduce the amount of health, and then check if the health has reached zero. If so, then delete the object.

![Screen Shot 2022-10-06 at 11.16.23 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-10-06_at_11.16.23_pm.png)

```python
func take_damage(damage):
	health -= 50
	if health <=0:
		queue_free()
```

Run the project and you should see the object be destroyed as health reaches 0.

![2022-10-06 23-13-27.2022-10-06 23_14_08.gif](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/2022-10-06_23-13-27.2022-10-06_23_14_08.gif)

<aside>
‼️ Remember this process can work for any damageable object in the game - enemies, walls, doors etc.

</aside>

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

![Screen Shot 2022-08-25 at 9.13.24 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-25_at_9.13.24_pm.png)

<aside>
‼️ Simple objects can be modelled in Godot, however to create more complex objects, you would need to use an external 3D modelling piece of software such as Blender. 
For a quick development process, create simple objects that you can quickly texture.

</aside>

When texturing objects, you can use Google Images to search for appropriate textures. If you’re creating an object that requires a repeating texture (like grass on the ground) it is advisable that you search for `<object> texture seamless`, for instance `grass texture seamless` as the images that it offers will not show any edges when tiled next to each other.

Find the images that you wish to texture your object. Import the image into the Godot project.

Select the mesh that you wish to texture.

![Screen Shot 2022-08-25 at 9.23.58 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-25_at_9.23.58_pm.png)

Click the down arrow next to Material and choose New ShaderMaterial.

![Screen Shot 2022-08-25 at 9.24.30 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-08-25_at_9.24.30_pm.png)

Drag the texture file from the file system tab to the Material. The mesh should then be textured with the image.

![2022-08-25 21-25-56.2022-08-25 21_27_22.gif](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/2022-08-25_21-25-56.2022-08-25_21_27_22.gif)

Continue the process until all the meshes in the scene are textured as desired.

# Points Mechanic

## Global Script

Create a new script called `Global.gd` (unless it’s already created).

![Screen Shot 2022-09-06 at 1.59.04 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-06_at_1.59.04_pm.png)

![Screen Shot 2022-09-06 at 1.59.39 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-06_at_1.59.39_pm.png)

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

![End Result](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-06_at_2.10.46_pm.png)

End Result

Click Close.

## Pickup Item

The pickup item can be any object you wish. It could be a simple cube or cylinder or a complex object that you’ve imported from 3D modelling software such as Blender. Regardless of the object itself, the object needs to be saved as it’s own Scene.

In this case, the file is saved as `Pickup.tscn` and there is a cylinder object created.

![Screen Shot 2022-09-06 at 2.14.32 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-06_at_2.14.32_pm.png)

Create child nodes of the original object to include a mesh that the player can collide with.

![Screen Shot 2022-09-06 at 2.15.18 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-06_at_2.15.18_pm.png)

Right Click on the Pickup node and attach a script, named `Pickup.gd`. Save the script. There is no need to change the code at this stage.

![Screen Shot 2022-09-06 at 2.18.05 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-06_at_2.18.05_pm.png)

Select the Area node, and switch to the Node tab.

![Screen Shot 2022-09-06 at 2.16.31 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-06_at_2.16.31_pm.png)

Double click on the Body Entered signal. Make sure the Pickup node is selected and click Connect. 

![Screen Shot 2022-09-06 at 2.18.58 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-06_at_2.18.58_pm.png)

Enter the following code for the `_on_Area_body_entered(body)` function.

This code check to see if the object that collides with the pickup item is the player. If so, it will add 10 points to the `current_score` variable in the Global script.

Then it deletes the pickup item.

![Screen Shot 2022-09-06 at 2.19.59 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-06_at_2.19.59_pm.png)

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

![Screen Shot 2022-09-06 at 2.24.42 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-06_at_2.24.42_pm.png)

```python
$Camera/playerScore.text = str(Global.current_score)
```

# Enemy Pathfinding

## Create an enemy

<aside>
‼️ The enemy mesh (the object that you can see) can be anything you want. This tutorial shows how to create a simple enemy of just a capsule. If you want to have a specific mesh, you may do so, but you will still need to create the other parts of the enemy object creation.

</aside>

Create a new scene (File→ New Scene) and create the root node as a `KinematicBody`. This will be the root node of the enemy object.

![Screen Shot 2022-09-12 at 10.39.19 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-12_at_10.39.19_am.png)

![Screen Shot 2022-09-12 at 10.39.36 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-12_at_10.39.36_am.png)

Rename the node as `Enemy`. 

![Screen Shot 2022-09-12 at 10.39.57 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-12_at_10.39.57_am.png)

Add a `MeshInstance` as a child of `Enemy`.

![Screen Shot 2022-09-12 at 10.40.39 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-12_at_10.40.39_am.png)

Click on the down arrow next to Mesh and choose New CapsuleMesh.

<aside>
‼️ This can be created as whatever type of object you wish, or a custom Mesh.

</aside>

![Screen Shot 2022-09-12 at 10.41.14 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-12_at_10.41.14_am.png)

Rotate the capsule by 90 degrees on the X axis.

![Screen Shot 2022-09-12 at 10.42.27 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-12_at_10.42.27_am.png)

Click on the Mesh preview and then set the Radius and Height.

These can be changed later, but you’ll need to make a note of them for later steps.

![Screen Shot 2022-09-12 at 10.43.35 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-12_at_10.43.35_am.png)

**If you wish**, you can change the colour of the enemy capsule by clicking on New SpatialMaterial in the inspector.

![Screen Shot 2022-09-12 at 10.46.21 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-12_at_10.46.21_am.png)

Under Albedo you can change the colour by clicking on the colour box and using the colour picker to choose the desired colour.

![Screen Shot 2022-09-12 at 10.47.13 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-12_at_10.47.13_am.png)

![Screen Shot 2022-09-12 at 10.47.42 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-12_at_10.47.42_am.png)

Add a Timer node as a child of enemy.

![Screen Shot 2022-09-12 at 10.48.08 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-12_at_10.48.08_am.png)

![Screen Shot 2022-09-12 at 10.48.16 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-12_at_10.48.16_am.png)

Select the enemy in the hierarchy and set the wait time and autostart options.

![Screen Shot 2022-09-12 at 10.48.33 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-12_at_10.48.33_am.png)

Save the scene as `Enemy.tscn`. 

![Screen Shot 2022-09-12 at 10.49.03 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-12_at_10.49.03_am.png)

## Create the Navmesh

<aside>
‼️ Navmesh is a Navigation Mesh that defines what area is traversable by the enemy objects (NPCs) and what is blocking terrain, such as walls, buildings etc.

</aside>

Open the scene for the main game. Add a child node to the scene root. Choose Navigation.

![Screen Shot 2022-09-12 at 10.49.48 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-12_at_10.49.48_am.png)

Create a child node of Navigation. This time choose `NavigationMeshInstance`.

Any children of this `NavigationMeshInstance` will be part of the Navmesh. This means that you need to move any floor or terrain nodes to be a child of this node. This should include most of your environment assets/nodes, including walls, lightposts, pickup items etc. 

![Screen Shot 2022-09-12 at 10.51.41 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-12_at_10.51.41_am.png)

Select the `NavigationMeshInstance` in the hierarchy and create a new **NavigationMesh** under **Navmesh** in the inspector.

![Screen Shot 2022-09-12 at 10.51.54 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-12_at_10.51.54_am.png)

Select **Bake NavMesh** in the tool bar.

You’ll notice that this has a blue highlight to the terrain. This indicates where the enemy objects can move around (traverse). 

![Before Navmesh.](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-12_at_10.52.22_am.png)

Before Navmesh.

![After Navmesh.](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-12_at_10.52.52_am.png)

After Navmesh.

You may also notice that any items that are children of the `NavigationMeshInstance` that are considered too tall, have gaps around the object. This indicates that these areas are **not traversable**.

![Screen Shot 2022-09-12 at 10.54.20 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-12_at_10.54.20_am.png)

Your scene should appear similar to this. All the environment nodes are children of `NavigationMeshInstance`.

![Screen Shot 2022-09-12 at 10.55.25 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-12_at_10.55.25_am.png)

Select `NavigationMeshInstance` in the hierarchy. Select the NavigationMesh in the inspector and set the size and the height of the Cell.

The height needs to be set as half of the enemy height defined when creating the enemy scene.

![Screen Shot 2022-09-12 at 10.56.27 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-12_at_10.56.27_am.png)

Under Agent, set the Height and Radius to match your enemy details.

![Screen Shot 2022-09-12 at 10.57.50 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-12_at_10.57.50_am.png)

Rebake the Navmesh

![Screen Shot 2022-09-12 at 10.59.09 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-12_at_10.59.09_am.png)

Save the Scene. 

$* \normalsize \mathcal {\color{black} \colorbox {orange}  {Save, Commit and Push Changes to Github!}}$ 

## Script the Enemy

Open the enemy scene, Right-click on the root node and choose Attach Script. 

![Screen Shot 2022-09-12 at 11.01.09 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-12_at_11.01.09_am.png)

Define the necessary variables.

| Variable | Purpose |
| --- | --- |
| nav | Stores the link to the Navigation node in the main game scene. |
| path | Array that contains the points the enemy will need to move through to get to the player. |
| path_node | The current index (position) in the path array. |
| speed | The enemies movement speed. This can be changed to whichever speed you wish and is appropriate for your game. |
| player | Links to the Player node in the main game. Important The path indicated needs to match your main game scene and match the node hierarchy.  |

`onready` is defined as - Initializes a variable once the Node the script is attached to and its children are part of the scene tree.

![Screen Shot 2022-09-12 at 11.04.12 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-12_at_11.04.12_am.png)

```python
onready var nav = get_parent()
var path = []
var path_node = 0
var speed = 10
onready var player = $"../../Player"
```

Add the following code to the enemy script.

![Screen Shot 2022-09-12 at 11.07.59 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-12_at_11.07.59_am.png)

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

![Screen Shot 2022-09-12 at 11.08.15 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-12_at_11.08.15_am.png)

Double click on the `timeout()` signal and click **Connect** on the Connect a Signal to a Method popup.

![Screen Shot 2022-09-12 at 11.08.43 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-12_at_11.08.43_am.png)

Add the following code to the new function.

Save the Enemy scene.

![Screen Shot 2022-09-12 at 11.57.42 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-12_at_11.57.42_am.png)

```python
move_to(player.global_transform.origin)
```

Add the Enemy scene to the main game. Add it as a child of the `Navigation` node.

![Screen Shot 2022-09-12 at 11.11.56 am.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-12_at_11.11.56_am.png)

Save the Main Game scene.

$* \normalsize \mathcal {\color{black} \colorbox {orange}  {Save, Commit and Push Changes to Github!}}$ 

Run the Game and your enemy should stalk you.

# Player Health

This stage of the tutorial will demonstrate how to implement a simple health system, where there is a player health and when the enemy collides with the player, the health reduces. As with many other aspects of game development, the exact implementation will depend on the requirements for the project, so apply as necessary.

<aside>
‼️ This process can be applied to ANY object that you wish to reduce the players health when a collision occurs.

</aside>

### Player Script

Open `Global.gd` and add a new variable named `player_health`. Set the initial value to be 100.

Save the file.

![Screen Shot 2022-09-12 at 9.05.32 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-12_at_9.05.32_pm.png)

### Update Enemy

Open `Enemy.tscn` to edit the Enemy scene, adding an `Area` node as a child of the root node. Add a CollisionShape node a child of that one.

![Screen Shot 2022-09-12 at 8.56.53 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-12_at_8.56.53_pm.png)

Select `CollisionShape` and change the shape attribute to a `CapsuleShape`.

![Screen Shot 2022-09-12 at 8.58.22 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-12_at_8.58.22_pm.png)

Select Area in the hierarchy, change to the Node tab, and double click on `body_entered()` in the list of signals.

![Screen Shot 2022-09-12 at 8.59.56 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-12_at_8.59.56_pm.png)

Click Connect.

![Screen Shot 2022-09-12 at 9.02.37 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-12_at_9.02.37_pm.png)

Replace the contents of the function with the code shown.

This code checks first if the object the enemy has collided with is the player, and if so, reduce  `player_health` by 10. Then delete the enemy object from the game.

<aside>
‼️ The exact value the health gets reduced by can be set to whatever value you chose. Just change the 10.

</aside>

![Screen Shot 2022-09-12 at 9.06.39 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-12_at_9.06.39_pm.png)

```python
if (body.name == "Player"):
		Global.player_health -= 10
		queue_free()
```

Save the Enemy script.

### Lose Scene

If not already done, create a new scene and save it as `Lose.tscn`. This scene will be loaded if the player has lost, or in this example, run out of health.

Design the scene in whichever way you wish, just ensure there is a way for the user to return to the main menu.

### Update Player Script

Open the Player script (`Player.gd`) and add the code to the end of the `_process()` function.

![Screen Shot 2022-09-12 at 9.42.29 pm.png](FPS%20Tutorials%208b2474c637c54fb68dfff57c46843b64/Screen_Shot_2022-09-12_at_9.42.29_pm.png)

```python
if Global.player_health <= 0:
		print("Dead")
		get_tree().change_scene("res://Lose.tscn")
```

$* \normalsize \mathcal {\color{black} \colorbox {orange}  {Save, Commit and Push Changes to Github!}}$