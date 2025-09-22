# SOS Game (C++ Console Version)

## Overview

This is a simple **two-player SOS game** implemented in C++ for the console. Players take turns placing letters **S** or **O** on a 5x5 grid to form the sequence **SOS**. Each SOS formed scores a point for the player. The game continues until all cells are filled, and the player with the highest score wins.  

## Features

- Two-player turn-based gameplay
- Player 1 chooses their letter (S or O) at the start; Player 2 automatically gets the other letter
- SOS sequences are highlighted on the board when formed (lowercase `s` and `o`)
- Accepts both uppercase and lowercase input (`s` or `S`, `o` or `O`)
- Prevents placing a letter in an already occupied cell
- Keeps track of scores and announces the winner

## How to Play

1. Run the game executable:
2. **Player 1 chooses their letter** (`S` or `O`) at the start.  
- Input is case-insensitive (`s` or `S` are both valid)
3. Players take turns entering the **row and column** to place their letter.  
- Example: To place a letter at row 1, column 2, type:
  ```
  1 2
  ```
4. The game **automatically detects SOS sequences** in all directions (horizontal, vertical, and diagonal) and highlights them
5. The game ends when all cells are filled. Scores are displayed and the winner is announced

## Controls

- Row and column input only after Player 1 chooses their letter
- No need to select S or O after the first choice; each player sticks to their assigned letter

## Board Representation

- `.` = empty cell  
- `S` / `O` = normal letters placed on the board  
- `s` / `o` = letters that are part of an SOS sequence  

### Example Board

0 1 2 3 4
0 . S . O .
1 . S s O .
2 . . . S .
3 . O . O .
4 . s . O .


Lowercase letters (`s` and `o`) indicate a completed SOS sequence.

## Compilation Instructions

- Use a C++ compiler that supports C++11 or later
- Compile using:
  ```bash
  g++ sos_game.cpp -o sos_game

Run the executable:
./sos_game   # Linux/macOS
sos_game.exe # Windows
