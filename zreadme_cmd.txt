
<Fly Around>
- Double-tap the SPACEBAR to fly
- Double-top the SPACEBAR agin to stop flying
- Holding the SPACEBAR to fly higher
- Holding SHIFT lower you toward the ground


<Testing Minecraft Python Setup>
1. Going to Minecraft Tools folder, run Start_Server.
2. Open Minecraft and connect to the Spigot server
   by selecting Minecraft Python World 
   from the multiplayer menu.
3. Hit Esc key to free your cursor from the Minecraft
   Open a Python shell in IDLE.
   
//This code teleports the player to a new position,
//the player will fly high into the air.  
# these two lines connect your program to Minecraft 
>>> from mcpi.minecraft import Minecraft
>>> mc = Minecraft.create()
# ask the player to move to the position(10, 110, 12)
>>> mc.player.setTilePos(10, 110, 12) 
# more precise
>>> mc.player.setPos(10.0, 110.0, 12.0) 
# find out where the player is
>>> position = mc.player.getTilePos()
>>> x = position.x
>>> y = position.y
>>> z = position.z

//Set wait
>>> import time
>>> time.sleep(10)    #wait for 10 seconds

//Coordinates: x, y and Z
//y - height,  x and z represent horizontal positions at a flat plane.

//Place a block
#the last argument is block type 
#air is 0, melon is 103, lava is 10, cobblestone is 4
#water is 9, leaves is 18, wood is 11
#diamond is 57, sapling is 6
>>> mc.setBlock(6, 5, 28, 103)

//Build Cuboid
>>> mc.setBlocks(x,y,z,x+width,y+height,z+length,blocktype)

//Display the output in the Minecraft chat
>>> mc.postToChat("Hello, Minecraft World")

//Python uses exception handling to make sure your program can 
//recover from errors and continue running when they occur.
>>> try:
>>>   blockType = int(input("Enter a block type: "))
>>>   mc.setBlock(x, y, z, blockType)
>>> except:
>>>   print("You did not enter a number! Enter a number next time.")

//Boolean
>>> light = False
>>> mc.setting("world_immutable", True)
>>> blockType = mc.getBlock(x, y, z)
>>> mc.postToChat(blockType == 0)  #check whether the block is air

//get y-coordinate of highest block at the player's current location
>>> highestBlockY = mc.getHeight(x, z)














