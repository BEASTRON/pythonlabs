# pythonlabs

#! /usr/bin/env python3

#Bernardo D. Villajuan
#April 28, 2015
#recursiveBinarySearch.py



def main():
    numbers = [0, 1, 3, 4, 5, 10, 12, 13, 15, 16]
    low = 0
    high = len(numbers)-1
    while True:
        number = input("Enter a number: ") 
        if number == "":
            break
        result = recBinSearch(eval(number), numbers, low, high)
        if result == True:
            print(number, "was in the list.")
        else:
            print(number, "was not in the list.")
        
def recBinSearch(y, nums, low, high):
    if low > high:
        return -1
    mid = (low + high) // 2
    items = nums[mid]
    if items == y:
        return True
    elif y < items:
        return recBinSearch(y, nums, low, mid - 1)
    else:
        return recBinSearch(y, nums, mid + 1, high)
        
        
        


#! /usr/bin/env python3

#Bernardo D. Villajuan
#February 22, 2015
#DarthBlu-ManMarauder.py

from graphics import *

def main():
    win = GraphWin("Snowman", 600, 600)
    base = Circle(Point(300, 400), 80)
    base.setFill("blue")
    base.draw(win)
    midsection = Circle(Point(300,300), 60)
    midsection.setFill("blue")
    midsection.draw(win)
    top = Circle(Point(300,220), 40)
    top.setFill("blue")
    top.draw(win)
    eyes1 = Circle(Point(280, 210),6)
    eyes1.setFill("black")
    eyes1.draw(win)
    eyes2 = Circle(Point(320, 210),6)
    eyes2.setFill("black")
    eyes2.draw(win)
    nose = Polygon(Point(296, 220), Point(330, 224), Point(296, 230))
    nose.setFill("yellow")
    nose.draw(win)
    arm1 = Line(Point(270,300), Point(300,380))
    arm1.draw(win)
    arm2 = Line(Point(330,308), Point(400,306))
    arm2.draw(win)
    lightsaber = Polygon(Point(400,306), Point(404,306), Point(404,120), Point(400,120))
    lightsaber.setFill("purple")
    lightsaber.draw(win)
    lightsaber2 = Polygon(Point(398,306), Point(406,306), Point(404,340), Point(398,340))
    lightsaber2.setFill("black")
    lightsaber2.draw(win)
    lightsaber3 = Polygon(Point(370,390), Point(364,390), Point(204,376), Point(300,376))
    lightsaber3.setFill("purple")
    lightsaber3.draw(win)
    lightsaber4 = Polygon(Point(), Point(), Point(), Point())
    lightsaber4.setFill("purple")
    lightsaber4.draw(win)
    win.getMouse()
    win.close()
    
main()




