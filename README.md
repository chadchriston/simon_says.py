# Simon-Says

#python 

#list of colours
colours = ['red', 'blue', 'green', 'yellow']

#initialize an empty list to store the sequence
    sequence = []

#Function to generate the next colour in the sequence
    def generate_next_colour():
      return random.choice(colours)

#Function to play the sequemnce
    def play_sequence():
       for colour in sequence:
       print(colour)
       time.sleep(1)
  
#Function to check if the player's input matches the sequence
        def check_input(input_sequence):
          if input_sequence == sequence:
            return True
          else:
            return False

#Main game loop
def simon_says():
  print("Welcome to Simon Say!")
  time.sleep(1)
  print("Get Ready...")
  time.sleep(1)

#Generate the first colour in the sequence
next_colour = generate_next_colour()
sequence.append(next_colour)

#Play the sequence
play_sequence()

#Prompt the player for their input
print("Your turn!Enter the colours in the sequence, one at a time.")
  play_sequence = []
  for i in range(len(sequence)):
  player_colour = input("Colour: ")

player_sequence.append(player_colour)

  #Check if the player's input matches the sequences
  if check_input(player_sequence):
    print("Congratulations! You got it right!")
    else:
        print("Oops! That's incorrect. Game over.")

        #Start the game
        simon_says()

      
