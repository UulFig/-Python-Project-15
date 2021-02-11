# -Python-Project-15
#15 Playing Jo Ken Po

import random

def main():
    def userinput():
        while True:
            userinput = str(input("Choose 'paper', 'rock', or 'scissor': ")).lower()
            if userinput == "paper":
                return userinput
            elif userinput == "rock":
                return userinput
            elif userinput == "scissor":
                return userinput
            else:
                print("No,no,no! You must choose between: \"paper,rock or scissor\"\n")

    def yes_no(message):
        while True:
            yes_no = input(message).lower()
            if yes_no == "yes":
                return True
            elif yes_no == "no":
                return False
            else:
                print("Please use 'yes' or 'no'")

    PRNG = random.randint(1, 3)
    if PRNG == 1:
        PRNG = "paper"
    elif PRNG == 2:
        PRNG = "rock"
    else:
        PRNG = "scissor"

    answer = userinput()
    if answer == PRNG:
        print(f"\nComputer choose: {PRNG.title()}, and our Challenger choose: {answer.title()}")
        print("That\'s a DRAW!\n")
    elif answer == "paper" and PRNG == "rock":
        print(f"\nComputer choose: {PRNG.title()}, and our Challenger choose: {answer.title()}")
        print("You win! Congratz\n")
    elif answer == "paper" and PRNG == "scissor":
        print(f"\nComputer choose: {PRNG.title()}, and our Challenger choose: {answer.title()}")
        print("You lose! Sorry :(\n")
    elif answer == "rock" and PRNG == "scissor":
        print(f"\nComputer choose: {PRNG.title()}, and our Challenger choose: {answer.title()}")
        print("You win! Congratz\n")
    elif answer == "rock" and PRNG == "paper":
        print(f"\nComputer choose: {PRNG.title()}, and our Challenger choose: {answer.title()}")
        print("You lose! Sorry :(\n")
    elif answer == "scissor" and PRNG == "paper":
        print(f"\nComputer choose: {PRNG.title()}, and our Challenger choose: {answer.title()}")
        print("You win! Congratz\n")
    elif answer == "scissor" and PRNG == "rock":
        print(f"\nComputer choose: {PRNG.title()}, and our Challenger choose: {answer.title()}")
        print("You lose! Sorry :(\n")


    while True:
        if yes_no("Do you want try again?\n"):
            print("Good luck!\n")
            return main()
        else:
            print("Good bye!")
            return


main()
