
# NUMBER GUESSING GAME

**1. Importing the `random` Module:**

- `import random`: This line imports the `random` module, which is essential for generating the secret number.

**2. Defining the `guess_number()` Function:**

- `def guess_number():`: This line defines a function named `guess_number()`, which will contain the core logic of the game.

**3. Generating the Secret Number:**

- `secret_number = random.randint(1, 100)`: This line uses the `random.randint()` function to generate a random integer between 1 and 100 (inclusive) and stores it in the `secret_number` variable.

**4. Initializing Attempts:**

- `attempts = 0`: This variable keeps track of the number of guesses the player has made. It's initialized to 0 at the beginning.

**5. Game Loop:**

- `while True:`: This creates an infinite loop that will continue until the player guesses the correct number.

- `try-except` Block:
    - `guess = int(input("Take a guess: "))`: 
        - Prompts the player to enter their guess.
        - Uses `int()` to convert the player's input (which is initially a string) into an integer.
        - If the player enters something that cannot be converted to an integer (e.g., letters), it will raise a `ValueError`.
    - `attempts += 1`: Increments the `attempts` counter by 1 after each guess.
    - `if guess < secret_number:`: 
        - If the player's guess is less than the secret number, it prints "Too low!".
    - `elif guess > secret_number:`:
        - If the player's guess is greater than the secret number, it prints "Too high!".
    - `else:`:
        - If the player's guess is equal to the secret number, it prints a congratulatory message along with the number of attempts, and then uses the `break` statement to exit the loop.
    - `except ValueError:`: 
        - This block handles the case where the player enters invalid input (e.g., letters).
        - It prints an error message and continues to the next iteration of the loop.

**6. Running the Game:**

- `if __name__ == "__main__":` 
    - This line ensures that the `guess_number()` function is only called when the script is executed directly (not when imported as a module).
- `guess_number()`: 
    - This line calls the `guess_number()` function to start the game.

This code provides a solid foundation for a simple number guessing game. You can further enhance it by:

- Allowing the user to specify the range of numbers.
- Adding hints to guide the player.
- Implementing a limited number of attempts.
- Creating a more user-friendly interface.
- And many more!
