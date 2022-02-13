# Ballbouncing-physics-with-SIN
Pygame animation
import pygame as py
import time
import math
print("This game uses sin to show the bouncing of a ball\n")
py.init()
width = 540
height = 480 
background_col = (0,32,68)
brown = (101, 67, 33)
green = (0, 100, 0)
screen = py.display.set_mode((width, height))
py.display.set_caption("PygameART")
screen.fill(background_col)
power = input("Enter the height you want to drop the square at (Recommended between 1000 - 2000m.) \n")
power = float(power)
for x1 in range(1, 700):
  screen.fill(background_col)
  x = x1 / 10
  y =  470 - abs(math.sin(x)/x * power) 
  print(y)
  ball = py.draw.rect(screen, brown, py.Rect(100  
, y, 40, 40))
  time.sleep(.02)

  py.display.update()
  for event in py.event.get():
    if event.type == py.QUIT:
     quit()
  
