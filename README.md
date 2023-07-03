
# Tenzies App

This is a simple React application called Tenzies. It is a dice rolling game where the objective is to roll the dice until all of them have the same value. The application uses React hooks to manage state and update the UI based on user interactions.

## Hooks
useState
The useState hook is used to manage the state of the dice and the game. It provides a way to define state variables and update them when needed. In the Tenzies app, the following state variables are defined using useState:

dice: Stores an array of dice objects with their values and whether they are held or not.
tenzies: Represents the state of the game, whether the player has achieved "Tenzies" or not.
useEffect
The useEffect hook is used to perform side effects or actions based on changes to the component's state. It runs after the component has rendered and whenever the specified dependencies change. In the Tenzies app, useEffect is used to check if all the dice are held and have the same value. If so, it sets the tenzies state variable to true. The effect is dependent on the dice state variable.

## Functions
### generateNewDie
This function generates a new die object with a random value between 1 and 6, assigns a unique identifier using nanoid, and sets the initial "held" state to false. It is called when creating a new set of dice.

### allNewDice
This function creates a new array of dice by calling the generateNewDie function multiple times. It returns an array with 10 new dice objects.

### rollDice
The rollDice function is called when the "Roll" button is clicked. It checks if the player has achieved "Tenzies" or not. If not, it updates the dice state by generating new dice for the ones that are not held. If "Tenzies" is achieved, it resets the game by setting the tenzies state to false and generating a new set of dice.

### holdDice
The holdDice function is called when a die is clicked. It toggles the "held" state of the clicked die by updating the dice state with the modified die object.

## Components
### Die
The Die component represents a single die in the UI. It receives the following props:

- value: The current value of the die.
- isHeld: A boolean indicating whether the die is held or not.
- holdDice: A function to be called when the die is clicked. It toggles the "held" state.
### Confetti
- The Confetti component is imported from the 'react-confetti' library. It is conditionally rendered when the player achieves "Tenzies". It adds a confetti effect to the UI.


 The main UI of the Tenzies app consists of the following elements:

- Title: Displays the game title "Tenzies".
- Instructions: Provides instructions for playing the game.
- Dice container: Displays all the dice as rendered by the Die component.
- Roll button: Triggers the rollDice function when clicked. The label of the button changes to "New Game" when "Tenzies" is achieved.

## How to Play
- Open the Tenzies app in a web browser.
- Read the instructions to understand the game objective.
- Click on each die to hold or release it.
- Click the "Roll" button to roll the dice.
- Continue rolling until all the dice have the same value.

Open [TenzieApp](https://tenzieapp.netlify.app/) 


