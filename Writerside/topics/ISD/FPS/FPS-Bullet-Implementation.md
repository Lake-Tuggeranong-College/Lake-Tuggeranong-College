# FPS - Bullet Implementation

There are numerous ways to implement shooting in an FPS (or other type of) game. 

The first is through creating projectiles (such as bullets) for the player to shoot. The bullets will hit objects in their direct path, and can cause damage. This method is the focus for this section of the project.

Another method, is to use **raycast**s, where the there is an imaginary line drawn from the camera, and seeing what object it hits first (if any). Raycasts will be covered in a later tutorial.

<aside>
‼️ What are the pros and cons of each approach? Why choose one over the other?

</aside>

## Bullet Mesh

<aside>
‼️ This tutorial is going to demonstrate how to create a simple bullet. Your implementation for the model may differ, however the process should be the same.

</aside>

Create a new Scene (Scene→New Scene).

Set the Root Node as `Area3D` by selecting Other Node and search for Area3D.

![Untitled](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Untitled%2029.png)

Create your bullet model. You can create your own mesh, or you can follow the instructions shown below.

### Simple Bullet

For a simple bullet shape, this can be done by creating a `CSGCylinder3D` and a `CSGSphere3D` and manipulating (move and rotate) them into a bullet shape.

![Screen Shot 2022-10-04 at 9.47.38 pm.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-10-04_at_9.47.38_pm.png)

Ensure that both of these CSG objects have Union Operation selected.

![Screen Shot 2022-10-04 at 9.45.55 pm.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-10-04_at_9.45.55_pm.png)

Then place them as children of a `CSGCombiner3D`. Name the new node as appropriate.

![Untitled](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Untitled%2030.png)

Texture the object as you would normally.

<aside>
💡 Search for "Metallic texture seamless” to find a metal texture for a bullet.

</aside>

![Screen Shot 2022-10-04 at 9.51.14 pm.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-10-04_at_9.51.14_pm.png)

Attach a `CollisionShape3D` node as a child of the scene root.

![Untitled](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Untitled%2031.png)

With the `CollisionShape3D` selected, set the Shape to be `CapsuleShape3D`.

![Screen Shot 2022-10-04 at 9.55.49 pm.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-10-04_at_9.55.49_pm.png)

Manipulate the Capsule shape, using the transform options, so that it completely surrounds the mesh.

![Untitled](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Untitled%2032.png)

Rename the Scene Root as `Bullet`.

![Screen Shot 2022-10-04 at 9.59.07 pm.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-10-04_at_9.59.07_pm.png)

Save the scene as `Bullet.tscn`.

![Untitled](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Untitled%2033.png)

## Bullet Script

Still in the Bullet scene, attach a new script to the root node (Bullet) and name it `Bullet.gd`.

![Untitled](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Untitled%2034.png)

![Untitled](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Untitled%2035.png)

Add two new variables to control how fast the bullet will travel, and how much damage it will inflict on the object it collides with (if configured to take damage). 

`speed` defines how fast the bullet will move through the game.

`damage` is how much damage the bullet can deal out.

<aside>
‼️ These can be set to whatever values are appropriate.

</aside>

<aside>
‼️ This can be used to allow for different weapons with different bullet speeds and damage.

</aside>

![Untitled](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Untitled%2036.png)

```python
var speed : float = 30.0
var damage : int = 1
```

Add code, within the `_process` function to move the bullet instance forward. 

![Untitled](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Untitled%2037.png)

```python
func _process (delta):
    # move the bullet forwards
    global_transform.origin -= transform.basis.z.normalized() * speed * delta
```

Save the Script.

Select the root node (Bullet) and change to the Node tab. 

![Untitled](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Untitled%2038.png)

Double click on `body_entered`. Press **Connect.**

This code will be used to detect when the bullet instance has collided with another object - when the bullet collider enters another node’s collider.

![Untitled](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Untitled%2039.png)

In order to only destroy objects that need to be destroyed, this code will first check if the other collider has a function called `take_damage` in its script. This means that a script attached to the enemy objects can have that function, and will take damage, however a wall doesn’t need that function, so it won’t be destroyed.

 `_on_Bullet_body_entered(body)` executes when the bullet enters another object. If that object has the `take_damage()` function (or method), it will then run that function on the other node, passing the `damage` value.

Also added is the `destroy()` function. This simply deletes the bullet from the game.

This has been added in such a way to allow for future modification as required.

![Untitled](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Untitled%2040.png)

```
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

![Screen Shot 2022-10-04 at 10.22.24 pm.png](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Screen_Shot_2022-10-04_at_10.22.24_pm.png)

Set the wait time to something appropriate, and Autostart to On.

![Untitled](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Untitled%2041.png)

Change to the Node tab and double-click on the `timeout()` signal. 

Set the Receiver Method to `destroy`.

<aside>
💡 You can either type in the function name, or use the Pick button to choose the correct function.

</aside>

Select Connect.

![Untitled](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Untitled%2042.png)

![Untitled](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Untitled%2043.png)

Save the Bullet Scene.