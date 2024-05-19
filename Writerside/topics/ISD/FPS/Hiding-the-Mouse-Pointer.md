# FPS - Hiding the Mouse Pointer

Open `Player.gd`.  Update the _ready() function to set the mouse to be hidden.

```
Input.set_mouse_mode(Input.MOUSE_MODE_HIDDEN)
```

![Untitled](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Untitled%2051.png)

# Showing the Mouse Pointer

To reenable the mouse pointer, for instance if the player returns to the main menu, add the following function below the _ready() function in the `Player.gd` script. 

This function runs automatically, when the player object is removed from the tree. In other words, when the player instance is removed from the game.

```
func _exit_tree():
    Input.set_mouse_mode(Input.MOUSE_MODE_VISIBLE)
```

![Untitled](FPS%20Tutorials%20GDScript%20v4%205d63afa7b5d04273b112b801ad85f4c0/Untitled%2052.png)
