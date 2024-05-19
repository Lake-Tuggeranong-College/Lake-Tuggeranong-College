# Points

## Global Script

Create a new script called `Global.gd` (unless it’s already created).

![Screen Shot 2022-09-06 at 1.59.04 pm.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-06_at_1.59.04_pm.png)

![Screen Shot 2022-09-06 at 1.59.39 pm.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-06_at_1.59.39_pm.png)

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

![End Result](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-06_at_2.10.46_pm.png)

End Result

Click Close.

## Pickup Item

The pickup item can be any object you wish. It could be a simple cube or cylinder or a complex object that you’ve imported from 3D modelling software such as Blender. Regardless of the object itself, the object needs to be saved as it’s own Scene.

In this case, the file is saved as `Pickup.tscn` and there is a cylinder object created.

![Screen Shot 2022-09-06 at 2.14.32 pm.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-06_at_2.14.32_pm.png)

Create child nodes of the original object to include a mesh that the player can collide with.

![Screen Shot 2022-09-06 at 2.15.18 pm.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-06_at_2.15.18_pm.png)

Right Click on the Pickup node and attach a script, named `Pickup.gd`. Save the script. There is no need to change the code at this stage.

![Screen Shot 2022-09-06 at 2.18.05 pm.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-06_at_2.18.05_pm.png)

Select the Area node, and switch to the Node tab.

![Screen Shot 2022-09-06 at 2.16.31 pm.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-06_at_2.16.31_pm.png)

Double click on the Body Entered signal. Make sure the Pickup node is selected and click Connect. 

![Screen Shot 2022-09-06 at 2.18.58 pm.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-06_at_2.18.58_pm.png)

Enter the following code for the `_on_Area_body_entered(body)` function.

This code check to see if the object that collides with the pickup item is the player. If so, it will add 10 points to the `current_score` variable in the Global script.

Then it deletes the pickup item.

![Screen Shot 2022-09-06 at 2.19.59 pm.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-06_at_2.19.59_pm.png)

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

![Screen Shot 2022-09-06 at 2.24.42 pm.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-06_at_2.24.42_pm.png)

```python
$Camera/playerScore.text = str(Global.current_score)
```