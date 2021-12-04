# Dice-Roll
#My first attempt at using GUI in a python program
#Main Code

from tkinter import *
from playsound import playsound
import random
root= Tk()

def DiceRoll():
    playsound('C:\\Users\\Anik\\Documents\\Python\\SnakeLadder\\dicethrow.mp3')
    
    ran= str(random.randrange(1,7))
    dice= str("You rolled a "+ran)
    my_label.config(text=dice)
    
    if ran=="1":
        b_label.config(image=one)
    elif ran=="2":
        b_label.config(image=two)
    elif ran=="3":
        b_label.config(image=three)
    elif ran=="4":
        b_label.config(image=four)
    elif ran=="5":
        b_label.config(image=five)
    elif ran=="6":
        b_label.config(image=six)
    
root.title('Roll a Dice!')

global one
one=PhotoImage(file= "C:\\Users\\Anik\\Documents\\Python\\SnakeLadder\\one.PNG")
global two
two=PhotoImage(file= "C:\\Users\\Anik\\Documents\\Python\\SnakeLadder\\two.PNG")
global three
three=PhotoImage(file= "C:\\Users\\Anik\\Documents\\Python\\SnakeLadder\\three.PNG")
global four
four=PhotoImage(file= "C:\\Users\\Anik\\Documents\\Python\\SnakeLadder\\four.PNG")
global five
five=PhotoImage(file= "C:\\Users\\Anik\\Documents\\Python\\SnakeLadder\\five.PNG")
global six
six=PhotoImage(file= "C:\\Users\\Anik\\Documents\\Python\\SnakeLadder\\six.PNG")

button = Button(root, text="Roll Dice", command=DiceRoll) 
button.pack()

global my_label
my_label = Label(root, text="")
my_label.pack() 

global b_label
root.geometry("512x512")
photo=PhotoImage(file= "C:\\Users\\Anik\\Documents\\Python\\SnakeLadder\\dice.PNG")
b_label = Label(image=photo)
b_label.pack()

root.mainloop()
