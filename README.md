import random

# Generate a random number from 1 to 100
secret_number = random.randint(1, 100)

print("Guess a number between 1 and 100!")

while True:
    try:
        guess = int(input("Enter your guess: "))

        if guess < secret_number:
            print("Your guess is too low.")
        elif guess > secret_number:
            print("Your guess is too high.")
        else:
            print(f"Correct! The answer is {secret_number}.")
            break

    except ValueError:
        print("Please enter a valid number.")
