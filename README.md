# 🐍 Snake, Water, Gun Game
A digital version of the popular childhood game (similar to Rock-Paper-Scissors) built entirely in C.

## 📝 Description
The player chooses between Snake (s), Water (w), or Gun (g). The computer makes a random choice. The program determines the winner based on the following rules:
- **Snake** drinks **Water** (Snake wins)
- **Water** douses **Gun** (Water wins)
- **Gun** kills **Snake** (Gun wins)

## 🛠️ Concepts Covered
- **Modular Programming**: Using functions for game logic.
- **Character Handling**: Processing `char` inputs and outputs.
- **Logic Mapping**: Converting random integers into game choices.
- **Pointer-like logic**: Efficiently returning values to the `main` function.

## 🚀 How to Run
1. Clone the repository.
2. Compile using GCC: `gcc swg_game.c -o swg_game`
3. Run the executable: `./swg_game`
