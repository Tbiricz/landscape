# landscape
x = 150
y = 120
sun = 50
z = 110
check = 0
def setup():
    size(350,350)
def draw():
    frameRate(60)
    noStroke()
    global x
    global y
    global z
    global check
    global sun
    if check == 0:
        background(115,110,300)
        fill(230,170,50)
    else:
        background(20,20,100)
        fill(220,220,220)
    ellipse(sun,sun,50,50)
    sun += .3
    if sun >= 350:
        sun = -25
        if check == 0:
            check = 1
        else:
            check = 0
    fill(255)
    ellipse(z,130,100,50)
    ellipse(x,110,100,50)
    ellipse(y,90,100,50)
    fill(120,100,60)
    rect(50,190,40,150)
    fill(90,250,80)
    ellipse(70,150,70,100)
    
    rect(-2,300,360,110)
    x += 1
    y += 1
    z += 1
    if x >= 410:
        x = -59
    if y >= 410:
        y = -59
    if z >= 410:
        z = -59
