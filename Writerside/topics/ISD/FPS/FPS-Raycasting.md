# FPS - Raycasting

<aside>
‼️ Raycasting is an alternative to firing projectiles in your game. Projectiles (bullets, lasers etc) that have a ‘physical’ object being fired in the game take up processing power, memory etc. Raycasting is a more efficient method of determining if shots hit, or if an object can see another etc.

</aside>

To implement raycasting for shooting or another method, you can extend the current functionality of your game without impacting existing functionality.

## Input Map

First, you can choose to create a new input trigger for raycasting. Go to Project → Project Settings → Input Map and create a new input map called `ray` and assign a key to it.

<aside>
‼️ In this example the key `r` has been assigned. You can choose another key or mouse button as required.

</aside>

![Untitled](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Untitled%2053.png)

## Player Object

Open the Player object (`player.tscn`) and create a **RayCast** child object of the Camera node.

![Untitled](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Untitled%2054.png)

With RayCast selected, set the Enabled option to be true in the Inspector. Additionally, get the **Cast To** settings to the 0, 0, -10. This will set the ray cast to be set to be in the direction of the camera.

<aside>
‼️ If your player’s camera is configured differently, you may need to change these settings.

</aside>

![Untitled](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Untitled%2055.png)

Create a **MeshInstance** as a child of the Player root node, calling it **HitPoint**.

![Untitled](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Untitled%2056.png)

In the inspector, Create a new SphereMesh, and change the radius and height to 0.1 and 0.2 respectively.

Set the colour of the mesh to red (or any other colour) to make it stand out in the game.

![Untitled](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Untitled%2057.png)

Save the `player.tscn` file.

## Player.gd script

Open `[player.gd](http://player.gd)` and add two new variables at the top of the script to store the raycast and the hitpoint nodes.

![Untitled](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Untitled%2058.png)

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

![Untitled](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Untitled%2059.png)

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

![Untitled](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Untitled%2060.png)

Attach a script to the Wall root node. Include the function and at this stage simply output that the raycast has been detected.

```python
func raycast_collision():
    print("ray hit")
```

![Untitled](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Untitled%2061.png)

Save the Wall scene.

When the game is now run, aim at a wall and press the `ray` input. The “ray hit” output should be visible in the Output.

![Untitled](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Untitled%2062.png)

$$
\utilde {\color{black} \fcolorbox{darkorange}{darkorange}  {Commit and Push to Github}}
$$

Any other objects in the game can react to raycasts but following the same process of adding a collider as a child, such as a CSGBox, and including a script with a `raycast_collision()` function included.

The `raycast_collision()` can delete the object, add points etc - whatever you need the object to do when it is “shot”.
