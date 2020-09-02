command = ""

while True:
    command = input("""~~~~~~~~ Guess Game ~~~~~~~~~
Type 'Rules' to read the rules.
Type 'Play' to start playing.
> """).lower()
    if command == "rules":
        print("""- You only have 3 guesses.
- You can only guess between 1 and 10,
  if you still guess outside that range,
  it won't count as a guess.""")
        break
    elif command == "play":
        break

import random
secret_number = random.randint(1, 10)
guess_count = 0
guess_limit = 3

while True:
    try:
        guess = int(input("""Guess a number between 1 - 10
> """))
        if not guess in range(1, 11):
            guess_count -= 1
            print("- Guess between 1 - 10.")
        if guess != secret_number:
            guess_count += 1
            if guess_count != 3:
                print("- Wrong number!")
                if secret_number > guess > 0:
                    print("- Try a higher number.")
                if secret_number < guess < 10:
                    print("- Try a lower number.")
                print(f"- Guesses: {guess_count}.")
            else:
                print(f"- The secret number was {secret_number}.")
                break
        if guess == secret_number:
            print("- Congratulations! You guessed the right number!")
            break
    except ValueError:
        continue
