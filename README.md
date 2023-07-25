# Simon-Says
```python
import random
import time

# List of possible colours
colors = ["red", "blue", "green", "yellow"]

# Function to generate a random sequence of colours
def generate_sequence(length):
    return [random.choice(colours) for _ in range(length)]

# Function to display the sequence of colours to the player
def display_sequence(sequence):
    for colour in sequence:
        print(colour)
        time.sleep(1)
        # Clear the screen
        print("\033c", end="")
        time.sleep(0.5)

# Function to get the player's guess
def get_player_guess():
    guess = input("Enter the colours in the sequence, separated by spaces: ")
    return guess.split()

# Function to check if the player's guess matches the sequence
def is_guess_correct(guess, sequence):
    return guess == sequence

# Function to play the Simon Says game
def play_game():
    level = 1
    sequence = generate_sequence(level)
    
    while True:
        print("Level", level)
        display_sequence(sequence)
        
        player_guess = get_player_guess()
        if not is_guess_correct(player_guess, sequence):
            print("Game over! You reached level", level)
            break
        
        level += 1
        sequence = generate_sequence(level)
    
    print("Thanks for playing!")

# Start the game
play_game()
```
