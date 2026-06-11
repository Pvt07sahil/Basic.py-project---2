# Basic.py-project---2

def draw_smile():
    draw_circle()
    draw_eyes()
    draw_mouth("smile")
    
    
def draw_frown():    
    draw_circle()
    draw_eyes()
    draw_mouth("frown")


def draw_circle():
    penup()
    setposition(0,-100)
    pendown()
    begin_fill()
    color("yellow")
    circle(100)
    end_fill()
    
def draw_eyes():
    penup()
    setposition(-25,25)
    begin_fill()
    color("black")
    circle(10)
    end_fill()
    penup()
    setposition(25,25)
    begin_fill()
    color("black")
    circle(10)
    end_fill()
    
def draw_mouth(type):
    if type == "smile" :
        penup()
        setposition(-75,0)
        right(90)
        pendown()
        pensize(5)
        circle(70,180)
        
    else  :
        penup()
        setposition(50,-50)
        left(90)
        pendown()
        pensize(5)
        circle(50,180)
    
    

speed(10)

happy = input("Are you happy?")
if happy == "yes" :  
    draw_smile()
else :
    draw_frown()
