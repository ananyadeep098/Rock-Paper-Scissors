import random

def play_game():
    choices = ["rock", "paper", "scissors"]

    while True:
        print("\n--- Rock-Paper-Scissors Game ---")
        user_choice = input("Enter rock, paper, or scissors (or 'exit' to quit): ").lower()

        # Exit condition
        if user_choice == "exit":
            print("Thanks for playing! Goodbye.")
            break

        # Validate input
        if user_choice not in choices:
            print("Invalid choice! Please select rock, paper, or scissors.")
            continue

        # Computer choice
        computer_choice = random.choice(choices)
        print(f"Computer chose: {computer_choice}")

        # Game logic
        if user_choice == computer_choice:
            print("It's a tie!")
        elif (user_choice == "rock" and computer_choice == "scissors") or \
             (user_choice == "paper" and computer_choice == "rock") or \
             (user_choice == "scissors" and computer_choice == "paper"):
            print("You win!")
        else:
            print("Computer wins!")

if __name__ == "__main__":
    play_game()
