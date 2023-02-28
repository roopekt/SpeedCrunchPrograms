# Bulls and Cows

The classic bulls and cows game.

## Instructions

1. Disable `Settings/Behaviour/Partial Results`
2. Enable `Settings/Behaviour/Complex Numbers`
3. Type in some random digits (the RNG will use this as a seed)
4. Run `gi 0` to start the game with a random number, or `gi <4 digit number>` to start with a specific number (for testing)
5. Run `g <your guess>` to make a guess. You will see `<number of bulls>,<number of cows>+<number of guesses>,<encrypted correct number>j`. Number of cows may not be shown if 0.
6. Repeat step 5 until you get 4 bulls. Then go back to step 4.

## Rules of the game

- You will be trying to guess a number
- The number is 4 digits long. Each digit is between 0 and 9 (inclusive).
- After a guess, the number of bulls and the number of cows will be printed
- Bull means a digit was correct and in correct place. e.g. true is 0123 and guess is 9129 -> 2 bulls.
- Cow means a digit was correct, but in the wrong place. e.g. true is 0123 and guess is 9219 -> 2 cows.
- A digit can't be both a bull and a cow (bulls are prioritized), and can only be counted once towards any counter.
