# Content

## Core Game Tutorials

### Project Configuration
<video src="https://youtu.be/MyH6Ddp60qg"/>


In this video you are shown how to configure a 2D project in Godot, and introduced to the various parts of the
interface.

### **Import image assets**

[https://youtu.be/J8wTFEexpBI](https://youtu.be/J8wTFEexpBI)

This link contains the images you'll need to start the clone of Space
Invaders: [2D Assets](https://drive.google.com/file/d/10LKQkemkH1q27rAZUYc9Sa900K2EIZi9/view?usp=sharing)

### Main menu - Initial

[https://youtu.be/DyaKLWr502M](https://youtu.be/DyaKLWr502M)

#### Part 1 - Main Menu Setup

In this video, you'll see how to configure the project window size and colour as well as start the layout of the menu.

You'll see how to add images into the scene as well as a label, with a brief introduction on how to layout these items.

[https://youtu.be/CBA3sxDbgog](https://youtu.be/CBA3sxDbgog)

#### Main Menu Buttons

This video focuses on the Buttons the title scene. You'll see how to create the buttons, and modify the fonts to match
the title font, and then change the font of all the buttons to a new font.

## Buttons

### Main Menu Buttons Functionality

[https://youtu.be/QH_5xVreQ-w](https://youtu.be/QH_5xVreQ-w)

In this video, you're shown one way of changing between scenes.

You're shown a number of aspects to the process:

- Creating the new Scene
- Creating scripts for the buttons to store the scene names
- Reusing the script between buttons and scenes
- Writing a script to manage all the buttons in the scene
- Parts of programming, such as loops, functions and arrays.

The code used in this video is:


```python
extends Control

# Called when the node enters the scene tree for the first time.
func _ready():
    for button in $"Menu/Menu Buttons/Buttons".get_children():
        button.connect("pressed", self, "_on_Button_pressed", [button.scene_to_load])

func _on_Button_pressed(scene_to_load):
    print("Changing Scene...")
    print(scene_to_load)
    get_tree().change_scene(scene_to_load)
```
{collapsible="true" collapsed-title="TitleScene.gd"}


```python
extends Button

export(String) var scene_to_load
```
{collapsible="true" collapsed-title="ButtonScript.gd"}



```python
extends Control

# Called when the node enters the scene tree for the first time.
func _ready():
    for button in $"Layout/Main/Buttons/GameScenes".get_children():
        button.connect("pressed", self, "_on_Button_Pressed", [button.scene_to_load])

func _on_Button_Pressed(scene_to_load):
    print(scene_to_load)
    get_tree().change_scene(scene_to_load)
```
{collapsible="true" collapsed-title="MainGame.gd"}

## Gameplay

### Game Play

[https://www.youtube.com/watch?v=nQfOhc6jumE](https://www.youtube.com/watch?v=nQfOhc6jumE)

This video shows the process of designing and coding the fundamental gameplay of space invaders.

### Border Containment

[https://youtu.be/ef0R6-4viOA](https://youtu.be/ef0R6-4viOA)

In this video, you're shown how to create (invisible) borders on the left and right of the screen using Area2D nodes,
and assigning them groups.

Then, the player object is modified to add it's own Area2D so that you can detect collisions between the object and the
newly created borders.

Finally, you're shown the code to restrict the player to the playing area between the two borders.

### Global Variables & Bullets

[https://youtu.be/cYXn_vcRRTk](https://youtu.be/cYXn_vcRRTk)

In this video you're shown how to create global variables. Global Variables can be accessed (used) by any script
throughout the entire project, from any script. This can be used to keep track of many variables needed throughout the
project, such as the high score, or in the case of this video - the limiting the number of bullets on screen at once.

bullet.gd

```
extends KinematicBody2D

var speed = 500

# Called when the node enters the scene tree for the first time.
func _ready():
    GlobalVariables.bulletInstanceCount += 1
    set_physics_process(true)

func _physics_process(delta):
    var collidedObject = move_and_collide(Vector2(0, -speed*delta))
    if (collidedObject):
        #print(collidedObject.collider.name)
        if "Enemy" in collidedObject.collider.name:
            collidedObject.get_collider().queue_free()
        
            
        
        queue_free()
        GlobalVariables.bulletInstanceCount -= 1
```

## Enemies

### Enemy Group Movement

[https://youtu.be/Hav91wHl3JA](https://youtu.be/Hav91wHl3JA)

In this video, you're shown how to group the enemy instances together and script them to "bounce" off the sides of the
game window when the first collision occurs.

- Enemies.gd

```python
extends Node2D

var speed = -200

func _ready():
    set_physics_process(true)
    
    
func _physics_process(delta):
    global_position.x += speed * delta
```

### Enemies Firing

[https://youtu.be/9XiSX3SM428](https://youtu.be/9XiSX3SM428)

In this first video, you're shown the configuration of the enemy bullets, and walked through the changes that need to be
made to the `global.gd`, `enemy.gd` scripts and the creation of the `enemy-bullets.gd` script.

Bullet-enemy.gd

```
extends KinematicBody2D

var speed = 500

# Called when the node enters the scene tree for the first time.
func _ready():
    GlobalVariables.enemyBulletInstanceCount += 1
    set_physics_process(true)

func _physics_process(delta):
    var collidedObject = move_and_collide(Vector2(0, +speed*delta*0.4))
    if (collidedObject):
        #print("Enemy collide: ",collidedObject.collider.name)
        if "Enemy" in collidedObject.collider.name:
            pass
            #collidedObject.get_collider().queue_free() #Don't kill the enemies.
        else:
            queue_free()
            GlobalVariables.enemyBulletInstanceCount -= 1
            print("Enemy Bullets: ", GlobalVariables.enemyBulletInstanceCount)
```

Enemy.gd

```
extends KinematicBody2D

var bullet = preload("res://Bullet-Enemy/Bullet-Enemy.tscn")

    
func _ready():
    $Area2D.connect("area_entered", self, "_colliding")
    

func _colliding(area):
    if area.is_in_group("right"):
        #print("emenies collide right")
        get_parent().global_position.y += 10
        get_parent().speed = -200
    if area.is_in_group("left"):
        #print("emenies collide left")
        get_parent().global_position.y += 10
        get_parent().speed = 200

func _process(delta):
#	while (true):
    var rng = RandomNumberGenerator.new()
    rng.randomize()
    var my_random_number = rng.randf_range(2.0, 30.0)
    #print("time: ",my_random_number)
    yield(get_tree().create_timer(my_random_number), "timeout")
    if GlobalVariables.enemyBulletInstanceCount < 5:
        var bulletInstance = bullet.instance()
        
        bulletInstance.position = Vector2(global_position.x, global_position.y+20)
        get_tree().get_root().add_child(bulletInstance)
```

Global.gd

```
extends Node

var bulletInstanceCount = 0 # Keeps track of how many bullet instances are current
var enemyBulletInstanceCount = 0
```

## Project Finalisation

### Quit Game Application

[https://youtu.be/eNWupsu4DWI](https://youtu.be/eNWupsu4DWI)

This video shows how to modify the main menu to include a quit button. With a bonus debugging session at the end!


> FYI, there is no audio on this video
> {style="tip"}

## Audio

[https://youtu.be/wKs7a6RBfaw](https://youtu.be/wKs7a6RBfaw)

In this video you're shown how to add background music in a scene and also "event-based" music - in this case, adding
sound to the firing of bullets.

## High Score System

### High Score

To store high scores the data needs to be saved to the local drive - this is known as persistent data (the data persists
even if the application is not running).

Before implementing any form of persistent data, the exact data that needs to be save must be determined. The points
where the data is loaded from and saved to the local drive must be decided.

Your application must also be prepared for attempting to load the data, however it doesn’t exist at that time - such as
when the application is run for the first time.

Godot has an inbuilt system to save data and nodes to the local drive, however this tutorial will focus on only saving
and loading the previous high scores.

Before implementing persistent data, there are a few topics to understand - where the user data is stored and
serialisation.

### Godot User Data

Most file access performed in Godot begins with `res://` (e.g. `res://Menu/Menu.tscn`), which refers to the project root
folder (the folder containing `project.godot`). A file path starting with `res://` looks for the file relative to that
root folder.

User data uses the `user://` prefix which points to a different folder which is not in the project folder.

> The`user://`prefix points to a different directory on the user's device. On mobile and consoles, this path is unique
> to the project. On desktop, the engine stores user files in:
`~/.local/share/godot/app_userdata/[project_name]` on
> Linux,`~/Library/Application Support/Godot/app_userdata/[project_name]` on macOS (since Catalina)
> and  APPDATA \Godot\app_userdata\[project_name] on Windows.
[https://docs.godotengine.org/en/stable/tutorials/io/data_paths.html](https://docs.godotengine.org/en/stable/tutorials/io/data_paths.html)
>
{style="note"}

### Serialisation

Serialisation is the process of preparing data and objects to save to disk or transmitted.

### Testing!

Testing the high score system and the saving and loading of data can be frustrating as the tester needs to try for
different scores to ensure that the rank order is correct.

One method for improving this process is to add a cheat code into the game.

For instance, in the `Player.gd` script, the script can be updated to check if the user presses the Up key. If so, this
changes the scene straight to the win scene.s

![Screen Shot 2022-04-30 at 11.34.35 pm.png](Screen_Shot_2022-04-30_at_11.34.35_pm.png)

Code

```python
if Input.is_action_pressed("ui_up"):
        get_tree().change_scene("res://WinScene.tscn")
```

## High Scores

Currently, the game may have a simple scoring system, with only the currentScore being used.

This will be expanded upon by implementing not only a highScore variable as shown, but also the top 3 scores, as well as
the current players score.


> Note: the players name is not within the scope of the tutorial at this stage. If you wish to implement this, you will
> need to track the names as well, collecting the data within your game.
> {style="note"}

```python
var scoringInformation = {
	"currentScore": 0,
	"currentPlayer": "User",
	"highScore": 0,
	"highScorePlayersName" : "Winner"
}
```

### Global.gd

Start by expanding `scoringInformation` to track the first, second and third top scores. This is done in Global.gd.

The starting values for each can be 0. As each player completes the game, their score will be compared to the top score,
and if greater, then shift the values down.

This is implemented through an array. The first element is the highest score, and down from there.

```python
var scoringInformation = {
	"currentScore": 0,
	"currentPlayer": "User",
	"highScores": [0,0,0],
	"highScorePlayersName" : "Winner"
}
```

### Win Scene

When the player wins the game, the Win Scene is loaded. It will be at this point that their score (stored
in `scoringInformation`) will be compared to the high scores.

If your win Scene doesn’t have a script attached

Add a script to the root node by right-clicking on it and choosing Attach Script. Choose the default settings.

![Screen Shot 2022-04-30 at 10.22.57 pm.png](Screen_Shot_2022-04-30_at_10.22.57_pm.png)

Remove the unnecessary code, leaving only the extends command on the first line, and `func _ready()` function.

![Screen Shot 2022-04-30 at 10.24.59 pm.png](Screen_Shot_2022-04-30_at_10.24.59_pm.png)

Update the _ready() function to store the current players score into the array in the correct position, if necessary.

![Screen Shot 2022-04-30 at 11.20.04 pm.png](Screen_Shot_2022-04-30_at_11.20.04_pm.png)


```python
func _ready():
    # Sorts the array
    GlobalVariables.scoringInformation["highScores"].sort()
    
    # Searches the array for the value, or the position in the array where it will "fit".
    var highScorePosition = GlobalVariables.scoringInformation["highScores"].bsearch(GlobalVariables.scoringInformation["currentScore"], true)
    print("position #", highScorePosition)
    
    # Inserts the value into the array at the correct position.
    GlobalVariables.scoringInformation["highScores"].insert(highScorePosition, GlobalVariables.scoringInformation["currentScore"])
    
    # Removes the first (and lowest) score.
    GlobalVariables.scoringInformation["highScores"].remove(0)
    
    # Debugging.
    print(GlobalVariables.scoringInformation["highScores"])
```

The high score system has been implemented!

<include from="reusableContent.topic" element-id="commitPush"/>

## Persistent Data

In this tutorial, you’ll be shown how to save and load the `scoringInformation` dictionary.

> In this tutorial, only a small amount of data will be saved and loaded, so not a lot of focus on serialisation is done. However if the game requires saving more complex data, you will need to ensure this is done.
{style="tip"}

Open [Global.g](http://Global.gs)d and create a new global variable which sets the save file.

![Screen Shot 2022-05-01 at 12.24.52 am.png](Screen_Shot_2022-05-01_at_12.24.52_am.png)

Code

```python
var saveFile = "user://save.dat"
```

### Saving the data

To ensure it’s saved when it is updated, the saving of high score data can be done in the Win Scene.

Open `WinScene.gd` and create a new function called `saveData()`.

![Screen Shot 2022-05-01 at 12.20.42 am.png](Screen_Shot_2022-05-01_at_12.20.42_am.png)

Code

```python
func saveData():
```

Update `saveData()` to attempt to access the file name specified in `Global.gd` called `saveFile`. If there is no issues
with that file, it will write the scoringInformation dictionary to the file and close the connection.

![Screen Shot 2022-05-01 at 12.25.56 am.png](Screen_Shot_2022-05-01_at_12.25.56_am.png)

Code

```python
func saveData():
    var file = File.new()
    var error = file.open(GlobalVariables.saveFile, file.WRITE)
    if error == OK:
        file.store_var(GlobalVariables.scoringInformation)
        file.close()
        print("!!Data Saved!!")
    else :
        print("!!Data Not Saved!!")
```

Lastly, update the `_ready()` function to call the `saveData()` function.

![Screen Shot 2022-05-01 at 12.33.02 am.png](Screen_Shot_2022-05-01_at_12.33.02_am.png)

### Loading the Data

Open the main menu and look at the script for the scene - `Menu.gd`.

Update the `_ready()` function to load (or attempt to load) the saved data.

This code checks to see if the file exists first - applications don’t like attempting to open files that don’t exist.

If the file is there, it replaces the `scoringInformation` data that’s coded by default with the loaded data. If there
is any error, it just leaves the default values.

![Screen Shot 2022-05-01 at 12.34.49 am.png](Screen_Shot_2022-05-01_at_12.34.49_am.png)

Code

```python
var file = File.new()
    if file.file_exists(GlobalVariables.saveFile):
        var error = file.open(GlobalVariables.saveFile, File.READ)
        if error == OK:
            var player_data = file.get_var()
            file.close()
            GlobalVariables.scoringInformation = player_data
```

<include from="reusableContent.topic" element-id="commitPush"/>

## Bug or Feature?

There’s a bug with the saving and loading of `scoringInformation`. Did you notice? It’s got to do with currentScore -
it’s not resetting correctly and is saving the current score in the save file.


## Win & Lose Conditions

The Win and Lose conditions refer to the state of gameplay to determine whether the player “wins” the game or “loses”
the game. Those states are determined by the game itself and what occurs after is up to the developer.

Some examples could be:

- Win Condition
    - All enemies are killed
    - The door at the end of the level is opened
    - The player survives the night
    - etc.
- Lose Condition
    - The player’s health reaches 0.
    - The player runs out of ammunition.
    - etc.

In our clone of space invaders, the following conditions exist (at a minimum)

| Win Condition/s          | Lose Condition/s               |
|--------------------------|--------------------------------|
| All enemies are defeated | The timer reaches 0.           |
|                          | The player’s health reaches 0. |

### Win Condition

Expand each of the following to implement the different conditions.

#### All Enemies are Defeated

Open `MainGame.tscn`, and click on the “Open in Editor” button next to one of the individual enemy nodes.

![Screen Shot 2022-04-30 at 10.30.47 pm.png](Screen_Shot_2022-04-30_at_10.30.47_pm.png)

This opens the original scene to edit. All of the individual enemies in the game are based on this one scene.

With the root node selected, click on the Node tab, then click on Groups. Enter “enemy” and click Add.

![Screen Shot 2022-04-30 at 10.31.40 pm.png](Screen_Shot_2022-04-30_at_10.31.40_pm.png)

Save the scene. This adds this tag to each individual enemy.

Return to Main Game.

Open `MainGame.gd`, and in the `_process()` function, check if there are no more nodes with the tag enemy left. If there
are none, then go to the Win Scene.

```python
func _process(delta):
	$HUD/CurrentScore.text = str(GlobalVariables.scoringInformation["currentScore"])
	if get_tree().get_nodes_in_group("enemy").size() == 0:
		get_tree().change_scene("res://WinScene.tscn")
```

Change `res://WinScene.tscn` to link to the Win Scene in your project.

### Lose Condition

Expand each of the following to implement the different conditions.

#### The Timer Reaches 0

To implement this condition check, open the MainGame.gd script and look in the _ready() function.

![Screen Shot 2022-04-26 at 11.18.58 pm.png](Screen_Shot_2022-04-26_at_11.18.58_pm.png)

If Line 17 is reached, it outputs `Game Over` to the console, which means the timer has reached 0. This is where the
code will need to go to make it perform a function. Luckily the condition check has already been performed!

Create a New Scene through the `Scene` Menu

![Screen Shot 2022-04-26 at 11.21.23 pm.png](Screen_Shot_2022-04-26_at_11.21.23_pm.png)

Choose Node2D in the hierarchy tab to start the scene, and then Right Click on the Node2D and choose `Add Child Node`.

![Screen Shot 2022-04-26 at 11.21.40 pm.png](Screen_Shot_2022-04-26_at_11.21.40_pm.png)

Search for, and add, a VBoxContainer

![Screen Shot 2022-04-26 at 11.21.57 pm.png](Screen_Shot_2022-04-26_at_11.21.57_pm.png)

Rename the VboxContainer as Layout. Right click on that, and choose Add Child Node.

![Screen Shot 2022-04-26 at 11.22.15 pm.png](Screen_Shot_2022-04-26_at_11.22.15_pm.png)

This time, search for and add a Label

![Screen Shot 2022-04-26 at 11.22.25 pm.png](Screen_Shot_2022-04-26_at_11.22.25_pm.png)

Rename the Label as Heading, and then change the text attribute to “You Lost” or anything else appropriate.

![Screen Shot 2022-04-26 at 11.22.52 pm.png](Screen_Shot_2022-04-26_at_11.22.52_pm.png)

Now add a button as a child of the VboxContainer called Layout.

![Screen Shot 2022-04-26 at 11.23.21 pm.png](Screen_Shot_2022-04-26_at_11.23.21_pm.png)

Change the text to `Return to the Main Menu,` or anything else appropriate.

![Screen Shot 2022-04-26 at 11.23.42 pm.png](Screen_Shot_2022-04-26_at_11.23.42_pm.png)

Right-click on the button in the heirarchy and choose `Attach Script`.

![Screen Shot 2022-04-26 at 11.24.26 pm.png](Screen_Shot_2022-04-26_at_11.24.26_pm.png)

Don’t change any of the defaults and just click Create.

![Screen Shot 2022-04-26 at 11.24.32 pm.png](Screen_Shot_2022-04-26_at_11.24.32_pm.png)

With the button selected, switch to the Node tab as shown.

![Screen Shot 2022-04-26 at 11.23.57 pm.png](Screen_Shot_2022-04-26_at_11.23.57_pm.png)

Double click on the `pressed` signal.

![Screen Shot 2022-04-26 at 11.24.14 pm.png](Screen_Shot_2022-04-26_at_11.24.14_pm.png)

Don’t change anything here - just click `Connect`.

![Screen Shot 2022-04-26 at 11.24.49 pm.png](Screen_Shot_2022-04-26_at_11.24.49_pm.png)

Change the script to the code shown below.

```python
func _on_Button_pressed():
	get_tree().change_scene("res://Menu/Menu.tscn")
```

> Note that the `res://Menu/Menu.tscn` may need to be modified to match your project. It needs to be the path to *your* main menu scene.
{style="note"}

![Screen Shot 2022-04-26 at 11.25.18 pm.png](Screen_Shot_2022-04-26_at_11.25.18_pm.png)

![Screen Shot 2022-04-26 at 11.25.27 pm.png](Screen_Shot_2022-04-26_at_11.25.27_pm.png)

Save the Scene.

![Screen Shot 2022-04-26 at 11.25.45 pm.png](Screen_Shot_2022-04-26_at_11.25.45_pm.png)

Go back to MainMenu.gd and after the print("Game Over") code, you will need to add the following:

```python
get_tree().change_scene("res://LoseScene.tscn")
```

> Remember the scene linked will need to match *your* project. Change `res://LoseScene.tscn` to whatever you need to link it to the scene you just created.
{style="note"}

### The Player’s Health Reaches 0.

## User Interface Improvements

Create the Main Menu Interface.


### Main Menu

#### **Part 1 - Menu Setup**

[https://youtu.be/DyaKLWr502M](https://youtu.be/DyaKLWr502M)

In this video, you'll see how to configure the project window size and colour as well as start the layout of the menu.

You'll see how to add images into the scene as well as a label, with a brief introduction on how to layout these items.

#### **Part 2**

[https://youtu.be/CBA3sxDbgog](https://youtu.be/CBA3sxDbgog)

In this video, you'll create the "AppInfo" section of the title screen, including the version number, developer and high
score information.

You'll also learn briefly about "Size Flags" to layout the App Info section, expanding labels to fill additional space
on screen.

#### **Part 3**

[https://youtu.be/PxyPHJmNflI](https://youtu.be/PxyPHJmNflI)

This video focuses on the Buttons the title scene. You'll see how to create the buttons, and modify the fonts to match
the title font, and then change the font of all the buttons to a new font.

### Buttons Functionality

[https://youtu.be/QH_5xVreQ-w](https://youtu.be/QH_5xVreQ-w)

Code - TitleScene.gd

```python
extends Control

# Called when the node enters the scene tree for the first time.
func _ready():
    for button in $"Menu/Menu Buttons/Buttons".get_children():
        button.connect("pressed", self, "_on_Button_pressed", [button.scene_to_load])

func _on_Button_pressed(scene_to_load):
    print("Changing Scene...")
    print(scene_to_load)
    get_tree().change_scene(scene_to_load)
```

Code - ButtonScript.gd

```python
extends Button

export(String) var scene_to_load
```

Code - MainGame.gd

```python
extends Control

# Called when the node enters the scene tree for the first time.
func _ready():
    for button in $HUD.get_children():
        button.connect("pressed", self, "_on_Button_pressed", [button.scene_to_load])

func _on_Button_pressed(scene_to_load):
    print("Changing Scene...")
    print(scene_to_load)
    get_tree().change_scene(scene_to_load)
```

In this video, you're shown one way of changing between scenes.

You're shown a number of aspects to the process:

- Creating the new Scene
- Creating scripts for the buttons to store the scene names
- Reusing the script between buttons and scenes
- Writing a script to manage all the buttons in the scene
- Parts of programming, such as loops, functions and arrays.

## Options Implementation

### Scene Creation

With the Space Invaders project open, Create a new scene.

![Screen Shot 2022-04-29 at 12.55.39 pm.png](Screen_Shot_2022-04-29_at_12.55.39_pm.png)

When the choice appears, choose User Interface out of the four options.

> It is possible to also create it as a 2D Scene.
{style="note"}

![Screen Shot 2022-04-29 at 12.55.47 pm.png](Screen_Shot_2022-04-29_at_12.55.47_pm.png)

Rename the scene `OptionsMenu`.

![Screen Shot 2022-04-29 at 12.56.52 pm.png](Screen_Shot_2022-04-29_at_12.56.52_pm.png)

Add a VBoxContainer node as a child of `OptionsMenu`. Rename the node as `Layout`

![Screen Shot 2022-04-29 at 12.57.33 pm.png](Screen_Shot_2022-04-29_at_12.57.33_pm.png)

Create a CheckButton node as a child of Layout. Rename this to `RapidFireSelect`.

![Screen Shot 2022-04-29 at 12.58.40 pm.png](Screen_Shot_2022-04-29_at_12.58.40_pm.png)

Set the text property of this box to Rapid Fire.

![Screen Shot 2022-04-29 at 1.41.12 pm.png](Screen_Shot_2022-04-29_at_1.41.12_pm.png)

As another child of `Layout`, create a Button, renamed to `ReturnToMainMenu`.

![Screen Shot 2022-04-29 at 1.06.59 pm.png](Screen_Shot_2022-04-29_at_1.06.59_pm.png)

Set the text property of `ReturnToMainMenu` button to “Return to the Main Menu”

![Screen Shot 2022-04-29 at 1.34.08 pm.png](Screen_Shot_2022-04-29_at_1.34.08_pm.png)

Save the Scene as OptionsMenu, saving it in a folder called Options in the root of the project.

![Screen Shot 2022-04-29 at 1.00.48 pm.png](Screen_Shot_2022-04-29_at_1.00.48_pm.png)

At the end of this process, your Scene and FileSystem should appear similar to this.

![Screen Shot 2022-04-29 at 1.02.06 pm.png](Screen_Shot_2022-04-29_at_1.02.06_pm.png)

#### Button Functionality

To quickly add the functionality to the single `ReturnToMainMenu` button in the scene, you can add a function to run
with the button is pressed.

Right-click on the `ReturnToMainMenu` button and choose Attach Script.

![Screen Shot 2022-04-29 at 1.16.55 pm.png](Screen_Shot_2022-04-29_at_1.16.55_pm.png)

Leave the settings and just click Create.

![Screen Shot 2022-04-29 at 1.17.05 pm.png](Screen_Shot_2022-04-29_at_1.17.05_pm.png)

Leave the script for the moment, and select the `ReturnToMainMenu` button in the hierarchy. Change to the Node options
and double click on the Pressed() signal.

![Screen Shot 2022-04-29 at 1.11.17 pm.png](Screen_Shot_2022-04-29_at_1.11.17_pm.png)

The Connect a Signal to a Method dialog appears. Leave all the values as is, and click Connect. This will take you back
to the script with a new function created.

![Screen Shot 2022-04-29 at 1.20.55 pm.png](Screen_Shot_2022-04-29_at_1.20.55_pm.png)

Change the pass command to the code shown, Godot will assist you by showing a menu with all the scenes. Choose your Main
Menu scene from the list.

`get_tree().change_scene(`

![2022-04-29 13-22-37.2022-04-29 13_23_16.gif](2022-04-29_13-22-37.2022-04-29_13_23_16.gif)

#### Link from the Main Menu

Open the main menu scene.

![Screen Shot 2022-04-29 at 1.29.44 pm.png](Screen_Shot_2022-04-29_at_1.29.44_pm.png)

Right-Click on the `OptionsMenu.tscn` and choose Copy Path.

![Screen Shot 2022-04-29 at 1.28.38 pm.png](Screen_Shot_2022-04-29_at_1.28.38_pm.png)

Select the Options Button in the hierarchy and set the Scene To Load variable in the Inspector to the path to the
options menu.

![Screen Shot 2022-04-29 at 1.31.07 pm.png](Screen_Shot_2022-04-29_at_1.31.07_pm.png)

#### Test the Buttons

Run the project, and check to make sure you can navigate from the Main Menu to the Options menu and back again.

![2022-04-29 13-35-40.2022-04-29 13_36_03.gif](2022-04-29_13-35-40.2022-04-29_13_36_03.gif)

### Rapid Fire Implementation

#### Global Variable

Open Global.gd and create a new variable called rapidFire and set it to `false`.

```python
var rapidFire = false
```

Save the script.

![Screen Shot 2022-04-29 at 1.48.24 pm.png](Screen_Shot_2022-04-29_at_1.48.24_pm.png)

#### Options Menu functionality

Now that the scene has been created, successfully linked and the global variable set, it’s now time to implement the
Rapid Fire option.


> Remember: This can be done for any option that will be used throughout the game. For instance, this could be used to set the difficulty setting, audio volume etc.
{style="note"}

Open the OptionsMenu Scene.

Right click on RapidFireSelect and choose Attach Script.

![Screen Shot 2022-04-29 at 1.41.57 pm.png](Screen_Shot_2022-04-29_at_1.41.57_pm.png)

Leave the settings on the dialog box and choose Create.

You do not need to make any changes to the code at this stage.

![Screen Shot 2022-04-29 at 1.42.11 pm.png](Screen_Shot_2022-04-29_at_1.42.11_pm.png)

With the button selected, change to the Node view and double click on the toggled signal.

![Screen Shot 2022-04-29 at 1.52.02 pm.png](Screen_Shot_2022-04-29_at_1.52.02_pm.png)

Leave all the settings as default and click on the Connect button.

![Screen Shot 2022-04-29 at 1.52.08 pm.png](Screen_Shot_2022-04-29_at_1.52.08_pm.png)

The default code is created.

![Screen Shot 2022-04-29 at 1.53.34 pm.png](Screen_Shot_2022-04-29_at_1.53.34_pm.png)

Replace the pass code with code to set the `rapidFire` variable in the Global script.


> This code works because the value that the check button is set to (on or off) equates to `true` or `false` which can set the rapidFire value in the global script.
{style="note"}

![Screen Shot 2022-04-29 at 1.54.52 pm.png](Screen_Shot_2022-04-29_at_1.54.52_pm.png)

```python
GlobalVariables.rapidFire = button_pressed
```

#### Using the Options

This has now completed this section as the collection and storage of the options through the menu. The next stage is to
use this within the rest of the game.

In this case, the `rapidFire` variable can be used in the Player.gd script to modify the functionality for the firing
process.

Code

```python
func _process(delta):
    if GlobalVariables.rapidFire:
        if Input.is_action_pressed("fire"):
            var bulletInstance = bulletSource.instance()
            bulletInstance.position = Vector2(position.x, position.y-20)
            get_tree().get_root().add_child(bulletInstance)
    else:
        if Input.is_action_just_pressed("fire"):
            var bulletInstance = bulletSource.instance()
            bulletInstance.position = Vector2(position.x, position.y-20)
            get_tree().get_root().add_child(bulletInstance)
```

![Screen Shot 2022-04-29 at 1.58.58 pm.png](Screen_Shot_2022-04-29_at_1.58.58_pm.png)

## Working Project

This is an example of how the project will run once implemented.

![2022-04-29 14-08-46.2022-04-29 14_09_44.gif](2022-04-29_14-08-46.2022-04-29_14_09_44.gif)

## Presentation Planning

The goals for this topic are:

- Plan the structure and content for the presentation


[Video presentation ideas - 17 of the best from Biteable - the world's simplest video maker](https://biteable.com/blog/video-presentation-ideas/)

[7 Different Types of Video Presentations_Presentation_ezTalks_Video Conferencing, Webinar, Online Meeting, Screensharing Tips and Reviews](https://eztalks.com/presentation/7-different-types-of-video-presentations.html)

[Video Production - Planning](https://www.notion.so/Video-Production-Planning-1ffb27d262474e04aedabd0653f63901?pvs=21)

[Best Kickstarter Videos of 2020 and Why Are They Successful](https://www.adjustproduction.com/news/best-kickstarter-videos-2020/)

[Best Kickstarter Videos](https://blog.thecrowdfundingformula.com/best-kickstarter-videos/)


### Documentation

Create a Google Doc and attach it to the assignment on Google Classroom.

1. Create Headings for each section and topic.
2. Under each heading and topic, write notes for what you want to cover. Include Screenshots as necessary.
3. Add a section for the style and type of video. Make notes, include examples of video styles that you will use as a
   guide to producing yours.

### Video Style

Consider the style that you wish to present the video? Will you use humour? Loud music etc.

Use the resources linked above to guide and inspire you.

### Examples

Look at the Assessment Examples page, focusing on the Video Presentations. What works well, what could be done better,
and what approaches could/would you take?

[Assessment Examples](https://www.notion.so/Assessment-Examples-ba9ee48cf95a4ca78c4a3653b16831a0?pvs=21)

### Storyboard

Using
the [Video Production - Planning](https://www.notion.so/Video-Production-Planning-1ffb27d262474e04aedabd0653f63901?pvs=21)
page, create a storyboard of your intended video.

Attach the storyboard to the assessment on Google Classroom.

## Extension Tutorials

### Countdown Timer

On this page, you'll be shown how to create a simple countdown Timer which updates the screen with the current time.

### Interface

Create a label node in the scene and note where in the hierarchy you created it. In the case below, the node is
called `Countdown` and it's stored under `HUD`.

![Screen_Shot_2021-05-04_at_10.09.14_am.png](Screen_Shot_2021-05-04_at_10.09.14_am.png)

That's it for the interface at this stage!

### Code

In the main Scene, update the `MainGame.gd` code to include two variables at the top:

```python
export(int) var countdownMax
var currentTimer
```

The `countdownMax` variable is used to store the starting value for the countdown and is set through the Inspector of
the main scene

![Screen_Shot_2021-05-04_at_10.03.34_am.png](Screen_Shot_2021-05-04_at_10.03.34_am.png)

The currentTimer variable is used to keep track of the current time, which will be reduced by 1 each second.

Next, update the _ready function to first set the currentTimer to the maximum, and update the Label.

```python
	currentTimer = countdownMax
	$HUD/Countdown.text = str(currentTimer)
```

> You will need to change the `$HUD/Countdown` to match where the countdown timer label is in your scene view!!
{style="note"}

Then you'll create a look which updates the Countdown label, waits a second using the `yield` function, and then reduces
the `currentTimer` value by 1

```python
while currentTimer > 0:
		print(currentTimer)
		$HUD/Countdown.text = str(currentTimer)
		yield(get_tree().create_timer(1.0), "timeout")
```

When the loop ends, (when `countdownTimer` reaches 0) then you can write the code to do whatever you want. In the case
below, it simply outputs Game Over, however you may want to change to another scene.

Here is the final code for the `_ready()` function.

```python
func _ready():
	#... Existing setup code...
	
	currentTimer = countdownMax
	$HUD/Countdown.text = str(currentTimer)
	while currentTimer > 0:
		print(currentTimer)
		$HUD/Countdown.text = str(currentTimer)
		yield(get_tree().create_timer(1.0), "timeout")
		currentTimer -= 1
	$HUD/Countdown.text = str(currentTimer)
	print("Game Over")
	#Change to next scene
```

## Tutorials

### Animation "Gifs"

To get an animation in an image (like an animated Gif) in your project, you could to use an AnimatedSprite.

[Godot Engine Tutorial Part 9-Sprite Animation - GameFromScratch.com](https://gamefromscratch.com/godot-engine-tutorial-part-9-sprite-animation/)

### Background Colour

[How can I change the default background color](https://godotengine.org/qa/386/how-can-i-change-the-default-background-color)

### Limiting Enemies to shoot (Raycast)


The goals for this topic are:

- Limit the enemy shooting to only the ones “in front”
- Implement raycasts into the enemy scene.



### Instructions


> Raycasts are an invisible line between two points in game. Using Raycasts you can detect collisions (or potential collisions). They have a number of uses such as calculating the destination of a bullet, without creating (instantiating) a bullet in game, or if an object can ‘see’ another object (if there’s a wall in the way).
{style="none"}

In the project, open the `enemy.tscn` file to edit the enemy object. This will update **all** enemy instances in the
game.

Add a child node to the Enemy. Search for RayCast2D in the list and choose Create.

![Screen Shot 2022-05-31 at 9.18.52 pm.png](Screen_Shot_2022-05-31_at_9.18.52_pm.png)

With the new RayCast2D node selected, change the Inspector values `Enabled` and `Cast To:.`

![Screen Shot 2022-05-31 at 9.28.31 pm.png](Screen_Shot_2022-05-31_at_9.28.31_pm.png)

Attach a script to the RayCast2D node.

![Screen Shot 2022-05-31 at 9.23.38 pm.png](Screen_Shot_2022-05-31_at_9.23.38_pm.png)

![Screen Shot 2022-05-31 at 9.23.43 pm.png](Screen_Shot_2022-05-31_at_9.23.43_pm.png)

Replace the contents with the following code.

Save the script.

```python
extends RayCast2D

# Called when the node enters the scene tree for the first time.
func _ready():
	set_process(true)

func _process(delta):
	if self.is_colliding():
		get_parent().canShoot = false
	else:
		get_parent().canShoot = true
```

Open Enemy.gd and create a new variable, declaring it at the top of the script.

```python
var canShoot = false
```

![Screen Shot 2022-05-31 at 9.24.41 pm.png](Screen_Shot_2022-05-31_at_9.24.41_pm.png)

**Update** the _process() function to first check if canShoot is true. If it is true, then the normal ‘shooting’ code
will execute.


> You only need to add the following line to the function - `if canShoot:`.
{style="tip"}

![Screen Shot 2022-05-31 at 9.26.59 pm.png](Screen_Shot_2022-05-31_at_9.26.59_pm.png)

## Export Game

Under Project menu, choose Export.

![Untitled](Untitled.png)

Click on the Add button, and choose the operating system that you’re attempting to export for.

![Untitled](export var health.png)

The first time you attempt to do this, you may be presented with information such as shown. Click on Manage Export
Templates.

![Untitled](Untitled2.png)

Click on the ****************************************Download and Install**************************************** link.

![Untitled](Untitled3.png)

This will take a minute or two…..

Once completed, click **********Close**********.

You may need to open the Export dialog again through the Project menu.

![Untitled](Untitled4.png)

You may see some more errors, and these will be dependent on the OS you’re exporting to.

You will need to research on how to solve these issues.

If required: For the identifier, you can enter : `au.edu.act.ltc.<Game Name>,` changing `<Game Name>` to the name of
your game.

![Untitled](Untitled5.png)

---

## Player Health

To enable health in the player, a few scripts need to be updated. Open `Player.gd` and add a new function at the bottom
of the script to reduce the health of the player.


> Depending on your requirements, you can change the value that health is reduced by.
{style="tip"}

![Untitled](Untitled.png)

```python
func reduceHealth():
	health -= 1
	if health == 0:
		get_tree().change_scene("res://Menu/Menu.tscn")
```

At the top of the script, add a new variable called `health` which can also be configured in the Godot IDE by including
the `export` keyword.

![Untitled](Untitled1.png)

```python
export (int) var health = 1
```

Save the script.

Open `Bullet-Enemy.gd` and update the code which runs when the bullet collides with an option. This code will check if
the collidedObject contains the word “Player”, and if so, run the `reduceHealth()` function on that object.

Save the script.

![Untitled](Untitled2.png)

```python
if "Player" in collidedObject.collider.name:
		collidedObject.collider.reduceHealth()
```

Test the functionality.

<include from="reusableContent.topic" element-id="commitPush"/>

---

## End of Game Bug

If your game is experiencing a bug where objects from the Main Game are appearing after a scene changes, such as when
the player dies or countdown finishes, this is one method of fixing the bug.

In `Global.gd` add a new variable called `Player`. This variable will be used as a ‘pointer’ to the player object. When
the player object gets created, the `Player` variable will set to point to the player object. When the scene ends (win
or lose) the `Player` variable will be set back to null.

Save the Script.

![Untitled](Untitled3.png)

In `[Player.gd](http://Player.gd)` update `_ready()` set the `GlobalVariables.Player` to be the Player object. This uses
the `self` keyword.

![Untitled](Untitled4.png)

```python
GlobalVariables.Player = self
```

For ******all****** objects that need to be deleted from the game when the player dies or the player wins (i.e. the
scene needs to change), add the following code to the **********start********** of the  `_process()`
or `_physics_process(delta)` functions

Repeat this for all objects. You may need to add this code to `enemy.gd` , `Bullet.gd`, and `Bullet-Enemy.gd` scripts.

![Untitled](Untitled5.png)

```python
if GlobalVariables.Player == null:
		queue_free()
```

Finally, Whenever the player object or game finished, set the `GlobalVariables.Player` variable back to `null`.

This will need to be added to any point where the scene changes in the main game. For instance, when the countdown
finishes.

![Untitled](Untitled6.png)

```python
GlobalVariables.Player = null
```

## Player Health Display

![Hearts for Health Implemented.](Untitled7.png)

Hearts for Health Implemented.

This is based on this tutorial.

[Heart Containers: 3 Ways :: Godot 3 Recipes](https://kidscancode.org/godot_recipes/3.x/ui/heart_containers_3/index.html)

Download the Asset library from this page.

[https://kenney.nl/assets/platformer-art-deluxe](https://kenney.nl/assets/platformer-art-deluxe)

Unzip the file and find the three heart images.

![Untitled](Untitled8.png)

Copy these into the Images folder in your project. In the example here, the images are stored in a folder called *
***********hearts************ however they can be stored anywhere in the project.

> The path to the images in the code later will need to match!
{style="tip"}

![Untitled](Untitled9.png)

Opening the desired scene, create a VBoxContainer, called `Health`. Create Five (or as many as the game requires) *
*******TextureRect********s as children of the VBoxContainer.

![Untitled](Untitled10.png)

Rename the TextureRects to 1..2..3.. etc. Drag the Heart image onto each of the TextureRects.

Additionally, set the StretchMode to be Keep

![Untitled](Untitled11.png)

Attach a script to the `Health` HboxContainer, naming the file `health.gd`. Replace the contents with the code shown.

At this stage, nothing will occur if the game is run. The `update_health` function will need to be called by the main
game script to update the hearts based on the players health.

```python
extends HBoxContainer

enum MODES {simple, empty, partial}

var heart_full = preload("res://Images/hearts/hud_heartFull.png")
var heart_empty = preload("res://Images/hearts/hud_heartEmpty.png")
var heart_half = preload("res://Images/hearts/hud_heartHalf.png")

export (MODES) var mode = MODES.simple

func update_health(value):
	match mode:
		MODES.simple:
			update_simple(value)
		MODES.empty:
			update_empty(value)
		MODES.partial:
			update_partial(value)

func update_simple(value):
	for i in get_child_count():
		get_child(i).visible = value > i

func update_empty(value):
	for i in get_child_count():
		if value > i:
			get_child(i).texture = heart_full
		else:
			get_child(i).texture = heart_empty
			
func update_partial(value):
	for i in get_child_count():
		if value > i * 2 + 1:
			get_child(i).texture = heart_full
		elif value > i * 2:
			get_child(i).texture = heart_half
		else:
			get_child(i).texture = heart_empty
```

********************REMEMBER!!!********************  The paths to the images need to match. Check capitalisations and
the **********exact********** path for each of the images.

![Untitled](Untitled12.png)

Edit the `[MainGame.gd](http://MainGame.gd)` and add the following code into  `_process(delta)`.


> The path to the Health and player nodes will depend on your setup. Change the `$HUD/Health` and `$Player` as necessary to fit the specific nodes.
{style="tip"}

![Untitled](Untitled13.png)

```python
$HUD/Health.update_health($Player.health)
```

Make sure the Players health variable is set to `export` in the player script.

Set the players health to match the number of hearts you need.

![Untitled](Untitled14.png)

Run the game!

![Jun-08-2023 12-59-56.gif](Jun-08-2023_12-59-56.gif)

## “Partial” Version

The Partial Version of the script uses the half hearts. This could be used if your player health was more than the
number of hearts you wanted on screen. For instance, if the player’s health was 10, but only had the space for 5 hearts.

To configure the partial version of the health bars, open `[Health.gd](http://Health.gd)` and change the `MODES`
to `partial`.

![Untitled](Untitled15.png)

Set the players health to an appropriate value and run the game.

![Jun-08-2023 13-05-52.gif](Jun-08-2023_13-05-52.gif)