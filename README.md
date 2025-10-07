# TEC-284-lab-12
programming with minecraft
#Import the api
from mcpi_addons.minecraft import Minecraft
#Initialize the api (MCPI must be open and in a world at this time)
mc = Minecraft.create()
#mc.postToChat("Hello World!")

x = input("x Coordinate: ")
y = input("y Coordinate: ")
z = input("z Coordinate: ")
x = int(x)
y = int(y)
z = int(z)

mc.setBlocks(x, y, z, x + 10, y + 20, z + 40, 3)
mc.setBlocks(x, y, z, x + 10, y + 20, z + 40, 0)

#part2
#import the API
from mcpi_addons.minecraft import Minecraft
#Initialize the API (MCPI must be open and in a world at this time)
mc = Minecraft.create()
import time

pos = mc.player.getPos()
mc.setBlock(pos.x, pos.y -1, pos.z, 12)
time.sleep(1)
