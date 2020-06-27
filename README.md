# freestyleproject instructions

# INSTALLING AND ACTIVATING A VIRTUAL ENVIRONMENT
First, let's make sure you are running an up-to-date version of Python by entering 

'python --version' into the CLI. I'm running 3.7.6 but I believe anythin 3.6+ is ok.

--

Next, enter

'python m venv env' into the CLI and activate your virtual environment by entering 

'source env/bin/activate' into the CLI.

--

You can confirm that you're in the virtual environment by checking the location of your Python interpreter by
entering 

'which python' into the CLI.

---

If you need leave the virtual environment enter

'deactivate' into your CLI.

# CREATING FILES
Create a hangman.py file
Create a words.py file

# The first thing you need to do is setup and get the word function

<!-- import random
from words import word_list

def get_word():
    word = random.choice(word_list)
    return word.upper() -->

# The next thing you need to do is define the play function and the outputs

<!-- def play(word):
    word_completion = "_" * len(word)
    guessed = False
    guessed_letters = []
    guessed_words = []
    tries = 6
    print("Let's play Hangman!")
    print(display_hangman(tries))
    print(word_completion)
    print("\n")
    while not guessed and tries > 0:
        guess = input("Please guess a letter or word: ").upper()
        if len(guess) == 1 and guess.isalpha():
            if guess in guessed_letters:
                print("You already guessed the letter", guess)
            elif guess not in word:
                print(guess, "is not in the word.")
                tries -= 1
                guessed_letters.append(guess)
            else:
                print("Good job,", guess, "is in the word!")
                guessed_letters.append(guess)
                word_as_list = list(word_completion)
                indices = [i for i, letter in enumerate(word) if letter == guess]
                for index in indices:
                    word_as_list[index] = guess
                word_completion = "".join(word_as_list)
                if "_" not in word_completion:
                    guessed = True
        elif len(guess) == len(word) and guess.isalpha():
            if guess in guessed_words:
                print("You already guessed the word", guess)
            elif guess != word:
                print(guess, "is not the word.")
                tries -= 1
                guessed_words.append(guess)
            else:
                guessed = True
                word_completion = word
        else:
            print("Not a valid guess.")
        print(display_hangman(tries))
        print(word_completion)
        print("\n")
    if guessed:
        print("Congrats, you guessed the word! You win!")
    else:
        print("Sorry, you ran out of tries. The word was " + word + ". Maybe next time!") -->

# The next thing you need to do is add a function to run the game

<!-- def main():
    word = get_word()
    play(word)
    while input("Play Again? (Y/N) ").upper() == "Y":
        word = get_word()
        play(word) -->

# The next thing you need to do is add a function to run the game on the CIL

<!-- if __name__ == "__main__":
    main() -->

# The next thing you need to do is add a function to display a hangman in stages

<!-- def display_hangman(tries):
    stages = [  # final state: head, torso, both arms, and both legs
                """
                   --------
                   |      |
                   |      O
                   |     \\|/
                   |      |
                   |     / \\
                   -
                """,
                # head, torso, both arms, and one leg
                """
                   --------
                   |      |
                   |      O
                   |     \\|/
                   |      |
                   |     / 
                   -
                """,
                # head, torso, and both arms
                """
                   --------
                   |      |
                   |      O
                   |     \\|/
                   |      |
                   |      
                   -
                """,
                # head, torso, and one arm
                """
                   --------
                   |      |
                   |      O
                   |     \\|
                   |      |
                   |     
                   -
                """,
                # head and torso
                """
                   --------
                   |      |
                   |      O
                   |      |
                   |      |
                   |     
                   -
                """,
                # head
                """
                   --------
                   |      |
                   |      O
                   |    
                   |      
                   |     
                   -
                """,
                # initial empty state
                """
                   --------
                   |      |
                   |      
                   |    
                   |      
                   |     
                   -
                """
    ]
    return stages[tries] -->

# The next thing you need to do is add a word list to support your game

The format is as follow

<!-- word_list = [
    'wares',
    'soup', 
    'enter word',
    ....
    ....
    ....
    'enter word']-->

# You are now done and can run your game in the CLI
