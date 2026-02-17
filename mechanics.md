# CryoShock - Mechanics Documentation

This document will give you an overview of the different elements of the CryoShock project that you will be expected to use and modify in scene when creating your level.

## Project overview
The CryoShock Unreal project includes a folder labelled COMP2150 inside the Content folder of the Unreal Project. This is where all the files we are concerned with for this unit are. If you have a look in here, you'll see the following folders:

* Core: Features core game management/player objects. You should not modify any of the items in this folder.
* Environment: Features blueprints (game objects) for checkpoints, doors, platforms and switches.
* Generic: Contains material data for most of the game. You may at times wish to apply different materials to game geometry to indicate different things.
* Geometry: Contains basic meshes for floors, walls and ceilings.
* Hazards: Contains the enemies, nasty objects and projectiles for the player to encounter.
* Level Prototyping: These are some more primitive meshes and materials provided by Unreal. You should use these if you are unable to achieve your geometry with the meshes we have provided.
* Maps: Contains the maps for the game. For the assignment, you'll have a particular map in here to edit.
* Pickups: Contains the various pick-ups the player will encounter in the game.

With the exception of geometry and level prototyping, you should only be placing objects into the game world with the BP_ prefix, which suggests they are a Blueprint (a game object), rather than a mesh. For this reason, most meshes have been placed away in respective "Mesh" folders to avoid confusion.

## The player
The player character is not to be edited, and but you can control where they spawn in the world. To place them into the game world, click the small cube with a green plus sign above the viewport and then go to Basic > Player Start. If you already have a Player Start in your level, instead you want to move this to where the player should spawn.

The player can run, jump, and (when unlocked) use the left mouse button to "blink" around the environment, or (when unlocked) the right mouse button to activate a shield. Blinking, and deflecting turret projectiles with the shield, both drain mana which regenerates over time. To regenerate health, the player must find a health pack. When the player runs out of health, they respawn at the start of the level or the most recently touched Checkpoint.

## Checkpoint
Checkpoints can be placed anywhere in the game world, but have no paramters to edit. When the player collides with a checkpoint, they will respawn there upon death.

## Pick-ups

### HealthPack Pick-up
The HealthPack is a pick-up which grants the player health on collision. Individual health packs can grant different amounts of health, based on the "health" paramater.

### Keys
Keys are needed to unlock the end game door. Three keys must be placed in every level to unlock the door. There are no editable paramaters.

### Blink Upgrade
The blink upgrade will grant the player the blink ability upon collision.  There are no editable paramaters.

### Shield Upgrade
The shield upgrade will grant the player the shield ability upon collision.  There are no editable paramaters.

## Environment and interactables### Moving Platform
The moving platform will move between two points. It has the following paramaters:
* Nodes: Other game objects in the game world, represented by spheres. After placing a moving platform in the scene, you can adjust the position of Node0Obj and Node1Obj to control the points the platform will move between. Be careful not to adjust the sphere meshes by mistake!
* Move Speed: How fast the platform will move.
* Hang Time: How long in seconds the platform will rest when it reaches a node before moving to the next.
* Active: Whether the platform is active or not. This is useful if you want to have it activated by a Switch.

### Door
Doors are closed by default, and open when their corresponding switch is activated. Parameters:

* Door Speed: How fast the door opens or closes.
* Open: Whether the door is open or not on start.

### Switch
Switches can be used to activate doors and moving platforms. To do this, they need to be linked to a BP_SwitchReceiver, which will be attached to a door or moving platform.

By default, doors already have a BP_SwitchReceiver attached to them. To link them up with a Switch, modify the "Receiver" paramater in the scene by selecting from the drop-down, or using the eyepicker to click on the corresponding object.

Note that by default the Receiver can be any object in the scene, to allow for modularity. Be careful of this and always double-check you've selected the right object.

To assign a switch to a moving platform, you'll first need to add a receiver to the platform. You can do this by selecting the platform in your scene, then pressing the + Add button in the Details panel and finding BP_SwitchReciever. Then, repeat the process above for assigning a receiver to a switch.

Other paramters:
* On: Whether the switch hs been hit or not. Should only really be used for debugging.
* Highlighted: Whether the player has the switch highlighted by looking at it. Should only really be used for debugging.
* One Way: If turned on, this switch will only be fired once when pressed, and will not work after that.

A switch will have a purple line moving from itself to its receiver.

### End-Game Door
The end game door. When the player enters it after collecting three keys, the game ends. Paramaters:
* Door speed: Controls how fast the door opens.
* Open: Whether it is open or not. Useful for debugging.
* Level to Load: The level the door loads when the player enters. You shouldn't change this.

## Hazards
### Spike Pit and Cryo Field
The spike pit is a solid object that damages the player on collision. The cryofield is transluscent, but will damage the player on collision unless they are blinking. Paramters:

* Damage Amount: How much damage the spikes do to the player.
* Type: The type of hazard this is. Changing this will effect its behaviour. For instance, setting this to "Projectile" would remove any knockback force and change how it interacted with turrets.
* Knockback Force: How much force the player is knocked back with on collision.

### Turret Head
A turret that will shoot projectiles at the player if it sees them. Paramaters:
* Rotation Speed: How fast the turret will rotate to "chase" the player.
* Cooldown rate: The rate between firing projectiles.
* Inactive Time: How long the turret turns off for if it is hit by a projectile.