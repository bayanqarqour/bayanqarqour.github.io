# Random Guessing Game Flowchart

```mermaid
flowchart TD
    Start([Start]) --> GenerateNumber["Generate a random number within a specific range"]
    GenerateNumber --> GetUserInput["Get user's guess"]
    GetUserInput --> CheckInput{"Is the input valid?"}
    CheckInput -- No --> InvalidInput["Invalid input message"] --> GetUserInput
    CheckInput -- Yes --> Compare{"Is the guess correct?"}
    Compare -- Yes --> CorrectGuess["Correct Guess"] --> EndGame(["End Game"])
    Compare -- No --> HighLow{"Is the guess too high or too low?"}
    HighLow -- "Too high" --> TooHigh["Too high"] --> GetUserInput
    HighLow -- "Too low" --> TooLow["Too low!"] --> GetUserInput
    EndGame --> End([End])
'''
