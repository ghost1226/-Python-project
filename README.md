import random

def display_title():
    print("Welcome to the Number Guessing Game!")
    print("You need to guess a number between 1 and 10.")

def play_game():
    number_to_guess = random.randint(1, 10)  # Pick a random number from 1 to 10
    guess = 0  # Start with a guess of 0

    while guess != number_to_guess:
        guess = int(input("Enter your guess: "))  # Get the player's guess

        if guess < number_to_guess:
            print("Too low! Try again.")
        elif guess > number_to_guess:
            print("Too high! Try again.")
        else:
            print("You guessed it! Well done!")

def main():
    display_title()  # Show the title and instructions

    play_again = "yes"  # Variable to control the loop

    while play_again.lower() == "yes":  # Loop to keep playing
        play_game()  # Start the guessing game
        play_again = input("Do you want to play again? (yes/no): ")  # Ask to play again

if __name__ == "__main__":
    main()  # Start the game
