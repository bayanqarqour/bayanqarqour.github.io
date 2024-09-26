# Random Guessing Game Flowchart

```mermaid
flowchart TD
    Start([Start]) --> GenerateNumber["Generate a random number within the range"]
    GenerateNumber --> GetUserInput["Get user's guess"]
    GetUserInput --> CheckInput{"Is the input valid?"}
    CheckInput -- No --> InvalidInput["Display invalid input message"] --> GetUserInput
    CheckInput -- Yes --> Compare{"Is the guess correct?"}
    Compare -- Yes --> CorrectGuess["Display 'Correct Guess!'"] --> EndGame(["End Game"])
    Compare -- No --> HighLow{"Is the guess too high or too low?"}
    HighLow -- "Too high" --> TooHigh["Display 'Too high!'"] --> GetUserInput
    HighLow -- "Too low" --> TooLow["Display 'Too low!'"] --> GetUserInput
    EndGame --> End([End])
