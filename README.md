# Rock-Paper-Scissors
import random

def determine_winner(user, computer):
    if user == computer:
        return "It's a tie!"
    elif (user == "rock" and computer == "scissors") or \
         (user == "scissors" and computer == "paper") or \
         (user == "paper" and computer == "rock"):
        return "You win!"
    else:
        return "Computer wins!"

def main():
    choices = ["rock", "paper", "scissors"]

    print("🎮 Welcome to Rock-Paper-Scissors Game!")

    while True:
        user_choice = input("\nEnter your move (rock/paper/scissors): ").lower()

        if user_choice not in choices:
            print("Invalid move. Please choose from rock, paper, or scissors.")
            continue

        computer_choice = random.choice(choices)
        print(f"Computer chose: {computer_choice}")

        result = determine_winner(user_choice, computer_choice)
        print(result)

        replay = input("Do you want to play again? (yes/no): ").lower()
        if replay != "yes":
            print("Thanks for playing!")
            break

if __name__ == "__main__":
    main()
