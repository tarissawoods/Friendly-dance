# Friendly-dance
#A stickman walking into frame, waving hello, dancing, waving goodbye, and leaving.
import simplegui
import random
counter= 0
x=-50
dots=[]
def draw_handler(canvas):
    global counter
    global x
    global a
    global b

    #shapes/lines for platform
    canvas.draw_polygon([(200, 525), (400, 525), (400, 550), (200, 550)], 2, "black", "#a6680d")
    canvas.draw_polygon([(180, 520), (370, 520), (400, 525), (200, 525)], 2, "black", "#a6680d")
    canvas.draw_polygon([(175, 520), (200, 525), (200, 550), (175, 550)], 2, "black", "#a6680d")
    canvas.draw_polygon([(155, 530), (190, 530), (190, 550), (155, 550)], 2, "#a6680d", "#a6680d")
    canvas.draw_polygon([(400, 530), (420, 530), (420, 550), (400, 550)], 2, "black", "#a6680d")
    canvas.draw_polygon([(0, 550), (600, 550), (600, 600), (0, 600)], 2, "black", "grey")
    canvas.draw_line((155, 530), (176, 530), 2, "black")
    canvas.draw_line((155, 530), (155, 550), 2, "black")
    canvas.draw_line((174, 530), (200, 535), 2, "black")
    canvas.draw_line((200, 535), (170, 535), 2, "black")
    canvas.draw_line((155, 530), (170, 535), 2, "black")
    canvas.draw_line((170, 535), (170, 550), 2, "black")
    
    if counter<25:
        canvas.draw_line((x, 520), (x+8, 550), 4, "black")
        canvas.draw_line((x, 520), (x-8, 550), 4, "black")
        canvas.draw_line((x, 460), (x, 520), 4, "black")
        canvas.draw_line((x, 485), (x+8, 510), 4, "black")
        canvas.draw_line((x, 485), (x-8, 510), 4, "black")
        canvas.draw_circle((x, 460), 16, 1, "black", "white")
        canvas.draw_circle((x-8, 455), 2, 1, "black", "black")#face
        canvas.draw_circle((x+8, 455), 2, 1, "black", "black")
        canvas.draw_circle((x, 465), 6, 1, "black", "black")
        canvas.draw_circle((x, 460), 6, 1, "white", "white")
        
        
        counter=counter+0.5
        x=x+2
    elif counter<100:
        canvas.draw_line((x, 520), (x+8, 550), 4, "black")
        canvas.draw_line((x, 520), (x-8, 550), 4, "black")
        canvas.draw_line((x, 485), (x+8, 510), 4, "black")
        canvas.draw_line((x, 460), (x, 520), 4, "black")
        canvas.draw_circle((x, 460), 16, 1, "black", "white")
        canvas.draw_line((x, 485), (x-8, 510), 4, "black")
        canvas.draw_circle((x-8, 455), 2, 1, "black", "black")#face
        canvas.draw_circle((x+8, 455), 2, 1, "black", "black")
        canvas.draw_circle((x, 465), 6, 1, "black", "black")
        canvas.draw_circle((x, 460), 6, 1, "white", "white")
        counter=counter+1
       
    elif counter<115:
        canvas.draw_line((x, 520), (x+8, 550), 4, "black")
        canvas.draw_line((x, 520), (x-8, 550), 4, "black")
        canvas.draw_line((x, 485), (x+20, 510-40), 4, "black")#right arm
        canvas.draw_line((x, 460), (x, 520), 4, "black")
        canvas.draw_circle((x, 460), 16, 1, "black", "white")
        canvas.draw_line((x, 485), (x-8, 510), 4, "black")
        canvas.draw_circle((x-8, 455), 2, 1, "black", "black")#face
        canvas.draw_circle((x+8, 455), 2, 1, "black", "black")
        canvas.draw_circle((x, 465), 6, 1, "black", "black")
        canvas.draw_circle((x, 460), 6, 1, "white", "white")
        counter=counter+.5
        
    elif counter<120:
        canvas.draw_line((x, 520), (x+8, 550), 4, "black")#right leg
        canvas.draw_line((x, 520), (x-8, 550), 4, "black")#left leg
        canvas.draw_line((x, 485), (x+25, 510-30), 4, "black")#right arm
        canvas.draw_line((x, 460), (x, 520), 4, "black")#body
        canvas.draw_circle((x, 460), 16, 1, "black", "white")#head 
        canvas.draw_line((x, 485), (x-8, 510), 4, "black")#left arm
        canvas.draw_circle((x-8, 455), 2, 1, "black", "black")#face
        canvas.draw_circle((x+8, 455), 2, 1, "black", "black")
        canvas.draw_circle((x, 465), 6, 1, "black", "black")
        canvas.draw_circle((x, 460), 6, 1, "white", "white")
        counter=counter+1
        
    elif counter<130:
        canvas.draw_line((x, 520), (x+8, 550), 4, "black")
        canvas.draw_line((x, 520), (x-8, 550), 4, "black")
        canvas.draw_line((x, 485), (x+20, 510-40), 4, "black")#right arm
        canvas.draw_line((x, 460), (x, 520), 4, "black")
        canvas.draw_circle((x, 460), 16, 1, "black", "white")
        canvas.draw_line((x, 485), (x-8, 510), 4, "black")
        canvas.draw_circle((x-8, 455), 2, 1, "black", "black")#face
        canvas.draw_circle((x+8, 455), 2, 1, "black", "black")
        canvas.draw_circle((x, 465), 6, 1, "black", "black")
        canvas.draw_circle((x, 460), 6, 1, "white", "white")
        counter=counter+1
        
    
    elif counter<235:
        canvas.draw_line((x, 520), (x+8, 550), 4, "black")
        canvas.draw_line((x, 520), (x-8, 550), 4, "black")
        canvas.draw_line((x, 460), (x, 520), 4, "black")
        canvas.draw_line((x, 485), (x+8, 510), 4, "black")
        canvas.draw_line((x, 485), (x-8, 510), 4, "black")
        canvas.draw_circle((x, 460), 16, 1, "black", "white")
        canvas.draw_circle((x-8, 455), 2, 1, "black", "black")#face
        canvas.draw_circle((x+8, 455), 2, 1, "black", "black")
        canvas.draw_circle((x, 465), 6, 1, "black", "black")
        canvas.draw_circle((x, 460), 6, 1, "white", "white")
        counter=counter+1
        x=x+2
        
    elif counter<250:
        canvas.draw_line((x-6, 520), (x+8, 550), 4, "black")
        canvas.draw_line((x-6, 520), (x-8, 550), 4, "black")
        canvas.draw_line((x, 460), (x-6, 520), 4, "black")
        canvas.draw_line((x-4, 485), (x+12, 510), 4, "black")
        canvas.draw_line((x-3, 485), (x-14, 510), 4, "black")
        canvas.draw_circle((x, 460), 16, 1, "black", "white")
        canvas.draw_circle((x-8, 455), 2, 1, "black", "black")#face
        canvas.draw_circle((x-8, 457), 2, 1, "white", "white")
        canvas.draw_circle((x+8, 455), 2, 1, "black", "black")
        canvas.draw_circle((x+8, 457), 2, 1, "white", "white")
        canvas.draw_circle((x, 465), 6, 1, "black", "black")
        canvas.draw_circle((x, 463), 6, 1, "white", "white")
        counter=counter+.5
        x=x+2
    
    elif counter<255:
        canvas.draw_line((x+6, 520), (x-8, 550), 4, "black")
        canvas.draw_line((x+6, 520), (x+8, 550), 4, "black")
        canvas.draw_line((x, 460), (x+6, 520), 4, "black")
        canvas.draw_line((x+4, 485), (x-12, 510), 4, "black")
        canvas.draw_line((x+3, 485), (x+14, 510), 4, "black")
        canvas.draw_circle((x, 460), 16, 1, "black", "white")
        canvas.draw_circle((x-8, 455), 2, 1, "black", "black")#face
        canvas.draw_circle((x-8, 457), 2, 1, "white", "white")
        canvas.draw_circle((x+8, 455), 2, 1, "black", "black")
        canvas.draw_circle((x+8, 457), 2, 1, "white", "white")
        canvas.draw_circle((x, 465), 6, 1, "black", "black")
        canvas.draw_circle((x, 463), 6, 1, "white", "white")
        counter=counter+.5
        x=x+2
        
    elif counter<260:
        canvas.draw_line((x-6, 520), (x+8, 550), 4, "black")
        canvas.draw_line((x-6, 520), (x-8, 550), 4, "black")
        canvas.draw_line((x, 460), (x-6, 520), 4, "black")
        canvas.draw_line((x-4, 485), (x+12, 510), 4, "black")
        canvas.draw_line((x-3, 485), (x-14, 510), 4, "black")
        canvas.draw_circle((x, 460), 16, 1, "black", "white")
        canvas.draw_circle((x-8, 455), 2, 1, "black", "black")#face
        canvas.draw_circle((x-8, 457), 2, 1, "white", "white")
        canvas.draw_circle((x+8, 455), 2, 1, "black", "black")
        canvas.draw_circle((x+8, 457), 2, 1, "white", "white")
        canvas.draw_circle((x, 465), 6, 1, "black", "black")
        canvas.draw_circle((x, 463), 6, 1, "white", "white")
        counter=counter+.5
        x=x+2
    
    elif counter<265:
        canvas.draw_line((x+6, 520), (x-8, 550), 4, "black")
        canvas.draw_line((x+6, 520), (x+8, 550), 4, "black")
        canvas.draw_line((x, 460), (x+6, 520), 4, "black")
        canvas.draw_line((x+4, 485), (x-12, 510), 4, "black")
        canvas.draw_line((x+3, 485), (x+14, 510), 4, "black")
        canvas.draw_circle((x, 460), 16, 1, "black", "white")
        canvas.draw_circle((x-8, 455), 2, 1, "black", "black")#face
        canvas.draw_circle((x-8, 457), 2, 1, "white", "white")
        canvas.draw_circle((x+8, 455), 2, 1, "black", "black")
        canvas.draw_circle((x+8, 457), 2, 1, "white", "white")
        canvas.draw_circle((x, 465), 6, 1, "black", "black")
        canvas.draw_circle((x, 463), 6, 1, "white", "white")
        counter=counter+2
        x=x+2
    
    elif counter<540:
        canvas.draw_line((x, 520), (x+8, 550), 4, "black")
        canvas.draw_line((x, 520), (x-8, 550), 4, "black")
        canvas.draw_line((x, 485), (x+8, 510), 4, "black")
        canvas.draw_line((x, 460), (x, 520), 4, "black")
        canvas.draw_circle((x, 460), 16, 1, "black", "white")
        canvas.draw_line((x, 485), (x-8, 510), 4, "black")
        canvas.draw_circle((x-8, 455), 2, 1, "black", "black")#face
        canvas.draw_circle((x+8, 455), 2, 1, "black", "black")
        canvas.draw_circle((x, 465), 6, 1, "black", "black")
        canvas.draw_circle((x, 460), 6, 1, "white", "white")
        counter=counter+5
        x=x+2
    
    elif counter<560:
        canvas.draw_line((x, 520), (x+8, 550), 4, "black")
        canvas.draw_line((x, 520), (x-8, 550), 4, "black")
        canvas.draw_line((x, 485), (x+8, 510), 4, "black")
        canvas.draw_line((x, 460), (x, 520), 4, "black")
        canvas.draw_circle((x, 460), 16, 1, "black", "white")
        canvas.draw_line((x, 485), (x-8, 510), 4, "black")
        canvas.draw_circle((x-8, 455), 2, 1, "black", "black")#face
        canvas.draw_circle((x+8, 455), 2, 1, "black", "black")
        canvas.draw_circle((x, 465), 6, 1, "black", "black")
        canvas.draw_circle((x, 460), 6, 1, "white", "white")
        counter=counter+1
        
    
    elif counter<575:
        canvas.draw_line((x, 520), (x+8, 550), 4, "black")
        canvas.draw_line((x, 520), (x-8, 550), 4, "black")
        canvas.draw_line((x, 485), (x+8, 510), 4, "black")
        canvas.draw_line((x, 460), (x, 520), 4, "black")
        canvas.draw_circle((x, 460), 16, 1, "black", "white")
        canvas.draw_line((x, 485), (x-20, 510-40), 4, "black")
        canvas.draw_circle((x-8, 455), 2, 1, "black", "black")#face
        canvas.draw_circle((x+8, 455), 2, 1, "black", "black")
        canvas.draw_circle((x, 465), 6, 1, "black", "black")
        canvas.draw_circle((x, 460), 6, 1, "white", "white")
        counter=counter+1
    
    elif counter<580:
        canvas.draw_line((x, 520), (x+8, 550), 4, "black")
        canvas.draw_line((x, 520), (x-8, 550), 4, "black")
        canvas.draw_line((x, 485), (x+8, 510), 4, "black")
        canvas.draw_line((x, 460), (x, 520), 4, "black")
        canvas.draw_circle((x, 460), 16, 1, "black", "white")
        canvas.draw_line((x, 485), (x-25, 510-30), 4, "black")
        canvas.draw_circle((x-8, 455), 2, 1, "black", "black")#face
        canvas.draw_circle((x+8, 455), 2, 1, "black", "black")
        canvas.draw_circle((x, 465), 6, 1, "black", "black")
        canvas.draw_circle((x, 460), 6, 1, "white", "white")
        counter=counter+1
    
    elif counter<585:
        canvas.draw_line((x, 520), (x+8, 550), 4, "black")
        canvas.draw_line((x, 520), (x-8, 550), 4, "black")
        canvas.draw_line((x, 485), (x+8, 510), 4, "black")
        canvas.draw_line((x, 460), (x, 520), 4, "black")
        canvas.draw_circle((x, 460), 16, 1, "black", "white")
        canvas.draw_line((x, 485), (x-20, 510-40), 4, "black")
        canvas.draw_circle((x-8, 455), 2, 1, "black", "black")#face
        canvas.draw_circle((x+8, 455), 2, 1, "black", "black")
        canvas.draw_circle((x, 465), 6, 1, "black", "black")
        canvas.draw_circle((x, 460), 6, 1, "white", "white")
        counter=counter+1
        x=x+2
    
    elif counter<670:
        canvas.draw_line((x, 520), (x+8, 550), 4, "black")
        canvas.draw_line((x, 520), (x-8, 550), 4, "black")
        canvas.draw_line((x, 460), (x, 520), 4, "black")
        canvas.draw_line((x, 485), (x+8, 510), 4, "black")
        canvas.draw_line((x, 485), (x-8, 510), 4, "black")
        canvas.draw_circle((x, 460), 16, 1, "black", "white")
        canvas.draw_circle((x-8, 455), 2, 1, "black", "black")#face
        canvas.draw_circle((x+8, 455), 2, 1, "black", "black")
        canvas.draw_circle((x, 465), 6, 1, "black", "black")
        canvas.draw_circle((x, 460), 6, 1, "white", "white")
        x=x+2
    if x>650:
        x=-50
        counter=0
        
    for dot in dots:
        canvas.draw_circle(dot, 4, 1, "#f6e8a9", "#f6e8a9")
    
for i in range(1, 40):
    a = random.randint(0, 600)
    b = random.randint(0, 460)
    dots.append((a,b))
        
for i in range(1,3):
    r = random.randint(0, 255)
    g = random.randint(0, 255)
    b = random.randint(0, 255)
    backg = "RGB( " + str(r) + "," + str(g) + "," + str(b) + ")"
    

frame = simplegui.create_frame('Testing', 600, 600)
frame.set_canvas_background(backg)
frame.set_draw_handler(draw_handler)
frame.start()
