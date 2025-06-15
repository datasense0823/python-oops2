# 🎮 Gamer & Game Platform – OOP Python Assignment

## 📘 Objective

Design a simple gaming platform using Object-Oriented Programming (OOP) principles in Python. This assignment will help you strengthen your understanding of:

- `__init__`, `self`
- Writing and calling methods
- Using `assert` statements for validation
- Adding type hints
- Object interactions (using one class inside another)

---

## 🧩 Real-World Scenario

You are building a backend for a basic gaming platform called **PlayZone**. On this platform:

- Users (called **Gamers**) can join various online games.
- Each game has a **minimum level** requirement.
- A gamer can only join a game if they meet the required level.
- You, as the developer, have to create two classes — `Gamer` and `Game` — and define how they interact.

---

## 🛠️ Requirements

### 🎮 Class: `Gamer`

Represents a player on the platform.

#### Attributes:
- `username: str` – The name of the gamer
- `level: int` – The gamer’s current level (must be >= 1)

#### Methods:
1. `level_up(self) -> None`  
   Increases the gamer's level by 1.
2. `get_info(self) -> str`  
   Returns a string in the format:  
   `"Player: Aryan | Level: 3"`

#### Constraints:
- Use `assert` to ensure the level is at least 1 in the constructor.

---

### 🕹️ Class: `Game`

Represents a game that can be joined by gamers.

#### Attributes:
- `name: str` – Name of the game
- `min_level: int` – Minimum level required to join the game (must be >= 1)
- `players: list` – A list of Gamer objects who joined the game (starts empty)

#### Methods:
1. `join_game(self, gamer: Gamer) -> str`  
   - Checks if the gamer's level is >= min_level.
   - If yes, adds the gamer to the game and returns a success message.
   - If not, returns a rejection message.
   - Use `assert` to ensure the input is a valid `Gamer` object.

2. `show_players(self) -> None`  
   - Prints the `get_info()` of all gamers who joined the game.

---

## 🧪 Task Instructions

### Step 1: Create Gamers
- Create at least **3 Gamer objects** with different usernames and levels (e.g., `Aryan`, `Teena`, `Ravi`).

### Step 2: Create Games
- Create at least **2 Game objects** with different `min_level` values (e.g., `BattleZone`, `DragonQuest`).

### Step 3: Join Attempt
- Try to have each gamer join each game.
- Print the result of each join attempt.

### Step 4: Level Up
- Level up some gamers and try joining again.
- Show final players for each game using `show_players()`.

---

## 🔄 Sample Output Example

Aryan joined BattleZone
Teena is not high enough level to join DragonQuest
Ravi joined DragonQuest

Players in BattleZone:
Player: Aryan | Level: 2

Players in DragonQuest:
Player: Ravi | Level: 5


---

## ✅ Evaluation Checklist

| Feature                            | Requirement Met |
|------------------------------------|------------------|
| `__init__`, `self` used correctly  | ✅               |
| Methods work as described          | ✅               |
| `assert` used for validations      | ✅               |
| Type hints used                    | ✅               |
| Object interaction (`Gamer` <-> `Game`) | ✅         |
| Code runs with proper output       | ✅               |

---

## 🌟 Bonus Challenge (Optional)

Add a method to the `Gamer` class:

```python
def play_game(self, game: Game) -> str
