# Player Health

This stage of the tutorial will demonstrate how to implement a simple health system, where there is a player health and when the enemy collides with the player, the health reduces. As with many other aspects of game development, the exact implementation will depend on the requirements for the project, so apply as necessary.

<aside>
‼️ This process can be applied to ANY object that you wish to reduce the players health when a collision occurs.

</aside>

## Player Script

Open `Global.gd` and add a new variable named `player_health`. Set the initial value to be 100.

Save the file.

![Screen Shot 2022-09-12 at 9.05.32 pm.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-12_at_9.05.32_pm.png)

## Update Enemy

Open `Enemy.tscn` to edit the Enemy scene, adding an `Area` node as a child of the root node. Add a CollisionShape node a child of that one.

![Screen Shot 2022-09-12 at 8.56.53 pm.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-12_at_8.56.53_pm.png)

Select `CollisionShape` and change the shape attribute to a `CapsuleShape`.

![Screen Shot 2022-09-12 at 8.58.22 pm.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-12_at_8.58.22_pm.png)

Select Area in the hierarchy, change to the Node tab, and double click on `body_entered()` in the list of signals.

![Screen Shot 2022-09-12 at 8.59.56 pm.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-12_at_8.59.56_pm.png)

Click Connect.

![Screen Shot 2022-09-12 at 9.02.37 pm.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-12_at_9.02.37_pm.png)

Replace the contents of the function with the code shown.

This code checks first if the object the enemy has collided with is the player, and if so, reduce  `player_health` by 10. Then delete the enemy object from the game.

<aside>
‼️ The exact value the health gets reduced by can be set to whatever value you chose. Just change the 10.

</aside>

![Screen Shot 2022-09-12 at 9.06.39 pm.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-12_at_9.06.39_pm.png)

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

![Screen Shot 2022-09-12 at 9.42.29 pm.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-09-12_at_9.42.29_pm.png)

```python
if Global.player_health <= 0:
        print("Dead")
        get_tree().change_scene("res://Lose.tscn")
```

$* \normalsize \mathcal {\color{black} \colorbox {orange}  {Save, Commit and Push Changes to Github!}}$ 
