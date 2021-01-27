# snake-water-gun-game-single-player
#............................................ snake water gun game .................................................
import random

print("\t\t\t\t Snake ,Water , Gun game\t\t\t\t")
print("s for snake ")
print("w for water ")
print("g for gun ")
print("per round winning point is 1")
print("In tied round points are shared equally i.e 0.5 to each.")
list = ["snake", "water", "gun"]
choice = random.choice(list)

num = 1
chance = 10
print("number of chance to be played is 10 times ")
cwins=0#points win by computer
ywins=0 #points won by us.
while (chance > 0):

    a = str(input("choose any snake ,water, gun:"))

    if a == "s":
        print("you have entered snake")
        print("computer has chosen", choice)
        chance = chance - 1
        print("chances left: ", chance)


    elif a == "w":
        print("you have entered water")
        print("computer has chosen", choice)
        chance = chance - 1
        print("chances left: ", chance)


    elif a == "g":
        print("you have entered gun")
        print("computer has chosen", choice)
        chance = chance - 1
        print("chances left:", chance)
    else:
        print("you have entered wrong input,plse enter any of these :'s,w,g'")

    if a == "s" and choice == "gun":#snaake gun
        print("computer is winner of this round")
        cwins= cwins+1
    elif a == "s" and choice == "snake": #snake snake
        print("this round is tied")
        cwins= cwins+0.5
        ywins= ywins+0.5
    elif a == "g" and choice == "gun": #gun gun
        print("this is tied round")
        cwins = cwins + 0.5
        ywins = ywins + 0.5
    elif a == "g" and choice == "water": #gun water
        print("computer is  the winner of this round")
        cwins = cwins + 1
    elif a == "g" and choice == "snake": #gun snake
        print("you are the winner of this round")
    elif a == "w" and choice == "water": #water water
        print("this round is tied")
        cwins = cwins + 0.5
        ywins = ywins + 0.5
    elif a == "w" and choice == "gun":  # water gun
        print("you are the winner of this round")
        ywins = ywins+1
    elif a=="s" and choice=="water": #snake water
        print("you are the winner of this round")
        ywins = ywins + 1
    elif a=="w" and choice=="snake": #water snake
        print("you are the winner of this round")
        ywins = ywins + 1
    if chance==0:
        print("\t\t\t\t\t game over \t\t\t\t\t")
        print(f"points of computer are:{cwins} and yours is: {ywins}")
        if cwins>ywins:
            print(".........................oops! computer is the winner of the game..........................")
        elif cwins==ywins:
            print("............................well tried !but game is tied....................................")
        else:
            print(".........................congrats! you are the winner of this game.........................")
