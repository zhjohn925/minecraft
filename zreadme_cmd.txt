
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
>>> from mcpi.minecraft import Minecraft
>>> mc = Minecraft.create()
>>> mc.player.setTilePos(0, 120, 0) 


