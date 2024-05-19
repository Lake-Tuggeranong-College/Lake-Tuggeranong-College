# FPS - Objects Taking Damage

The bullets and enemy have been created, the bullets fire. Now it’s time to put it together - having the enemies take damage. 

Unlike the player’s health, which is a global variable, each enemy (or any other object with health) will have its own health that will need to be diminished for it to be destroyed. 

**Each object or enemy that you wish to take damage needs to be configured in the same way.**

<aside>
‼️

The object taking damage will need to have a Collision Shape configured as a direct child of the root node.

![Screen Shot 2022-10-06 at 10.02.18 pm.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-10-06_at_10.02.18_pm.png)

</aside>

Open the (or attach a) script for the object that you wish to take damage.

Add a simple `take_damage(damage)` function to the script, which simply outputs a test message to ensure that the process works.

![Screen Shot 2022-10-06 at 10.37.49 pm.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-10-06_at_10.37.49_pm.png)

```python
func take_damage(damage):
    print("ouch")
```

Run the game at this stage to test the collision. 

![2022-10-06 23-02-38.2022-10-06 23_04_11.gif](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/2022-10-06_23-02-38.2022-10-06_23_04_11.gif)

<aside>
‼️ You may find it useful to slow the bullets down to properly test, as can be seen in this example.

</aside>

Open the script for the object. Add a `health` variable at the top of the script and set the value to 100.

![Screen Shot 2022-10-06 at 11.14.44 pm.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-10-06_at_11.14.44_pm.png)

```python
var health = 100
```

Update `take_damage()` to reduce the amount of health, and then check if the health has reached zero. If so, then delete the object.

![Screen Shot 2022-10-06 at 11.16.23 pm.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-10-06_at_11.16.23_pm.png)

```python
func take_damage(damage):
    health -= 50
    if health <=0:
        queue_free()
```

Run the project and you should see the object be destroyed as health reaches 0.

![2022-10-06 23-13-27.2022-10-06 23_14_08.gif](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/2022-10-06_23-13-27.2022-10-06_23_14_08.gif)

<aside>
‼️ Remember this process can work for any damageable object in the game - enemies, walls, doors etc.

</aside>