# 🌍 Country Capital Quiz

A Python-based geography quiz that tests your knowledge of countries and their capitals around the world.

The program randomly shuffles a collection of countries, asks the player to identify each capital, and tracks their score. It also supports multiple accepted answers for countries with more than one capital or alternative capital names.

## ✨ Features

- 🌎 **Extensive country database:** A dictionary containing countries and their associated capitals.
- 🔀 **Randomized questions:** Questions appear in a different order each time the quiz starts.
- 🧠 **Interactive gameplay:** Enter your answer directly in the terminal.
- ✅ **Multiple accepted answers:** Supports comma-separated and slash-separated alternatives.
- 🔡 **Case-insensitive matching:** Answers such as `tokyo`, `Tokyo`, and `TOKYO` are treated equally.
- 🧹 **Whitespace handling:** Extra spaces around answers are ignored.
- 📊 **Score tracking:** Earn one point for every correct answer.
- 🚪 **Early exit:** Type `quit` at any time to leave the game.
- 📦 **No external dependencies:** Uses Python's built-in `random` module.

## 🛠️ Technologies Used

- **Python 3**
- `random` — shuffles the order of questions.

No third-party libraries are required.

## 📋 Requirements

- Python 3 installed on your computer.
- A terminal or code editor, such as Visual Studio Code.

## 🚀 Getting Started

### 1. Clone the repository

If the project is hosted on GitHub:

```bash
git clone <repository-url>
```

Replace `<repository-url>` with your repository's URL.

### 2. Navigate to the project directory

```bash
cd <project-folder>
```

### 3. Run the quiz

If your Python file is named `capital_quiz.py`, run:

```bash
python capital_quiz.py
```

On some Windows systems, use:

```bash
py capital_quiz.py
```

## 🎮 How to Play

1. Launch the program.
2. Read the country displayed in the terminal.
3. Enter its capital and press Enter.
4. Receive immediate feedback on your answer.
5. Continue until all questions have been answered.
6. Type `quit` at any time to exit early.

### Example Gameplay

```text
Loaded 195 countries from dictionary! Let's test your knowledge.
Type 'quit' at any time to exit the game.

----------------------------------------
What is the capital of India? New Delhi
Correct!

What is the capital of South Africa? Pretoria
Correct!

What is the capital of Japan? sydney
Incorrect. Accepted answer(s): Tokyo

What is the capital of France? quit

Game exited early. Your final score: 2/195
```

*The example is illustrative. The actual number of questions depends on the entries in the dictionary.*

## 🧮 Scoring System

- Each correct answer earns **1 point**.
- Incorrect answers earn **0 points**.
- Answers are compared without regard to capitalization.
- Leading and trailing spaces are ignored.
- The final score is displayed when the quiz is completed.
- If the player quits early, their current score is displayed.

For example:

```text
Quiz Complete! Your final score: 150/195
```

## 🔍 Multiple Accepted Answers

Some dictionary entries contain multiple answers separated by commas or slashes.

For example:

```python
"Bolivia": "La Paz/Sucre",
"South Africa": "Pretoria,Bloemfontein,Cape Town",
"Ukraine": "Kyiv/Kiev",
```

The quiz splits these entries into individual accepted answers.

| Country | Example accepted answers |
|---|---|
| Bolivia | La Paz, Sucre |
| South Africa | Pretoria, Bloemfontein, Cape Town |
| Ukraine | Kyiv, Kiev |

The program uses `replace()`, `split()`, `strip()`, and `casefold()` to normalize and compare answers.

**Note:** Every comma-separated or slash-separated item is treated as an accepted answer. The dictionary should therefore be formatted carefully to avoid accepting unintended answers.

## ⚙️ How It Works

1. Country-capital pairs are retrieved from the dictionary.
2. `random.shuffle()` randomizes the order of questions.
3. A `for` loop iterates through the shuffled list.
4. `input()` collects the player's guess.
5. The program checks whether the player entered `quit`.
6. The stored capital is split into alternative answers.
7. Each accepted answer is normalized using `strip()` and `casefold()`.
8. The guess is compared against the accepted answers.
9. The score increases when the guess matches.
10. The final score is displayed after the quiz ends.

## 🔮 Future Improvements

- [ ] Add continent-based quiz modes.
- [ ] Introduce multiple-choice questions.
- [ ] Add difficulty levels.
- [ ] Display the final score as a percentage.
- [ ] Track high scores across multiple sessions.
- [ ] Add a timer for each question.
- [ ] Improve validation of country and capital data.
- [ ] Support more alternative spellings and transliterations.
- [ ] Add a graphical user interface.
- [ ] Save quiz results to a local file.
