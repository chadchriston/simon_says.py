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
        def check_input(
