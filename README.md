# Stone-Paper-Scissors-Game-using-Python
Stone paper scissors is a game manually played by people, but I have created this game using Python programming language where you can play this game on your hardware

comp= print("Computer : A(stone) B(paper) C(scissor) ")
you= input("Your turn  : A(stone) B(paper) C(scissor) ")
import random
def game(comp,you):
    if comp == you:
        return None
    elif comp== "stone":
        if you== "paper":
            return True
        elif you== "scissor":
            return False
        
    elif comp== "paper":
        if you== "stone":
            return False
        elif you== "scissor":
            return True

    elif comp== "scissor":
        if you== "stone":
            return True
        elif you== "paper":
            return False
rnum = random.randint(1,3)
# print(rnum)    prints a random number between 1-3
if rnum== 1:
    comp= "stone"
elif rnum== 2:
    comp= "paper"
elif rnum== 3:
    comp= "scissor"

winner= game(comp,you)
print(f"Computer chose: {comp}")
print(f"You chose: {you}")

if winner == None:
    print("The game is a tie")
elif winner:
    print("Congratulations! you won")
else:
    print("You lost")
